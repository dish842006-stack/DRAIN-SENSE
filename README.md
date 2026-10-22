# DRAIN-SENSE
### Smart Urban Drainage Health Monitoring and Flood Early-Warning System

**Application Unique ID:** VK26-IITH-SC-0073  
**Competition:** Vishwakarma Awards 2026–27  
**Domain:** Sustainable Cities  
**Project Category:** Hardware-Based Urban Infrastructure Monitoring

## 1. Project Overview

DRAIN-SENSE is a proposed smart monitoring system designed to demonstrate how water-level sensing and threshold-based alerts can support urban drainage monitoring and early identification of potential waterlogging conditions.

The system combines an ultrasonic distance sensor, an ESP32 microcontroller, and visual and audible indicators. The proposed arrangement monitors the distance between a sensor mounted above the water and the water surface. Changes in the measured distance can be used to estimate water-level changes and trigger alerts when predefined thresholds are reached.

The project is intended to demonstrate a practical, low-cost approach to drainage monitoring through a controlled tabletop model.

## 2. Problem Statement

Urban drainage systems may experience rising water levels and blockages during periods of heavy rainfall. When such conditions are not identified promptly, they can contribute to local waterlogging, traffic disruption, and difficulties for urban residents.

Conventional visual inspection may not provide continuous information about changing water levels. An affordable monitoring concept that detects water-level changes and provides clear alerts could help demonstrate an additional approach to drainage observation.

## 3. Proposed Solution

DRAIN-SENSE proposes a sensor-based monitoring unit that measures water-surface distance and evaluates the resulting measurements against predefined thresholds.

The proposed system consists of:

- **Ultrasonic sensing:** Measures the distance from the sensor to the water surface without requiring the sensor to be submerged.
- **ESP32 controller:** Processes sensor readings and applies programmed threshold logic.
- **Visual indicators:** LEDs communicate the system's configured status.
- **Audible indicator:** A buzzer provides an alert when a specified threshold is crossed.
- **Tabletop drainage model:** Represents a simplified drainage channel for demonstrating the proposed monitoring concept.

The present design focuses on water-level monitoring. Actual blockage detection, field deployment, and city-scale flood prediction are not claimed as established capabilities.

## 4. Project Objectives

1. Develop a low-cost hardware concept for monitoring water-level changes in a drainage-channel model.
2. Demonstrate non-contact water-level measurement using an ultrasonic sensor.
3. Implement threshold-based visual and audible alerts using an ESP32.
4. Establish a framework for evaluating sensor readings and alert responses under controlled conditions.
5. Explore the potential application of affordable sensing technology to future urban drainage monitoring systems.

## 5. System Architecture

The proposed monitoring sequence is:

**Water-level change → Ultrasonic distance measurement → ESP32 processing → Threshold evaluation → LED and buzzer indication**

The sensor is positioned above the water surface. As the water level rises, the measured distance is expected to decrease. The controller compares the measured value with configured thresholds and activates the corresponding indicator.

The accuracy and reliability of this sequence remain subject to physical testing and calibration.

## 6. Preliminary Hardware and Budget

| Component | Function | Estimated Cost |
|---|---|---:|
| ESP32 development board | Sensor processing and control | ₹650 |
| HC-SR04 ultrasonic sensor | Water-surface distance measurement | ₹250 |
| LEDs, resistors and buzzer | Status and alert indication | ₹250 |
| Breadboard and jumper wires | Circuit prototyping | ₹350 |
| USB cable and 5 V power accessories | Power and programming | ₹300 |
| Drain channel and model materials | Tabletop demonstration model | ₹800 |
| Base, mounting bracket, catch tray and sealant | Mechanical support and water containment | ₹800 |
| Miscellaneous materials and contingency | Additional small components and incidental costs | ₹800 |
| **Total preliminary estimate** | | **₹4,200** |

The proposed budget range is ₹3,000–₹5,000. The ₹4,200 figure is a preliminary planning estimate rather than a verified supplier quotation. Final costs may vary depending on procurement and reusable materials available in the laboratory.

## 7. Development and Validation Status

DRAIN-SENSE is currently at the proposed-design and planning stage. The system architecture, intended operating principle, preliminary component selection, and initial budget have been documented.

Physical assembly, sensor calibration, controlled experiments, and performance validation remain pending. Consequently, no measured detection accuracy, response time, reliability figure, or field-performance result is claimed.

Future validation is intended to examine water-level measurement, repeatability, threshold-alert behaviour, and the response of the system under controlled demonstration conditions.

## 8. Safety and Design Considerations

The ultrasonic sensor is intended to remain above the water surface and protected from direct water contact. If the selected sensor provides a 5 V ECHO output, an appropriate voltage divider or logic-level shifter is required before connecting it to an ESP32 GPIO input.

The electronic circuit and water-containing model are intended to be arranged to reduce the risk of splashes or spills reaching electrical components.

## 9. Potential Impact

If successfully developed and validated, DRAIN-SENSE could serve as an educational demonstration of affordable sensor-based drainage monitoring. The concept may provide a foundation for future investigation into distributed water-level monitoring and early warning at selected drainage locations.

Any use in operational municipal infrastructure would require further engineering development, environmental protection, calibration, communications integration, and field validation.

## 10. Project Resources

- **GitHub Repository:** https://github.com/dish842006-stack/DRAIN-SENSE
- **Application Unique ID:** VK26-IITH-SC-0073

## 11. Conclusion

DRAIN-SENSE presents a proposed hardware-based approach to demonstrating drainage water-level monitoring through ultrasonic sensing and threshold-based alerts. Its emphasis is on affordability, a straightforward system architecture, and a testable engineering concept relevant to sustainable urban infrastructure.

The project's effectiveness will be assessed through physical implementation and controlled testing before any claims of operational performance are made.
