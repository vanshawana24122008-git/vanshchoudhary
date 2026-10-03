# AeroNav-ML: Autonomous Drone Navigation Engine

## Project Context & Overview
Developed as a B.Tech CSAIML Semester 1 project, this repository implements a Supervised Machine Learning classification framework to simulate an automated flight control system for an autonomous Unmanned Aerial Vehicle (UAV). Building rule-based navigation modules mirrors obstacle-avoidance and collision-mitigation pipelines engineered by drone tech sectors like DJI, Skydio, and automated delivery platforms like Amazon Prime Air.

## Software Stack
- **Language Stack:** Python 3
- **Algorithmic Library:** Scikit-Learn
- **Data Engineering Blocks:** Pandas

## Feature Matrix Architecture
The flight computer evaluates collision hazards and navigation vectors based on these real-time LiDAR/Ultrasonic telemetry metrics:
- `Front_Sensor_Dist`: Distance to the nearest obstacle directly ahead of the aircraft, measured in meters (Continuous)
- `Left_Sensor_Dist`: Distance to obstacles flanking the aircraft's left corridor, measured in meters (Continuous)
- `Right_Sensor_Dist`: Distance to obstacles flanking the aircraft's right corridor, measured in meters (Continuous)
- `Altitude`: Current flight height above ground level, measured in meters (Continuous)
- **Target Output Categories:** `Flight_Action` (0: Move Forward, 1: Turn Left, 2: Turn Right, 3: Hover/Emergency Stop)

## Deployed Algorithm
The logic runs on a **Decision Tree Classifier**, which constructs a mathematical flowchart mapping sensor boundaries to safe navigation decisions. This eliminates rigid manual programming by allowing the drone to dynamically deduce clear flight paths.
