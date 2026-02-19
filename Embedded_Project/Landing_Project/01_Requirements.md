# Requirements – Landing Gear Safety 

## Identification Convention

Requirements are identified using the following format:

REQ-LG-XXX

Where:
- REQ = Requirement
- LG = Landing Gear
- XXX = Sequential number

---

## Functional Requirements

### REQ-LG-001 – Takeoff Authorization

The system shall prevent takeoff if the landing gear is not in LOCKED state.

---

### REQ-LG-002 – Gear Retraction Condition

The system shall allow landing gear retraction only when the aircraft mode is AIRBORNE.

If the aircraft mode is GROUND, gear retraction shall be rejected.

---

### REQ-LG-003 – Automatic Gear Deployment During Descent

If the aircraft is in DESCENT phase and altitude is below 1000 ft,  
the system shall automatically set landing gear to EXTENDED.

---

### REQ-LG-004 – Sensor Inconsistency Detection

If inconsistent data is detected between aircraft mode and altitude  
(e.g., mode = GROUND while altitude > 1000 ft),  
the system shall enter SAFE_STATE.

---

### REQ-LG-005 – SAFE_STATE Behavior

When SAFE_STATE is activated, the system shall:

- Maintain current gear position
- Generate an alert message
