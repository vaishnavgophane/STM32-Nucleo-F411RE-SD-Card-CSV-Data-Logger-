## 🧑‍💻 Author

**Vaishnav Gophane**  
Embedded Firmware & IoT Developer
<br>
Pune, India.

📫 **Connect:** [Gmail](mailto:mr.vaishnavgophane@gmail.com) • [GitHub](https://github.com/vaishnavgophane) • [LinkedIn](https://www.linkedin.com/in/vaishnav-gophane-417686284/)

---

# STM32 SD Card CSV Data Logger

A production-style embedded firmware project demonstrating reliable data logging
to an SD card using **STM32**, **SPI**, and **FATFS**. The system periodically records
sensor and system telemetry in **CSV format** for offline analysis.

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

### SD Card & File System
- SPI-based SD card communication
- FATFS integration (diskio layer)
- Automatic file creation and append mode
- CSV header written only once
- Safe file open/close operations

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



