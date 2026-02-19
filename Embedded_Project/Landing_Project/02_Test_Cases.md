# Test cases – Landing gear safety 

---

## TC-LG-001 – Prevent takeoff if gear not locked

Related requirement: REQ-LG-001

Preconditions:
- Aircraft mode = GROUND
- Landing gear status = EXTENDED (not LOCKED)

Step:
1. Simulate takeoff attempt.

Expected result:
- Takeoff is prevented.
- Alert message is generated.

---

## TC-LG-002 – Allow gear retraction in flight

Related requirement: REQ-LG-002

Preconditions:
- Aircraft mode = AIRBORNE
- Landing gear status = EXTENDED

Step:
1. Send pilot command: RETRACT.

Expected result:
- Landing gear state changes to RETRACTED.
- No alert is generated.

---

## TC-LG-003 – Prevent gear retraction on ground

Related requirement: REQ-LG-002

Preconditions:
- Aircraft mode = GROUND
- Landing gear status = EXTENDED

Step:
1. Send pilot command: RETRACT.

Expected result:
- Landing gear remains EXTENDED.
- Alert message is generated.

---

## TC-LG-004 – Automatic gear deployment during descent

Related requirement: REQ-LG-003

Preconditions:
- Aircraft mode = AIRBORNE
- Flight phase = DESCENT
- Altitude = 800 ft
- Landing gear status = RETRACTED

Step:
1. Simulate descent below 1000 ft.

Expected result:
- Landing gear automatically changes to EXTENDED.
- No alert is generated.

---

## TC-LG-005 – Sensor inconsistency triggers SAFE_STATE

Related Requirement: REQ-LG-004
Related Requirement: REQ-LG-005

Preconditions:
- Aircraft mode = GROUND
- Altitude = 2000 ft
- Landing gear status = EXTENDED

Step:
1. Simulate system evaluation.

Expected result:
- SAFE_STATE is activated.
- Landing gear position remains unchanged.
- Alert message is generated.
