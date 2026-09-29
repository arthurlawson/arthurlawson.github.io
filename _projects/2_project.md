---
layout: page
title: Self Balancing Robot V1 (Prototype)
description: The foundational proof-of-concept for a Brushed DC self-balancing robot.
img: assets/img/projects/self-balancing-robot-v1/cover.jpg
importance: 2
category: robotics
related_publications: false
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
            
            <div class="section-divider" style="width: 100%; margin-top: 24px; margin-bottom: 24px;"></div>

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
        <div class="w-100 w-md-40 d-flex flex-column align-items-center justify-content-start focus-group" 
            data-group="synopsis-photo"
            style="z-index: 10;">

            <!-- Smart Media structural bounding container -->
            <div class="shadowy zoomy8" style="width: 100%; aspect-ratio: 1 / 1;">
                <img src="{{ 'assets/img/projects/self-balancing-robot-v1/demo_balancing.gif' | relative_url }}" 
                     alt="V1 Prototype Active Balancing Loop" 
                     draggable="false"
                     style="width: 100%; height: 100%; object-fit: contain;"> 
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
                <div class="card-content-shift">
                    <span class="card-title">Embedded Architecture</span>
                    <p class="card-body">
                        Configured memory partitions, clock limits, and hardware I2C transmission on the ESP32-S3 (N16R8) microcontroller.
                    </p>
                </div>
            </div>
        </div>

        <div class="col-md-6 col-12 mb-4">
            <div class="card-container">
                <div class="card-content-shift">
                    <span class="card-title">Power Distribution</span>
                    <p class="card-body">
                        Integrated a buck converter to regulate the voltage rails, ensuring high current motors do not starve MCU logic.
                    </p>
                </div>
            </div>
        </div>

        <div class="col-md-6 col-12 mb-4">
            <div class="card-container">
                <div class="card-content-shift">
                    <span class="card-title">State Estimation</span>
                    <p class="card-body">
                        Implemented a discrete multivariable Kalman Filter algorithm to fuse noisy sensor data and resolve gyroscopic drift.
                    </p>
                </div>
            </div>
        </div>

        <div class="col-md-6 col-12 mb-4">
            <div class="card-container">
                <div class="card-content-shift">
                    <span class="card-title">Non-Linear Control</span>
                    <p class="card-body">
                        Designed an independent PID controller to map vertical setpoint error into discrete PWM duty cycles for motor actuation.
                    </p>
                </div>
            </div>
        </div>
    </div>

</div>

<hr class="section-divider">

<div class="focus-group" data-group="mechanical-design">
    <h3 class="section-heading" style="margin-bottom: 10px">Mechanical Design</h3>
    
    <div class="discrete-card-carousel" style="margin-top: 1px; margin-bottom: 0px;">
        <div class="carousel-centering-frame">
            
            <!-- Kinetic Gear Train Track -->
            <div class="kinetic-gear-assembly-track">
                <div><i id="kinetic-gear-left" class="fa-solid fa-gear"></i></div>
                <div><i id="kinetic-gear-right" class="fa-solid fa-gear" style="transform: rotate(30deg);"></i></div>
            </div>

            <!-- Viewport Surface Container -->
            <div id="discrete-slider-surface" class="carousel-viewport-surface">
                
                <!-- Left Navigation Control Button -->
                <button id="discrete-btn-left" class="carousel-nav-btn btn-left" aria-label="Slide Left">
                    <i class="fa-solid fa-chevron-left"></i>
                </button>

                <span class="console-drag-hint" style="opacity: 0.85 !important;"><i class="fa-solid fa-hand-rock"></i> Drag Card or Click Arrows to Browse</span>

                <div class="carousel-card-chamber">
                    <div id="discrete-slider-rail" class="carousel-slider-rail">
                        
                        <!-- CARD 1 -->
                        <div class="discrete-content-card shadowy clicky">
                            <div class="zoomy10" style="position: relative; width: 100%; aspect-ratio: 4 / 3; overflow: hidden; border-radius: 6px; margin-bottom: 14px; background-color: transparent">
                                <span class="console-drag-hint" style="position: absolute; top: 10px; left: 10px; z-index: 10; opacity: 1 !important;">
                                    <i class="fa-solid fa-maximize"></i> Click to Expand
                                </span>
                                <img class="img-zoomable" data-zoomable
                                    src="{{ 'assets/img/projects/self-balancing-robot-v1/chassis-cad.png' | relative_url }}" 
                                    alt="SolidWorks CAD View" 
                                    draggable="false"
                                    style="width: 100%; height: 100%; object-fit: cover;">
                            </div>
                            <h4>01 // Monolithic CAD Model</h4>
                            <p>The chassis, which incorporates inset motor mounts and two decks, was modelled as a single integrated part within SolidWorks for prototype simplicity.</p>
                        </div>

                        <!-- CARD 2 -->
                        <div class="discrete-content-card shadowy clicky">
                            <div class="zoomy10" style="position: relative; width: 100%; aspect-ratio: 4 / 3; overflow: hidden; border-radius: 6px; margin-bottom: 14px; background-color: var(--global-bg-color);">
                                <img class="img-zoomable" data-zoomable
                                    src="{{ 'assets/img/projects/self-balancing-robot-v1/chassis-empty.jpg' | relative_url }}" 
                                    alt="Empty Chassis View" 
                                    draggable="false"
                                    style="width: 100%; height: 100%; object-fit: cover;">
                            </div>
                            <h4>02 // FDM Fabrication</h4>
                            <p>The integrated chassis was fabricated using fused deposition modelling (FDM) 3D printing, and printed in Standard PLA.</p>
                        </div>

                        <!-- CARD 3 -->
                        <div class="discrete-content-card shadowy clicky">
                            <div class="zoomy10" style="position: relative; width: 100%; aspect-ratio: 4 / 3; overflow: hidden; border-radius: 6px; margin-bottom: 14px; background-color: var(--global-bg-color);">
                                <img class="img-zoomable" data-zoomable
                                    src="{{ 'assets/img/projects/self-balancing-robot-v1/chassis-full.jpg' | relative_url }}" 
                                    alt="Populated Chassis View" 
                                    draggable="false"
                                    style="width: 100%; height: 100%; object-fit: cover;">
                            </div>
                            <h4>03 // Component Placement</h4>
                            <p>The heaviest component (2S LiPo battery) was intentionally placed on the highest deck. This increases the system's total moment of inertia (<span style="font-family: serif; font-style: italic; font-weight: 600;">I</span>), minimizing angular acceleration (<span style="font-family: serif; font-style: italic; font-weight: 600;">α = τ / I</span>) to grant the PID controller more recovery time to counteract rapid tilt changes.</p>
                        </div>

                    </div>
                </div>

                <!-- Right Navigation Control Button -->
                <button id="discrete-btn-right" class="carousel-nav-btn btn-right" aria-label="Slide Right">
                    <i class="fa-solid fa-chevron-right"></i>
                </button>

            </div>
        </div>

        <!-- Navigation Dash Dots Indicator Trackway -->
        <div style="display: flex; justify-content: center; gap: 8px; margin-top: 0px; margin-bottom: 40px; align-items: center; position: relative; z-index: 15;">
            <button class="carousel-dot-indicator" onclick="jumpToCarouselIndex(0)" aria-label="Go to Slide 1" style="width: 24px; height: 3px; background: var(--global-theme-color); border: none; border-radius: 2px; padding: 0; cursor: pointer; transition: width 0.3s ease, background 0.3s ease; opacity: 1;"></button>
            <button class="carousel-dot-indicator" onclick="jumpToCarouselIndex(1)" aria-label="Go to Slide 2" style="width: 12px; height: 3px; background: var(--global-text-color); border: none; border-radius: 2px; padding: 0; cursor: pointer; transition: width 0.3s ease, background 0.3s ease; opacity: 0.25;"></button>
            <button class="carousel-dot-indicator" onclick="jumpToCarouselIndex(2)" aria-label="Go to Slide 3" style="width: 12px; height: 3px; background: var(--global-text-color); border: none; border-radius: 2px; padding: 0; cursor: pointer; transition: width 0.3s ease, background 0.3s ease; opacity: 0.25;"></button>
        </div>
    </div>
