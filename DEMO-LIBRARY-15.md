# Demo Library: 15 Tracks (Tagged)

**Date:** May 16, 2026  
**Tagger:** Jasmine Sabio  
**Status:** Ready for MVP integration

---

## Overview

15 real, Creative Commons/royalty-free tracks manually tagged with per-tag confidence scores. All tracks have 0 play count (truly underplayed). Mix of genres: house, melodic techno, deep house, afro house, indie dance, electronica, dance/pop, hip-hop.

**Note:** These 15 tracks serve as the initial demo library. Full library target is 150 tracks for MVP Pool Party constellation.

---

## Markdown Table

| Artist | Title | Duration | Play Count | Time | Role | Crowd | Notes |
|--------|-------|----------|------------|------|------|-------|-------|
| Rampa | 2000 (Original Mix) | 6:16 | 0 | Afterglow (8) + Late Night Warehouse (7) | Bridge (8), Reset (8) | Arrivals (6), Lock In (8) | Indie Dance |
| Rhye, Adam Ten | 3 Days Later (Extended) | 6:47 | 0 | Sunrise Reset (7) + Warm Up (8) + Festival Brunch (8) + Pool Party (8) + Afterglow (7) | Opener (8), Reset (7), Home Stretch (8) | Arrivals (8), Wanderers (8) | Melodic House & Techno |
| Lucas Dekker | A Fire Inside Of Me | 4:44 | 0 | Festival Brunch (6) + Pool Party (8) | Bridge (8) | Arrivals (8), Wanderers (8) | House |
| Coldplay | A Sky Full of Stars (Kölsch Remix) | 9:21 | 0 | Sunrise Reset (7) + Afterglow (7) | Home Stretch (7) | Wanderers (8) | Electronica |
| Tchami | Adieu (Original Mix) | 6:53 | 0 | Sunrise Reset (8) + Club (6) | Bridge (8), Home Stretch (7) | Arrivals (6), Lock In (8) | Mainstage |
| L'Imperatrice | Agitations tropicales | 4:08 | 0 | Warm Up (7) + Pool Party (9) + Afterglow (7) | Opener (8), Reset (6) | Arrivals (6), Wanderers (8) | Dance / Pop |
| Mita Gami | All By Myself (Original Mix) | 5:09 | 0 | Club (8) | Opener (6), Bridge (8) | Arrivals (6), Lock In (8) | Deep House |
| LP Giobbi | All I Need (DESIREE Remix) | 5:39 | 0 | Sunrise Reset (8) + Warm Up (7) + Afterglow (6) | Opener (8), Reset (8) | Arrivals (8), Wanderers (8) | Afro House |
| DJ Tennis, Joseph Ashworth, LP Giobbi | All In A Dream feat. DJ Tennis feat. Joseph Ashworth (Extended Mix) | 6:08 | 0 | Sunrise Reset (8) + Warm Up (7) + Afterglow (8) | Opener (8), Reset (8) | Arrivals (8), Wanderers (8) | Melodic House & Techno |
| Le Youth | Aquiver | 6:45 | 0 | Sunrise Reset (8) + Warm Up (6) | Bridge (8) | Arrivals (8), Lock In (6) | Melodic House & Techno |
| Noir, Haze | Around (Solomun Vox) | 6:58 | 0 | Festival Brunch (6) + Club (8) | Opener (7) | Arrivals (8), Lock In (8) | Deep House |
| Tiga, Hudson Mohawke, Elisabeth Troy | Ascending Into The Clouds (Original Mix) | 6:14 | 0 | Club (8) + Late Night Warehouse (7) | Bridge (6), Home Stretch (7) | Lock In (7) | Dance / Pop |
| Andre Nickatina | Ayo for Yayo (feat. San Quinn) | 3:14 | 0 | Afterglow (9) | Bridge (8) | Lock In (8), Wanderers (7) | Hip-Hop/Rap |
| Interplanetary Criminal, Eliza Rose | B.O.T.A. (Baddest Of Them All) (Original Mix) | 5:58 | 0 | Sunrise Reset (7) + Festival Brunch (7) + Pool Party (8) + Club (8) | Bridge (8) | Arrivals (7), Lock In (7), Wanderers (7) | House |
| Adriatique, JAiMES, Samm (BE) | Back to Life (Extended Mix) | 6:29 | 0 | Afterglow (7) + Late Night Warehouse (8) | Opener (8), Bridge (7) | Arrivals (7), Wanderers (7) | Dance / Pop |

---

## JSON Format

