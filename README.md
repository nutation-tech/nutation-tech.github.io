# RNAV — Market Analysis & Go‑to‑Market

> Potential customers, prioritised top‑10 with histograms, how to reach each, and
> what they're worth (pricing). Numbers are **order‑of‑magnitude estimates** for
> planning, not audited market data — refine with primary research before betting on them.

---

## 1. What we are actually selling

RNAV is a **maritime situational‑awareness & collision‑avoidance engine**:

- **AIS + radar sensor fusion** (Mahalanobis association, track fusion)
- **CPA / collision risk + COLREG advice** ("STOP / SLOW DOWN / TURN")
- **Ego navigation** — GNSS/IMU UKF tracking, heave/roll/pitch, datum management
- **A\* sea‑route planning** + dynamic obstacle/congestion avoidance, land‑aware
- **2D chart + 3D perspective view**, weather/marine overlay, OSM map layers
- **Congestion detection**, shore‑proximity & grounding warnings
- Portable **C++ core** with Compose **Desktop** and **Android** front‑ends → embeddable

That gives **three sellable shapes** of the same IP:

| Shape | What it is | Who buys |
|------|------------|----------|
| **A. End‑user app** | On‑vessel display/app (desktop/tablet) | vessel owners/operators |
| **B. Embeddable engine / SDK** | Fusion+CPA+routing library licensed in | electronics OEMs, autonomy devs |
| **C. Shore / fleet analytics** | Traffic picture, risk analytics | ports/VTS, insurers, fleets |

The packaging shape, not just the segment, drives the price — that's why OEM/SDK
deals sit at the top of the priority list below.

---

## 2. Top 10 potential customers — priority ranking

Priority = blend of **product fit × willingness‑to‑pay × reachability × market size**
(0–100). Higher = pursue first.

```
                                     priority (0–100)
 1 Electronics OEMs / integrators  92 ██████████████████████████████████████████████
 2 Autonomous / USV developers     88 ████████████████████████████████████████████
 3 Workboats: tugs/pilots/port     80 ████████████████████████████████████████
 4 Commercial shipping fleets      78 ███████████████████████████████████████
 5 Ferries & passenger vessels     74 █████████████████████████████████████
 6 Offshore energy support (OSV)   70 ███████████████████████████████████
 7 Commercial fishing fleets       62 ███████████████████████████████
 8 Port authorities / VTS          60 ██████████████████████████████
 9 Naval / coast guard / defense   58 █████████████████████████████
10 Recreational / prosumer boats   55 ███████████████████████████
```

---

## 3. Segment detail — size, how to find them, pricing

ACV = typical **annual contract value** of a first realistic deal. WTP = willingness to
pay per vessel/unit. "Sell" = packaging shape (A/B/C from §1).

| # | Segment | Sell | Rough market size | How to find them | Price / WTP | First‑deal ACV |
|---|---------|------|-------------------|------------------|-------------|----------------|
| 1 | **Electronics OEMs / integrators** (Furuno/JRC/Raymarine‑tier + dozens of mid/small ECDIS, plotter, radar makers) | B | ~50–150 serious OEMs worldwide | METSTRADE & SMM trade shows; IEC/IMO ECDIS vendor lists; LinkedIn to VP Eng/Product; partner pages of chart vendors | License $50k–250k/yr + **$50–300/unit** royalty | **$150k/yr** + royalties |
| 2 | **Autonomous / USV developers** (survey USVs, defense USVs, autonomy startups, research) | B | ~300–600 programs globally, fast‑growing | DSEI/Ocean Business/AUVSI; gov R&D awards (DARPA, EU Horizon, DoD SBIR); GitHub/marine‑robotics communities | SDK $20k–100k/yr + **$5k–25k/vehicle** | **$60k/yr** |
| 3 | **Workboats: tugs, pilot boats, port service** | A | ~100k+ vessels; high‑traffic, high‑risk | Pilot associations (IMPA), tug operators (Svitzer, Boluda), port chandlers, regional workboat shows | **$3k–8k/vessel** + $500–1.5k/yr sub | **$40k/yr** (20‑vessel deal) |
| 4 | **Commercial shipping fleets** (cargo, container, tanker, bulk) | A/C | ~60k+ vessels >300 GT | Owners/managers (V.Group, Anglo‑Eastern, Synergy); class societies (DNV, ABS, LR); Posidonia/Nor‑Shipping | $5k–12k/vessel + fleet SaaS | **$80k/yr** (fleet pilot) |
| 5 | **Ferries & passenger vessels** | A | ~15k+ ferries/passenger craft | Interferry assoc.; operators (Stena, DFDS); domestic ferry authorities | **$6k–15k/vessel** + support | **$30k/yr** |
| 6 | **Offshore energy support (OSV, wind‑farm SOV/CTV, survey)** | A/B | ~6k OSVs + booming offshore‑wind fleet | Offshore wind O&M operators; survey firms (Fugro); WindEurope/Offshore Energy events | **$8k–20k/vessel** | **$50k/yr** |
| 7 | **Commercial fishing fleets** | A | ~hundreds of thousands of decked vessels | Fishing‑gear distributors; co‑ops & associations; regional expos; subsidy/safety programs | **$1.5k–4k/vessel** (price‑sensitive) | **$15k/yr** (co‑op deal) |
| 8 | **Port authorities / VTS** | C | ~1,000+ VTS centers worldwide | IALA membership/events; port‑authority tenders; SI partners (Saab, Kongsberg, Wärtsilä) | **$100k–1M / site** project | **$300k** (project) |
| 9 | **Naval / coast guard / defense** | B/A | ~100+ navies & coast guards | Defense primes & teaming; DSEI/Euronaval; SBIR/defense innovation units | **$50k–500k/platform**; long cycle | **$500k+** |
| 10 | **Recreational / prosumer** (yachts, fast motorboats) | A | millions of craft; tiny ACV | App stores; marine retail (West Marine); chartplotter add‑on; influencers/YouTube | **$99–499** one‑time or **$5–15/mo** | **$0.1k/user** → needs volume |

