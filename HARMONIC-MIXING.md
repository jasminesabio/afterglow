# Harmonic Mixing in the Constellation (Feature Brief)

**Status:** Design Phase  
**For:** Valerie (UI Implementation)  
**Purpose:** Show which tracks can be mixed together in key without cluttering the spatial view

---

## The Problem

When you're DJing, after you play a track, you need another track that:
1. Fits the moment spatially (role + crowd state)
2. **AND** harmonically blends with the previous track (mixing in key)

The Camelot wheel provides this: two tracks in compatible keys can be mixed smoothly.

Right now, the constellation shows spatial relationships but not harmonic ones. We have Key data for all 73 tracks; we should use it.

---

## The Solution: On-Click Harmonic Mapping

**Core principle:** Only show harmonic relationships when a DJ selects a specific track. This keeps the baseline constellation clean while revealing rich harmonic pathways on demand.

### What Happens When You Click a Track

1. **Track detail view opens** (artist, duration, tags, confidence scores)
2. **Harmonic compatible tracks light up** in the constellation behind the detail view
3. **Visual indicator:** Color highlight, glow, or edge connection shows which tracks mix well with the selected track
4. **Interaction:** User can click a highlighted track to play it next, or click the current track's highlighted neighbor to see *its* harmonic map

### Visual Pattern

```
Constellation view (baseline — no connections visible)
├─ User clicks track: "Bridge Track (Key 7A)"
└─ Harmonic map activates:
   ├─ All compatible keys highlight in the constellation
   ├─ Highlighted tracks: Key 6A, 7A, 8A, 8B (Camelot wheel neighbors)
   ├─ Visual: Soft glow or color wash over compatible tracks
   └─ Detail view shows: "Mixes well with 8 tracks in this vibe"
```

---

## Camelot Wheel: Quick Primer

The Camelot wheel groups keys into 12 positions, each with major (A) and minor (B) variants.

**Mixing compatibility** (tracks that blend smoothly):
- **Same position** (e.g., 7A + 7A) — Perfect match
- **±1 position** (e.g., 7A + 6A or 7A + 8A) — Great blend
- **±1 position, opposite letter** (e.g., 7A + 8B) — Also works; changes mood slightly
- **Rarely: +5 or -5** (e.g., 7A + 12A) — Harmonic surprise; advanced mixing

**For MVP:** Focus on same key + ±1 compatibility. Skip ±5 surprises (can add later).

---

## Data You Already Have

All 73 tracks in `afterglow-tags.json` include a **Key** field:

```json
{
  "artist": "Artist Name",
  "title": "Track Title",
  "key": "7A",  // ← This is what we use
  "tags": { ... }
}
```

**Example keys in your library:** 7A, 6A, 8A, 8B, 1A, 12B, etc.

---

## Implementation Approach

### Step 1: Build a Key Compatibility Map

Create a lookup function that, given a key, returns all compatible keys:

```
getCompatibleKeys("7A") → ["6A", "7A", "8A", "8B"]
getCompatibleKeys("12B") → ["11B", "12A", "12B", "1A"]
```

**Logic:**
- Parse key string: "7A" = position 7, major (A)
- Return current position + ±1 positions, both A and B variants
- Handle wraparound (position 12 + 1 = position 1)

### Step 2: On Track Click, Identify Harmonic Matches

When user clicks track with key "7A":

```
1. Find all tracks in constellation with compatible keys
2. Store their positions in memory (for highlighting)
3. Pass to rendering engine: { highlightedTrackIds: [14, 27, 43, ...] }
```

### Step 3: Visual Feedback in Constellation

In the background constellation (behind the detail view):

```
• Unselected track: Normal opacity, no connection
• Compatible track: Soft glow, highlight color, or border
• Very compatible (same key): Stronger glow
• Non-compatible: Dim/fade background
```

**Suggested visual:**
- Compatible tracks: `opacity: 1, fill: hsl(120, 70%, 50%)` (green glow)
- Very compatible (same key): `opacity: 1, fill: hsl(120, 100%, 40%)` (brighter green)
- Others: `opacity: 0.2, fill: gray` (fade to background)

### Step 4: Detail View Shows Mix Count

When detail view opens, include:

```
Track: "Solar Pool"
Key: 7A
Mixes well with: 8 other tracks in Afterglow
└─ 2 in same key (7A)
└─ 3 in compatible higher key (8A)
└─ 3 in compatible lower key (6A)
```

Optional: Show a mini-list of the 3–5 closest matches spatially.

---

## UI/UX Pattern

### Baseline State (No Track Selected)
- Constellation shows all 70 tracks
- No connections visible
- Clean spatial view

### After Clicking a Track
- Detail view **overlay** on the right (or bottom)
- Constellation **behind** the detail view
- Compatible tracks **glow** in the constellation
- User sees: "This track mixes with these 8 others"
- User can click a glowing track to switch selection (explore harmonic pathways)

### Interaction Loop
```
1. Click track A (key 7A)
2. See harmonic neighbors glow
3. Click glowing track B (key 8A)
4. Detail view updates; new harmonic map shows (now highlighting 7A, 8B, etc.)
5. DJ explores harmonic pathways visually
```

---

## Why This Works

✅ **Doesn't clutter the baseline view** — Harmonic relationships only appear on demand  
✅ **Reveals intent** — DJ can see "which tracks can I play next?"  
✅ **Supports exploration** — Clicking a compatible track switches focus, revealing new pathways  
✅ **Respects spatial logic** — Harmonic compatibility *and* spatial positioning matter  
✅ **Uses existing data** — All 73 tracks already have keys; no new tagging needed  

---

## Data Structure Notes

### For the JSON:
Already have key; no changes needed.

```json
{
  "num": "1",
  "artist": "...",
  "title": "...",
  "key": "7A",  // Keep this as-is
  "tags": { ... }
}
```

### For the UI State:
Add to your state manager:

```javascript
{
  selectedTrackId: 1,           // Track user clicked
  selectedTrackKey: "7A",       // Its key
  compatibleKeys: ["6A", "7A", "8A", "8B"],  // Derived from Camelot logic
  highlightedTrackIds: [3, 7, 14, 22, ...],  // Tracks in constellation matching compatible keys
}
```

---

## Implementation Priority

### MVP (For Hackathon)
- ✅ Build key compatibility lookup
- ✅ On track click, identify and highlight compatible tracks
- ✅ Simple visual feedback (glow or border on compatible tracks)
- ✅ Show "Mixes well with X tracks" in detail view

### Post-Hackathon Nice-to-Haves
- Draw connection lines between selected track and compatible neighbors (subtle arcs)
- Show harmonic strength (same key = solid line; ±1 = dashed line)
- "Mix pathway" feature: show a sequence of compatible tracks across the constellation
- Audio preview of harmonic transition
- Advanced Camelot logic (±5 "harmonic surprise" transitions)

---

## Example Scenario

**User opens Afterglow constellation:**
- Sees 70 tracks spread across Bridge+Lock-in to Reset+Wanderers

**User clicks track at Bridge+Lock-in (key 7A):**
- Detail view shows: "Solar Pool" | Key 7A | Mixes well with 8 tracks
- In constellation, 8 tracks glow softly (harmonically compatible)
- Those 8 tracks are scattered across the spatial view but all have key 6A, 7A, 8A, or 8B

**User clicks a glowing neighbor (key 8A, in Wanderers zone):**
- Detail view switches to that track
- New harmonic map highlights (now showing 7A, 8A, 8B, 9A, 9B)
- DJ thinks: "I can transition from that Bridge track → this Lock-in track → this Wanderers track, and they all mix harmonically"

---

## Questions for Alignment

1. **Visual style:** Glow? Border highlight? Color wash? Opacity fade?
2. **Detail view placement:** Overlay on right, bottom, or modal?
3. **Show harmonic strength:** Simple yes/no, or differentiate "perfect mix" vs. "compatible"?
4. **MVP scope:** Just highlight in constellation, or also show a mini-list in detail view?

---

## References

- **Camelot Wheel:** Standard in DJ software (Serato, rekordbox, djay)
- **Mixing in Key:** Industry-standard practice for harmonic blending
- **Key detection:** Your data already has keys; no audio analysis needed

---

**Ready to implement?** Let me know if you want to adjust the visual pattern or add anything. Valerie, this should be straightforward to implement once the baseline constellation is working.

You've got this. 🎵