</div>

<hr class="section-divider">

<!-- Focus Group 3 -->
<div class="focus-group" data-group="schematics">

    <h2 class="section-heading">Electrical Hardware</h2>

    <p class="body-long" style="margin-bottom: 30px;">
        The electrical network was constructed across two half-sized breadboards, mated together with their power rails removed:
    </p>

    <div class="row g-4" style="margin-bottom: 25px;">
    
        <!-- Left Column Frame: Physical Breadboard Prototype Showcase -->
        <div class="col-12 col-md-6 d-flex flex-column align-items-center">
            <div class="shadowy clicky zoomy7" style="width: 100%; aspect-ratio: 4 / 3;">
                <img class="img-zoomable" data-zoomable
                    src="{{ 'assets/img/projects/self-balancing-robot-v1/breadboard.jpg' | relative_url }}" 
                    alt="Physical Dual Half-Size Breadboard Prototyping Assembly" 
                    draggable="false"
                    style="width: 100%; height: 100%; object-fit: cover;">   
            </div>
            <div class="image-caption">
                <span class="image-fig-text">Fig 1.2</span> 
                Physical dual half-size breadboard assembly with wiring.
            </div>
        </div>

        <!-- Right Column Frame: Professional Schematic CAD Blueprint Showcase -->
        <div class="col-12 col-md-6 d-flex flex-column align-items-center">
            <div class="shadowy clicky zoomy8" style="width: 100%; aspect-ratio: 4 / 3;">
                <img class="img-zoomable" data-zoomable
                    src="{{ 'assets/img/projects/self-balancing-robot-v1/circuit-schematic.png' | relative_url }}" 
                    alt="Electrical Circuit Diagram Schematic" 
                    draggable="false"
                    style="width: 110%; height: 110%; object-fit: fit;">
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
                <div class="card-content-shift">
                    <span class="card-title">Power Routing</span>
                    <p class="card-body">
                        The 2S LiPo Battery delivers a raw 7.4V voltage directly to the DRV8833 motor driver pins. Concurrently, the MPM3610 step-down buck converter drops that shifting battery voltage down to 3.3V to drive the ESP32-S3 and IMU.
                    </p>
                </div>
            </div>
        </div>

        <div class="col-md-6 col-12 mb-4">
            <div class="card-container">
                <div class="card-content-shift">
                    <span class="card-title">Signal Topology</span>
                    <p class="card-body">
                        The MPU6050 communicates with the ESP32-S3 over a dedicated hardware I2C bus operating at 400kHz clock speed to ensure low latency data retrieval.
                    </p>
                </div>
            </div>
        </div>
    </div>

</div>

<hr class="section-divider">

<div class="focus-group" data-group="state-estimation">
    <h2 class="section-heading">Firmware Architecture</h2>

    <p class="body-long">
    The firmware executes on a non-blocking timing loop within the Arduino framework to ensure fixed-interval control updates.
    </p>

    <h3 class="section-subheading">State Estimation via a Custom Kalman Filter</h3>

    <!-- Dotted Timeline System Track -->
    <div style="border-left: 2px dotted var(--global-theme-color); padding-left: 30px; margin-left: 15px; margin-top: 20px; margin-bottom: 30px;">
        
        <!-- Step 1: Challenge -->
        <div class="timeline-step outliny hovery4" style="position: relative; margin-bottom: 25px; max-width: 800px;">
            <div class="timeline-node" style="position: absolute; left: -42px; top: 13px; width: 22px; height: 22px; border-radius: 50%; background: var(--global-bg-color); border: 2px solid var(--global-theme-color); color: var(--global-theme-color); display: flex; align-items: center; justify-content: center; font-size: 0.75rem; font-weight: bold; font-family: monospace; z-index: 2;">1</div>
            
            <h4 class="card-title">The Challenge</h4>
            <p class ="card-body" style="opacity: 0.85; max-width: 768px;">
                Raw IMU accelerometer readings are highly susceptible to high-frequency noise from chassis vibrations, while gyroscope 
                readings experience cumulative, low-frequency sensor drift over time.
            </p>
        </div>

        <!-- Step 2: Solution -->
        <div class="timeline-step outliny hovery4" style="position: relative; margin-bottom: 25px; max-width: 800px;">
            <div class="timeline-node" style="position: absolute; left: -42px; top: 13px; width: 22px; height: 22px; border-radius: 50%; background: var(--global-bg-color); border: 2px solid var(--global-theme-color); color: var(--global-theme-color); display: flex; align-items: center; justify-content: center; font-size: 0.75rem; font-weight: bold; font-family: monospace; z-index: 2;">2</div>
            
            <h4 class="card-title">The Solution</h4>
            <p class ="card-body" style="opacity: 0.85; max-width: 768px;">
                Developed a discrete, two-state Kalman filter that fuses the gyroscope and accelerometer data and dynamically injects
                process noise (Q) and measurement noise (R) to model real-world uncertainties.
            </p>
        </div>

        <!-- Step 3: Outcome -->
        <div class="timeline-step outliny hovery4" style="position: relative; max-width: 800px;">
            <div class="timeline-node" style="position: absolute; left: -42px; top: 13px; width: 22px; height: 22px; border-radius: 50%; background: var(--global-bg-color); border: 2px solid var(--global-theme-color); color: var(--global-theme-color); display: flex; align-items: center; justify-content: center; font-size: 0.75rem; font-weight: bold; font-family: monospace; z-index: 2;">3</div>
            
            <h4 class="card-title">The Outcome</h4>
            <p class ="card-body" style="opacity: 0.85; max-width: 768px;">
                Isolates the true tilt angle (θ) by eliminating noise, providing clean state estimation for the robot controller.
            </p>
        </div>

    </div>


    <!-- Code Accordion -->
    <input type="checkbox" id="kalman-code-toggle" class="accordion-toggle-input">
    
    <div class="portfolio-accordion shadowy">
        <!-- The header row click target -->
        <label for="kalman-code-toggle" class="accordion-header hovery1">
            <span>View C++ Kalman Filter Implementation</span>
            <span class="accordion-icon"></span>
        </label>

        <!-- The content tray -->
        <div class="accordion-content">
            {% highlight cpp %}
void KalmanFilter::predict(float *gyro) { 
    // A Priori State Estimate with Gyroscope Readings ( New_Angle = Old_Angle + (Angular_Velocity * dt_sec) )
    roll  += gyro[0] * RAD_TO_DEG * dt_sec;
    pitch += gyro[1] * RAD_TO_DEG * dt_sec;

    // Uncertainty Grows (To account for gyroscopic drift, inject Process Noise Q into the Covariance matrix)
    Sigma[0] += Q[0] * dt_sec;
    Sigma[3] += Q[1] * dt_sec;
}
            {% endhighlight %}

            {% highlight cpp %}
