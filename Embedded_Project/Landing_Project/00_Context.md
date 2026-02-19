# Embedded Mini Project – Landing Gear Safety

## 1. Objective

The purpose of this mini-project is to demonstrate a structured software testing approach applied to a embedded system.

The system under test manages the Landing Gear safety of an aircraft.

The objective is to validate that the system correctly enforces safety rules during takeoff, flight, and landing phases.

---

## 2. System Overview

The software is responsible for:

- Authorizing or preventing landing gear retraction
- Verifying that the landing gear is properly locked before takeoff
- Automatically deploying the landing gear during descent
- Detecting incoherent sensor data
- Entering a SAFE_STATE in case of anomaly

---

## 3. Inputs

The system receives the following inputs:

- Aircraft mode: GROUND / AIRBORNE
- Altitude (in feet)
- Flight phase: CLIMB / CRUISE / DESCENT
- Landing gear status:
  - EXTENDED
  - RETRACTED
  - LOCKED
- Pilot command: RETRACT / EXTEND / NONE

---

## 4. Safety Concept

In case of inconsistent or unsafe conditions, the system shall enter a SAFE_STATE.

In this project, SAFE_STATE is defined as:

- Blocking critical commands
- Maintaining current gear position
- Generating an alert message

---

## 5. Glossary 

- AIRBONE : aircraft state indicating that the aircraft is in flight
- GROUND : aircraft state indicating that the aircraft is on the ground
- CLIMB : flight phase during which the aircraft is gaining altitude after takeoff
- CRUISE : flight phase during which the aircraft maintains a relatively constant altitude and speed
- DESCENT : flight phase during which the aircraft is decreasing altitude in preparation for landing
- EXTENDED : landing gear position where the wheels are deployed
- RETRACTED : landing gear position where the wheels are folded inside the aircraft structure
- LOCKED : landing gear state indicating that the gear is mechanically secured in position and safe for takeoff or landing
