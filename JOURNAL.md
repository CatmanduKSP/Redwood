---
title: "Redwood"
github: "https://github.com/CatmanduKSP/Redwood.git"
description: "Osprey-style VTOL drone with a small gimbal-mounted camera and port for larger scanner modules, similar to DJI's Zenmuse modules"
created_at: "2026-10-12"
total_time: "4h"
---

# October 13, 2026: Created fuselage parameters, electronic/cargo requirements
<!-- fabricate:entry 372 -->

## 10/12/2026
## Overview
Figured out broad-strokes design for fuselage and surfaces and figured out camera and compute-stack requirements.
## Control surfaces and props
Tail will be V-shaped to minimize propwash in hover config by hiding as much in the fuselage's aerodynamic shadow as possible and so 2 servos can control combo elevator-rudder control surfaces. An inverted-v configuration will be used to combat wings blocking airflow to the tail fins at high AoAs, and so yaw-roll coupling is proverse. Because propellers can quickly change speed and can be quickly vectored by servos, control is high and stall AoA is virtually eliminated. This removes the need for traditional control surfaces like wing elevators and ailerons, as well as stall-prevention surfaces like wing flaps and slats. Single axis swashplates will control prop blade angle so both high thrust in hovering config and high speed in cruising config can be achieved. Props will be mounted in front/above wingtips to improve low-speed flying characteristics by forcing air over wingtips, preventing wingtip stalling. Altogether the avionics servo count is 6: 2 for tail flaps, 2 for prop angle, and 2 for swashplates. The total avionics motor count is 2, one for each prop.
## Wing design
Wings will be attached to the top for the fuselage so they do not impede camera view and so a central spar can run through the wingspan without intersecting the avionics or cargo bays. Wing are has yet to be calculated as the final weight is not known yet, but will be calculated for a stall speed of 30 mph fully loaded, taking advantage of the nature of the variable-angle props and sacrificing some low-speed maneuverability for range and efficiency at high speed. Wing aspect ratio will be ~1:15, taking advantage again of the nature of the props so maneuverability is an issue and increasing efficiency. The only issue with increasing aspect ratio is structural stability. Carbon-fiber continuous spars should solve this and ultrathin Dyneema or Vectran strings could connect wingtips to nose and tail to mitigate this issue, though that solution is likely out of the question due to aerodynamic implications. Taper ratio will be 1:0.45 to achieve the most ideal spanwise lift distribution possible without manufacturing ellipses. Wing leading edge will be perpendicular to fuselage to maximize efficiency (stability tradeoffs are, again, mostly irrelevant due to powerful and quick control offered by variable angle props, plus top-mounted wings.) Trailing edge will be swept forward so mean aerodynamic chord will be as close to between propeller centers as possible, so center of lift does not change much from hovering to cruising configurations. Wings will have no dihedral or twist because top-mounted wings and wingtip props fix stability and wingtip stall issues, and this vastly reduces manufacturing complexity and allows for a continuous straight spar tunning through the wingspan.
## Avionics, camera, and cargo requirements
Camera will be mounted on a 4 axis gimbal: the 3 rotational axes + translation up and down so the camera can recess into a cavity in the fuselage for reduces drag or extend downwards for a greater available field of view. Camera will also be mounted on come cort of suspension in order to mitigate effects of turbulence and fuselage vibrations. Cargo hold will be below wings so as to minimally affect weight distribution, and avionics will be located in the tail section of the fuselage. PID loop will need to be minimum 400Hz. Airplane sensors must include a gyroscope and IMU and may contain an anemometer. Servos will need to accept PWN or SBUS at above 300Hz, and must rotate at a rate of at most 10ms/60 degrees under full load, factoring in rotational inertia of props. Servo and prop power cannot be calculated until aircraft weight and propeller stem and nacelle design is known.
![Rough fuselage blueprint](https://fabricate.hackclub-assets.com/80d139c75061897d4e122a8f240e8ef13a7b7fa301cf35c0ac574b9dd448a80b/image-png/image.png)

**Total time spent: 4h**
