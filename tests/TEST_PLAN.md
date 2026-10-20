# DRAIN-SENSE — Test and Validation Plan

**Application Unique ID:** VK26-IITH-SC-0073  
**Project:** Smart Urban Drainage Health Monitoring and Flood Early-Warning System

**Status:** Planned tests; no physical test results available yet.

## 1. Objective

This plan defines how the proposed DRAIN-SENSE tabletop prototype will be assessed after assembly. The objective is to evaluate water-level detection, alert operation, repeatability, and response time under controlled conditions.

## 2. Planned Tests

| Test ID | Test | Procedure | Data to Record |
|---|---|---|---|
| T01 | Initial power-on | Power the assembled circuit using its intended supply | Startup behaviour and any faults |
| T02 | Low-level condition | Introduce a water level below the configured warning threshold | Sensor reading and alert state |
| T03 | Threshold detection | Raise the water level through the configured threshold | Threshold reading and alert activation |
| T04 | High-level condition | Raise the water level above the warning threshold | Sensor reading and alert state |
| T05 | Reset behaviour | Lower the water level after triggering an alert | Reset condition and alert deactivation |
| T06 | Repeatability | Repeat the same controlled threshold test several times | Readings and activation consistency |
| T07 | Response time | Measure elapsed time between crossing the threshold and alert activation | Time for each trial |
| T08 | Stability | Observe readings at a fixed water level for a defined period | Reading variation and unexpected alerts |

## 3. Test Method

1. Confirm the selected sensor and its operating requirements.
2. Assemble the circuit and inspect all connections before powering it.
3. Establish a safe, controlled test arrangement.
4. Record the sensor output at known water levels using a suitable reference measurement.
5. Identify the threshold and alert behaviour specified in the implemented design.
6. Repeat tests under comparable conditions.
7. Record failures, inconsistent readings, and corrective changes.
8. Preserve genuine photographs and dated test records.

The number of trials, reference measurement method, and acceptance criteria must be finalised before formal testing begins.

## 4. Data Recording Template

| Trial | Reference Water Level | Sensor Reading | Alert Activated? | Response Time | Remarks |
|---|---|---|---|---|---|
| 1 | Pending | Pending | Pending | Pending | Not tested |
| 2 | Pending | Pending | Pending | Pending | Not tested |
| 3 | Pending | Pending | Pending | Pending | Not tested |

Replace the pending entries with measured values only after conducting the corresponding trials.

## 5. Evaluation Criteria

The prototype will be evaluated for:

- Correct alert operation at the configured threshold.
- Consistent behaviour across repeated trials.
- Reasonable agreement between sensor readings and reference measurements.
- Repeatable response-time measurements.
- Safe operation and clearly documented limitations.

Numerical acceptance limits will be set after the sensor and circuit design have been finalised.

## 6. Limitations

A successful tabletop test would not establish field reliability or flood-prediction accuracy. Real drains involve varying flow, sediment, debris, rainfall, and installation conditions that require separate investigation.

## 7. Results Status

**Testing has not yet been completed.** No measured accuracy, response time, repeatability, or field-performance result is claimed in this document.

Test records will be updated after actual prototype assembly and validation.

