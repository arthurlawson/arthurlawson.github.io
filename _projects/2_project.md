---
layout: page
title: Self Balancing Robot V1 (Prototype)
description: The foundational proof-of-concept for a Brushed DC self-balancing robot.
img: assets/img/projects/self-balancing-robot-v1/cover.jpg
importance: 2
category: robotics
related_publications: false

_styles: >
    .section-heading {
        font-family: 'Playfair Display', Georgia, serif;
        font-size: 2.6rem;
        font-weight: normal;
        margin-top: 0px;
        margin-bottom: 24px;
        color: var(--global-text-color);
        letter-spacing: -0.5px;
    }
    .section-subheading {
        font-family: 'Playfair Display', Georgia, serif;
        font-size: 1.9rem;
        font-weight: normal;
        margin-top: 40px;
        margin-bottom: 30px;
        color: var(--global-text-color);
        letter-spacing: -0.5px;
    }
    .section-divider {
        border: 0;
        border-top: 1px solid var(--global-divider-color);
        width: 100%;
        margin-top: 50px;
        margin-bottom: 50px;
    }
    .subtitle-theme {
        line-height: 1.6;
        font-size: 1rem;
        font-weight: 400;
        letter-spacing: 1.5px;
        color: var(--global-theme-color);
        min-width: 140px;
        display: inline-block;
        padding-top: 3px;
        text-transform: uppercase;
    }
    .body-long {
        line-height: 1.65;
        font-size: 1.1rem;
        font-weight: 350;
        text-align: justify;
        color: var(--global-text-color);
    }
    .body-normal {
        line-height: 1.6;
        font-size: 1rem;
        font-weight: 300;
        text-align: left;
        color: var(--global-text-color);
    }
    .highlight {
        color: var(--global-theme-color) !important;
        font-weight: inherit !important;
    }
    .image-fig-text {
        line-height: 1.6;
        font-size: 0.85rem;
        font-weight: 400;
        min-width: auto;
        padding: 0;
        margin-top: 5px;
        margin-right: 6px;
        letter-spacing: 1.5px;
        color: var(--global-theme-color);
        display: inline-block;
        text-transform: uppercase;
    }
    .image-caption {
        font-size: 0.85rem !important;
        font-weight: 300 !important;
        letter-spacing: 0.3px !important;
        margin-top: 5px;
        text-align: center;
        color: var(--global-text-color);
        opacity: 0.8;
    }
    .card-container {
        border-left: 4px solid var(--global-theme-color);
        padding-left: 15px;
        height: 100%;
    }
    .card-title {
        font-size: 1rem;
        font-weight: bold;
        color: var(--global-text-color);
        margin-bottom: 5px !important;
    }
    .card-body {
        line-height: 1.6 !important;
        font-size: 1rem;
        margin: 0px !important;
        padding: 0px !important;
        color: var(--global-text-color);
        text-align: left;
    }

    /* --- DYNAMIC FOCUSING --- */
    .focus-group {
        opacity: 0.03 !important; 
        filter: blur(2px);
        transition: 
            opacity 0.5s cubic-bezier(0.215, 0.610, 0.355, 1),
            filter 0.5s cubic-bezier(0.215, 0.610, 0.355, 1);
        will-change: opacity, filter;
    }
    
    .focus-group.is-focused {
        opacity: 1 !important;
        filter: blur(0px) !important;
    }

    /* --- AUTO PLAYBACK COUPLING --- */
    /* Controls the robot GIF loop instantly when its parent block gains focus */
    .focus-group:not(.is-focused) .live-gif-loop {
        opacity: 0 !important;
        pointer-events: none;
    }
    .focus-group.is-focused .live-gif-loop {
        opacity: 1 !important;
    }

    /* --- DESKTOP AND MOBILE LAYOUT CONTROLS --- */
    @media (max-width: 767.98px) {
        .sticky-media-column {
            position: relative !important;
            top: 0 !important;
            margin-top: 30px;
        }
    }

    @media (prefers-reduced-motion: reduce) {
        .focus-group, .live-gif-loop {
            opacity: 1 !important;
            transition: none !important;
        }
    }
---

