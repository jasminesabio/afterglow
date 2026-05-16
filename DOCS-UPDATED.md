# Documentation Update: Option A Narrative (May 16, 2026)

**Change:** Shifted from multi-context demo (Pool Party/5 phases) to **single-context focus (Afterglow/within-context clarity)**

**Status:** ✅ All docs aligned. Ready to push.

---

## Updated Files

### Core Documents

**PRD.md**
- Problem Statement: Shifted from "ready for any scenario" → "clarity within a single moment"
- User Stories: Reframed primary story from "spontaneous gigs" → "rediscovery within Afterglow"
- Demo narrative: From "Burning Man across contexts" → "prep and clarity within one set"
- Constellation View: Pool Party (40–50) → Afterglow (70 tracks)
- MVP Scope: 150 tracks → 70 tracks
- Target User: Refined to emphasize within-context clarity

**GREENLIGHT.md**
- MVP Scope: "Pool Party constellation" → "Afterglow constellation"
- Demo Library: 150 → 70 tracks
- Tagging Approach: Manual → Manual + Hybrid Efficiency
- Demo Scenario: Pool Party walkthrough → Afterglow walkthrough
- Rediscovery Track: Pool Party context → Afterglow context
- Timeline: Library (6–10h) → Tagging (6–8h)
- TL;DR: Updated all references

**06-demo-story.md (Demo Narrative)**
- 30-sec pitch: Reframed from spontaneous gigs → clarity within Afterglow
- 60-sec pitch: New framing around within-context visibility vs. metadata
- 5–7 min walkthrough: Afterglow story (instead of Pool Party)
- Emphasis: "Your library, your artistry" (not automation)

### Supporting Documents

**TAGGING-WORKFLOW.md**
- Total tracks: 73 → 70 (select best for constellation)
- Time/Setting guidance: Afterglow primary; rare multi-tags
- Hybrid tagging templates: 4–6 clusters with templates (not 150 individual tags)
- Timeline: 8–10 hours → 6–8 hours
- Sample completed rows: Updated for Afterglow context
- Tools: Added batch-tagger.html reference

**AFTERGLOW-TAGS-73.csv (NEW)**
- 73 tracks from Afterglow playlist
- Sorted alphabetically by Track Title
- Metadata pre-populated: Artist, Duration, Genre, BPM, Key
- Empty tagging columns: Time/Setting, Journey Role, Crowd State, Notes
- Proper CSV quoting for artist names with commas (Kaskade, deadmau5, etc.)
- Ready for batch-tagger.html or direct spreadsheet editing

**batch-tagger.html (FIXED)**
- Fixed CSV parser to properly handle quoted fields with commas
- Now correctly parses artist names like "DJ Tennis, Joseph Ashworth, LP Giobbi"
- Loads AFTERGLOW-TAGS-73.csv without column misalignment
- Ready for visual tagging workflow

---

## Key Narrative Shift

### Old (Option B/C): Multi-Context
- **User story:** "I might get asked to play sunrise or 4 AM at Burning Man"
- **Value prop:** "Be ready for any scenario across multiple times of day"
- **Demo:** Timeline → 5 phases visible; Pool Party fully built
- **Scope:** 150 tracks across multiple contexts

### New (Option A): Within-Context Clarity
- **User story:** "I'm prepping an Afterglow set; I can't see what I actually have"
- **Value prop:** "See your 70-track library clearly by role & crowd state; rediscover forgotten gems"
- **Demo:** Timeline visible (7 phases); Afterglow fully built, polished, complete
- **Scope:** 70 tracks from Afterglow playlist, deeply explored

---

## Why This Works

1. **Tighter narrative:** One beautiful constellation > multiple scattered ones
2. **Real rediscovery:** 70 tracks, find 3–5 gems = powerful moment
3. **Spatial magic:** X=Role, Y=Crowd becomes visible & obvious with full Afterglow
4. **Judges see the concept:** Timeline shows future phases; Afterglow proves it works
5. **DJ-centric:** "Clarity within your moment" resonates with judges' values

---

## What Didn't Change

- ✓ Three-dimensional tagging system (Time/Setting, Journey Role, Crowd State)
- ✓ Per-tag confidence scores (1–10)
- ✓ Spatial positioning logic (X=Role, Y=Crowd)
- ✓ Judge context and resonance thinking
- ✓ DJ decision-making language (not "mood")
- ✓ Rediscovery mechanic (underplayed tracks)

---

## Ready-to-Go Checklist

### Documentation ✅
- [x] PRD.md — Afterglow focus, within-context clarity narrative
- [x] GREENLIGHT.md — 70 tracks, hybrid tagging, Afterglow constellation
- [x] 06-demo-story.md — 30s/60s/5–7m pitches (Afterglow narrative)
- [x] TAGGING-WORKFLOW.md — Hybrid approach, templates, 6–8 hour timeline
- [x] DOCS-UPDATED.md — Change summary (this file)

### Tools & Data ✅
- [x] batch-tagger.html — Fixed CSV parser, ready for tagging
- [x] AFTERGLOW-TAGS-73.csv — 73 tracks, alphabetical, properly quoted
- [x] track-tagger.html — Single-track fallback (if needed)

### What's NOT in the repo (external)
- Rekordbox XML/afterglow.txt exports (used for metadata, not pushed)
- Tagged output JSON (generated during tagging)

---

## Immediate Next Steps for Hackathon

1. **Tagging (6–8 hours)**
   - Open batch-tagger.html
   - Load AFTERGLOW-TAGS-73.csv
   - Group by genre, create 4–6 templates, apply + spot-check
   - Identify 3–5 rediscovery stars (low play count, perfect placement)

2. **UI Build (12–14 hours)**
   - Timeline view (7 phases, Afterglow interactive)
   - Afterglow constellation (70 tracks, X=Role, Y=Crowd)
   - Zone labels (Arrivals, Lock-in, Wanderers)
   - Hover interaction + track detail view

3. **Polish & Demo (3–5 hours)**
   - Responsive interactions (<100ms hover latency)
   - Practice demo walkthrough (5–7 min script)
   - QA: Spatial browsing faster? Rediscovery genuine?

---

**Updated by:** Claude  
**Date:** May 16, 2026, 1:15 PM  
**Status:** ✅ Ready to push to GitHub
