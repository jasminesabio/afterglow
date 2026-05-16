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
DJs prepare for gigs by organizing music into playlists—but they don't know which vibe they'll need until they arrive. At a festival or multi-day event, you might play Afterglow, sunrise wind-down, late-night warehouse, or a daytime pool vibe. You need to be ready for *any* of it.

Current solutions: Create 10–15 playlists (which takes hours), or wing it on the fly (which kills confidence). Neither works.

The deeper issue: **Even if you organize by vibe, you navigate within each vibe using genre/BPM.** But when you're actually DJing a moment, you don't think "play all 120 BPM house." You think "I need a Bridge moment that locks people in" or "something that works with a wandering crowd." Great tracks get lost because they don't fit the metadata you're browsing.

**Current friction:**
- Prepping multiple vibes (Afterglow, Sunrise, Club) takes hours of playlist building
- You don't know what you actually have for each vibe until you start browsing
- Within each vibe, genre/BPM organization doesn't match how you navigate
- You're not confident you'll find the right track fast
- Great material stays invisible because you can't see role + crowd relationships

### Why It Matters
A confident DJ with organized vibes can say "yes" to a surprise sunset set. An unprepared DJ has to say no. Organization directly impacts opportunity and performance. When you can see your library organized by **vibe AND by how you navigate each vibe**—you prep multiple scenarios in minutes, not hours. You know what you have. You're ready.

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
- **For the DJ:** Open a vibe and suddenly understand how your tracks relate. See what you own but hadn't reconsidered. Navigate by *how you actually think* (role + crowd state, not genre/BPM) and rediscover your own library. Feel genuinely prepared for any moment in that vibe.
- **For emerging DJs:** Build confidence in your library organization. Quickly prep multiple vibes when festival bookings are uncertain. Make better use of what you already own.
- **For the product:** Organize libraries by DJ decision-making (when/why/crowd), not just metadata. Spatial browsing reveals relationships and supports rediscovery within each vibe.

---

## 4. Target User

### Primary User
**Emerging and casual DJs** (playing 1–8 gigs/month, 500–5,000 tracks)
- Play multi-day events (festivals, Burning Man, camps) with uncertain set times
- Need to prep multiple vibes quickly (Afterglow, Sunrise, Club, Pool, etc.)
- Feel overwhelmed building separate playlists for each scenario
- Wants confidence to say yes to unexpected gigs
- Thinks in moments and contexts ("What if I get the sunrise slot?"), not genre/BPM

### Secondary User
**Experienced DJs** who want to:
- Organize around performance contexts across multiple vibes (not just metadata)
- Prep festival scenarios faster
- Explore cross-vibe combinations

### All Users
Anyone preparing for **uncertain performance scenarios** where they need to be ready for multiple possible moments.

---

## 5. User Stories (MVP Scope)

### Primary Story: Rediscover Your Library Within a Vibe
**As a** DJ who's recently added music to my Afterglow vibe (or hasn't browsed it spatially in a while)  
**I want to** see how all my tracks relate to each other—by the roles they play and the crowd energy they fit—instead of scrolling a linear list  
**So that** I discover combinations I own but hadn't considered, understand my library more deeply, and feel genuinely prepared for any moment in that vibe

**Acceptance Criteria:**
- I can open Afterglow and see all 70 tracks organized spatially at once
- Within the vibe, I navigate by role + crowd state (not genre/BPM)
- I quickly spot tracks I own but hadn't reconsidered for specific moments
- Spatial proximity shows me relationships between tracks I didn't consciously know I had
- Clicking a track explains why it belongs in that zone (tags + reasoning)
- I feel like I'm exploring *my own knowledge*, not fighting a system
- In 10–15 minutes, I've scanned a vibe and rediscovered 3–5 tracks I want to use differently

**Real-world example:** I added 8 new tracks to my Afterglow playlist last week. I open Afterglow and see 70 tracks organized by Bridge + Lock-in vs. Reset + Wanderers. I scan the constellation and notice one of the new tracks is perfectly positioned as a Bridge moment—exactly what I need between two lock-in moments. I find 3 other tracks I'd forgotten about that work beautifully in the Wanderers zone. In 12 minutes, I understand my library way better and feel confident I have material for any moment in that vibe.

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
You're heading to a festival. You might play Afterglow, sunrise wind-down, or late-night warehouse. You need multiple vibes prepped on a USB. Afterglow shows you your library organized by vibe AND by how you actually navigate each vibe—no more hours of playlist building. You're ready for anything.

### 60-Second Full Story
**Problem:** Multi-day events force you to prep multiple scenarios, but you don't know which one you'll need. Building separate playlists takes hours. And within each vibe, you navigate by genre/BPM—not by role and crowd state.

**Insight:** If you organize your library into distinct vibes, AND you organize within each vibe by *how you actually navigate* (role, crowd state), you can prep for uncertainty in minutes.

**Solution:** A system where you see all your vibes at once (timeline), dive into each one (constellation), and navigate spatially within each vibe (X=Role, Y=Crowd State).

**Benefit:** You arrive at a festival with 3–4 organized vibes ready. You feel confident. You can say yes to unexpected opportunities.

### 5–7 Minute Walkthrough
1. **Setup:** "I'm going to a festival. Could play Afterglow, sunrise, late-night, or daytime. I need to be ready for any of it." (30 sec)
2. **Show the system:** "Here's my library organized into vibes. Seven different moments I might need to DJ." (Timeline view, explain the 7 contexts) (40 sec)
3. **Dive into Afterglow:** "Let me show you what I have for Afterglow. 70 tracks organized by role and crowd state." (Open constellation) (40 sec)
4. **Explain the spatial logic:** "X-axis = Journey Role (Opener to Home Stretch). Y-axis = Crowd State (people arriving to wandering). I can instantly see what Bridge moments I have for locked-in crowds." (60 sec)
5. **Hover interaction:** Show nearby tracks and relationships (30 sec)
6. **Find the right track:** Click a track at Bridge + Lock-in, show why it's perfect for that moment (60 sec)
7. **Show multi-vibe readiness:** "And if I get pulled to sunrise?" (Quick flip to Sunrise Reset constellation) "I have 42 tracks for that vibe too. Different context, same navigation logic." (60 sec)
8. **Close:** "That's how I prep for festivals. I know exactly what I have for every scenario. I'm ready." (20 sec)

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
