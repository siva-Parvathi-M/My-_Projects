# Machine Uptime & Fault Trend Analysis in Tableau

## Project Overview

This project focuses on analyzing manufacturing machine performance using Tableau. By visualizing **machine uptime, downtime**, and **hourly fault trends**, we aim to uncover patterns that impact operational efficiency on the factory floor.

Using a dataset containing timestamped logs for multiple machines, the dashboard highlights when and how frequently machines are experiencing faults and how it affects their overall performance.

---

## Dataset Features

The dataset contains the following columns:

| Column Name     | Description                               |
|------------------|-------------------------------------------|
| `MachineID`      | Unique identifier for each machine         |
| `CycleTime`      | Time taken to complete one production cycle |
| `Temperature`    | Recorded machine temperature               |
| `Pressure`       | Pressure reading at a given time           |
| `Fault`          | 1 = Fault occurred, 0 = No fault           |
| `Timestamp`      | Date and time of the event recorded        |

---

## Key Visualizations

1. **Uptime vs Downtime per Machine per Day**  
   - Shows how long each machine was running vs. down on a daily basis.

2. **Hourly Fault Trend**  
   - Highlights the number of faults that occur during each hour of the day.

3. *(Optional additional insights can be added based on dataset)*

---

## Insights Derived

- Identification of machines with the highest fault rates.
- Pinpoint hours in the day with increased fault frequency.
- Overall machine efficiency trends across days and shifts.

---

## Tools Used

- **Tableau Public** – for interactive dashboard creation.
- **Microsoft Excel / CSV** – for source data formatting and preparation.
