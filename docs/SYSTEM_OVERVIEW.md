# DRAIN-SENSE — System Overview

**Application Unique ID:** VK26-IITH-SC-0073  
**Project domain:** Sustainable Cities  
**Status:** Proposed design; implementation and testing pending

## 1. System Purpose

DRAIN-SENSE is a proposed low-cost drainage monitoring demonstrator. It is intended to detect selected water-level thresholds and provide local alerts that can help demonstrate an early-warning approach for urban drainage systems.

## 2. Proposed System Architecture

The planned system consists of four main functional blocks:

1. **Water-level sensing:** A selected sensor measures a water-level-related input in a controlled tabletop setup.
2. **Microcontroller:** An Arduino-compatible board reads the input and compares it with configured thresholds.
3. **Alert logic:** The controller determines whether a warning condition has been reached.
4. **Local alerts:** An LED and buzzer indicate the configured warning state.

### Functional Flow

Water-level input → Microcontroller → Threshold comparison → LED/buzzer alert

This is a conceptual functional flow, not a verified circuit diagram.

## 3. Proposed Working Principle

1. Set up a controlled water-level demonstrator.
2. Read the sensor output through the microcontroller.
3. Compare the reading with a predefined threshold.
4. Activate the relevant visual and audible alert when the threshold condition is met.
5. Record the sensor reading and alert behaviour during controlled tests.
6. Repeat the procedure at multiple water levels to assess consistency.

The exact sensor, threshold values, circuit connections, and reset logic will be documented after component selection and implementation.

## 4. Civil Engineering Relevance

Urban drainage systems are important for managing stormwater runoff and reducing localised waterlogging. A low-cost monitoring concept may help demonstrate how water-level information can support timely inspection and maintenance decisions.

However, water level alone cannot reliably confirm that a drain is blocked. Actual field conditions may require additional observations, flow measurements, rainfall information, and site-specific validation.

## 5. Initial Prototype Scope

Included in the proposed initial demonstrator:

- Water-level-related sensing
- Microcontroller-based threshold logic
- LED alert
- Buzzer alert
- Controlled tabletop testing

Not included in the initial scope:

- Cloud-connected dashboard
- Custom printed circuit board
- Municipal-scale deployment
- Validated flood prediction
- Automatic confirmation of drain blockage

## 6. Safety and Validation

Testing should use a stable container, low-voltage electronics, and appropriate separation of water from exposed electrical connections. Power must be disconnected before changing wiring.

Calibration, threshold accuracy, response time, repeatability, and limitations must be assessed experimentally before performance claims are made.

## 7. Evidence Status

The architecture described here is proposed. Final wiring diagrams, component specifications, implementation photographs, and test results will be added when they are available.

**Current status:** Concept design; fabrication and validation pending.