void KalmanFilter::measurement_task(float *accel) {
    // Calculate True Measured Tilt with Accelerometer Readings
    m_roll  = atan2(accel[1],  sqrt(sqr(accel[0]) + sqr(accel[2]))) * RAD_TO_DEG;
    m_pitch = atan2(-accel[0], sqrt(sqr(accel[1]) + sqr(accel[2]))) * RAD_TO_DEG;
    
    // Compute Innovation Covariance S (Fuse initial uncertainty with Accelerometer measurement Noise R)
    float S0 = Sigma[0] + R[0];
    float S1 = Sigma[1];
    float S2 = Sigma[2];
    float S3 = Sigma[3] + R[1];

    // Compute Kalman Gains (($K = \Sigma * S^(-1)$))
    k_det = 1.0f / (S0 * S3 - S1 * S2);

    k_gain[0] = (Sigma[0] * S3 - Sigma[1] * S2) * k_det;
    k_gain[1] = (Sigma[1] * S0 - Sigma[0] * S1) * k_det;
    k_gain[2] = (Sigma[2] * S3 - Sigma[3] * S2) * k_det;
    k_gain[3] = (Sigma[3] * S0 - Sigma[2] * S1) * k_det;

    // Calculate the Error Between the Accelerometer Reading and the A Priori Estimate
    float r_error = m_roll - roll;
    float p_error = m_pitch - pitch;

    // Update the Roll and Pitch with Kalman Gains
    roll  += (k_gain[0] * r_error) + (k_gain[1] * p_error);
    pitch += (k_gain[2] * r_error) + (k_gain[3] * p_error);

    // Update Error Covariance Matrix (A Posteriori Estimation)
    float s0 = Sigma[0], s1 = Sigma[1], s2 = Sigma[2], s3 = Sigma[3];
    Sigma[0] = (1.0f - k_gain[0]) * s0 - k_gain[1] * s2;
    Sigma[1] = (1.0f - k_gain[0]) * s1 - k_gain[1] * s3;
    Sigma[2] = -k_gain[2] * s0 + (1.0f - k_gain[3]) * s2;
    Sigma[3] = -k_gain[2] * s1 + (1.0f - k_gain[3]) * s3;

    // Enforce Matrix Symmetry (If any rounding errors accumulate)
    float relationship_avg = (Sigma[1] + Sigma[2]) * 0.5f;
    Sigma[1] = Sigma[2] = relationship_avg;
}
            {% endhighlight %}
        </div>
    </div>
</div>

<!-- Sub-Section 2: PID Control Loop -->
<div class="focus-group" data-group="pid-implementation" style="margin-top: 40px; margin-bottom: 30px;">
    <h3 class="section-subheading" style="margin-bottom: 15px;">PID Control Loop Implementation</h3>
    
    <!-- Dotted Timeline System Track -->
    <div style="border-left: 2px dotted var(--global-theme-color); padding-left: 30px; margin-left: 15px; margin-top: 25px; margin-bottom: 30px;">
        
        <!-- Step 1: The Challenge -->
        <div class="timeline-step outliny hovery4" style="position: relative; margin-bottom: 25px; max-width: 800px; width: 100%;">
            <div class="timeline-node" style="position: absolute; left: -42px; top: 13px; width: 22px; height: 22px; border-radius: 50%; background: var(--global-bg-color); border: 2px solid var(--global-theme-color); color: var(--global-theme-color); display: flex; align-items: center; justify-content: center; font-size: 0.75rem; font-weight: bold; font-family: monospace; z-index: 2;">1</div>
            
            <h4 class="card-title">The Challenge</h4>
            <p class ="card-body" style="opacity: 0.85; max-width: 768px;">
                A self-balancing robot (similar to an inverted pendulum) is inherently unstable and falls due to gravity. Simple binary motor 
                commands fail to maintain equilibrium and cause violent over-corrections.
            </p>
        </div>

        <!-- Step 2: The Solution -->
        <div class="timeline-step outliny hovery4" style="position: relative; margin-bottom: 25px; max-width: 800px; width: 100%;">
            <div class="timeline-node" style="position: absolute; left: -42px; top: 13px; width: 22px; height: 22px; border-radius: 50%; background: var(--global-bg-color); border: 2px solid var(--global-theme-color); color: var(--global-theme-color); display: flex; align-items: center; justify-content: center; font-size: 0.75rem; font-weight: bold; font-family: monospace; z-index: 2;">2</div>
            
            <h4 class="card-title">The Solution</h4>
            <p class ="card-body" style="opacity: 0.85; max-width: 768px;">
                Instead of binary motor outputs, a PID controller breaks the motor output into three scaled adjustments:
            </p>
            <p class="card-body" style="opacity: 0.85; max-width: 768px; margin: 3px 0 8px 0 !important; padding-left: 5px;">
                <span style="margin-right: 10px; font-size: 0.85rem;">▪</span><strong>Proportional (P):</strong> Scales output power proportionally to tilt amount.
            </p>
            <p class="card-body" style="opacity: 0.85; max-width: 768px; margin: 0 0 8px 0 !important; padding-left: 5px;">
                <span style="margin-right: 10px; font-size: 0.85rem;">▪</span><strong>Integral (I):</strong> Tracks past errors over time to eliminate lingering tilts.
            </p>
            <p class="card-body" style="opacity: 0.85; max-width: 768px; margin: 0 !important; padding-left: 5px;">
                <span style="margin-right: 10px; font-size: 0.85rem;">▪</span><strong>Derivative (D):</strong> Applies a low-pass filter to the future rate of change of error, suppressing over-corrections.
            </p>
        </div>

        <!-- Step 3: The Outcome -->
        <div class="timeline-step outliny hovery4" style="position: relative; max-width: 800px; width: 100%;">
            <div class="timeline-node" style="position: absolute; left: -42px; top: 13px; width: 22px; height: 22px; border-radius: 50%; background: var(--global-bg-color); border: 2px solid var(--global-theme-color); color: var(--global-theme-color); display: flex; align-items: center; justify-content: center; font-size: 0.75rem; font-weight: bold; font-family: monospace; z-index: 2;">3</div>
            
            <h4 class="card-title">The Outcome</h4>
            <p class ="card-body" style="opacity: 0.85; max-width: 768px;">
                Optimal tuning of the PID parameters generates motor outputs that reliably maintain vertical equilibrium.
            </p>
        </div>

    </div>

    <!-- Code Accordion -->
    <input type="checkbox" id="pid-code-toggle" class="accordion-toggle-input">
    
    <div class="portfolio-accordion shadowy">
        <!-- The header row click target -->
        <label for="pid-code-toggle" class="accordion-header hovery1">
            <span>View C++ PID Algorithm Implementation</span>
            <span class="accordion-icon"></span>
        </label>

        <!-- The content tray -->
        <div class="accordion-content">
            {% highlight cpp %}
float PID::control(float cur_angle, float max)
{
    error = setpoint - cur_angle;

    // DERIVATIVE: Compute raw rate of error change and apply an 80/20 discrete low-pass filter
    float raw_derivative = (error - previous_error) / dt;
    derivative = (0.80f * previous_derivative) + (0.2f * raw_derivative);
    
    previous_error = error;
    previous_derivative = derivative;

    // INTEGRAL: Constrained to prevent integral windup from saturating the motor capacity
    integral = constrain((integral + (error * dt)), -1.20f, 1.20f);

    // Output the PID corrected motor output
    out = (kp * error) + (ki * integral) + (kd * derivative);
    return constrain(out, -max, max); 
}
            {% endhighlight %}
        </div>
    </div>
</div>

<hr class="section-divider">

