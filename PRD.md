# Product Requirements Document: Afterglow

**Version:** 1.0  
**Status:** Greenlit  
**Date:** May 15, 2026  
**Hackathon:** Music Hackspace Music Technology Hackathon, Lisbon

---

## 1. Overview

**Product Name:** Afterglow

**One-Line Description:** A spatial DJ library browsing system organized by timeline of day and performance contexts instead of metadata alone.

**Tagline:** "Organize your library by how you actually DJ. Discover what you have. Feel confident in uncertain gigs."

---

## 2. Problem Statement

### The Real Problem
DJs organize their libraries with technical metadata (genre, BPM, key) because that's what existing tools support. But when actually preparing to perform, DJs navigate by emotional and situational logic: **When would I play this? Why? What's the crowd state?**

This mismatch means that within a single moment (e.g., an Afterglow set), a DJ's library becomes invisible. You know the genre, BPM, and key—but not which tracks bridge moments, which lock people in, and which work for a wandering crowd. Great tracks get lost because they don't fit metadata folders.

**Current friction:**
- Great tracks are buried in lists organized by genre/BPM, not by how you actually navigate them
- Organization is mentally heavy; you spend prep time scrolling instead of selecting
- You rediscover the same 20 tracks because you don't see what else you have
- Browse experience is linear (lists, filters) not exploratory or spatial
- Confidence in your selections depends on memory, not clarity

### Why It Matters
An emerging DJ who feels lost in their own library stops DJing. A confident DJ discovers cross-genre combinations they wouldn't have found otherwise. Organization directly impacts creativity and performance. When you can see your full Afterglow library mapped by "How do I actually navigate this?" instead of "What genre is it?"—you prep faster, rediscover forgotten gems, and feel genuinely ready.

---

## 3. Solution Overview

### What Afterglow Is
A three-layer library browsing system:

