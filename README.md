# Production Throughput & Bottleneck Analysis
#### OEE Tracking | Power Query ETL | Root Cause Isolation | Operations Analytics

[![Excel](https://img.shields.io/badge/Excel-Power_Query-217346.svg)](https://www.microsoft.com/en-us/microsoft-365/excel)
[![Methodology](https://img.shields.io/badge/Methodology-OEE_%26_Pareto_Analysis-blue.svg)](https://en.wikipedia.org/wiki/Overall_equipment_effectiveness)
[![Domain](https://img.shields.io/badge/Domain-Manufacturing_%26_Operations-0D6EFD.svg)](https://en.wikipedia.org/wiki/Manufacturing_execution_system)

> [!IMPORTANT]
> **Executive Summary:** This project recovers **20% of lost production capacity** on a high-volume manufacturing line. By engineering an automated root-cause model using Power Query, management assumptions blaming operators for production slowdowns were overturned — and the analysis mathematically proved that **systemic machine instability, not human performance**, was the primary driver of unplanned downtime. Pareto analysis isolated the "Vital Few" failure categories responsible for 80% of all lost throughput.

---

> [!NOTE]
> **Supply Chain & Operations Analytics Connection:** OEE tracking, MTBF analysis, and bottleneck isolation are core analytics methodologies in pharmaceutical manufacturing (cold chain line performance), medical device production, and healthcare supply chain distribution operations. The Power Query ETL pattern — wide-to-tall unpivoting of machine log exports — applies directly to any MES, SCADA, or ERP system generating fragmented operational data. The Pareto framework and Operator-Controllable vs. Systemic accountability partition are transferable to any operations environment where downtime root cause needs to be defensibly attributed.

---

## The Problem

A high-volume production line was losing 15–20% of daily capacity to unexplained unplanned downtime. Operations management hypothesized that operator performance was the primary bottleneck and was preparing to hold staff accountable for throughput losses. Without a unified analytical model of machine log data, leadership had no data-driven basis for that conclusion — and was targeting the wrong variable.

**Description:** Built a data-driven Overall Equipment Effectiveness (OEE) tracking model to isolate the "Vital Few" root causes of unplanned machine downtime using Power Query and Excel analytics.

**Objective:** Transition the operation from reactive firefighting to proactive capacity management, recover the 20% throughput loss, and provide definitively data-backed accountability.

## Data Sources

1. **Primary Datasets:** Raw machine logs exported from the Manufacturing Execution System (MES) tracking individual downtime events across 12 distinct failure categories.
2. **Additional Data:** Equipment nameplate capacity specifications (theoretical max throughput speed) and planned production shift schedules.

## Process

- Quantified baseline performance across the three pillars of OEE: **Availability** (uptime %), **Performance** (speed vs. nameplate), and **Quality** (output vs. standard).
- Measured Mean Time Between Failures (MTBF) to quantify the precise duration between systemic machine stops — separating chronic failure patterns from random one-off events.
- Executed a Pareto Analysis on all 12 downtime categories to mathematically isolate which failure types were producing 80% of lost production time.
- Partitioned all downtime explicitly into "Operator-Controllable" vs. "Systemic" (hardware/supply chain) buckets to create a defensible accountability framework.

## Technical Pivot

**From Wide Spreadsheets to Tall Data (Power Query Unpivoting)**

Raw MES machine logs were exported with 12 separate downtime columns per row — preventing accurate aggregate math and making standard pivot analysis impossible. A Power Query Unpivot transformed the wide, fragmented dataset into a strict tall analytical schema. This single technical step is what enabled the Pareto analysis to prove that Machine Adjustments and Hardware Failures — not operator speed — accounted for 80% of all lost throughput time.

## Key Insights

- **Operators Were Not the Bottleneck:** Hardware instability and material shortages were driving financial losses — not human performance. Management assumptions were overturned by data.
- **Predictable Disruption Windows:** Lost time clustered sharply around shift changes and mandated break periods (12 PM, 2 PM, 7 PM) — creating daily, predictable capacity losses that could be structurally resolved.
- **The Preventative Maintenance Disconnect:** The line was operating on a reactive break-fix model rather than a preventative maintenance schedule, leading to compounding failure patterns on the primary equipment.

## Recommendations

- **Temporal Friction Correction:** Implement staggered break protocols to maintain continuous line operation during peak throughput windows, eliminating predictable flatlines in production output.
- **Preventative Maintenance Prioritization:** Shift to a data-driven PM schedule prioritizing the specific unstable equipment clusters identified in the Pareto failure analysis.
- **Supply Chain Alignment:** Launch a cross-functional investigation into the root cause of "Inventory Shortage" downtime events to align incoming material planning with actual production velocity.

## Next Steps

- **Automated OEE Dashboards:** Deploy real-time Availability and Performance tracking dashboards for the primary production line, enabling floor managers to intervene the moment output drops below threshold.
- **Downtime Variance Alerts:** Institute weekly reviews of the top-3 downtime drivers to prevent documented systemic failures from re-establishing themselves as baseline operating conditions.