<div class="focus-group" data-group="engineering-retrospective">
    <h2 class="section-heading">Evaluation & Moving Forward</h2>

    <p class="body-long">
        While the V1 prototype successfully validated my core stability algorithms, it highlighted critical structural, electrical, and architectural bottlenecks. The roadmap below tracks these failure modes alongside their engineered V2 solutions:
    </p>

    <div id="retrospective-flip-grid" class="flip-cards mechanical-reveal-viewport">

        <!-- CARD 1: CIRCUIT STABILITY -->
        <div class="flip-card-3d-wrapper">
            <div class="flip-card-inner-engine" onclick="toggleCard3DFlipEngine(this)">
                <!-- Front Plate: Defect -->
                <div class="card-face-front">
                    <div class="meta-flag" style="color: #858585;">// 01_PROTOTYPE_DEFECT</div>
                    <h4>Physical Circuit Instability</h4>
                    <p>Jumper wires on breadboards are highly prone to disconnections caused by continuous chassis vibrations during operation.</p>
                    <div class="hint-flag">[ CLICK_TO_REVEAL_UPGRADE ]</div>
                </div>
                <!-- Back Plate: Upgrade -->
                <div class="card-face-back">
                    <div class="meta-flag" style="color: var(--global-theme-color);">// NEXT_GEN_UPGRADE</div>
                    <h4 style="color: var(--global-theme-color);">Custom PCB Implementation</h4>
                    <p>Transitioning away from messy breadboards to a custom printed circuit board designed in KiCad to secure all traces.</p>
                    <div class="hint-flag" style="color: var(--global-theme-color);">[ CLICK_TO_VIEW_DEFECT ]</div>
                </div>
            </div>
        </div>

        <!-- CARD 2: POWER INTEGRITY -->
        <div class="flip-card-3d-wrapper">
            <div class="flip-card-inner-engine" onclick="toggleCard3DFlipEngine(this)">
                <div class="card-face-front">
                    <div class="meta-flag" style="color: #858585;">// 02_PROTOTYPE_DEFECT</div>
                    <h4>Microcontroller Logic Resetting</h4>
                    <p>Inductive spikes from sudden motor switching periodically causes sags across power paths, introducing noise and risking ESP32 brownouts.</p>
                    <div class="hint-flag">[ CLICK_TO_REVEAL_UPGRADE ]</div>
                </div>
                <div class="card-face-back">
                    <div class="meta-flag" style="color: var(--global-theme-color);">// NEXT_GEN_UPGRADE</div>
                    <h4 style="color: var(--global-theme-color);">Power Isolation & Decoupling</h4>
                    <p>Combating sags by using dedicated decoupling capacitors across motor signals and incorporating bulk storage capacitors near the main voltage source rails.</p>
                    <div class="hint-flag" style="color: var(--global-theme-color);">[ CLICK_TO_VIEW_DEFECT ]</div>
                </div>
            </div>
        </div>

        <!-- CARD 3: CHASSIS MECHANICS -->
        <div class="flip-card-3d-wrapper">
            <div class="flip-card-inner-engine" onclick="toggleCard3DFlipEngine(this)">
                <div class="card-face-front">
                    <div class="meta-flag" style="color: #858585;">// 03_PROTOTYPE_DEFECT</div>
                    <h4>Chassis Rotational Torsion</h4>
                    <p>The initial single-part chassis faced issues with rotational torsion due to the lack of a reinforcing connecting platform at the chassis base near the wheels.</p>
                    <div class="hint-flag">[ CLICK_TO_REVEAL_UPGRADE ]</div>
                </div>
                <div class="card-face-back">
                    <div class="meta-flag" style="color: var(--global-theme-color);">// NEXT_GEN_UPGRADE</div>
                    <h4 style="color: var(--global-theme-color);">Multiple-Part Enclosure</h4>
                    <p>Redesigning the chassis as an assembly of structural components within SolidWorks, featuring a fully enclosed frame to minimize rotational torsion issues.</p>
                    <div class="hint-flag" style="color: var(--global-theme-color);">[ CLICK_TO_VIEW_DEFECT ]</div>
                </div>
            </div>
        </div>

        <!-- CARD 4: USER TELEMETRY -->
        <div class="flip-card-3d-wrapper">
            <div class="flip-card-inner-engine" onclick="toggleCard3DFlipEngine(this)">
                <div class="card-face-front">
                    <div class="meta-flag" style="color: #858585;">// 04_PROTOTYPE_DEFECT</div>
                    <h4>Lack of Feedback Telemetry</h4>
                    <p>The current design lacked any telemetry, state indication, or physical warning systems to signify failures or falling to the user.</p>
                    <div class="hint-flag">[ CLICK_TO_REVEAL_UPGRADE ]</div>
                </div>
                <div class="card-face-back">
                    <div class="meta-flag" style="color: var(--global-theme-color);">// NEXT_GEN_UPGRADE</div>
                    <h4 style="color: var(--global-theme-color);">Active Auditory & Visual I/O</h4>
                    <p>Integrating user feedback loops using Edison filaments paired with a front light diffuser panel for status, alongside a speaker alert to signify fallen states.</p>
                    <div class="hint-flag" style="color: var(--global-theme-color);">[ CLICK_TO_VIEW_DEFECT ]</div>
                </div>
            </div>
        </div>

        <!-- CARD 5: STATE CONTROLLER -->
        <div class="flip-card-3d-wrapper">
            <div class="flip-card-inner-engine" onclick="toggleCard3DFlipEngine(this)">
                <div class="card-face-front">
                    <div class="meta-flag" style="color: #858585;">// 05_PROTOTYPE_DEFECT</div>
                    <h4>Static Behaviour</h4>
                    <p>The system lacked flexibility in runtime, operating only on a singule execution layer with no capacity for transitioning to remote driving states.</p>
                    <div class="hint-flag">[ CLICK_TO_REVEAL_UPGRADE ]</div>
                </div>
                <div class="card-face-back">
                    <div class="meta-flag" style="color: var(--global-theme-color);">// NEXT_GEN_UPGRADE</div>
                    <h4 style="color: var(--global-theme-color);">Remote State Machine</h4>
                    <p>Developing a secondary ESP32 remote transmitter using the ESP-NOW protocol to feed real-time inputs (Forward, Reverse, Steering) into an active FSM.</p>
                    <div class="hint-flag" style="color: var(--global-theme-color);">[ CLICK_TO_VIEW_DEFECT ]</div>
                </div>
            </div>
        </div>

    </div>
</div>

<hr class="section-divider">

