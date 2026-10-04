# Overall Equipment Effectiveness (OEE) Monitoring Dashboard

## 📊 Project Overview
This project delivers an interactive, enterprise-grade **Overall Equipment Effectiveness (OEE)** analytics solution built in **Microsoft Power BI**. The dashboard connects directly to manufacturing execution data to track, break down, and optimize factory floor productivity across three core pillars: **Availability**, **Performance**, and **Quality**.

By transforming raw machine logs and shift schedules into actionable insights, this tool enables plant managers, maintenance teams, and executives to pinpoint the root causes of capacity loss and apply the **80/20 rule** to eliminate structural downtime.

---

## 🚀 Key Features & Visuals

The report follows a proven structural drill-down layout:
*   **Executive KPI Banner:** Real-time visibility into **OEE %**, **Availability %**, **Performance %**, and **Quality %** with Week-over-Week (WoW) delta tracking.
*   **Machine wise downtime :** Machine wise downtime is critical for OEE calculations.
*   **produced qty and defect items :made line and bar graph for produced qty and defect qty material wise.
*   **Added month wise interactive slicers for more engage


---

## 🛠️ Tech Stack & Architecture
*   **BI Platform:** Microsoft Power BI Desktop
*   **Data Models:** Star Schema design featuring optimized **FactProduction** tables joined with dimension tables (`DimMachines`, `DimCalendar`, `DimShifts`, `DimProducts`).
*   **Calculations:** Custom DAX measures for OEE pillars, defect qty, and machine downtime.
*   **Data Sources:** kaggel and google

---

## 📈 Core DAX Formulas Applied
The data model calculates OEE using standard manufacturing logic:

1. **Availability:** `Run Time / Planned Production Time`
2. **Performance:** `(Ideal Cycle Time × Total Count) / Run Time`
3. **Quality:** `Good Count / Total Count`
4. **OEE:** `Availability × Performance × Quality`

*Note: Custom DAX snippets for time-intelligence metrics can be found in the `/dax_measures` folder.*

---

## 📁 Repository Structure
```text
├── assets/                  # Dashboard screenshots and wireframes
├── data/                    # Sample CSV/Excel schemas for data validation
├── dax_measures/            # Text documentation of core DAX formulas
├── documentation/           # Data dictionary and business logic rules
└── OEE_Manufacturing.pbix   # Main Power BI Desktop file
```

---

## 🔧 Getting Started

### Prerequisites
*   [Power BI Desktop](https://microsoft.com) (Latest Version Recommended)
*   Access tokens or connection permissions to the primary data warehouse.

### Deployment & Local Setup
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com
   ```
2. Open `OEE_Manufacturing.pbix` in Power BI Desktop.
3. Navigate to **Home > Transform Data > Data source settings** to re-point the parameters to your local or staging server.
4. Click **Refresh** to populate the data model.

---

## 👥 Dashboard Audience & Usage
*   **Plant Executives:** Review weekly plant-wide performance benchmarks and macro loss trends.
*   **Shift Supervisors:** Monitor shift-level throughput, active lines, and operational quality metrics.
*   **Maintenance Engineers:** Utilize the Pareto downtime tool to proactively address highly frequent machine component failures.


