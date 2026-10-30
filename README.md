# network data dcp 26
This repo is for my dcp 26 assignment, i will be collecting and working on hand picked nework data.


## Project Overview
This project investigates the reliability, speed, and behavior of accommodation Wi-Fi networks under real-world conditions. By manually collecting network metrics over the course of 2-3 weeks, this dataset captures how network performance fluctuates across different times of day, physical locations, connected devices, and measurement tools.

## Research Questions
Before beginning data collection, this project was designed to answer the following core questions:
1. **Ask4 Resident vs. Ask4 Wireless:** Does `Ask4 Resident` provide systematically lower latency and higher download speeds than `Ask4 Wireless` across all dorm locations?
2. **Tool Discrepancy:** Do Google Internet Speed Test and Speedtest.net yield statistically different speed and latency results when testing the same network at the same time?
3. **Device Impact:** Does the device connected to the network significantly affect internet speed and latency?

---

## Data Collection Methodology
Data is collected strictly through **manual, real-world observation and human effort**. No automated scraping, APIs, or historical back-filling are used

* **Frequency:** Data is recorded 6 (hopefully i remember haha) times daily across structured morning, afternoon, and evening windows.
* **Process:** At each collection point, a device is connected to a specific Wi-Fi network at a given location. A speed test is executed manually via Google Internet Speed Test or Speedtest.net, and the values displayed on the screen are recorded by hand[cite: 2] into `data/networkdata.csv`.
* **Evidence:** Daily commits to GitHub serve as the primary verification of consistent, daily human effort. Photos of the collection setup are included below.

---

## Data Dictionary

| Column Name | Type | Units / Format | Description / How Measured |
| :--- | :--- | :--- | :--- |
| **`date`** | Categorical / Date | `YYYY-MM-DD` | The date the speed test was run. |
| **`time`** | Categorical / Time | `HH:MM` | The exact time the test was run. |
| **`location`** | Categorical | Text | Specific physical spot (e.g., `Dorm Room - Desk`, `Study Room`, `Gym`). |
| **`network_name`** | Categorical | Text | The Wi-Fi network connected to (e.g., `Ask4 Resident`, `Ask4 Wireless`). |
| **`device`** | Categorical | Text | The device used for testing (e.g., `Laptop`, `Phone`). |
| **`tool`** | Categorical | Text | The platform used (`Google Speed Test` or `Speedtest.net`). |
| **`download_mbps`** | Numeric | Mbps | Download speed read directly from the screen[cite: 2]. |
| **`upload_mbps`** | Numeric | Mbps | Upload speed read directly from the screen[cite: 2]. |
| **`latency_ms`** | Numeric | Milliseconds (ms) | Ping/latency value read directly from the screen[cite: 2]. |


