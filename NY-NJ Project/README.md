## Analysis of different Projects based on Solar energy in NY/NJ >=100MW 

<details>
<summary>DataOne × Nebius – Vineland, NJ AI Data Center</summary>
  
# DataOne × Nebius – Vineland, NJ AI Data Center (Up to 300 MW)

> **Purpose of this document:**  
> I want to understand **how this data center will really work**, what DataOne builds, how Nebius uses it, what the local utility (VMEU) controls, and which unknowns I need answered to reduce risk before any commitment.

---

## 📍 Project Overview
- **Location:** 805 Sheridan Avenue, Vineland, New Jersey, USA  
- **Developer / Owner:** **DataOne** (site developer and infrastructure operator)  
- **Anchor Tenant:** **Nebius** – AI cloud company running GPU clusters  
- **Total Planned IT Load:** **Up to 300 MW** (Phase 1 ≈ 100 MW; expandable with utility upgrades)  
- **Go-Live Goal:** First capacity ~Summer 2025 (developer cites ~20-week first phase build)

---

## 🏗 Roles & Responsibilities

| Actor | What They Own / Lead |
|-------|---------------------|
| **DataOne** | Land & permits, on-site solar & BESS, customer substation & MV/LV distribution, UPS, cooling plants, shells/MEP, facility & energy operations, interconnection negotiation |
| **Nebius** | GPU/AI servers, racks, high-speed network & storage, AI platform & customers |
| **VMEU (Vineland Municipal Electric Utility)** | Grants interconnection, sets import/export caps, applies tariffs & standby charges, maintains grid reliability |
| **EPC/Contractors** | Build shells, MEP, substation, PV/BESS yards, liquid cooling plants |
| **Carriers/ISPs** | Diverse fiber paths to Secaucus, 60 Hudson, 111 8th (NYC/NJ network hubs) |

---

## ⚡ Power Architecture

### Behind-the-Meter (BTM)
- **Solar PV + Battery Energy Storage (BESS)** inside the campus fence feed IT loads first.  
- **Grid tie** remains for backup and to supplement supply.  
- BTM does not mean off-grid. The project still needs a **formal interconnection agreement** with VMEU.

### Distributed Generation (DG) Limits
- **Current VMEU published caps:**  
  - ≤ 4 MW per DG project (≤ 2 MW if net-metered)  
  - System-wide DG total ≤ 50 MW  
- Our site: **100–300 MW** → **way outside normal rules** → requires **custom engineering studies and a special interconnection contract**.

### Tariff / Cost of Power
- **Imports:** billed under a **large-load or custom tariff** (NJ bill A5462 pushes for a ≥100 MW data-center class).  
- **Exports:** only if VMEU allows; otherwise plant is “non-export.”  
- Tariff defines **standby/demand charges**, **power factor rules**, and how credits (if any) for renewable energy are handled.

---

## 🌡 Cooling System

- **Rack power:** 60 – 500 kW each → **liquid cooling required**.
- **IT side:** direct-to-chip cold plates; immersion possible for extreme loads.  
- **CDUs:** isolate IT coolant from facility loop.  
- **Facility loop:** warm-water (≈35 – 45 °C) for efficient heat rejection.  
- **Heat rejection:** **dry or hybrid-dry coolers** (low water use, air-based) — confirmed by local planning notes.  
- **Heat recovery:** planned; can supply nearby industrial or building loads.  
- **Controls:** BMS/DCIM + EMS/SCADA dispatch energy and cooling safely.  
- **Commissioning:** leak detection, black-start, thermal soak tests.

---

## 🚀 Phased Growth Plan

| Phase | IT Load | How Powered | Notes |
|-------|---------|-------------|-------|
| **Phase 1 (2025)** | ~100 MW | On-site PV & BESS plus limited grid import | Allows early go-live while grid upgrades catch up |
| **Phase 2–3** | → 300 MW | Expanded PV/BESS + increased grid import as VMEU builds substation/feeders | Needs signed custom interconnection & tariff clarity |

---

## 🛠 Implementation Workflow

1. **Planning & Permitting** – land/zoning/environmental approvals, DG studies with VMEU  
2. **Design** –  
   - *DataOne:* campus layout, BTM power plant, substation, liquid cooling, network rooms  
   - *Nebius:* rack density & IT architecture  
3. **Construction** – precast shells, PV fields, BESS, MV distribution, UPS, cooling yards  
4. **Commissioning** – power plant & grid tie, cooling IST, protection & SCADA testing  
5. **IT Install (Nebius)** – GPU racks, fabric, storage  
6. **Operations** – DataOne runs facilities & energy, Nebius runs AI, VMEU handles grid billing/reliability

---

## ❓ Key Questions I Need Answered

### Power & Grid
- **Import caps** per phase? (MW and timing)  
- **Export policy:** non-export or limited export allowed?  
- **Who pays for substation / feeder upgrades?**  
- **Islanding ability:** how long can Phase 1 run on PV+BESS alone?  
- **Protection settings & telemetry** required by VMEU?  
- **REC / renewable attribute ownership** (DataOne vs Nebius)?

### Tariff & Costs
- Which **large-load tariff** or **special data-center tariff** (A5462) will apply?  
- How are **standby and demand charges** calculated?  
- Are there **credits or incentives** for waste-heat recovery or high efficiency?

### Cooling
- Exact **split** of cold-plate vs immersion per hall?  
- **Supply/return temperatures** on the facility loop?  
- **Dry vs hybrid-dry** coolers: vendor, design ambient temp, water use profile?  
- Details of the **heat-recovery** use case (MW thermal, offtaker)?  
- **PUE & WUE targets** by phase?

### Network
- Confirm **diverse fiber paths** and latency to Secaucus/60 Hudson/111 8th.  
- Who owns/manage **meet-me rooms** and cross-connects?

### Construction / Supply Chain
- Lead times for **transformers, switchgear, UPS, BESS, CDUs, dry coolers**?  
- Frame agreements or phased deliveries to avoid delays?

---

## ⚠️ Major Risks

| Risk | Impact | Mitigation |
|------|--------|-----------|
| Utility interconnection delays | Can stall Phase 2/3 capacity | Early custom agreement & fund upgrades |
| Tariff uncertainty | Cost overruns | Track NJ A5462, lock option clauses |
| Cooling tech mismatch | Limits GPU density | Pilot small pod, validate before full rollout |
| Equipment lead times | Schedule slip | Pre-order long-lead gear, modular build |
| Network single path | Outages | Require two diverse fiber routes & SLAs |

---

## 🏆 Success Markers for Phase 1
- ~100 MW IT live by **Summer 2025**.  
- PV & BESS producing majority of daytime power; **non-export logic** proven.  
- Import cap from VMEU sufficient for worst-case weather.  
- PUE and WUE at or better than design targets.  
- Dual diverse fiber fully operational.  

---

## 📚 References
- Nebius blog (Mar 2025): 300 MW region, **behind-the-meter** strategy, **energy-efficient cooling & heat recovery**  
- DCD (Mar 2025): DataOne’s **20-week first phase** build  
- VMEU DG Interconnection Rules: **≤4 MW/project, 50 MW system cap**  
- NJ Bill **A5462**: ≥100 MW data center tariff initiative
- Local planning: air-cooling vs water-cooling preference
</details>


