# IIoT-Predictive-Maintenance-ESP32

# Industrial IoT Predictive Maintenance System

## Project Overview
This project simulates an **IIoT (Industrial Internet of Things)** solution designed for predictive maintenance. Instead of waiting for factory machinery to break (reactive), this system monitors real-time vibration data to detect anomalies and trigger preventative alerts before failure occurs.

## Key Features
- **Real-time Monitoring:** Uses an ESP32 to monitor vibration levels via an analog potentiometer sensor.
- **Edge Computing:** Local logic processes sensor data to identify critical thresholds (Over 75% vibration).
- **Cloud Connectivity:** Implements the **MQTT protocol** to publish telemetry data and emergency alerts to a cloud broker (HiveMQ).
- **Visual Alerts:** Integrated local warning LED indicator for immediate on-site status notification.

## Tech Stack
- **Hardware:** ESP32 DevKit, Potentiometer (Sensor), LED (Actuator)
- **Software/Protocols:** C++, Arduino IDE, MQTT Protocol
- **Simulation:** Wokwi ESP32 Simulator

## Architecture
1. **Sensor Layer:** Potentiometer simulates industrial motor vibration (0-100%).
2. **Processing Layer:** ESP32 samples vibration and runs threshold logic.
3. **Communication Layer:** MQTT client pushes telemetry to `broker.hivemq.com`.
4. **Alerting Layer:** Critical faults trigger both a cloud notification and a physical LED warning.

## How to Run
1. Open the project in the [Wokwi ESP32 Simulator](https://wokwi.com/).
2. Copy the code from `sketch.ino` into the simulator.
3. Configure the wiring according to `diagram.json`.
4. Run the simulation and check the **Serial Monitor** to see live MQTT broker connection status.

## Future Scope
- Integration with a live dashboard (Node-RED or Grafana).
- Transition from simulation to physical prototype using industrial-grade MEMS vibration sensors (ADXL345).