<div class="focus-group" data-group="project-assets">
    <h2 class="section-heading">Repository, Assets, and BOM</h2>

    <div class="project-outro" id="mechanical-dispatch-terminal">
        <div class="outro-structural-bounds">

            <!-- MOBILE ESCAPE BREAKOUT TABS LAYER -->
            <div class="outro-fallback-tabs">
                <button class="fallback-tab-btn active-fallback-tab" onclick="switchMobileFallbackStage(0)">Bill of Materials</button>
                <button class="fallback-tab-btn" onclick="switchMobileFallbackStage(1)">Repository Info</button>
                <button class="fallback-tab-btn" onclick="switchMobileFallbackStage(2)">View Repository</button>
            </div>

            <!-- DESKTOP CHASSIS LAYER -->
            <div class="gear-viewport-hull" id="kinetic-swipe-hull">
                <!-- ACCENT POINTER REMOVED COMPLETELY FOR SCREEN BALANCING -->
                <canvas id="mechanical-rotary-canvas"></canvas>

                <!-- TEXT LABEL NODE ASSEMBLY LAYER -->
                <div class="gear-text-tooth-orbit" id="kinetic-text-orbit-node">
                    <div class="tooth-text-anchor active-tooth-label" data-index="0">Bill of Materials</div>
                    <div class="tooth-text-anchor" data-index="1">Repository Info</div>
                    <div class="tooth-text-anchor" data-index="2">View Repository</div>
                    <div class="tooth-text-anchor" data-index="3">Bill of Materials</div>
                    <div class="tooth-text-anchor" data-index="4">Repository Info</div>
                    <div class="tooth-text-anchor" data-index="5">View Repository</div>
                </div>
            </div>

            <!-- RIGHT CORE: THE ADAPTIVE DRAWER PANELS -->
            <div class="outro-console-chamber">

                <!-- STAGE 01: HARDWARE SOURCING BILL OF MATERIALS -->
                <div id="outro-stage-0" class="outro-content-stage active-outro-stage run-stage-reveal">
                    <h3 class="section-heading animate-cascade" style="font-size: 1.6rem; margin: 0 0 6px 0; border: none; padding: 0;">Bill of Materials (BOM)</h3>
                    <p class="body-long animate-cascade" style="margin: 0 0 24px 0; font-size: 0.95rem; opacity: 0.85;">To establish a clear development history, all component selections and unit costs are logged below:</p>
                    
                    <!-- 4-ITEM TRACK SCROLLBAR PANEL -->
                    <div class="ledger-mini-track animate-cascade">
                        <!-- Item 1 -->
                        <div class="ledger-mini-row">   
                            <div class="bom-item-split-container">
                                <div class="bom-category-box">POWER SOURCE</div>
                                <div class="bom-content-block">
                                    <h5><a href="https://www.aliexpress.com/item/1005009821398927.html" target="_blank" rel="noopener noreferrer">2x 3.7V LiPo Battery ↗</a></h5>
                                    <p>High-discharge power source necessary to counter immediate motor torque spikes.</p>
                                </div>
                            </div>
                            <div class="cost-tag">£4.49</div>
                        </div>

                        <!-- Item 2 -->
                        <div class="ledger-mini-row">
                            <div class="bom-item-split-container">
                                <div class="bom-category-box">BATTERY HOLDER</div>
                                <div class="bom-content-block">
                                    <h5><a href="https://www.aliexpress.com/item/1005010290798449.html" target="_blank" rel="noopener noreferrer">1x 2 Slots LiPo Battery Holder ↗</a></h5>
                                    <p>Secure the batteries in a 2S configuration for a raw 7.4V.</p>
                                </div>
                            </div>
                            <div class="cost-tag">£0.58</div>
                        </div>

                        <!-- Item 3 -->
                        <div class="ledger-mini-row">
                            <div class="bom-item-split-container">
                                <div class="bom-category-box">BUCK CONVERTER</div>
                                <div class="bom-content-block">
                                    <h5><a href="https://thepihut.com/products/adafruit-mpm3610-3-3v-buck-converter-breakout-21v-in-3-3v-out-at-1-2a" target="_blank" rel="noopener noreferrer">1x MPM3610 3V3 ↗</a></h5>
                                    <p>Ultra-compact 21V, 1.2A step-down module providing clean 3.3V logic power.</p>
                                </div>
                            </div>
                            <div class="cost-tag">£5.80</div>
                        </div>

                        <!-- Item 4 -->
                        <div class="ledger-mini-row">
                            <div class="bom-item-split-container">
                                <div class="bom-category-box">MICROCONTROLLER</div>
                                <div class="bom-content-block">
                                    <h5><a href="https://www.aliexpress.com/item/1005007319706057.html" target="_blank" rel="noopener noreferrer">1x ESP32-S3 (N16R8) ↗</a></h5>
                                    <p>240MHz dual-core processing power with ample flash space for control calculations.</p>
                                </div>
                            </div>
                            <div class="cost-tag">£5.00</div>
                        </div>

                        <!-- Item 5 -->
                        <div class="ledger-mini-row">
                            <div class="bom-item-split-container">
                                <div class="bom-category-box">IMU</div>
                                <div class="bom-content-block">
                                    <h5><a href="https://www.aliexpress.com/item/1005010057794277.html" target="_blank" rel="noopener noreferrer">1x MPU6050 GY-521 ↗</a></h5>
                                    <p>3-axis accelerometer and 3-axis gyroscope combined on a single I2C bus.</p>
                                </div>
                            </div>
                            <div class="cost-tag">£1.27</div>
                        </div>

                        <!-- Item 6 -->
                        <div class="ledger-mini-row">
                            <div class="bom-item-split-container">
                                <div class="bom-category-box">DC MOTOR DRIVER</div>
                                <div class="bom-content-block">
                                    <h5><a href="https://www.aliexpress.com/item/1005009044264044.html" target="_blank" rel="noopener noreferrer">1x DRV8833 ↗</a></h5>
                                    <p>Dual MOSFET H-Bridge supporting low-saturation resistance and slow-decay active braking routines.</p>
                                </div>
                            </div>
                            <div class="cost-tag">£0.90</div>
                        </div>

                        <!-- Item 7 -->
                        <div class="ledger-mini-row">
                            <div class="bom-item-split-container">
                                <div class="bom-category-box">ACTUATORS</div>
                                <div class="bom-content-block">
                                    <h5><a href="https://www.aliexpress.com/item/1005007227331566.html" target="_blank" rel="noopener noreferrer">2x BDC TT Geared Motors with Wheels ↗</a></h5>
                                    <p>Budget-friendly brushed DC motors with wheels.</p>
                                </div>
                            </div>
                            <div class="cost-tag">£2.60</div>
                        </div>

                        <!-- Item 8 -->
                        <div class="ledger-mini-row">
                            <div class="bom-item-split-container">
                                <div class="bom-category-box">3D MODEL</div>
                                <div class="bom-content-block">
                                    <h5>Custom 3D Printed Chassis (~91g PLA)</h5>
                                    <p>Custom structural frame designed to mount the TT motors, battery holder, and breadboard.</p>
                                </div>
                            </div>
                            <div class="cost-tag">-</div>
                        </div>

                        <!-- Item 9 -->
                        <div class="ledger-mini-row">
                            <div class="bom-item-split-container">
                                <div class="bom-category-box">MISC</div>
                                <div class="bom-content-block">
                                    <h5>2x Half-size Breadboards, Assorted Jumper Wires</h5>
                                    <p>Rapid prototyping framework allowing quick hardware loop signal adjustments.</p>
                                </div>
                            </div>
                            <div class="cost-tag">-</div>
                        </div>
                    </div> <!-- SCROLL CONTEXT CLOSES SECURELY HERE -->

                    <!-- FIXED IMMOBILE OUTFLOW FOOTER BLOCK -->
                    <div class="ledger-summary-row animate-cascade">
                        <span class="body-long">TOTAL_PROTOTYPE_COST</span>
                        <span>£20.64</span>
                    </div>
                </div>

                <!-- STAGE 02: REPOSITORY INFORMATION STACK -->
                <div id="outro-stage-1" class="outro-content-stage">
                    <h3 class="section-heading animate-cascade" style="font-size: 1.6rem; margin: 0 0 6px 0; border: none; padding: 0;">Repository Information</h3>
                    <p class="body-long animate-cascade" style="text-align: left; letter-spacing: normal; margin : 0 0 24px 0; font-size: 0.95rem; opacity: 0.85;">All firmware and hardware files are completely open-source:</p>
                    
                    <!-- FIXED UTILITY WRAPPER: Replaced Bootstrap columns with a safe auto-wrapping Flex matrix to prevent margin bleedout -->
                    <div class="animate-cascade" style="display: flex; flex-wrap: wrap; gap: 16px; width: 100%; box-sizing: border-box; margin: 0; padding: 0;">
                        <div style="flex: 1 1 280px; box-sizing: border-box;">
                            <div class="cyber-pillar-card" style="height: 100%;">
                                <h4 style="text-align: center;margin: 0 0 6px 0; font-size: 1.05rem; font-weight: 600;">Firmware</h4>
                                <p class="body-long" style="text-align: center; margin: 0; font-size: 0.85rem; opacity: 0.8; line-height: 1.55;">
                                    Directory containing the primary <code>balancing_robot.ino</code> logic core, alongside custom Kalman 
                                    Filtering and PID Control Algorithm header files
                                </p>
                            </div>
                        </div>
                        <div style="flex: 1 1 280px; box-sizing: border-box;">
                            <div class="cyber-pillar-card" style="height: 100%;">
                                <h4 style="text-align: center; margin: 0 0 6px 0; font-size: 1.05rem; font-weight: 600;">Hardware</h4>
                                <p class="body-long" style="text-align: center; margin: 0; font-size: 0.85rem; opacity: 0.8; line-height: 1.55;">
                                    Production asset directory containing original SolidWorks CAD source models (<code>.SLDPRT</code>) and 
                                    slice configurations (<code>.3mf</code>) ready for manufacturing.
                                </p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- STAGE 03: FILES DOWNLOAD TERMINAL -->
                <div id="outro-stage-2" class="outro-content-stage">
                    <div class="git-outro-center" style="padding-bottom: 40px;">
                        <div class="git-huge-icon animate-cascade"><i class="fa-brands fa-github"></i></div>
                        <h3 class="section-heading animate-cascade" style="font-size: 1.6rem; margin: 0 0 6px 0; border: none; padding: 0;">View The Repository</h3>
                        <p class="body-long animate-cascade" style="margin: 0 0 28px 0; font-size: 0.92rem; opacity: 0.8; max-width: 480px;">
                            All resources and dependencies are can be downloaded directly from the open-source branch master directory tree.
                        </p>
                        <div class="action-capsule-wrapper animate-cascade" style="box-sizing: border-box;">
                            <a href="https://github.com/arthurlawson/self-balancing-robot-v1" class="shadowy hovery3 clicky" target="_blank" rel="noopener noreferrer" style="display: inline-flex; align-items: center; justify-content: center; gap: 10px; text-decoration: none; padding: 14px 24px; background-color: var(--global-code-bg-color, #1e1e24); border-radius: 6px; border: 1px solid var(--global-divider-color, #2d2d34);">
                                <i class="fa-brands fa-github" style="font-size: 1.1rem; color: var(--global-theme-color);"></i>
                                <span style="font-size: 0.85rem; font-weight: 600; color: var(--global-text-color);">View the Github Project</span>
                            </a>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </div>
