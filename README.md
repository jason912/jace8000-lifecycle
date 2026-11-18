# JACE-8000 & Niagara 4 — Lifecycle, End-of-Life and Migration Guide

> **Last verified: 18 November 2026.** Dates below are quoted from Tridium-published FAQ material (sources at the end).
>
> 本指南最后核对日期：2026-11-18。所有日期均引自 Tridium 公布的 FAQ 原文，出处见文末。

---

## TL;DR — the five dates that matter

| Date | What happens | Who is affected |
|---|---|---|
| **31 Dec 2025** | JACE-8000 **last order date passed** in Europe | European projects — already closed |
| **31 Dec 2026** | JACE-8000 **last order date** — North America, Middle East, Africa, **Asia Pacific** | **43 days from this update** |
| **Q4 2026** | Niagara 5 **General Availability** | Everyone planning new work |
| **Q3 2028** | **Niagara 4 End of Life.** 4.15 is the LTS release and stops receiving updates | Every N4 station in service |
| **After 2028** | SMA can **still be purchased** for N4 JACEs and Supervisors | Maintenance-only sites |

**One sentence:** you can still buy a JACE-8000 in APAC until the end of 2026, it will be fully supported until Q3 2028, and it will **never** run Niagara 5.

---

## 1. What each date actually means

### 31 December 2026 — last order, not last day of use

This is a **purchasing** deadline, not an operational one. A JACE-8000 ordered on 30 December 2026 is a current, fully warrantied, fully supported controller. It will receive N4 updates until 2028 like every other unit.

The distinction matters commercially: after 2026-12-31 the supply of **new** JACE-8000 units ends, but the installed base does not shrink. Every unit already in the field keeps running, keeps breaking, and eventually needs **replacement with an identical unit** — because re-engineering a working station to a different model costs far more than the hardware.

**That is the spare-parts market, and it opens on 1 January 2027.**

### Q3 2028 — Niagara 4 End of Life

Niagara 4.15 is the Long-Term Support (LTS) release. Tridium has stated that 4.15 continues to receive updates **through Q3 2028**. After that:

- No new features
- No further security patches
- No new driver updates

Operationally, stations keep running. Commercially, 2028 Q3 is when "we're still on N4" becomes a compliance question rather than a technical one — particularly for sites with cybersecurity requirements, insurance conditions, or enterprise IT policies that mandate patched software.

### After 2028 — SMA still available

This is the question every N4 owner asks, and the answer is favourable:

> *"Yes, you will be able to purchase an SMA for N4 JACEs and Supervisors after the N4 EOL date."*

So a site that decides to stay on N4 past 2028 can still license it. It just cannot receive software updates, because there are none.

---

## 2. JACE-8000 vs JACE-9000

Both are current, both run Niagara 4, both are supported to 2028. The difference is what happens **after** 2028.

| | **JACE-8000** | **JACE-9000** |
|---|---|---|
| **Niagara 5 upgrade path** | ❌ **No** | ✅ **Yes** (N4 → N5) |
| Processor | — | Quad-core; all 4 cores used at startup, then 2 to station, 1 to daemon, 1 reserve |
| RAM | — | 2 GB |
| Flash | — | 8 GB |
| Backup storage | Backup port | **8 GB uSD**, no backup port; automatic full backup daily at 02:00, incremental after, oldest pruned when full |
| History capacity | Baseline | **10,000 histories** × 8,640 records ≈ 90 days at 15-minute intervals — **1.6×** the JACE-8000 |
| Option modules | Up to **four** IO-R modules | Current generation |
| Wi-Fi | Native | Available (wireless and fully depopulated variants) |
| Environmental specs | — | **Identical** to JACE-8000 |
| Power | 24 VAC/DC | 24 VAC/DC |
| Licensing model | NC-800x | NC-900x (e.g. **NC-9005 ≡ NC-8005**) |
| Last order | **APAC: 2026-12-31** | Through N4 End of Life (2028) |
| Supported until | Q3 2028 | Q3 2028 on N4; **beyond, on N5** |

### The upgrade question, in Tridium's own words

> **Q: Will the JACE 8000 be upgraded to Niagara 5?**
> **A: No.** The JACE-8000 was able to transition from AX to N4; the JACE-9000 can transition from N4 to N5. We are working on a license change option so that a JACE-8000 license can be transferred to a JACE-9000.

Two things to take from this:

1. **The hardware cannot be upgraded.** This is not a licensing restriction you can buy your way out of — there is no N5 build for the 8000.
2. **The licence may be transferable.** Tridium has stated it is working on a licence-change option. If that ships, a customer's existing 8000 entitlement can move to a 9000 rather than being written off. **Ask your distributor for the current status before quoting** — as of this update it is announced intent, not published procedure.

---

## 3. Smaller sites: what to consider

Tridium's small-site and edge portfolio runs on Niagara 4 as well, including the **Niagara Edge 10** and the China-market **JACE IoT**.

For planning purposes, treat them the same way you treat any N4 controller:

- They are covered by the **Niagara 4 End of Life date of Q3 2028** for software updates
- They do **not** have a Niagara 5 upgrade path — N5 migration is a JACE-9000 and Supervisor conversation
- Sizing, licensing and commercial terms differ by model and by region — **confirm with Tridium or your distributor before you specify**

