---
layout: page
title: Self Balancing Robot V1 (Prototype)
description: The foundational autonomous proof-of-concept self-balancing robot.
img: assets/img/projects/self-balancing-robot-v1/cover.jpg
importance: 2
category: fun
related_publications: false
---

The original, foundational self-balancing robot utilizing the **ESP32-S3 (N16R8)** computing core, driven by a custom **Kalman Filter** and high-frequency **PID control loop** system. 

This initial version was a raw engineering prototype built entirely within the ArduinoIDE toolchain to validate our baseline control loops and structural balancing physics before expanding into the upgraded V2 architecture. It focuses purely on autonomous upright stability.

<div class="row">
    <!-- Image 1 (Takes up exactly half the width from mobile up) -->
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/self-balancing-robot-v1/cover.jpg" title="Assembled Mechanical Chassis" class="img-fluid rounded z-depth-1" %}
    </div>
    <!-- Image 2 (Takes up the other half of the width) -->
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/self-balancing-robot-v1/breadboard.jpg" title="Breadboard Layout" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Prototype Overview: The left image shows the raw V1 hardware setup balancing autonomously. The right image shows the breadboard layout.
</div>

## Core Features

*   **State Estimation:** Custom Kalman Filter implementation paired with an MPU6050 IMU for precise autonomous roll angle determination.
*   **Non-Linear Control:** Closed-loop feedback PID controller mechanics featuring manual integral leak adjustments to prevent deadzone windup.
*   **Dynamic Tuning:** Exponential gain-scaling algorithms that automatically scale motor loop coefficients during high-deviation tilts.
*   **Power Management:** Active analog voltage checks safeguarding the 2S LiPo system from dropping beneath unsafe cell margins.
*   **Crash Recovery:** Automated emergency motor shutdown constraints to instantly cut power if the platform tips over past 80 degrees.

<hr class="my-5">

## Repository & Asset Downloads

All production files, mechanical CAD structures, firmware deployment packages, and assembly blueprints for this legacy platform are completely open-source and hosted on GitHub.

👉 **[Download Files & View Project on GitHub](https://github.com/arthurlawson/self-balancing-robot-v1)**

### Repository Highlights:
*   **Firmware Code:** Access to our packaged local dependencies, modular custom PID filters, and raw Kalman matrix calculations.
*   **CAD:** Access to the master SolidWorks (`.SLDPRT`) structural model file alongside print-ready, sliced assembly configurations (`.3mf`).