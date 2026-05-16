# GREENLIGHT: Approved Decisions (No Debate)

**These decisions are locked in.** You don't need to debate them. They've been vetted against both "solves real DJ problem" and "feasible in 24-hour sprint."

**Date Greenlit:** May 15, 2026  
**Team:** Jasmine (PM) + Visualizer/Technologist

---

## 1. MVP Scope

✓ **Build Afterglow constellation only** (not all seven time phases)

- Timeline view shows all seven phases as options
- Only Afterglow has a complete, fully-built constellation (70 tracks)
- Other phases can be greyed out or sketched (future work)
- This scope proves the concept works for within-context clarity and rediscovery
- Fits 24-hour sprint timeline

---

## 2. Spatial Positioning

✓ **Positions are intentional, not algorithmic**

- Hardcoded or manually arranged (no force-directed graphs)
- X-axis = Journey Role (Opener → Home Stretch)
- Y-axis = Crowd State (Arrivals → Wanderers)
- Color/grouping = Time/Setting (Afterglow)
- Every position is traceable to track's tags
- DJ can understand "why is this track positioned here?"

---

## 3. Demo Library

✓ **Real tracks, 70 total, manually tagged**

- Use Creative Commons, royalty-free, or licensed music
- Real artist names (no dummy data)
- Authentic DJ curation from your Afterglow playlist (you listen, you tag)
- Mix of genres (house, garage, soul, funk, ambient, breaks, world)
- Include 3–5 underplayed candidates (play count < 5) as rediscovery heroes
- Tagging approach: Manual + hybrid efficiency (answer three questions per cluster/template)

---

## 4. Tagging System

✓ **Three dimensions (locked in), with per-tag confidence scores (1-10)**

### Time/Setting (pick 1–2, each with confidence)
- Sunrise Reset
- Warm-up
- Festival Brunch
- Pool Party
- Afterglow ← MVP focus (70 tracks from your Afterglow playlist)
- Club
- Late Night Warehouse

Most Afterglow tracks fit one time/setting (tag as Afterglow 9). A few might genuinely work in multiple contexts (e.g., ethereal tracks that also work for Sunrise Reset). Tag both with confidence: "Afterglow (9) + Sunrise Reset (6)"—primarily Afterglow but could bridge into sunrise.

### Journey Role (pick 1–2+, each with confidence)
- Opener
- Bridge
- Reset
- Home Stretch

A track can legitimately serve multiple roles. "Bridge (9) + Reset (4)"—primarily a transition but secondarily works as a recalibration moment.

### Crowd State (pick 1–2, each with confidence)
- Arrivals
- Lock-in
- Wanderers

A track might work in multiple crowd states: "Lock-in (8) + Wanderers (5)"—best with focused crowd but still works when people are chatting.

### Confidence Scoring
**Each selected tag gets its own 1-10 confidence score.** This allows nuance at every level:
- "This is 90% Pool Party (9) but could work Sunrise Reset (4)"
- "This is equally Opener and Bridge (both 8)"
- "This works best Lock-in (9) but also fine with Wanderers (6)"

**MVP scope:** Afterglow constellation only. Other time/settings available for future phases. **No custom tags.** These nine tags are sufficient. Post-hackathon: explore user customization and multi-phase build.

---

## 5. Demo Scenario

✓ **Afterglow walkthrough**