<div class="synopsis-block">
    <div class="d-flex flex-column flex-md-row align-items-start" style="margin-top: 40px; gap: 50px;">
    
        <!-- Left Side: Text (60% Width) -->
        <div class="w-100 w-md-60 d-flex flex-column justify-content-start">

            <!-- Focus Group 1 -->
            <div class="focus-group is-focused" data-group="synopsis">
                <h2 class="section-heading">Project Synopsis</h2>
            
                <p class="body-long">
                    The V1 platform serves as the foundational hardware proof-of-concept for a <span class="highlight">Brushed DC Self-Balancing Robot</span>.
                </p>
                <p class="body-long">
                    Developed entirely within the <span class="highlight">Arduino IDE toolchain</span>, this initial prototype focused on establishing the <span class="highlight">real-time control loops</span> 
                    and verifying the ability to balance despite the inherent nonlinearities of <span class="highlight">encoderless Brushed DC Motors</span>.
                </p>
            </div>
            
            <div class="section-divider" style="width: 100%; margin-top: 30px; margin-bottom: 24px;"></div>

            <!-- Focus Group 2 -->
            <div class="focus-group" data-group="metadata">
                <div class="d-flex flex-column" style="gap: 20px;">
                    <div class="d-flex flex-column flex-sm-row align-items-start" style="gap: 8px 16px;">
                        <span class="subtitle-theme">
                            Focus Area
                        </span>
                        <span class="body-normal">
                            Breadboard prototyping, low-level firmware architecture, and control loop verification.
                        </span>
                    </div>

                    <div class="d-flex flex-column flex-sm-row align-items-start" style="gap: 8px 16px;">
                        <span class="subtitle-theme">
                            Key Achievements
                        </span>
                        <span class="body-normal">
                            Successfully maintained continuous upright stability against light external disturbances.
                        </span>
                    </div>
                </div>
            </div>

        </div>

        <!-- Right Side: The Media Showcase Frame (40% Width) -->
        <div class="w-100 w-md-40 d-flex flex-column align-items-center justify-content-start sticky-media-column focus-group" 
            data-group="synopsis-photo"
            style="position: -webkit-sticky; position: sticky; top: 100px; z-index: 10;">

            <!-- Smart Media structural bounding container -->
            <div class="smart-gif-frame zoomable" style="width: 100%; aspect-ratio: 1 / 1; border-radius: 6px; border: 2px solid var(--global-text-color); overflow: hidden; position: relative;">
                
                <!-- BASE LAYER: Static, unmoving placeholder photo handling the out-of-focus layout safely -->
                <img class="frozen-gif-placeholder" 
                    src="{{ 'assets/img/projects/self-balancing-robot-v1/cover.jpg' | relative_url }}" 
                    alt="V1 Prototype Frozen Baseline Pose" 
                    style="width: 100%; height: 100%; object-fit: cover; display: block; position: absolute; top: 0; left: 0; z-index: 1;">
                
                <!-- SURFACE LAYER: Live looping animation transitioning smoothly based on viewport focus -->
                <img class="live-gif-loop" 
                    src="{{ 'assets/img/projects/self-balancing-robot-v1/demo_balancing.gif' | relative_url }}" 
                    alt="V1 Prototype Active Balancing Loop" 
                    style="width: 100%; height: 100%; object-fit: cover; display: block; position: absolute; top: 0; left: 0; z-index: 2; transition: opacity 0.4s cubic-bezier(0.4, 0, 0.2, 1); will-change: opacity;">
                    
            </div>
            
            <!-- Minimalist Caption Centered Directly Below Frame -->
            <div class="image-caption">
                <span class="image-fig-text">Fig 1.1</span> 
                V1 balancing demonstration under light external disturbances.
            </div>

        </div>
    </div>
</div>

