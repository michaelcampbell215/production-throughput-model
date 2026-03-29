# Production Throughput & Bottleneck Analysis

[![Excel](https://img.shields.io/badge/Excel-Power_Query-217346.svg)](https://www.microsoft.com/)

> [!IMPORTANT]
> **Executive Summary:** This project recovers 20% of lost production capacity on a high-volume manufacturing line. By engineering an automated root-cause model using Power Query, we debunked assumptions that blamed operators for the slowdowns and identified systemic machine instability as the primary financial driver of unplanned downtime.

**Strategic Asset:** 
*   **Operational Model:** [Manufacturing Line Productivity Analysis](./Manufacturing_Line_Productivity_Analysis.xlsx)

---

## Project Overview

A high-volume beverage bottling line (CO-600) was bleeding 15% to 20% of its daily capacity to unexplained production downtime. Operations management hypothesized that operator performance was the primary bottleneck. Lacking a unified, aggregated view of machine logs, leadership was preparing to penalize staff for lost throughput that was actually systemic in nature.

1. **Description:** We built a data-driven Overall Equipment Effectiveness (OEE) tracking model to isolate the "Vital Few" causes of unplanned machine downtime.
2. **Objective:** Transition the plant from reactive "firefighting" to proactive capacity management, and recover the 20% of lost production throughput.

## Data Sources

1. **Primary Datasets:** Raw machine logs exported from the Manufacturing Execution System (MES) tracking individual downtime events.
2. **Additional Data:** Equipment nameplate capacity specifications (theoretical max speed) and planned production shift schedules.

## Process

*   Quantified baseline performance across the three pillars of OEE: Availability, Performance, and Quality.
*   Measured Mean Time Between Failures (MTBF) to quantify the precise duration between systemic machine stops.
*   Executed a Pareto Analysis on 12 distinct downtime categories to mathematically isolate the root causes of production friction.
*   Explicitly partitioned all downtime into "Operator-Controllable" vs. "Systemic" (hardware/supply chain) buckets.

## Technical Pivot

*   **From Wide Spreadsheets to Tall Data (Power Query Unpivoting):** Raw machine logs exported with 12 separate columns for downtime, preventing accurate aggregate math and making standard pivot tables impossible to use. We executed a massive Power Query Unpivot to transform the wide, messy dataset into a strict "tall" analytical schema. This specific technical step is what allowed us to mathematically prove that Machine Adjustments and Hardware Failures not operator speed actually accounted for 80% of all lost time.

## Key Insights

*   **Operators Were Not the Bottleneck:** The data conclusively proved that human performance was not the capacity constraint; hardware instability and material shortages were driving the financial losses.
*   **Systemic Disruption Windows:** Discovered that lost time clustered sharply around specific shift changes and mandated break periods (12 PM, 2 PM, 7 PM), creating daily, predictable losses in throughput capacity.
*   **The Preventative Maintenance Disconnect:** The line was operating on a highly reactive "break-fix" model rather than a preventative schedule, leading to compounding failures on the CO-600 equipment.

## Recommendations

*   **Temporal Friction Correction:** Implement "Staggered Break" protocols to maintain continuous line operation instead of allowing throughput to flatline entirely during scheduled operator breaks.
*   **Preventative Maintenance (PM) Prioritization:** Shift immediately to a structured, data-driven PM schedule, specifically prioritizing the unstable equipment clusters identified in the Pareto analysis.
*   **Supply Chain Alignment:** Launch a cross-functional investigation into the root cause of "Inventory Shortages" to align incoming material planning with true production velocity.

## Next Steps & Action Plan

*   **Automated OEE Trackers:** Deploy real-time visibility dashboards for Availability and Performance metrics for the CO-600 line, allowing floor managers to intervene instantly when output drops.
*   **Downtime Variance Alerts:** Institute strict weekly reviews of the "Top 3" downtime drivers to prevent the recurrence of documented systemic hardware failures.
