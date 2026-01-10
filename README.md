## 🧑‍💻 Author

**Vaishnav Gophane**  
Embedded Firmware & IoT Developer
<br>
Pune, India.

📫 **Connect:** [Gmail](mailto:mr.vaishnavgophane@gmail.com) • [GitHub](https://github.com/vaishnavgophane) • [LinkedIn](https://www.linkedin.com/in/vaishnav-gophane-417686284/)

---

# STM32 SD Card CSV Data Logger

📊 Embedded Data Acquisition & Logging System (STM32F411)

A professional-grade embedded data acquisition system featuring a quad-DMA architecture (SPI + ADC), real-time RTC timestamping, and CSV data export for seamless Excel analysis.
Built on NUCLEO-F411RE using STM32CubeIDE and HAL drivers.

---

## 📌 Project Motivation

Data logging is a core requirement in many embedded systems such as:
- Energy meters
- Industrial monitoring devices
- IoT edge nodes
- Automotive data recorders

This project replicates **real-world embedded logging requirements** with a focus on
reliability, modular firmware design, and efficient memory usage.

---

## 🎯 Project Objectives

- Interface an SD card using SPI
- Integrate FATFS for file system management
- Log structured telemetry data in CSV format
- Ensure data integrity and safe file handling
- Follow production-grade embedded firmware architecture

---

## ✨ Key Features

| Feature                     | Implementation                        | Performance                                 |
| --------------------------- | ------------------------------------- | ------------------------------------------- |
| Internal Temperature Sensor | ADC1 Channel 16 + DMA (Circular Mode) | Continuous sampling with **0 CPU overhead** |
| MicroSD Storage             | SPI1 with DMA (TX/RX streams)         | **250+ KB/s** sustained write speed         |
| Real-Time Clock (RTC)       | RTC + LSE 32.768 kHz crystal          | Battery-backed, accurate timestamps         |
| File System                 | FatFs v0.14 + SPI Disk I/O            | Append-mode **CSV logging**                 |
| Debug Interface             | USART2 @ 115200 baud                  | Live telemetry & error diagnostics          |


## 🏗️ Advanced System Architecture
flowchart TB
    ADC["ADC1 + DMA2<br/>CH16 Temp<br/>Circular Mode<br/>0 CPU Load"]
    SPI["SPI1 + DMA2<br/>TX: Stream2<br/>RX: Stream0<br/>250+ KB/s"]
    RTC["RTC<br/>LSE 32.768 kHz<br/>Timestamps"]
    FAT["FatFs<br/>Append CSV"]
    SD["SD Card<br/>FAT32"]

    ADC --> FAT
    SPI --> FAT
    RTC --> FAT
    FAT --> SD


### Data Logging
- Periodic data sampling
- Timestamp-based logging
- Human-readable CSV output
- Buffer-based writes to reduce SD access cycles

### Firmware Architecture
- Layered design (Application / Service / BSP)
- Hardware abstraction for portability
- Configurable logging interval
- Centralized error handling

### Reliability
- SD card presence detection
- File system error handling
- Graceful recovery from write failures
- UART-based debug logging

---

## 🧰 Hardware Used

| Component | Description |
|--------|-------------|
| MCU | STM32 Nucleo-F411RE |
| Storage | Micro SD Card (SPI mode) |
| Interface | SPI |
| Debug | USB-UART |
| Power | USB (5V) |

---

## 🧠 Software Stack

| Layer | Technology |
|-----|-----------|
| Application | Embedded C |
| Middleware | FATFS |
| Drivers | STM32 HAL |
| IDE | STM32CubeIDE |
| Debug | UART (Putty) |