<!-- Focus Group 3 -->
<div class="focus-group" data-group="skills">

    <h3 class="section-subheading">
        Core Engineering Skills Acquired
    </h3>

    <!-- Row container using standard theme spacing gutters -->
    <div class="row g-5">

        <div class="col-md-6 col-12 mb-4">
            <div class="card-container">
                <span class="card-title">Embedded Architecture</span>
                <p class="card-body">
                    Configured memory partitions, clock limits, and hardware I2C transmission on the ESP32-S3 (N16R8) microcontroller.
                </p>
            </div>
        </div>

        <div class="col-md-6 col-12 mb-4">
            <div class="card-container">
                <span class="card-title">Power Distribution</span>
                <p class="card-body">
                    Integrated a buck converter to regulate the voltage rails, ensuring high current motors do not starve MCU logic.
                </p>
            </div>
        </div>

        <div class="col-md-6 col-12 mb-4">
            <div class="card-container">
                <span class="card-title">State Estimation</span>
                <p class="card-body">
                    Implemented a discrete multivariable Kalman Filter algorithm to fuse noisy sensor data and resolve gyroscopic drift.
                </p>
            </div>
        </div>

        <div class="col-md-6 col-12 mb-4">
            <div class="card-container">
                <span class="card-title">Non-Linear Control</span>
                <p class="card-body">
                    Designed an independent PID controller to map vertical setpoint error into discrete PWM duty cycles for motor actuation.
                </p>
            </div>
        </div>
    </div>

</div>

<hr class="section-divider">

<!-- Bill of Materials -->
<!-- Focus Group 4 -->
<div class="focus-group" data-group="bom">

<h2 class="section-heading">Bill of Materials (BOM)</h2>

<p class="body-long" style="margin-bottom: 30px;">
    To establish a clear development history, all component selections, primary vendors, and unit costs are logged below:
</p>

<div markdown="1">