</div>

<!-- ==========================================================================
     ARTHUR'S Gear Spinning Outro Engine
     ========================================================================== -->
<script>
window.switchMobileFallbackStage = () => {};

document.addEventListener("DOMContentLoaded", () => {
    const canvas = document.getElementById("mechanical-rotary-canvas");
    const swipeHull = document.getElementById("kinetic-swipe-hull");
    const labelAnchors = Array.from(document.querySelectorAll(".tooth-text-anchor"));
    const contentDrawers = Array.from(document.querySelectorAll(".outro-content-stage"));
    const mobileTabs = Array.from(document.querySelectorAll(".fallback-tab-btn"));
    
    if (!canvas || labelAnchors.length === 0) return;
    const ctx = canvas.getContext("2d");

    const canvasDiameter = 420;
    canvas.width = canvasDiameter;
    canvas.height = canvasDiameter;

    const totalTeethCount = 6;
    const innerRadius = 105; 
    const outerRadius = 140; 
    const toothStepAngle = (Math.PI * 2) / totalTeethCount;
    const toothModuleMap = [0, 1, 2, 0, 1, 2]; 
    const ALIGNMENT_TOOTH_OFFSET_BIAS = toothStepAngle * 0.425; 
    
    let targetRotationalAngle = - ALIGNMENT_TOOTH_OFFSET_BIAS;
    let runningCurrentAngle = - ALIGNMENT_TOOTH_OFFSET_BIAS;
    let selectedActiveIndex = 0;

    let isDragging = false;
    let startY = 0;
    let baseAngleAtDragStart = 0;
    const swipeThreshold = 35; 

    function drawMechanicalGearManifold() {
        ctx.clearRect(0, 0, canvasDiameter, canvasDiameter);
        ctx.save();
        ctx.translate(canvasDiameter / 2, canvasDiameter / 2);
        ctx.rotate(runningCurrentAngle);

        // 1. HARDENED LIVE ACCENT REGISTRY SCANNER
        const rootThemeNode = document.documentElement;
        const computedStylesRef = window.getComputedStyle(rootThemeNode);
        
        // Pulls directly from your root light/dark theme manager variables
        const dynamicLiveThemeColor = computedStylesRef.getPropertyValue('--global-theme-color').trim() || "#ff5e00";
        const dynamicLiveCardBackground = computedStylesRef.getPropertyValue('--global-card-bg-color').trim() || "#16171d";
        const dynamicLiveBodyBackground = computedStylesRef.getPropertyValue('--global-body-bg-color').trim() || "#0b0c10";
        const dynamicLiveTextColor = computedStylesRef.getPropertyValue('--global-text-color').trim() || "#ffffff";

        // 2. APPLY SYSTEM THEMING PARAMETERS TO VECTOR COG
        ctx.strokeStyle = dynamicLiveThemeColor;
        ctx.fillStyle = dynamicLiveCardBackground;
        ctx.lineWidth = 4;

        // Draw structural outer block cog teeth
        ctx.beginPath();
        for (let i = 0; i < totalTeethCount; i++) {
            let angleBase = i * toothStepAngle;
            let pt1 = angleBase;
            let pt2 = angleBase + toothStepAngle * 0.20;
            let pt3 = angleBase + toothStepAngle * 0.65;
            let pt4 = angleBase + toothStepAngle * 0.85;

            ctx.lineTo(Math.cos(pt1) * innerRadius, Math.sin(pt1) * innerRadius);
            ctx.lineTo(Math.cos(pt2) * outerRadius, Math.sin(pt2) * outerRadius);
            ctx.lineTo(Math.cos(pt3) * outerRadius, Math.sin(pt3) * outerRadius);
            ctx.lineTo(Math.cos(pt4) * innerRadius, Math.sin(pt4) * innerRadius);
        }
        ctx.closePath();
        ctx.fill();
        ctx.stroke();

        ctx.beginPath();
        ctx.arc(0, 0, 32, 0, Math.PI * 2);
        ctx.fillStyle = dynamicLiveCardBackground; // Matches your clean card fill background exactly
        ctx.strokeStyle = dynamicLiveThemeColor;   // Outlined with your active global accent theme color
        ctx.lineWidth = 3;
        ctx.fill();
        ctx.stroke();

        ctx.restore();
    }

    let cachedThemeColor = "#ff5e00";
    function updateCachedAccentColor() {
        const structuralDummy = document.createElement("div");
        structuralDummy.style.color = "var(--global-theme-color)";
        document.body.appendChild(structuralDummy);
        const resolvedThemeColor = window.getComputedStyle(structuralDummy).color;
        document.body.removeChild(structuralDummy);
        cachedThemeColor = resolvedThemeColor || "#ff5e00";
    }
    updateCachedAccentColor();

    function updateMechanicalEngineTimeline() {
        let angleDeltaDifference = targetRotationalAngle - runningCurrentAngle;
        runningCurrentAngle += angleDeltaDifference * 0.12; 

        labelAnchors.forEach((label, idx) => {
            let initialToothOffset = (idx * toothStepAngle) + ALIGNMENT_TOOTH_OFFSET_BIAS;
            let netLabelAngle = runningCurrentAngle + initialToothOffset;

            let standardizedAngle = ((netLabelAngle % (Math.PI * 2)) + Math.PI * 2) % (Math.PI * 2);
            let rawDistanceToCenter = Math.abs(standardizedAngle > Math.PI ? (Math.PI * 2 - standardizedAngle) : standardizedAngle);
            let proximityFactor = Math.max(0, 1 - (rawDistanceToCenter / (Math.PI / 2.5)));
            let smoothProximityCurve = Math.pow(proximityFactor, 3); 

            let baseLabelExtensionGap = 20;
            let targetedActivePeakBoost = 70; 
            let textRadiusPlacement = outerRadius + baseLabelExtensionGap + (targetedActivePeakBoost * smoothProximityCurve); 

            let canvasLeftViewportCorrection = -280; 
            let canvasTopViewportCorrection = 300; 

            let textX = canvasLeftViewportCorrection + (canvasDiameter / 2) + Math.cos(netLabelAngle) * textRadiusPlacement;
            let textY = canvasTopViewportCorrection + Math.sin(netLabelAngle) * textRadiusPlacement;
            let degrees = netLabelAngle * (180 / Math.PI);

            label.style.transform = `translate3d(${textX}px, ${textY}px, 0) rotate(${degrees}deg)`;

            if (window.innerWidth > 820) {
                standardizedAngle = ((netLabelAngle % (Math.PI * 2)) + Math.PI * 2) % (Math.PI * 2);
                if (standardizedAngle < 0.3 || standardizedAngle > (Math.PI * 2 - 0.3)) {
                    let structuralTargetIndex = toothModuleMap[idx];
                    if (structuralTargetIndex !== selectedActiveIndex) {
                        selectedActiveIndex = structuralTargetIndex;
                        executeStageConsoleSwap(selectedActiveIndex);

                        labelAnchors.forEach(l => l.classList.remove("active-tooth-label"));
                        label.classList.add("active-tooth-label");
                    }
                }
            }
        });

        drawMechanicalGearManifold();
        requestAnimationFrame(updateMechanicalEngineTimeline);
    }

    function executeStageConsoleSwap(targetIndex) {
        contentDrawers.forEach((drawer, idx) => {
            if (idx === targetIndex) {
                drawer.classList.add("active-outro-stage", "run-stage-reveal");
            } else {
                drawer.classList.remove("active-outro-stage", "run-stage-reveal");
            }
        });
        
        mobileTabs.forEach((tab, idx) => {
            if (idx === targetIndex) {
                tab.classList.add("active-fallback-tab");
            } else {
                tab.classList.remove("active-fallback-tab");
            }
        });
    }

    function dragStart(e, y) {
        if (e.type === "mousedown" && e.button !== 0) return; 
        isDragging = true;
        swipeHull.style.cursor = "grabbing";
        startY = y;
        baseAngleAtDragStart = targetRotationalAngle;
    }

    function dragMove(y) {
        if (!isDragging) return;
        const currentY = y;
        const dragDistance = currentY - startY; 
        const pixelToRadianSensitivityRatio = 180; 
        const realTimeAngleAdjustment = (dragDistance / pixelToRadianSensitivityRatio) * toothStepAngle;
        targetRotationalAngle = baseAngleAtDragStart + realTimeAngleAdjustment;
    }

    function dragEnd(y) {
        if (!isDragging) return;
        isDragging = false;
        swipeHull.style.cursor = "pointer";
        
        const endY = y;
        const finalMovedDistance = endY - startY;

        if (finalMovedDistance < -swipeThreshold) {
            let rawUnwoundRadianSteps = Math.ceil((targetRotationalAngle + ALIGNMENT_TOOTH_OFFSET_BIAS) / toothStepAngle) * toothStepAngle - ALIGNMENT_TOOTH_OFFSET_BIAS;
            targetRotationalAngle = rawUnwoundRadianSteps;
        } else if (finalMovedDistance > swipeThreshold) {
            let rawUnwoundRadianSteps = Math.floor((targetRotationalAngle + ALIGNMENT_TOOTH_OFFSET_BIAS) / toothStepAngle) * toothStepAngle - ALIGNMENT_TOOTH_OFFSET_BIAS;
            targetRotationalAngle = rawUnwoundRadianSteps;
        } else {
            let rawUnwoundRadianSteps = Math.round((targetRotationalAngle + ALIGNMENT_TOOTH_OFFSET_BIAS) / toothStepAngle) * toothStepAngle - ALIGNMENT_TOOTH_OFFSET_BIAS;
            targetRotationalAngle = rawUnwoundRadianSteps;
        }
    }

    swipeHull.addEventListener("mousedown", e => dragStart(e, e.clientY));
    window.addEventListener("mousemove", e => { if (isDragging) dragMove(e.clientY); });
    window.addEventListener("mouseup", e => { if (isDragging) dragEnd(e.clientY); });
    swipeHull.addEventListener("mouseleave", () => { 
        if (isDragging) { 
            isDragging = false; 
            swipeHull.style.cursor = "pointer"; 
            let steps = Math.round((targetRotationalAngle + ALIGNMENT_TOOTH_OFFSET_BIAS) / toothStepAngle) * toothStepAngle - ALIGNMENT_TOOTH_OFFSET_BIAS; 
            targetRotationalAngle = steps; 
        } 
    });

    swipeHull.addEventListener("touchstart", e => { 
        if (e.touches.length) dragStart(e, e.touches[0].clientY); 
    }, { passive: true });

    window.addEventListener("touchmove", e => { 
        if (isDragging && e.touches.length) {
            if (e.cancelable) e.preventDefault(); 
            dragMove(e.touches[0].clientY); 
        } 
    }, { passive: false });

    window.addEventListener("touchend", e => { 
        if (!isDragging) return; 
        if (e.changedTouches.length) dragEnd(e.changedTouches[0].clientY); 
    });

    swipeHull.addEventListener("wheel", (e) => {
        e.preventDefault(); 
        let scrollDirectionMultiplier = e.deltaY > 0 ? 1 : -1;
        targetRotationalAngle += scrollDirectionMultiplier * toothStepAngle;
    }, { passive: false });

    labelAnchors.forEach((label, idx) => {
        label.addEventListener("click", () => {
            let rawUnwoundRadianSteps = - (idx * toothStepAngle) - ALIGNMENT_TOOTH_OFFSET_BIAS;
            let targetOffsetIncrement = Math.round((targetRotationalAngle - rawUnwoundRadianSteps) / (Math.PI * 2)) * (Math.PI * 2);
            targetRotationalAngle = rawUnwoundRadianSteps + targetOffsetIncrement;
        });
    });

    window.switchMobileFallbackStage = (targetIndex) => {
        selectedActiveIndex = targetIndex;
        executeStageConsoleSwap(targetIndex);
    };

    window.addEventListener("resize", () => {
        updateCachedAccentColor();
        executeStageConsoleSwap(selectedActiveIndex);
    });

    executeStageConsoleSwap(selectedActiveIndex);
    requestAnimationFrame(updateMechanicalEngineTimeline);
});
</script>