---

## 4. Price / willingness‑to‑pay per vessel‑or‑unit (USD, log scale)

Where each segment sits on the value‑per‑unit axis (drives whether you sell direct,
via channel, or by volume app):

```
 $50–300/unit    OEM royalty        ▏(volume × leverage — best $/effort)
 $99–499         Recreational       █ (needs huge volume / app‑store)
 $1.5k–4k        Fishing            ███
 $3k–8k          Workboats          █████
 $5k–12k         Cargo/tanker       ███████
 $6k–15k         Ferries            ████████
 $8k–20k         Offshore OSV       ██████████
 $5k–25k         USV per vehicle    ████████████
 $50k–500k       Naval / platform   ███████████████████████
 $100k–1M        VTS / port site    ████████████████████████████
```

## 5. First‑deal annual contract value (USD thousands)

```
 Recreational         0.1  ▏
 Fishing (co‑op)       15  ███
 Ferries               30  ██████
 Workboats (fleet)     40  ████████
 Offshore (fleet)      50  ██████████
 USV SDK               60  ████████████
 Shipping (fleet)      80  ████████████████
 OEM license          150  ██████████████████████████████
 VTS (project)        300  ████████████████████████████████████████████████████████████
 Naval (program)      500  ██████████████████████████████████████████████████████ ... (off‑scale)
```

---

## 6. Go‑to‑market funnel (per channel)

```
   ┌─────────────────────────────────────────────────────────┐
   │  TOP OF FUNNEL — where they congregate                   │
   │  trade shows (SMM, METSTRADE, Posidonia, Ocean Business),│
   │  class societies, associations (IMPA, Interferry, IALA), │
   │  defense/EU R&D programs, app stores, marine retail       │
   └───────────────┬─────────────────────────────────────────┘
                   │  inbound demo / pilot request
                   ▼
   ┌─────────────────────────────────────────────────────────┐
   │  EVALUATION — free trial app (A) │ eval SDK + sample (B)  │
   │  on‑vessel pilot (1–3 vessels)   │ integration POC (OEM)  │
   └───────────────┬─────────────────────────────────────────┘
                   │  proof of value (fewer near‑misses, time saved)
                   ▼
   ┌─────────────────────────────────────────────────────────┐
   │  CONTRACT — fleet rollout │ OEM license + royalty │ tender│
   └─────────────────────────────────────────────────────────┘
```

---

## 7. Pricing strategy (summary)

- **Lead with the engine (B), monetise the app (A) for volume, land‑and‑expand on fleets/ports (C).**
- **OEM/SDK = highest leverage**: a per‑unit royalty rides on the OEM's existing distribution
  (one deal → thousands of units). Charge an annual platform license + per‑unit royalty.
- **On‑vessel (A)**: hardware‑agnostic software → **per‑vessel one‑time + annual subscription**
  (support, chart/weather data, updates). Subscription is where the lifetime value is.
- **Recreational**: only attractive as a **freemium app at scale** (free basic AIS view →
  paid CPA/route/3D tier). Don't sell it direct; let the app store be the channel.
- **Ports/Naval (C/B)**: project/tender pricing; expect 9–18 month cycles, partner with a
  prime/SI to clear procurement and certification.
- **Certification reality check**: anything sold as *primary* navigation (type‑approved ECDIS)
  needs IMO/IEC type approval — expensive and slow. Position first as a **decision‑support /
  collision‑avoidance aid** (not primary nav) to sell now, pursue type approval later for shipping/naval.

---

## 8. Recommended beachhead (where to start)

1. **Autonomous/USV developers (B)** — fastest sales cycle, technical buyers who value the
   fusion+CPA+routing stack directly, pay for SDKs, and give you reference logos + hard tech feedback.
2. **One electronics OEM (B)** — a single integration unlocks volume via their distribution.
3. **Workboats/pilots (A)** — clearest day‑one pain (congested, high‑traffic water) and a fast
   per‑vessel sale to prove the on‑vessel product and subscription model.

Then expand into shipping fleets and ports once you have type‑approval progress and references.

---

*Generated as a planning aid. Validate market sizes, pricing and channel assumptions with
primary interviews (5–10 per target segment) before committing GTM spend.*