If you are choosing between a small-site controller and a JACE-9000, the deciding question is not capacity but **planning horizon**: a controller that must carry a site into the 2030s needs an N5 path; a controller serving a site that will be re-engineered before 2028 does not.

*Configuration details, availability and commercial terms for specific small-site models are available on request.*

---

## 4. Spare-parts and stock planning

### For owners of existing JACE-8000 sites

**If your site has a JACE-8000 and no N5 plan**, the practical question is not "should I buy a 9000" — it is "what happens when this unit fails in 2027 or 2028, when new 8000s can no longer be ordered?"

Three options, in order of cost:

1. **Hold a cold spare.** One identical unit per critical site, powered down, on the shelf. Cheapest insurance; covers the failure scenario completely.
2. **Pre-buy for known expansion.** If point counts will grow before 2028, buy the additional units and IO-R modules now, while they are orderable.
3. **Plan the 9000 migration.** Correct for long-horizon sites, but it is a re-engineering project, not a swap — budget station rework and re-commissioning, not just hardware.

**What to check on your site list:**

- Which sites are on JACE-8000 vs 9000 vs legacy
- Installation year and warranty expiry per unit
- Point count and headroom (are they near licence capacity?)
- Whether the station has any N5 dependency in the next 5 years
- Criticality — a failed controller in a plant room and a failed controller in a retail back office are not the same risk

### For integrators and contractors

The window that matters is **2027**. From January 2027, a JACE-8000 replacement order has no factory lead time to offer — only whatever is in the channel. Integrators holding maintenance contracts on 8000 sites will need a source.

If you service 8000 sites, the decision to hold stock is made **before 31 December 2026**, not after.

---

## 5. FAQ

**Can I still order a JACE-8000?**
In Asia Pacific, yes — until **31 December 2026**. Europe's window closed 31 December 2025. North America, Middle East and Africa share the APAC deadline.

**Will my JACE-8000 stop working in 2028?**
No. End of Life means end of *software updates*, not end of operation. Stations continue to run.

**Can I buy an SMA after 2028?**
Yes. Tridium has confirmed SMA purchase remains available for N4 JACEs and Supervisors after the N4 EOL date.

**Can a JACE-8000 be upgraded to Niagara 5?**
No. Tridium's answer is explicit. Only the JACE-9000 has an N4 → N5 path. A licence-transfer option from 8000 to 9000 has been announced as in development.

**Is the JACE-9000 a drop-in replacement?**
Hardware and environmental specs are the same, and licence models map 1:1 (NC-9005 ≡ NC-8005). But it is a **different model with different storage architecture** (uSD backup, no backup port). Treat it as a migration with station verification, not a blind swap.

**What about controllers made by other manufacturers on the Niagara platform?**
Tridium's position: portability partners set their own eligibility and timing. Ask the manufacturer directly — do not assume the JACE-8000 timeline applies.

**Should I buy now or wait for Niagara 5?**
Depends on the project. If it must be delivered and commissioned before 2027 and the design is already N4, buy within the window. If it is a new design with a 10-year horizon, design for N5 and specify JACE-9000.

**What about small-site controllers like Edge 10 or JACE IoT?**
They run Niagara 4 and share the N4 End of Life date of Q3 2028. They do not have an N5 upgrade path. For sizing and commercial terms, confirm with Tridium or your distributor.

---

## 6. What this guide is not

- It is not a quotation. Prices are not published here.
- It is not a substitute for Tridium's official documentation — where this guide and Tridium's published material disagree, Tridium governs.
- It does not cover Niagara AX, which reached its own end of life earlier and is out of scope.

---

## Contact

**Shanghai Gline Net Co., Ltd. (GLINENET)** — Tridium partner since 2014.

- JACE-8000 / JACE-9000 supply and spare-parts planning
- Niagara 4 station engineering, migration assessment, remote operations
- Small-site controller selection and availability
- Email: **jason.zhang@gline-net.com**

*If you are planning 8000-class replacement or expansion in Asia Pacific, ask before the 2026-12-31 order deadline. Sales policy and product terms are set by Tridium — confirm before any purchase decision.*

---

## Sources

1. **Tridium — Niagara 5 FAQ** (published 6 February 2025): last-order dates by region, N4 End of Life in Q3 2028, 4.15 as the LTS release, the JACE-8000 → N5 answer, SMA availability after EOL, and N5 release phasing (alpha Q1 2026, EA Q3 2026, beta end Q3 2026, GA Q4 2026).
2. **Tridium — JACE-9000 FAQ** (2023): quad-core / 2 GB / 8 GB specification, uSD backup behaviour, the 10,000-history recommendation, NC-900x ↔ NC-800x model mapping, and the two-visible-CPU behaviour.
3. **Tridium — JACE-8000 product documentation**: option module capacity, Wi-Fi, power, and environmental equivalence with the 9000.
4. **Tridium — IO R documentation**: IO R 16 / IO R 34 modules, up to four IO-R-16 per host.
5. **Tridium — Niagara Edge 10 and small-site product documentation**: positioning and framework version.