1. **Timeline of the Day** — Choose your scenario (Pool Party, Sunrise Reset, Afterglow, etc.)
2. **Spatial Mood Constellation** — Spatial arrangement of your library by performance contexts (who's here? what role does this track play?)
3. **Track Details** — Click to see artist, duration, tags, play count, and why it belongs in this zone

### What Afterglow Is NOT
- A recommendation engine (DJ decides; system organizes)
- A mixing or playback tool (prep tool, not performance tool)
- An all-in-one DJ platform (scoped library browsing only)
- A mood tagging system (tags reflect DJ decision-making: when/why/crowd)

### Core Value
- **For the DJ:** Within a single set (e.g., Afterglow), navigate your library by *how you actually think*. Find the track that bridges moments. Rediscover forgotten gems. Feel confident in your selections.
- **For emerging DJs:** Reduce mental load of organizing. See your full library instantly. Make better use of what you already have.
- **For the product:** Organize libraries by DJ decision-making (when/why/crowd) instead of metadata alone. Spatial browsing is faster and more exploratory than lists.

---

## 4. Target User

### Primary User
**Emerging and casual DJs** (playing 1–4 gigs/month, 500–5,000 tracks)
- Feel lost in their own library (great tracks buried in lists)
- May feel overwhelmed by organization systems
- Needs clarity and confidence within a single moment/set
- Thinks in moods and moments ("What role does this play?"), not BPM/genre
- Wants to rediscover underplayed material easily

### Secondary User
**Experienced DJs** who want to:
- Rediscover underplayed material in context
- Explore cross-genre combinations they wouldn't find in metadata views
- Organize around performance contexts (not just metadata)

### All Users
Anyone who wants to **see their library clearly, organized by how they actually navigate it**.

---

## 5. User Stories (MVP Scope)

### Primary Story: Clarity and Rediscovery Within a Single Set
**As a** DJ prepping an Afterglow set (or any single moment)  
**I want to** see my full library organized by how I *actually navigate it* (what role, what crowd state)—not genre/BPM  
**So that** I discover tracks I'd forgotten, understand why they belong together, and feel confident in my selections

**Acceptance Criteria:**
- I can scan 70 Afterglow tracks spatially in <2 minutes and find exactly what I need
- I can understand why each track is positioned where it is (see its tags and role)
- I discover new ways to use tracks I already own because of how they're positioned
- The constellation shows me relationships I wouldn't see in a list (e.g., "there are lots of Bridge + Lock-in tracks here")
- I can navigate by performance context (role + crowd) instead of scrolling lists

**Real-world example:** I'm prepping an Afterglow set. I open the constellation. I instantly see tracks grouped by "Bridge + Lock-in" vs. "Reset + Wanderers." I spot a track I own that's perfectly positioned for a Bridge moment with a focused crowd. I prep in 15 minutes instead of 45.

---

### Secondary Story: Discover Relationships in Your Library
**As a** DJ browsing the constellation  
**I want to** find tracks I hadn't considered for certain moments because they weren't categorized that way  
**So that** I have fresh perspectives on my library and discover new combinations

**Acceptance Criteria:**
- Tracks are positioned clearly by role and crowd state
- I can see relationships I wouldn't find in a list ("Oh, these Bridge + Lock-in tracks work together")
- I discover 3–5 tracks per context that I'd use differently because of where they're positioned
- The spatial view reveals patterns in my library I didn't consciously know I had

---

### Supporting Story: Understand the Logic Behind Track Placement
**As a** DJ browsing the constellation  
**I want to** click a track and see why it's positioned in this zone  
**So that** I understand the system's logic and trust the organization (instead of feeling like a black box)

**Acceptance Criteria:**
- Click track → detail view shows artist, duration, tags
- Tags clearly explain: When (Time/Setting)? Why (Journey Role)? What crowd (Crowd State)?
- Can see play count so I know if this is underplayed
- The tags directly justify the position

---

## 6. Functional Requirements

### Timeline View
- **Display:** Seven time/setting phases (Sunrise Reset, Warm-up, Festival Brunch, Pool Party, Afterglow, Club, Late Night Warehouse)
- **Interaction:** Click phase → loads constellation view
- **Behavior:** Visual feedback on selected phase

### Constellation View (Afterglow Only)
- **Display:** Spatial arrangement of 70 Afterglow tracks
- **Zones:** Three visually distinct zones (Arrivals, Lock-in, Wanderers) across the Y-axis
- **Zone labels:** Clear text labels or visual grouping
- **Spatial logic:** X-axis = Journey Role (Opener → Home Stretch), Y-axis = Crowd State (Arrivals → Wanderers)
- **Interaction:** Hover shows nearby tracks; click shows details
- **Visual feedback:** Responsive (<100ms latency)

### Track Detail View
- **Display:** Artist, duration, tags (Time/Setting, Journey Role, Crowd State)
- **Interaction:** Click to view, back to constellation

### Spatial Positioning
- **Approach:** Intentional (hardcoded/manual), not algorithmic
- **Justification:** Every track position traceable to its tags
- **Result:** DJ can understand "why is this track positioned here?"

---

## 7. Non-Functional Requirements

### Performance
- Hover interaction response: <100ms
- Navigation between views: smooth, <300ms
- No crashes or broken states during demo

### Data
- 150 tracks in demo library
- Track metadata: artist, title, duration, play count, three tags (Time, Role, Crowd)
- Format: JSON or similar (loadable in frontend)

### Responsiveness
- Works on laptop/desktop (primary)
- Readable at presentation distance (10+ feet away)
- Color contrast is accessible

---

## 8. Out of Scope (MVP)

### Explicitly NOT Building
- Audio playback / music player
- AI or algorithmic recommendations
- Real djay SDK integration
- User accounts or persistent storage
- Custom tag creation
- Search or filter UI
- Analytics dashboard
- Multiple fully-built time phases (Pool Party only)

### Why These Are Out of Scope
- Keep technical scope light (24-hour sprint)
- Solve the core problem (library browsing) before adding features
- Don't confuse the user with extra features
- Maintain focus on demo narrative

### Post-Hackathon Roadmap
- Real djay integration
- User accounts + cloud sync
- All five time phases
- Optional algorithmic tag suggestions
- Analytics and insights

---

## 9. MVP Scope Summary

### What You're Building
1. **Timeline view** showing seven time/setting phases (future roadmap visible; Afterglow selected)
2. **Afterglow constellation** with three zones (Arrivals, Lock-in, Wanderers), 70 real tracks
3. **Track detail view** showing artist, tags, confidence scores
4. **Demo library:** 70 real tracks from user's Afterglow collection, manually tagged
5. **Hover interaction** showing spatial proximity
6. **Clear zone labels** (Arrivals, Lock-in, Wanderers)

### What You're NOT Building
- Other time phases (fully built) — shown on timeline but greyed out/future
- Audio or playback
- AI or recommendations
- User signup or persistence
- djay integration
- Search or advanced filtering

### Why This Scope
- Proves the concept works for one real moment (Afterglow)
- Fits in 24-hour sprint (35–50 hours)
- Shows quality over quantity (one beautifully built phase > three scattered)
- Solves the core problem (clarity + rediscovery within a single set)

---

## 10. Key Decisions (Greenlit)

| Decision | Status | Why |
|----------|--------|-----|
| Pool Party phase only | ✓ Greenlit | Proves concept, realistic scope, one beautiful demo |
| Intentional spatial positioning | ✓ Greenlit | Controllable, traceable logic, DJ understands placement |
| Real track demo library | ✓ Greenlit | Authenticity matters; dummy data would be obvious |
| Three dimensions, nine tags | ✓ Greenlit | Reflects real DJ thinking; not reductive |
| Manual tagging | ✓ Greenlit | Quality > speed; DJ curation is honest |
| "DJ decision-making" language | ✓ Greenlit | Respects musical sophistication; not "mood" reduction |
| Emphasis on DJ artistry in demo | ✓ Greenlit | System organizes; DJ decides (no automation) |

---

## 11. Success Criteria (For Hackathon)

### Minimum Success
- Judges understand the core idea (three-layer model)
- Demo runs without crashes
- Rediscovery moment resonates

### Target Success
- A judge asks "when can I try this?"
- Real DJ in the crowd engages with the concept
- Judges mention it to other judges

### Must-Have Technical Success
- Timeline view works reliably
- Constellation loads with real tracks
- Zone labels are clear
- Hover interaction is responsive
- Detail view shows all track info
- Demo script is practiced and under 7 minutes

---

## 12. Demo Narrative (High-Level)

### 30-Second Hook
You're prepping an Afterglow set. You have 70 tracks. You know their genre and BPM. But you can't see which ones bridge moments or work with a wandering crowd. You spend 45 minutes scrolling. Afterglow shows you your library organized by *how you actually navigate it*—in minutes, you prep and rediscover forgotten gems.

### 60-Second Full Story
**Problem:** DJs organize by metadata (genre, BPM). But that's not how you navigate when prepping. You think: What role does this track play? Does it lock people in or work with a wandering crowd? When in the arc?

**Insight:** If we organize by *DJ decision-making* (role, crowd state) instead of metadata, you see your library clearly, prep faster, and rediscover material you'd forgotten.

**Solution:** Spatial constellation: X-axis = Journey Role (Opener → Home Stretch), Y-axis = Crowd State. Same 70 tracks, arranged by how you actually think about them.

**Benefit:** You see relationships you'd never find in a list. You rediscover underplayed tracks that are perfect. You prep in 15 minutes instead of 45.

### 5–7 Minute Walkthrough
1. **Setup:** "I'm prepping an Afterglow set. I have 70 tracks. I know genre and BPM, but not how they fit together." (30 sec)
2. **Show the problem:** "Lists don't show me the relationships. This track is great, but where does it sit in my arc?" (30 sec)
3. **Open the constellation:** "Same 70 tracks, different view. X-axis = Journey Role. Y-axis = Crowd State." (60 sec)
4. **Explain the logic:** "I can instantly see all my Bridge tracks, all my Lock-in moments. That's how I think." (60 sec)
5. **Hover interaction:** Show nearby tracks and how they relate in space (30 sec)
6. **Find a well-positioned track:** Click on a track positioned at Bridge + Lock-in, show why it's perfect (60 sec)
7. **The moment:** "This track is positioned exactly where it belongs—Bridge moment, focused crowd. That's the clarity spatial browsing gives you." (30 sec)
8. **Close:** "That's the power of organizing by DJ decision-making, not metadata. See your library clearly." (15 sec)

---

## 13. Team & Timeline

### Team Composition
- **PM / Visionary:** Curate demo library, own narrative, make product calls
- **Visualizer / Creative Technologist:** Design spatial encoding, build UI, implement interactions

### Timeline (Hackathon)
- **Hours 0–2:** Planning & setup (confirm spatial encoding, start library)
- **Hours 2–8:** Heavy lift (finish library, build timeline + constellation structure)
- **Hours 8–16:** Integration (load real data, add zone labels, implement hover)
- **Hours 16–22:** Testing & refinement (walkthrough, fix bugs, polish)
- **Hours 22–24:** Final polish & backup (one full run-through, screenshots, fallback plan)

### Success Definition
- **By hour 24:** Walkable demo, no crashes, rediscovery moment testable, script practiced

---

## 14. Assumptions & Risks

### Assumptions
- Real CC/royalty-free tracks are available and findable (Creative Commons Music, Bandcamp, Free Music Archive)
- Spatial browsing is genuinely faster than list browsing (hypothesis to prove in demo)
- Manual tagging for 150 tracks is feasible in 6–8 hours
- Judges value understanding real DJ problems over visual polish

### Risks & Mitigations
| Risk | Mitigation |
|------|-----------|
| Demo library tagging takes too long | Have pre-curated list ready; alias method (tag 50, extrapolate) |
| Spatial interaction is sluggish | Prioritize responsiveness; test hover latency early |
| Rediscovery track doesn't land | Have 3–5 backup candidates identified during curation |
| Tech breaks during demo | Screenshots, second laptop, printed fallback |
| Judge doesn't understand spatial logic | Clear zone labels, demo script explains logic |

---

## 15. Open Questions (For Alignment)

These are resolved or will be during planning/build:

- [ ] Exact spatial encoding details (will be confirmed with visualizer)
- [ ] Final track count (150 target; 100 minimum)
- [ ] Which Creative Commons sources to use
- [ ] Exact rediscovery track (will be chosen during curation)
- [ ] Tech stack (React? Vue? HTML+JS?)
- [ ] Responsive breakpoints (focus on desktop; mobile nice-to-have)

---

## 16. Glossary

| Term | Definition |
|------|-----------|
| **Constellation** | Spatial arrangement of tracks by performance contexts (zones) |
| **Zone** | Cluster within constellation (Arrivals, Lock-in, Wanderers) |
| **Time/Setting** | When/where you'd play a track (Pool Party, Sunrise Reset, etc.). Pick 1–2, each with confidence (1-10). |
| **Journey Role** | What a track does in a set (Opener, Bridge, Reset, Home Stretch). Pick 1–2+, each with confidence (1-10). |
| **Crowd State** | Who's here and what's their attention (Arrivals, Lock-in, Wanderers). Pick 1–2, each with confidence (1-10). |
| **Confidence** | 1-10 rating for each tag indicating certainty. 1=barely fits, 10=definitely. Allows "Pool Party (9) + Afterglow (4)". |
| **MVP** | Minimum viable product for hackathon (Afterglow constellation, 70 tracks) |

---

## 17. Sign-Off

**Product Owner (Vision):** Jasmine Sabio  
**Status:** Approved for implementation

**Team Alignment:** Pending (read PRD, then align in meeting)

**Next Step:** Planning mode with Claude → detailed implementation plan

---

**For questions or changes:** Update this PRD. It lives with the project.