<!-- ==========================================================================
     ARTHUR'S STEPPED STAGGERED REVEAL DRIVER SCRIPT
     ========================================================================== -->
<script>
function toggleCard3DFlipEngine(cardElement) {
    if (!cardElement) return;
    
    // Toggle active flip layout variables
    const isFlipped = cardElement.classList.toggle('is-flipped');
    
    // Direct forced repaint pipeline to prevent sticky browser hover border bugs
    const frontFace = cardElement.querySelector('.card-face-front');
    const backFace = cardElement.querySelector('.card-face-back');
    
    if (isFlipped) {
        if (backFace) {
            backFace.style.borderColor = 'var(--global-theme-color)';
        }
        if (frontFace) {
            frontFace.style.borderColor = 'transparent'; 
        }
    } else {
        if (frontFace) {
            frontFace.style.borderColor = 'color-mix(in srgb, var(--global-text-color, #ffffff) 15%, transparent)';
        }
        if (backFace) {
            backFace.style.borderColor = 'transparent';
        }
    }
}

document.addEventListener("DOMContentLoaded", () => {
    const flipGrid = document.getElementById("retrospective-flip-grid");
    const cards = Array.from(document.querySelectorAll('.flip-card-inner-engine'));

    cards.forEach(card => {
        const front = card.querySelector('.card-face-front');
        const back = card.querySelector('.card-face-back');

        card.addEventListener('mouseleave', () => {
            if (front) front.style.borderColor = '';
            if (back) back.style.borderColor = '';
        });
    });
    
    if ('IntersectionObserver' in window) {
        const gridObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    flipGrid.classList.add('spawn-active');
                    gridObserver.unobserve(flipGrid); 
                }
            });
        }, { threshold: 0.05 });
        
        if (flipGrid) gridObserver.observe(flipGrid);
    } else {
        if (flipGrid) flipGrid.classList.add('spawn-active');
    }
});
</script>