```json
{
  "tracks": [
    {
      "artist": "Rampa",
      "title": "2000 (Original Mix)",
      "duration": "6:16",
      "genre": "Indie Dance",
      "bpm": "123",
      "key": "8A",
      "playCount": 0,
      "tags": {
        "time": [
          {
            "value": "afterglow",
            "confidence": 8
          },
          {
            "value": "late-night-warehouse",
            "confidence": 7
          }
        ],
        "role": [
          {
            "value": "bridge",
            "confidence": 8
          },
          {
            "value": "reset",
            "confidence": 8
          }
        ],
        "crowd": [
          {
            "value": "arrivals",
            "confidence": 6
          },
          {
            "value": "lock-in",
            "confidence": 8
          }
        ]
      },
      "spatial": {
        "x": 0,
        "y": 0
      }
    },
    {
      "artist": "Rhye, Adam Ten",
      "title": "3 Days Later (Extended)",
      "duration": "6:47",
      "genre": "Melodic House & Techno",
      "bpm": "123",
      "key": "12A",
      "playCount": 0,
      "tags": {
        "time": [
          {
            "value": "sunrise-reset",
            "confidence": 7
          },
          {
            "value": "warm-up",
            "confidence": 8
          },
          {
            "value": "festival-brunch",
            "confidence": 8
          },
          {
            "value": "pool-party",
            "confidence": 8
          },
          {
            "value": "afterglow",
            "confidence": 7
          }
        ],
        "role": [
          {
            "value": "opener",
            "confidence": 8
          },
          {
            "value": "reset",
            "confidence": 7
          },
          {
            "value": "home-stretch",
            "confidence": 8
          }
        ],
        "crowd": [
          {
            "value": "arrivals",
            "confidence": 8
          },
          {
            "value": "wanderers",
            "confidence": 8
          }
        ]
      },
      "spatial": {
        "x": 0,
        "y": 0
      }
    },
    {
      "artist": "Lucas Dekker",
      "title": "A Fire Inside Of Me",
      "duration": "4:44",
      "genre": "House",
      "bpm": "125",
      "key": "7A",
      "playCount": 0,
      "tags": {
        "time": [
          {
            "value": "festival-brunch",
            "confidence": 6
          },
          {
            "value": "pool-party",
            "confidence": 8
          }
        ],
        "role": [
          {
            "value": "bridge",
            "confidence": 8
          }
        ],
        "crowd": [
          {
            "value": "arrivals",
            "confidence": 8
          },
          {
            "value": "wanderers",
            "confidence": 8
          }
        ]
      },
      "spatial": {
        "x": 0,
        "y": 0
      }
    },
    {
      "artist": "Coldplay",
      "title": "A Sky Full of Stars (Kölsch Remix)",
      "duration": "9:21",
      "genre": "Electronica",
      "bpm": "123",
      "key": "1A",
      "playCount": 0,
      "tags": {
        "time": [
          {
            "value": "sunrise-reset",
            "confidence": 7
          },
          {
            "value": "afterglow",
            "confidence": 7
          }
        ],
        "role": [
          {
            "value": "home-stretch",
            "confidence": 7
          }
        ],
        "crowd": [
          {
            "value": "wanderers",
            "confidence": 8
          }
        ]
      },
      "spatial": {
        "x": 0,
        "y": 0
      }
    },
    {
      "artist": "Tchami",
      "title": "Adieu (Original Mix)",
      "duration": "6:53",
      "genre": "Mainstage",
      "bpm": "126",
      "key": "10A",
      "playCount": 0,
      "tags": {
        "time": [
          {
            "value": "sunrise-reset",
            "confidence": 8
          },
          {
            "value": "club",
            "confidence": 6
          }
        ],
        "role": [
          {
            "value": "bridge",
            "confidence": 8
          },
          {
            "value": "home-stretch",
            "confidence": 7
          }
        ],
        "crowd": [
          {
            "value": "arrivals",
            "confidence": 6
          },
          {
            "value": "lock-in",
            "confidence": 8
          }
        ]
      },
      "spatial": {
        "x": 0,
        "y": 0
      }
    },
    {
      "artist": "L'Imperatrice",
      "title": "Agitations tropicales",
      "duration": "4:08",
      "genre": "Dance / Pop",
      "bpm": "116",
      "key": "1A",
      "playCount": 0,
      "tags": {
        "time": [
          {
            "value": "warm-up",
            "confidence": 7
          },
          {
            "value": "pool-party",
            "confidence": 9
          },
          {
            "value": "afterglow",
            "confidence": 7
          }
        ],
        "role": [
          {
            "value": "opener",
            "confidence": 8
          },
          {
            "value": "reset",
            "confidence": 6
          }
        ],
        "crowd": [
          {
            "value": "arrivals",
            "confidence": 6
          },
          {
            "value": "wanderers",
            "confidence": 8
          }
        ]
      },
      "spatial": {
        "x": 0,
        "y": 0
      }
    },
    {
      "artist": "Mita Gami",
      "title": "All By Myself (Original Mix)",
      "duration": "5:09",
      "genre": "Deep House",
      "bpm": "124",
      "key": "6A",
      "playCount": 0,
      "tags": {
        "time": [
          {
            "value": "club",
            "confidence": 8
          }
        ],
        "role": [
          {
            "value": "opener",
            "confidence": 6
          },
          {
            "value": "bridge",
            "confidence": 8
          }
        ],
        "crowd": [
          {
            "value": "arrivals",
            "confidence": 6
          },
          {
            "value": "lock-in",
            "confidence": 8
          }
        ]
      },
      "spatial": {
        "x": 0,
        "y": 0
      }
    },
    {
      "artist": "LP Giobbi",
      "title": "All I Need (DESIREE Remix)",
      "duration": "5:39",
      "genre": "Afro House",
      "bpm": "120",
      "key": "5B",
      "playCount": 0,
      "tags": {
        "time": [
          {
            "value": "sunrise-reset",
            "confidence": 8
          },
          {
            "value": "warm-up",
            "confidence": 7
          },
          {
            "value": "afterglow",
            "confidence": 6
          }
        ],
        "role": [
          {
            "value": "opener",
            "confidence": 8
          },
          {
            "value": "reset",
            "confidence": 8
          }
        ],
        "crowd": [
          {
            "value": "arrivals",
            "confidence": 8
          },
          {
            "value": "wanderers",
            "confidence": 8
          }
        ]
      },
      "spatial": {
        "x": 0,
        "y": 0
      }
    },
    {
      "artist": "DJ Tennis, Joseph Ashworth, LP Giobbi",
      "title": "All In A Dream feat. DJ Tennis feat. Joseph Ashworth (Extended Mix)",
      "duration": "6:08",
      "genre": "Melodic House & Techno",
      "bpm": "120",
      "key": "7A",
      "playCount": 0,
      "tags": {
        "time": [
          {
            "value": "sunrise-reset",
            "confidence": 8
          },
          {
            "value": "warm-up",
            "confidence": 7
          },
          {
            "value": "afterglow",
            "confidence": 8
          }
        ],
        "role": [
          {
            "value": "opener",
            "confidence": 8
          },
          {
            "value": "reset",
            "confidence": 8
          }
        ],
        "crowd": [
          {
            "value": "arrivals",
            "confidence": 8
          },
          {
            "value": "wanderers",
            "confidence": 8
          }
        ]
      },
      "spatial": {
        "x": 0,
        "y": 0
      }
    },
    {
      "artist": "Le Youth",
      "title": "Aquiver",
      "duration": "6:45",
      "genre": "Melodic House & Techno",
      "bpm": "124",
      "key": "4A",
      "playCount": 0,
      "tags": {
        "time": [
          {
            "value": "sunrise-reset",
            "confidence": 8
          },
          {
            "value": "warm-up",
            "confidence": 6
          }
        ],
        "role": [
          {
            "value": "bridge",
            "confidence": 8
          }
        ],
        "crowd": [
          {
            "value": "arrivals",
            "confidence": 8
          },
          {
            "value": "lock-in",
            "confidence": 6
          }
        ]
      },
      "spatial": {
        "x": 0,
        "y": 0
      }
    },
    {
      "artist": "Noir, Haze",
      "title": "Around (Solomun Vox)",
      "duration": "6:58",
      "genre": "Deep House",
      "bpm": "115",
      "key": "11A",
      "playCount": 0,
      "tags": {
        "time": [
          {
            "value": "festival-brunch",
            "confidence": 6
          },
          {
            "value": "club",
            "confidence": 8
          }
        ],
        "role": [
          {
            "value": "opener",
            "confidence": 7
          }
        ],
        "crowd": [
          {
            "value": "arrivals",
            "confidence": 8
          },
          {
            "value": "lock-in",
            "confidence": 8
          }
        ]
      },
      "spatial": {
        "x": 0,
        "y": 0
      }
    },
    {
      "artist": "Tiga, Hudson Mohawke, Elisabeth Troy",
      "title": "Ascending Into The Clouds (Original Mix)",
      "duration": "6:14",
      "genre": "Dance / Pop",
      "bpm": "141",
      "key": "2A",
      "playCount": 0,
      "tags": {
        "time": [
          {
            "value": "club",
            "confidence": 8
          },
          {
            "value": "late-night-warehouse",
            "confidence": 7
          }
        ],
        "role": [
          {
            "value": "bridge",
            "confidence": 6
          },
          {
            "value": "home-stretch",
            "confidence": 7
          }
        ],
        "crowd": [
          {
            "value": "lock-in",
            "confidence": 7
          }
        ]
      },
      "spatial": {
        "x": 0,
        "y": 0
      }
    },
    {
      "artist": "Andre Nickatina",
      "title": "Ayo for Yayo (feat. San Quinn)",
      "duration": "3:14",
      "genre": "Hip-Hop/Rap",
      "bpm": "128.4",
      "key": "10A",
      "playCount": 0,
      "tags": {
        "time": [
          {
            "value": "afterglow",
            "confidence": 9
          }
        ],
        "role": [
          {
            "value": "bridge",
            "confidence": 8
          }
        ],
        "crowd": [
          {
            "value": "lock-in",
            "confidence": 8
          },
          {
            "value": "wanderers",
            "confidence": 7
          }
        ]
      },
      "spatial": {
        "x": 0,
        "y": 0
      }
    },
    {
      "artist": "Interplanetary Criminal, Eliza Rose",
      "title": "B.O.T.A. (Baddest Of Them All) (Original Mix)",
      "duration": "5:58",
      "genre": "House",
      "bpm": "137",
      "key": "8B",
      "playCount": 0,
      "tags": {
        "time": [
          {
            "value": "sunrise-reset",
            "confidence": 7
          },
          {
            "value": "festival-brunch",
            "confidence": 7
          },
          {
            "value": "pool-party",
            "confidence": 8
          },
          {
            "value": "club",
            "confidence": 8
          }
        ],
        "role": [
          {
            "value": "bridge",
            "confidence": 8
          }
        ],
        "crowd": [
          {
            "value": "arrivals",
            "confidence": 7
          },
          {
            "value": "lock-in",
            "confidence": 7
          },
          {
            "value": "wanderers",
            "confidence": 7
          }
        ]
      },
      "spatial": {
        "x": 0,
        "y": 0
      }
    },
    {
      "artist": "Adriatique, JAiMES, Samm (BE)",
      "title": "Back to Life (Extended Mix)",
      "duration": "6:29",
      "genre": "Dance / Pop",
      "bpm": "120",
      "key": "2A",
      "playCount": 0,
      "tags": {
        "time": [
          {
            "value": "afterglow",
            "confidence": 7
          },
          {
            "value": "late-night-warehouse",
            "confidence": 8
          }
        ],
        "role": [
          {
            "value": "opener",
            "confidence": 8
          },
          {
            "value": "bridge",
            "confidence": 7
          }
        ],
        "crowd": [
          {
            "value": "arrivals",
            "confidence": 7
          },
          {
            "value": "wanderers",
            "confidence": 7
          }
        ]
      },
      "spatial": {
        "x": 0,
        "y": 0
      }
    }
  ]
}
```

---

## Tagging Notes

### Key Observations

- **High-context tracks:** "3 Days Later" (Rhye, Adam Ten) and "B.O.T.A." (Interplanetary Criminal, Eliza Rose) work across 4-5 time contexts—extremely versatile
- **Pool Party standout:** "Agitations tropicales" (L'Imperatrice) rated 9/10 for Pool Party—strong candidate for demo context
- **Opener-heavy:** Many tracks can open sets (6-8 confidence), showing diverse entry points
- **Bridge-dominant:** Most tracks serve as bridges, reflecting their transitional versatility
- **Crowd flexibility:** Most tracks work in multiple crowd states (Arrivals + Wanderers, or Lock-in + Wanderers)

### Next Steps for MVP

1. **Expand to 40–50 Pool Party tracks** — These 15 will seed the collection; identify tracks with high Pool Party confidence (8+)
2. **Cross-reference for rediscovery track** — All 15 have playCount=0, so any could be the demo "hero moment"
3. **Spatial positioning** — Once Valerie builds the constellation view, positions will be computed from these tags

---

## For Valerie

Use the JSON data directly in the frontend. The `spatial` coordinates are placeholder (0, 0)—these will be calculated during constellation rendering based on tags (x = journey role index, y = crowd state index).
