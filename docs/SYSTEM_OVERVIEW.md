# DRAIN-SENSE — System Overview

**Application Unique ID:** VK26-IITH-SC-0073  
**Project:** Smart Urban Drainage Health Monitoring and Flood Early-Warning System  
**Domain:** Sustainable Cities  
**Development Stage:** Proposed design and planning

## 1. Introduction

DRAIN-SENSE is a proposed hardware-based system for demonstrating water-level monitoring and threshold-based alerts in an urban drainage model. It combines an ultrasonic distance sensor, an ESP32 microcontroller, and visual and audible indicators to represent a simplified drainage-monitoring application.

The system is intended to demonstrate how sensor readings can be processed to identify water levels approaching predefined limits. Physical implementation and validation are required before its measurement performance or practical effectiveness can be established.

## 2. System Objectives

The proposed system has the following objectives:

1. Measure the distance between an elevated sensor and the water surface.
2. Process sensor readings through an ESP32 microcontroller.
3. evaluate readings against configurable water-level thresholds.
4. Provide visual and audible indications when specified thresholds are crossed.
5. Establish a controlled demonstration platform for evaluating water-level monitoring and alert behaviour.

## 3. System Architecture

The system follows a sensor–controller–alert architecture.

<CodeBlock language="mermaid" editable={false}>flowchart TD
    A["Water Surface in Drainage Model"] --> B["Ultrasonic Distance Sensor"]
    B --> C["ESP32 Microcontroller"]
    C --> D["Sensor Reading Processing"]
    D --> E["Threshold Evaluation"]
    E --> F["LED Status Indicators"]
    E --> G["Audible Buzzer Alert"]</CodeBlock>

### 3.1 Ultrasonic Sensor

The proposed HC-SR04 ultrasonic sensor measures the distance between its mounting position and the water surface. The sensor is intended to remain above the water rather than being submerged.

A decrease in the measured distance indicates that the water surface has moved closer to the sensor. The relationship between distance and actual water depth depends on the sensor's mounting height and the geometry of the drainage model.

### 3.2 ESP32 Microcontroller

The ESP32 serves as the proposed processing and control unit. It receives the sensor signal, derives the distance measurement, and evaluates the reading against programmed thresholds.

The final implementation will require suitable handling of invalid readings, sensor noise, and repeated measurements to reduce unintended alert changes.

### 3.3 Alert Subsystem

The proposed alert subsystem uses LEDs and a buzzer to communicate configured system states.

The LED states and buzzer activation conditions will be defined in the controller program. The thresholds must be selected and evaluated during implementation; the alert behaviour has not yet been experimentally validated.

## 4. Operating Principle

The intended operating sequence is as follows:

1. The ultrasonic sensor emits a sound pulse toward the water surface.
2. The reflected pulse is received by the sensor.
3. The sensor's timing signal is used to estimate the distance to the water surface.
4. The ESP32 processes the measurement.
5. The controller compares the measurement with configured thresholds.
6. The corresponding visual and/or audible indication is activated when the programmed conditions are satisfied.

For a fixed sensor mounting height, the estimated water depth can be expressed as:

\[
h = H-d
\]

where:

- \(h\) = estimated water depth relative to the chosen channel reference
- \(H\) = vertical distance from the sensor reference point to the channel's depth reference
- \(d\) = measured distance from the sensor to the water surface

This relationship assumes consistent reference points and a suitable sensor orientation. The measurement range, mounting geometry, and calibration must be established for the final model.

## 5. Threshold-Based Alert Logic

The proposed controller evaluates the measured water level against predefined thresholds. A simplified conceptual arrangement is shown below.

| System State | Conceptual Condition | Intended Indication |
|---|---|---|
| Normal | Water level below the warning threshold | Normal-status indication |
| Warning | Water level reaches the configured warning threshold | Warning indication |
| High level | Water level reaches the configured high-level threshold | High-level indication and audible alert |

The table describes the intended design logic, not measured test results. Actual threshold values, indicator patterns, and transition behaviour will be determined during implementation and testing.

## 6. Proposed Hardware Configuration

| Component | Role in the System |
|---|---|
| ESP32 development board | Control and sensor-data processing |
| HC-SR04 ultrasonic sensor | Water-surface distance measurement |
| LEDs and resistors | Visual status indication |
| Buzzer | Audible alert |
| Breadboard and jumper wires | Circuit prototyping |
| Drain channel and model materials | Controlled demonstration environment |
| Base, bracket and catch tray | Mechanical support and water containment |
| USB cable and power accessories | Programming and power supply |

The preliminary component estimate is documented in [`BILL_OF_MATERIALS.md`](../BILL_OF_MATERIALS.md).

## 7. Electrical and Mechanical Considerations

The ultrasonic sensor is intended to be mounted above the water surface and protected from direct water contact.

The ESP32 uses 3.3 V GPIO logic. If the selected HC-SR04 module produces a 5 V ECHO signal, an appropriately designed voltage divider or compatible logic-level shifter is required. The final circuit must follow the electrical specifications of the selected components.

Mechanical mounting should maintain a stable sensor position and suitable alignment with the water surface. The channel and catch tray are intended to contain demonstration water and reduce the risk of spills reaching electrical components.

## 8. Scope and Limitations

The present concept focuses on water-level measurement and threshold-based local alerts in a controlled drainage model.

The current design does not establish:

- Automatic identification of physical drain blockages.
- Rainfall forecasting or city-scale flood prediction.
- Wireless monitoring, cloud dashboards, or municipal control-room integration.
- Reliability under outdoor weather, debris, sediment, or long-term operating conditions.
- Field-ready performance or verified early-warning lead times.

These capabilities would require additional hardware or software, system integration, and appropriate validation.

## 9. Testing and Validation Approach

Following physical assembly, the proposed system can be evaluated through controlled changes in water level.

The planned evaluation areas include:

- Comparison of sensor measurements against reference distance or depth measurements.
- Repeatability of measurements at different water levels.
- Correct activation of configured warning thresholds.
- Response of LEDs and the buzzer to changes in system state.
- Behaviour under invalid readings and sensor interruptions.
- Electrical safety and protection from water spills.

No experimental outcomes are reported here because physical testing and calibration remain pending.

## 10. Current Development Status

The proposed architecture, operating principle, preliminary hardware configuration, and conceptual threshold logic have been documented. Physical fabrication, circuit integration, calibration, and performance testing remain to be completed.

DRAIN-SENSE is therefore presented as a proposed engineering design rather than a completed or field-validated monitoring system.