<!-- ==========================================================================
     ARTHUR'S DISCRETE CARD CAROUSEL ENGINE
     ========================================================================== -->
<script>
let jumpToCarouselIndex = () => {};

document.addEventListener("DOMContentLoaded", () => {
    const surf = document.getElementById("discrete-slider-surface");
    const rail = document.getElementById("discrete-slider-rail");
    const bLeft = document.getElementById("discrete-btn-left");
    const bRight = document.getElementById("discrete-btn-right");
    const cards = Array.from(rail.querySelectorAll(".discrete-content-card"));
    const dots = Array.from(document.querySelectorAll(".carousel-dot-indicator"));
    
    const gearLeft = document.getElementById("kinetic-gear-left");
    const gearRight = document.getElementById("kinetic-gear-right");
    const totalCards = cards.length;

    let currentIndex = 0;
    let isDragging = false;
    let startX = 0;
    let currentTranslate = 0;
    let prevTranslate = 0;
    const swipeThreshold = 60; 

    let currentRotationLeft = 0;
    let currentRotationRight = 30; 
    let gearVelocity = 0;          
    const friction = 0.90;         
    const impulseForce = 20;       

    function physicsTicker() {
        if (Math.abs(gearVelocity) > 0.01) {
            gearVelocity *= friction;
            currentRotationLeft += gearVelocity;
            currentRotationRight -= gearVelocity;
            
            if (gearLeft) gearLeft.style.transform = `rotate(${currentRotationLeft}deg)`;
            if (gearRight) gearRight.style.transform = `rotate(${currentRotationRight}deg)`;
        } else {
            gearVelocity = 0; 
        }
        requestAnimationFrame(physicsTicker);
    }
    requestAnimationFrame(physicsTicker);

    function injectTorqueImpulse(direction) {
        gearVelocity = direction * impulseForce;
    }

    function updateCarouselPosition(smooth = true) {
        // NATIVE EDGE MATRIX SPECIFICATION: Calculates translations cleanly using the 
        // cards' exact layout offsets. This automatically eliminates alignment lean.
        if (cards[currentIndex]) {
            currentTranslate = -cards[currentIndex].offsetLeft;
        } else {
            currentTranslate = 0;
        }
        
        rail.style.transition = smooth ? "transform 0.5s cubic-bezier(0.25, 1, 0.33, 1)" : "transform 0s linear";
        rail.style.transform = `translate3d(${currentTranslate}px, 0, 0)`;
        
        cards.forEach((card, index) => {
            if (index === currentIndex) {
                card.style.opacity = "1";
                card.style.transform = "scale3d(1, 1, 1)";
            } else {
                card.style.opacity = "0.15";
                card.style.transform = "scale3d(0.93, 0.93, 0.93)";
            }
        });

        dots.forEach((dot, index) => {
            if (index === currentIndex) {
                dot.style.width = "24px";
                dot.style.background = "var(--global-theme-color)";
                dot.style.opacity = "1";
            } else {
                dot.style.width = "12px";
                dot.style.background = "var(--global-text-color)";
                dot.style.opacity = "0.25";
            }
        });

        prevTranslate = currentTranslate;
    }

    function slideNext() {
        injectTorqueImpulse(-1); 
        currentIndex = (currentIndex + 1) % totalCards; 
        updateCarouselPosition(true);
    }

    function slidePrev() {
        injectTorqueImpulse(1); 
        currentIndex = (currentIndex - 1 + totalCards) % totalCards;
        updateCarouselPosition(true);
    }

    function shouldBlockDrag(target) {
        return target.hasAttribute('data-zoomable') || 
               target.classList.contains('img-zoomable') || 
               target.closest('[data-zoomable]');
    }

    jumpToCarouselIndex = (index) => {
        if (index >= 0 && index < totalCards && !isDragging) {
            const pathDirection = (index > currentIndex) ? -1 : 1;
            injectTorqueImpulse(pathDirection);
            currentIndex = index;
            updateCarouselPosition(true);
        }
    };

    function dragStart(e, x) {
        if (shouldBlockDrag(e.target)) return;
        isDragging = true;
        surf.style.cursor = "grabbing";
        startX = x;
        rail.style.transition = "transform 0s linear";
        cards.forEach(card => card.style.transition = "transform 0s linear, opacity 0s linear");
    }

    function dragMove(x) {
        if (!isDragging) return;
        const currentX = x;
        const dragDistance = currentX - startX;
        const translateValue = prevTranslate + dragDistance;
        rail.style.transform = `translate3d(${translateValue}px, 0, 0)`;
        
        gearVelocity = (dragDistance > 0) ? 1.5 : -1.5;
        
        const cardWidth = cards[currentIndex] ? cards[currentIndex].offsetWidth : 460;
        const dragPercent = Math.min(Math.abs(dragDistance) / (cardWidth + 16), 0.6);
        
        cards[currentIndex].style.opacity = 1 - (dragPercent * 0.4);
        cards[currentIndex].style.transform = `scale3d(${1 - (dragPercent * 0.07)}, ${1 - (dragPercent * 0.07)}, 1)`;
    }

    function dragEnd(x) {
        if (!isDragging) return;
        isDragging = false;
        surf.style.cursor = "grab";
        
        cards.forEach(card => card.style.transition = "transform 0.5s cubic-bezier(0.25, 1, 0.33, 1), opacity 0.4s ease, border-color 0.25s ease");
        
        const endX = x;
        const finalMovedDistance = endX - startX;

        if (finalMovedDistance < -swipeThreshold) {
            slideNext();
        } else if (finalMovedDistance > swipeThreshold) {
            slidePrev();
        } else {
            updateCarouselPosition(true); 
        }
    }

    // Event Wireups
    surf.addEventListener("mousedown", e => dragStart(e, e.clientX));
    window.addEventListener("mousemove", e => { if (isDragging) dragMove(e.clientX); });
    window.addEventListener("mouseup", e => { if (isDragging) dragEnd(e.clientX); });

    surf.addEventListener("touchstart", e => { if (e.touches.length) dragStart(e, e.touches[0].clientX); }, { passive: true });
    window.addEventListener("touchmove", e => { if (isDragging && e.touches.length) dragMove(e.touches[0].clientX); }, { passive: true });
    window.addEventListener("touchend", e => { if (!isDragging) return; if (e.changedTouches.length) dragEnd(e.changedTouches[0].clientX); });

    bLeft.addEventListener("click", slidePrev);
    bRight.addEventListener("click", slideNext);

    window.addEventListener("keydown", e => {
        const rect = surf.getBoundingClientRect();
        const isInViewport = (rect.top >= 0 && rect.bottom <= (window.innerHeight || document.documentElement.clientHeight));
        if (isInViewport) {
            if (e.key === "ArrowLeft") slidePrev();
            else if (e.key === "ArrowRight") slideNext();
        }
    });

    window.addEventListener("resize", () => updateCarouselPosition(false));
    updateCarouselPosition(false);
});
</script>

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