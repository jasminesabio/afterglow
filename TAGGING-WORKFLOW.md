# Afterglow Tagging Workflow (70 Tracks)

**Status:** Ready to tag  
**File:** `AFTERGLOW-TAGS-73.csv` (73 tracks; select 70 best for constellation)  
**Total tracks to tag:** 70  
**Columns ready:** Artist, Track Title, Duration, Genre, BPM, Key  
**Columns to fill:** Time/Setting, Journey Role, Crowd State, Notes

---

## Quick Start

1. **Open the file:** `AFTERGLOW-TAGS-73.csv` in Excel or Google Sheets (use batch-tagger.html for visual UI)
2. **Use the tag options:**
   - **Time/Setting:** Afterglow (primary); maybe Sunrise Reset for a few ethereal tracks
   - **Journey Role:** Bridge (most), Reset, Home Stretch, Opener
   - **Crowd State:** Lock-in, Wanderers, Arrivals

3. **Format for multi-select:** Separate with `;` if a track fits multiple categories
   - Example: `Afterglow;Sunrise Reset` for Time/Setting (rare—only if genuinely bridges)
   - Example: `Bridge;Reset` for Journey Role (if it does both)
   - Example: `Lock-in;Wanderers` for Crowd State (if it works in both)

4. **Add confidence scores:** Add confidence (1-10) in parentheses after each tag
   - Example: `Afterglow (9);Sunrise Reset (4)` = primarily Afterglow, but hints of sunrise
   - Example: `Bridge (9)` = very confident this is a bridge
   - Most Afterglow tracks: `Afterglow (9)` (single tag, high confidence)

---

## Hybrid Tagging Strategy (6–8 hours for 70 tracks)

### Phase 1: Group & Analyze (1–1.5 hours)

Sort the CSV by Genre and BPM to identify patterns. For Afterglow, you'll probably see:

1. **Identify clusters** (listen to Genre/BPM groupings)
   - Deep House (120–122 BPM) — lingering, groovy, Wanderers
   - Melodic House (122–125 BPM) — builds slightly, Bridge energy
   - Hip-Hop/Rap (95–128 BPM) — lyrics, groove shifts, Reset potential
   - Ambient/Ethereal (90–110 BPM) — reflective, closing, Home Stretch
   - Soul/Funk Hybrids — groove + vocals, depends on energy

2. **Sample each cluster**
   - Listen to 2–3 representative tracks per group
   - Ask: "Does this feel like a Bridge moment or more of a lingering Wanderers vibe?"
   - Note: "Fast but melodic" vs. "Slow and spacious"

### Phase 2: Create Templates (1–1.5 hours)

For each cluster, write ONE template tag set. Apply it to all similar tracks:

**Template A: Deep House (120–122 BPM, 5–7 tracks)**
- `Afterglow (9) | Bridge (6) | Wanderers (8)`
- Rationale: Groovy, lingering. Doesn't push energy; works ambient. Deep vibe fits Wanderers well.

**Template B: Melodic House (122–125 BPM, 6–8 tracks)**
- `Afterglow (9) | Bridge (8) | Lock-in (7)`
- Rationale: Stronger beat, melodic. These bridge moments. People lock into them.

**Template C: Hip-Hop/Rap (95–128 BPM, 3–5 tracks)**
- `Afterglow (7) | Reset (8) | Lock-in (8)`
- Rationale: Rhythmic, lyrical. Can shift mood or cool things. Demands attention but might reset energy.

**Template D: Ambient/Ethereal (90–110 BPM, 2–4 tracks)**
- `Afterglow (9);Sunrise Reset (5) | Home Stretch (7) | Wanderers (9)`
- Rationale: Floating, closing. Perfect Afterglow. Some genuinely work for sunrise. Background magic.

**Template E: Soul/Funk Hybrids (100–120 BPM, 3–5 tracks)**
- `Afterglow (9) | Bridge (7) | Lock-in (8)` OR `Wanderers (7)`
- Rationale: Groove + emotion. Depends on the specific track. Listen carefully; adjust confidence per track.

### Phase 3: Apply & Verify (3–5 hours)

1. **Apply templates to all tracks in each group**
   - Tag all 4 Deep House tracks with the Deep House template
   - Tag all 8 Melodic House tracks with the Melodic House template
   - Etc.

2. **Spot-check 2–3 tracks per group**
   - Listen to 15–30 seconds of track
   - Confidence score high if template fits perfectly (8–10)
   - Adjust confidence down (5–7) if something feels different
   - Add notes in the Notes column if you deviate from template

3. **Flag outliers**
   - If a track in the Deep House group feels like a Home Stretch instead of Wanderers, note it
   - Adjust confidence or add secondary tags

---

## Key Principles

### Confidence Scores Reflect Uncertainty, Not Perfection
- **9–10:** "This absolutely fits this context"
- **7–8:** "Strong fit; I'm confident"
- **5–6:** "Could work; reasonable fit but not obvious"
- **3–4:** "Weak fit; reaches a bit"
- **1–2:** "Barely; only if desperate"

