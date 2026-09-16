---
layout: page
title: Self Balancing Robot V2
description: A drivable self-balancing robot that screams when it falls!
img: assets/img/projects/self_balancing_robot_v2/cover.jpg
importance: 1
category: fun
related_publications: false
---

An advanced self-balancing robot utilizing the **ESP32-S3 (N16R8)** computing core, driven by a custom **Kalman Filter** and high-frequency **PID control loop** system. 

This project features a fully **custom-designed main controller PCB, proudly sponsored and manufactured by JLCPCB**. Built entirely within the PlatformIO ecosystem, this hardware platform integrates an MPU6050 IMU, DRV8833 motor driver, 2S LiPo battery safety logic, lighting, and onboard speaker playback systems.

<div class="row">
    <!-- Image 1 (Takes up exactly half the width from mobile up) -->
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/self_balancing_robot_v2/chassis_up.jpg" title="Assembled Mechanical Chassis" class="img-fluid rounded z-depth-1" %}
    </div>
    <!-- Image 2 (Takes up the other half of the width) -->
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/self_balancing_robot_v2/pcb.jpg" title="Custom PCB Details" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Hardware Overview: The left image shows the fully assembled robot actively balancing. The right image displays the fully populated custom controller PCB designed by me and manufactured by JLCPCB.
</div>

## Core Features

*   **Advanced Estimation:** Custom Kalman Filter implementation paired with an MPU6050 IMU for precise roll angle determination.
*   **Wireless Remote Control:** Directional steering control handled over a dedicated **ESP-NOW** wireless connection.
*   **Motion Control:** Dual-motor balancing algorithms with custom gain scheduling to aid in active stabilization.
*   **Hardware Protection:** Automated motor shutdown constraints to prevent destructive runaway crashes.
*   **Power Management:** Active voltage checks safeguarding the 2S LiPo system from dropping beneath unsafe cell margins.
*   **Audio & Visuals:** Integrated 2P Edison filament LEDs with status animations alongside real-time sample-synchronized audio playback configured to make the robot scream.

<hr class="my-5">

## Repository & Asset Downloads

All production files, mechanical CAD folders, firmware deployment packages, and assembly setup blueprints are completely open-source and hosted on GitHub.

👉 **[Download Files & View Project on GitHub](https://github.com/arthurlawson/self-balancing-robot-v2)**

### Repository Highlights:
*   **Bill of Materials:** Complete component checklist detailing the TT Motors, MPM3610 buck regulator, speaker setups, and fastener sizing.
*   **Firmware Setup Guide:** Comprehensive `config.h` parameter walkthrough, audio tracking conversions, and PlatformIO environment properties.
*   **Hardware Setup Guide:** Access to production-ready `.3mf` print structures, raw SolidWorks history logs, and factory-ready Gerber export packages.
