# Requirements Traceability Matrix

This matrix ensures that each requirement is covered by at least one test case.

| Requirement ID | Description | Related Test Case(s) |
|----------------|------------|----------------------|
| REQ-LG-001 | Prevent takeoff if gear not LOCKED | TC-LG-001 |
| REQ-LG-002 | Allow gear retraction only when AIRBORNE | TC-LG-002, TC-LG-003 |
| REQ-LG-003 | Automatic gear deployment below 1000 ft during descent | TC-LG-004 |
| REQ-LG-004 | Enter SAFE_STATE in case of sensor inconsistency | TC-LG-005 |
| REQ-LG-005 | SAFE_STATE behavior definition | TC-LG-005 |