Most of your Afterglow tracks will be 8–9 for Time/Setting because they're literally from the Afterglow playlist.

### Multi-tagging is Honest, Not Exhaustive
- **Do:** Tag Bridge + Reset if genuinely both (e.g., "Bridge (9) + Reset (5)")
- **Don't:** Tag every possible combination. Be selective.
- Most tracks are primarily one role. If a track is 80% Bridge and 10% Reset, that's worth the multi-tag.

### Afterglow is the Default Time/Setting
- 73 tracks are from your Afterglow playlist
- Default: `Afterglow (9)`
- Only add secondary tags if a track genuinely also works for Sunrise Reset (emotional quality, timeless vibe)
- Most will be single-tagged

---

## Sample Tagging Completed

Here's what 5 completed rows might look like (from your Afterglow playlist):

```
#,Artist,Track Title,Duration,Genre,BPM,Key,Time/Setting,Journey Role,Crowd State,Notes
1,The Dead Rose Music Company,Just a Bitter Love,07:55,House,109.33,6A,Afterglow (9),Bridge (7),Wanderers (8),Deep house groove—lingers
3,Disclosure,Boiling (feat. Sinead Harnett),03:46,Electronic,128.00,11A,Afterglow (9),Bridge (9),Lock-in (8),Melodic house—locks people in
5,rusowsky & Ralphie Choo,Dolores,03:38,Pop,122.00,10A,Afterglow (9);Sunrise Reset (5),Reset (8),Wanderers (9),Ethereal; could work both
8,FKJ,Lying Together,04:28,,102.00,2A,Afterglow (9),Home Stretch (7),Wanderers (9),Hero candidate—tender closing
10,Radiohead,Videotape (Original Mix),04:42,Electronica,154.77,12A,Afterglow (8),Bridge (5),Lock-in (6),Spacey but structured
```

**Notes on these examples:**
- Most have `Afterglow (9)` as primary (high confidence, from Afterglow playlist)
- Row 5 has secondary `Sunrise Reset (5)` (genuine bridge potential)
- Row 8: perfectly positioned (can be highlighted in demo)
- Confidence scores are honest, not all 8–9

---

## Tools Available

### Option 1: Use track-tagger.html (Visual UI)
1. Open `track-tagger.html` in your browser
2. Select tags with confidence sliders for each track
3. Generates JSON output you can copy-paste into the CSV (Notes column)

### Option 2: Fill CSV Directly
- Type tags and confidence scores directly into the CSV columns
- Faster if you're comfortable with the tagging system
- Recommended for clusters (faster to fill once you've identified the pattern)

---

## Timeline Estimate

| Phase | Time | Activity |
|-------|------|----------|
| 1. Group & Analyze | 1–1.5 hours | Sort CSV, listen to 2–3 per cluster, identify patterns |
| 2. Create Templates | 1–1.5 hours | Write 4–6 template tag sets (one per cluster) |
| 3. Apply & Verify | 3–5 hours | Apply templates, spot-check 2–3 per cluster, adjust confidence |
| **Total** | **6–8 hours** | **Complete 70 tracks ready for UI build** |

---

## Next Steps

1. **Download AFTERGLOW-TAGS-73.csv** and open in a spreadsheet (or use batch-tagger.html)
2. **Sort by Genre + BPM** to identify clusters (5–6 groups expected)
3. **Listen to 2–3 representatives** from each cluster
4. **Create 4–6 template tag sets** (write them down; one per cluster)
5. **Apply templates** to all tracks in each cluster
6. **Spot-check 2–3 per cluster** and adjust confidence scores as needed
7. **Note well-positioned tracks** (for potential demo hero moment)
8. **Save when done** (CSV or JSON output from batch-tagger.html)
9. **Import into constellation UI** for final spatial arrangement

---

## Tools

- **batch-tagger.html:** Visual multi-select UI with confidence sliders. Easier for complex tags.
- **Spreadsheet:** Direct CSV editing if you prefer typing.
- Either works; batch-tagger handles per-tag confidence more visually.

---

## Questions?

Refer back to:
- **Tag definitions:** `03-mood-taxonomy.md` (detailed descriptions of all 9 tags)
- **Confidence guidance:** See "Key Principles" section above
- **Format examples:** `DEMO-LIBRARY-15.md` (shows 15 completed tracks with tags)
- **Afterglow focus:** Remember—most tracks are `Afterglow (9)`. The Journey Role + Crowd State differentiate.

---

**Once tagging is complete:** The constellation UI will load your tags and arrange tracks spatially (X = Role, Y = Crowd). You'll see patterns emerge—clusters of Bridge + Lock-in, zones of Home Stretch + Wanderers. That's when the magic happens.

You've got 70 tracks and 6–8 hours. Focused clustering makes this doable and honest. Let's go. 🎵
