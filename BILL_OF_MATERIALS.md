# DRAIN-SENSE — Preliminary Bill of Materials

**Application Unique ID:** VK26-IITH-SC-0073  
**Project:** Smart Urban Drainage Health Monitoring and Flood Early-Warning System  
**Budget target:** ₹3,000–₹5,000  
**Preliminary planning estimate:** ₹4,200

## 1. Proposed Components

| No. | Component | Purpose | Estimated Cost (INR) |
|---:|---|---|---:|
| 1 | ESP32 development board | Reads sensor values and controls alerts | ₹650 |
| 2 | HC-SR04 ultrasonic sensor | Measures distance to the water surface from a dry, elevated mounting position | ₹250 |
| 3 | LEDs, resistors and buzzer | Provide visual and audible status alerts | ₹250 |
| 4 | Breadboard and jumper wires | Circuit prototyping and connections | ₹350 |
| 5 | USB cable / 5 V power accessories | Power and programming | ₹300 |
| 6 | Drain channel / model materials | Tabletop drainage demonstration channel | ₹800 |
| 7 | Base, bracket, catch tray and sealant | Stable mounting and water containment | ₹800 |
| 8 | Miscellaneous materials and contingency | Small parts and unforeseen expenses | ₹800 |
| | **Estimated total** | | **₹4,200** |

## 2. Budget Status

The target budget range is ₹3,000–₹5,000, with a preliminary planning estimate of ₹4,200. Actual costs may change with selected components, vendor prices, shipping, and materials already available in the lab.

The optional flow sensor is excluded from this estimate.


## 3. Important Electrical and Evidence Notes

The HC-SR04 module should be mounted above the water and kept dry. If its ECHO output is 5 V, use a correctly calculated voltage divider or compatible level shifter before connecting it to an ESP32 GPIO, which uses 3.3 V logic. Disconnect power before changing wiring or making wet adjustments.

This is a preliminary cost plan only; it does not establish that the prototype has been assembled or tested. No performance claims are made from this preliminary budget.

**Current status:** Proposed components; procurement and physical testing pending.