| Component Description | Part Specification (with link) | Primary Sourcing | Unit Cost (GBP) | Engineering Rationale |
| :--- | :--- | :--- | :--- | :--- |
| **Power Source** | [2x 3.7V LiPo Battery](https://www.aliexpress.com/item/1005009821398927.html) | AliExpress | £4.49 | High-discharge power source necessary to counter immediate motor torque spikes. |
| **Battery Holder** | [1x 2 Slots LiPo Battery Holder](https://www.aliexpress.com/item/1005010290798449.html) | AliExpress | £0.58 | Secure the batteries in a 2S configuration for a raw 7.4V. |
| **Buck Converter** | [1x MPM3610 3V3](https://thepihut.com/products/adafruit-mpm3610-3-3v-buck-converter-breakout-21v-in-3-3v-out-at-1-2a) | The Pi Hut | £5.80 | Ultra-compact 21V, 1.2A step-down module providing clean 3.3V logic power. |
| **Microcontroller Core** | [1x ESP32-S3 (N16R8)](https://www.aliexpress.com/item/1005007319706057.html) | AliExpress | £5.00 | 240MHz dual-core processing power with ample flash space for control calculations. |
| **Inertial Measurement Unit** | [1x MPU6050 GY-521](https://www.aliexpress.com/item/1005010057794277.html) | AliExpress | £1.27 | 3-axis accelerometer and 3-axis gyroscope combined on a single I2C bus. |
| **Dual Motor Driver** | [1x DRV8833](https://www.aliexpress.com/item/1005009044264044.html) | AliExpress | £0.90 | Dual MOSFET H-Bridge supporting low-saturation resistance and slow-decay active braking routines. |
| **Actuators And Wheel Pack** | [2x BDC TT Geared Motors with Wheels](https://www.aliexpress.com/item/1005007227331566.html) | AliExpress | £2.60 | Budget-friendly brushed DC motors with wheels. |
| **Chassis Structure** | Custom 3D Printed Chassis (~91g PLA) | University Sourced Printer | — | Custom structural frame designed to mount the TT motors, battery holder, and breadboard. |
| **Miscellaneous** | 2x Half-size Breadboards (rails removed/merged), Assorted jumper wires | Sourced in-house | — | Rapid prototyping framework utilized for fast signal path adjustments. |
| **Total Prototype Cost** | | | **£20.64** | |

</div>

</div>

<hr class="section-divider">

<!-- Focus Group 3 -->
<div class="focus-group" data-group="schematics">

    <h2 class="section-heading">Hardware and Electrical Schematics</h2>

    <p class="body-long" style="margin-bottom: 30px;">
        The electrical network was constructed across two half-sized breadboards, mated together with their power rails removed:
    </p>

    <div class="row g-4" style="margin-bottom: 25px;">
    
        <!-- Left Column Frame: Physical Breadboard Prototype Showcase -->
        <div class="col-12 col-md-6 d-flex flex-column align-items-center">
            <!-- Aspect ratio set to standard 4/3 photography bounds -->
            <div class="zoomable" style="width: 100%; aspect-ratio: 4 / 3; border-radius: 6px; border: 2px solid var(--global-text-color); overflow: hidden; background-color: var(--global-bg-overlay); position: relative; display: flex; align-items: center; justify-content: center;">
                
                <!-- Replace with the exact local directory path string to your physical setup photo -->
                <img class="img-zoomable" data-zoomable
                    src="{{ 'assets/img/projects/self-balancing-robot-v1/breadboard.jpg' | relative_url }}" 
                    alt="Physical Dual Half-Size Breadboard Prototyping Assembly" 
                    style="width: 100%; height: 100%; object-fit: cover; display: block;">
                    
            </div>
            <div class="image-caption">
                <span class="image-fig-text">Fig 1.2</span> 
                Physical dual half-size breadboard assembly with wiring.
            </div>
        </div>

        <!-- Right Column Frame: Professional Schematic CAD Blueprint Showcase -->
        <div class="col-12 col-md-6 d-flex flex-column align-items-center">
            <!-- Object fit set to contain to protect fine wire layout tracks without cropping symbols -->
            <div class="zoomable" style="width: 100%; aspect-ratio: 4 / 3; border-radius: 6px; border: 2px solid var(--global-text-color); overflow: hidden; background-color: var(--global-bg-overlay); position: relative; display: flex; align-items: center; justify-content: center;">
                
                <!-- Replace with the exact local directory path string to your compiled vector drawing blueprint -->
                <img class="img-zoomable" data-zoomable
                    src="{{ 'assets/img/projects/self-balancing-robot-v1/circuit-schematic.png' | relative_url }}" 
                    alt="Electrical Circuit Diagram Schematic" 
                    style="width: 110%; height: 110%; object-fit: fit; display: block;">
                    
            </div>
            <div class="image-caption">
                <span class="image-fig-text">Fig 1.3</span> 
                Electrical circuit diagram schematic detailing logic lines and pin layouts.
            </div>
        </div>
    </div>

</div>

<div class="focus-group" data-group="highlights">

    <h3 class="section-subheading">
        Circuit Architecture Highlights
    </h3>

    <div class="row g-5">

        <div class="col-md-6 col-12 mb-4">
            <div class="card-container">
                <span class="card-title">Power Routing</span>
                <p class="card-body">
                    The 2S LiPo Battery delivers a raw 7.4V voltage directly to the DRV8833 motor driver pins. Concurrently, the MPM3610 step-down buck converter drops that shifting battery voltage down to 3.3V to drive the ESP32-S3 and IMU.
                </p>
            </div>
        </div>

        <div class="col-md-6 col-12 mb-4">
            <div class="card-container">
                <span class="card-title">Signal Topology</span>
                <p class="card-body">
                    The MPU6050 communicates with the ESP32-S3 over a dedicated hardware I2C bus operating at 400kHz clock speed to ensure low latency data retrieval.
                </p>
            </div>
        </div>
    </div>

</div>

<hr class="section-divider">

<div class="focus-group" data-group="firmware">

    <h2 class="section-heading">Firmware Architecture</h2>

    <p class="body-long" style="margin-bottom: 30px;">
        The firmware executes on a non-blocking timing loop within the Arduino framework to ensure fixed-interval control updates.
    </p>

</div>

### 1. State Estimation via a Custom Kalman Filter
* Raw IMU accelerometer readings are susceptible to high-frequency noise from chassis vibrations, while the gyroscope exhibits long term drift.
* To isolate the true tilt angle, a custom two-state Kalman Filter calculates the error covariance matrices in real time, yielding clean and drift free orientation data.

### 2. PID Control loop Implementation
* The filtered tilt angle estimate is compared against the vertical setpoint. 
* A discrete Proportional-Integral-Derivative (PID) loop continuously recalculates this tilt error to output updated motor speeds.

### 3. Gain Scaling
* Exponential curves were used to scale controller outputs dynamically if the robot suffers from sudden deep tilt variations, maximizing recovery torque.

<hr class="my-5">

## Mechanical Chassis

* **CAD Modelling:** The chassis, which incorporates motor mounts and two decks, was modelled as a single integrated part within SolidWorks.
* **Component Placement:** Heavy components (such as the 2S LiPo battery) were intentionally fixed onto the highest deck of the robot. This increases the system's overall moment of inertia, which minimizes angular acceleration ($α = \tau / I$) and grants the controller more recovery time to counteract rapid changes in tilt.
* **Fabrication:** The chassis was fabricated using FDM 3D printing.

<hr class="my-5">

## Design Issues with V1 (Prototype)
While the V1 prototype successfully validated my stability algorithms, it highlighted critical physical and architectural drawbacks:
1. **Physical Circuit Instability:** Jumper wires on breadboards are prone to disconnection caused by vibrations during operation.
2. **Logic Resetting:** Inductive spikes from sudden motor switching periodically caused voltage sags across the shared power paths, introducing noise and risking unexpected ESP32 brownouts.
3. **Chassis Torsion:** The initial single part chassis, though simplistic, faced issues with rotational torsion due to the lack of reinforcing connecting platform at the physical base of the chassis (near the wheels). 
4. **Lack of Feedback Telemetry:** The current design lacked any telemetry, state indication, or physical warning systems to signify failures or tipping to the user.
5. **Static Behaviour (No State Machine):** The system lacked flexibilty in run time, operating strictly on a single execution layer with no capacity for transitioning to other states or driving modes.

<hr class="my-5">

## Improvements for V2
To target the structural and electrical bottlenecks identified in the prototype phase, the design criteria for the upcoming V2 iteration focuses on these 5 areas:
1. **Custom PCB Implementation:** Transitioning away from messy breadboards to a custom PCB designed in KiCAD.
2. **Power Isolation and Optimization:** Combating microcontroller sags by using dedicated decoupling capacitors directly across high-frequency motor signal paths and incorporating bulk storage capacitors near the main voltage source.
3. **Multiple-Part Modular Enclosure** Redesigning the chassis as an assembly of structural components within SolidWorks. The new chassis will have a fully enclosed frame and minimizes the rotational torsion issues.
4. **Active Visual and Auditory Telemetry:** V2 will integrate user feedback using both edison filaments paired with a front facing light diffuser panel for status lighting, alongside a speaker to alert the user when the robot has fallen over (passed a certain tilt threshold).
5. **Wireless Remote Control via ESP-NOW:** Developing a secondary ESP32 remote control transmitter that uses the ESP-NOW protocol to pass directional inputs via a D-pad of buttons to the robot. This will support four new movement states: forward, backwards, left, and right.

<hr class="my-5">

## Repository & Asset Downloads
All production files, mechanical CAD structures, firmware deployment packages, and assembly blueprints for this legacy platform are completely open-source and hosted on GitHub.
*   **Firmware Code:** Access to the packaged local dependencies, custom PID filter, and raw Kalman matrix calculations.
*   **CAD:** Access to the master SolidWorks (`.SLDPRT`) structural model file alongside print-ready, sliced assembly configurations (`.3mf`).

👉 **[Download Files & View Project on GitHub](https://github.com/arthurlawson/self-balancing-robot-v1)**


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

<!-- Scroll Focus Engine -->
<script>
  document.addEventListener("DOMContentLoaded", function () {
    const focusItems = document.querySelectorAll(".focus-group");
    if (!focusItems.length) return;

    // Sets focal target arcs (Wakes up sections gracefully when crossing center view limits)
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        entry.target.classList.toggle("is-focused", entry.isIntersecting);
      });
    }, { rootMargin: "-25% 0px -15% 0px", threshold: [0, 0.15] }); // dont show for top 27% and bottom 17% of screen

    focusItems.forEach(item => observer.observe(item));
  });
</script>