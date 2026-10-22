# DRAIN-SENSE — Test and Validation Plan

**Application Unique ID:** VK26-IITH-SC-0073  
**Project:** Smart Urban Drainage Health Monitoring and Flood Early-Warning System  
**Domain:** Sustainable Cities  
**Testing Stage:** Planned; physical validation pending

## 1. Purpose

This document defines the proposed test methodology for evaluating DRAIN-SENSE, a hardware-based concept for monitoring water levels in a tabletop drainage model and generating threshold-based alerts.

The test plan establishes the conditions to be examined, the expected system behaviour, and the evidence required to assess performance after implementation. The tests described below are planned activities, not completed experiments.

## 2. Testing Objectives

The proposed testing process aims to:

1. Evaluate ultrasonic water-surface distance measurements against reference measurements.
2. Examine measurement consistency at different water levels.
3. Verify the controller's response to configured warning thresholds.
4. Assess LED and buzzer activation under defined operating conditions.
5. Examine the system's response to invalid readings and sensor interruptions.
6. Evaluate the physical arrangement for electrical safety and water containment.

## 3. Test Environment

Testing is intended to take place in a controlled tabletop drainage model incorporating the ultrasonic sensor, ESP32 controller, alert indicators, and water-containing channel.

Reference distance or depth measurements will be obtained using an appropriate measuring instrument. The sensor mounting height, channel reference level, configured thresholds, power arrangement, and test conditions will be documented before testing.

Testing should begin with a dry setup and proceed to controlled water-level changes only after the electrical assembly has been checked.

## 4. Planned Test Cases

| Test ID | Test Description | Method | Expected Result |
|---|---|---|---|
| DS-T01 | Sensor initialization | Power the assembled system and inspect sensor readings | The sensor initializes and provides usable readings under suitable conditions |
| DS-T02 | Distance measurement | Compare sensor readings with reference distances at selected positions | Measurements fall within the tolerance established for the test |
| DS-T03 | Water-level tracking | Change the water level in controlled increments | Measured distance decreases as the water surface rises, subject to sensor limitations |
| DS-T04 | Normal-state indication | Operate the model below the warning threshold | The configured normal-status indication is maintained |
| DS-T05 | Warning-threshold activation | Raise the water level through the configured warning threshold | The warning indication activates according to the programmed logic |
| DS-T06 | High-level alert | Raise the water level through the configured high-level threshold | The configured high-level indication and audible alert activate |
| DS-T07 | Threshold transition | Raise and lower the water level around configured thresholds | State changes follow the implemented logic without unintended rapid switching |
| DS-T08 | Invalid sensor reading | Introduce a controlled sensor interruption or invalid measurement | The system handles the invalid reading according to its implemented error-handling logic |
| DS-T09 | Repeatability | Repeat measurements at the same reference levels | The spread of readings can be quantified and compared across trials |
| DS-T10 | Water containment and electrical arrangement | Inspect the physical layout during controlled operation | Electrical components remain protected from direct water contact and spills under the tested conditions |

## 5. Measurement and Evaluation

### 5.1 Distance Measurement Error

The absolute distance error for each trial can be calculated as:

\[
E_{\mathrm{abs}}=|d_{\mathrm{sensor}}-d_{\mathrm{reference}}|
\]

where:

- \(d_{\mathrm{sensor}}\) is the distance measured by the ultrasonic sensor.
- \(d_{\mathrm{reference}}\) is the corresponding reference distance.

If the reference distance is non-zero, percentage error may be calculated as:

\[
E_{\%}=\frac{|d_{\mathrm{sensor}}-d_{\mathrm{reference}}|}{d_{\mathrm{reference}}}\times100
\]

The reference measurement and the conditions under which it was taken must be recorded. Percentage error is not appropriate when the reference value is zero.

### 5.2 Threshold Response

Threshold tests will record the reference water level, measured sensor distance, configured threshold, controller state, and indicator response.

The response time, if measured, will be calculated from the time the defined threshold condition is reached to the time the corresponding alert activates. Any timing method and measurement uncertainty will be documented.

### 5.3 Repeatability

Repeated readings will be collected at selected fixed water levels. Their range, mean, or standard deviation may be calculated to describe measurement variation.

Acceptance tolerances will be established before the relevant test is conducted and will reflect the intended demonstration requirements and selected sensor specifications.

## 6. Evidence and Record Keeping

The validation record is intended to include:

- Test date and setup description.
- Sensor mounting height and reference measurements.
- Component configuration and programmed threshold values.
- Raw sensor readings and calculated measurement errors.
- Observed LED and buzzer behaviour.
- Any invalid readings, interruptions, or unexpected responses.
- Photographs or video of the actual test setup, where available.
- Test outcome and any corrective changes made.

Only evidence from tests actually performed will be reported as an observed result.

## 7. Limitations

Successful tabletop testing would demonstrate behaviour only under the tested conditions. It would not, by itself, establish reliable operation in real drainage infrastructure.

Outdoor deployment would require further evaluation of sensor protection, debris, sediment, water turbulence, weather exposure, long-term reliability, power continuity, and communication requirements.

The present test plan does not claim validation of automatic blockage detection, rainfall forecasting, or city-scale flood prediction.

## 8. Current Status

The test cases and evaluation methods have been defined at the planning stage. Physical assembly, calibration, test execution, and results recording remain pending.

**Current validation status:** Tests planned; no experimental results claimed.
