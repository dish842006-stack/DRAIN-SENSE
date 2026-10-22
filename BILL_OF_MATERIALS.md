# DRAIN-SENSE — Preliminary Bill of Materials

**Application Unique ID:** VK26-IITH-SC-0073  
**Project:** Smart Urban Drainage Health Monitoring and Flood Early-Warning System  
**Domain:** Sustainable Cities

## 1. Overview

This bill of materials identifies the proposed electronic, electrical, and mechanical components required to develop the DRAIN-SENSE tabletop drainage-monitoring demonstration system. The preliminary cost estimate is ₹4,200, within the proposed project budget range of ₹3,000–₹5,000.

## 2. Component Specifications and Cost Estimate

| No. | Component | Proposed Function | Estimated Cost (INR) |
|---:|---|---|---:|
| 1 | ESP32 development board | Processes sensor readings and controls alert outputs | ₹650 |
| 2 | HC-SR04 ultrasonic sensor | Measures the distance between the sensor and water surface | ₹250 |
| 3 | LEDs, resistors and buzzer | Provide visual status indications and audible alerts | ₹250 |
| 4 | Breadboard and jumper wires | Support circuit prototyping and electrical connections | ₹350 |
| 5 | USB cable and 5 V power accessories | Support programming and power supply | ₹300 |
| 6 | Drain channel and model materials | Represent a simplified drainage channel | ₹800 |
| 7 | Base, mounting bracket, catch tray and sealant | Provide structural support, sensor mounting and water containment | ₹800 |
| 8 | Miscellaneous materials and contingency allowance | Cover additional small components and incidental expenses | ₹800 |
| | **Total Preliminary Estimated Cost** | | **₹4,200** |

## 3. Budget Justification

The proposed budget covers the primary control unit, water-level sensing component, alert hardware, prototyping accessories, and mechanical materials for a tabletop demonstration.

The preliminary estimate is ₹4,200, against a target budget range of ₹3,000–₹5,000. These figures are planning estimates and have not yet been verified against supplier quotations. Actual expenditure will depend on component specifications, market prices, shipping charges, and the availability of reusable laboratory materials.

An optional flow sensor is excluded from the current estimate.

## 4. Engineering and Safety Considerations

- **Sensor placement:** The ultrasonic sensor is intended to be mounted above the water surface, without direct immersion.
- **Voltage compatibility:** If the selected HC-SR04 module provides a 5 V ECHO output, a suitably designed voltage divider or compatible logic-level shifter is required before connection to the ESP32's 3.3 V GPIO input.
- **Water containment:** The proposed base and catch tray are intended to reduce the risk of spills reaching electrical components.
- **Power and wiring:** The final circuit arrangement must follow the selected components' electrical ratings and applicable laboratory safety practices.

## 5. Procurement and Implementation Status

The listed components represent the proposed hardware configuration. Procurement, assembly, and physical testing remain pending. Therefore, the costs are preliminary estimates rather than confirmed purchase prices, and the bill does not indicate that the hardware has already been acquired or installed.

## 6. Summary

The proposed component set provides a preliminary basis for developing a low-cost demonstration of ultrasonic water-level measurement and threshold-based alerts. The final bill of materials will reflect the components selected for implementation and the actual expenditure recorded during procurement.