- "You're prepping an Afterglow set. You have 70 tracks organized by genre/BPM."
- "15-minute prep window. You need to understand the shape of your library and find the right track for a bridge moment."
- Real constraint: spatial discovery is faster than scrolling lists
- Demo shows full three-layer flow (Timeline → Constellation → Track Detail)
- Ends with rediscovery moment + clarity (underplayed track that's perfectly positioned)

---

## 6. Hero Track for Demo

✓ **Ready to identify during UI demo**

- Requirements: Afterglow context, genuinely positioned well (Bridge or Reset role), works with Lock-in or Arrivals crowd
- You'll identify this during demo walkthrough (click a well-positioned track)
- Must be real track from your Afterglow collection (not contrived)
- Will be the moment in the walkthrough where spatial positioning makes sense ("Look, this track is perfectly positioned for this moment")

---

## 7. Team & Timeline

✓ **24-hour sprint with clear role split**

**PM / Visionary (Jasmine):**
- Tag demo library (70 Afterglow tracks, use hybrid efficiency approach)
- Own demo narrative (one focused story for Afterglow)
- Make product decisions during build
- Identify 3–5 rediscovery candidates
- QA: Does it solve within-context clarity + rediscovery?

**Visualizer / Creative Technologist (Teammate):**
- Design spatial encoding (confirm X/Y/color mapping)
- Build timeline view (all seven phases, only Afterglow interactive)
- Build Afterglow constellation (70 tracks)
- Implement zone labels + hover interaction
- Polish interactions (responsive, no lag)

**Timeline:** 24 hours total  
**Breakdown:** Tagging (6–8h) + UI (12–14h) + Polish (3–5h) + Demo Practice (2–3h)

---

## 8. Tagging Approach

✓ **Manual tagging with hybrid efficiency**

- Group tracks by genre/BPM to identify templates
- Create 4–6 template tag sets (one per cluster)
- Apply templates to cluster members with per-tag confidence scores
- Spot-check 2–3 per cluster; adjust confidence as needed
- Identify 3–5 rediscovery candidates (low play count, perfect placement)
- Time estimate: 6–8 hours for 70 tracks
- Quality + efficiency (templates speed up tagging without sacrificing honesty)

---

## 9. Language & Framing

✓ **"DJ decision-making dimensions" (mandatory)**

### Use this language:
- "DJ decision-making dimensions" (not "mood tags")
- "Performance contexts" (not "vibes")
- "When would you play this?" (not "what mood is it?")
- "Your library, organized your way" (not "algorithm decides")

### Avoid this language:
- "Mood" or "feel"
- "AI-powered" or "recommend"
- "Emotional categories"
- Anything suggesting automation replaces DJ judgment

**Why:** Respects musical sophistication. Frames system as DJ tool, not mood tagger.

---

## 10. Judge Context

✓ **Keep as reference (not primary driver)**

- Reference `08-judge-context-and-decisions.md` to understand why each decision was made
- Useful for demo framing and trade-off decisions
- Don't optimize FOR judges; optimize for DJ problem; judges will see the thinking

---

## What's NOT Greenlit (Out of Scope)

| What | Why Not |
|------|---------|
| Audio playback | Out of scope; prep tool, not player |
| djay integration | Future; design for it, don't build it |
| AI recommendations | Removes DJ agency; contradicts core message |
| User accounts | Not needed for demo; MVP is stateless |
| Custom tags | Adds complexity; nine tags are sufficient |
| Multiple phases | Afterglow only; proves concept within one context |
| Search/filter UI | Spatial discovery is primary; search is secondary |
| Analytics | Nice later; not core to demo |

---

## What Happens If You Hit a Blocker?

### If demo library tagging takes too long:
- You have 50 deeply-tagged "anchor" tracks
- For remaining 100: use pattern-matching (same genre/energy = similar tags)
- Quality drops slightly but proves concept still works

### If spatial interaction is sluggish:
- Prioritize hover latency (<100ms)
- Simplify hover effect if needed (just brighten, no fade)
- Test early and often

### If rediscovery track doesn't feel right:
- You identified 3–5 candidates
- Pick the next best one
- Doesn't need to be perfect; just needs to be real and honest

### If tech breaks during demo:
- You have screenshots of key moments
- Second laptop with demo ready
- Fallback: walk judges through screenshots + explain the demo
- Concept is solid enough to survive tech failure

---

## How to Use This Document

- **Before starting:** Read this (5 min). You don't need to debate these decisions.
- **During build:** If you hit a choice point and think "wait, should we do this differently?" — check here first. Probably already answered.
- **If something feels off:** Don't change greenlit decisions without talking to Jasmine. But small tweaks are fine (e.g., "hover effect is a fade instead of brighten").

---

## TL;DR

✓ Afterglow constellation only (70 tracks)
✓ Intentional spatial positioning (X=Role, Y=Crowd)
✓ Real tracks from your Afterglow playlist, real tags
✓ Nine tags (no custom)
✓ Hybrid tagging efficiency (templates + spot-check)
✓ Within-context clarity + rediscovery demo narrative
✓ DJ decision-making language (not "mood")
✓ 24-hour sprint with role split
✓ Judge context for reference (not primary)


**Everything else** is either implementation detail (planning mode will clarify) or explicitly out of scope.

---

## Sign-Off (Updated May 16)

**Greenlit by:** Jasmine Sabio  
**Tagging complete:** ✅ Yes (73 tracks tagged, afterglow-tags.json ready)  
**Ready for UI build:** Yes  
**Ready to hack:** Yes  

**Next step:** Read TAGGING-COMPLETE.md + PRD + IMPLEMENTATION-BRIEF with your teammate, then start UI build.

You're good to go. 🎵
