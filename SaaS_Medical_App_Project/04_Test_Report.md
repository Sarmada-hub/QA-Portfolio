# Test report  

## Test objective

The objective of this test campaign was to validate the functional behavior of the Medical Appointment SaaS application.

Testing activities focused on authentication, access control and appointment management.


## Test scope

- User authentication
- Account registration
- Access control
- Appointment booking
- Appointment cancellation


## Environment

| Parameter | Value |
|-----------|-------|
| Application Type | Web SaaS |
| Environnement | Google Chrome |
| Test Type | Manual functional |


## 4. Executed test cases

| Module | Total Tests | Passed | Failed |
|--------|-------------|--------|--------|
| Authentication | 5 | 5 | 0 |
| Appointment Booking | 3 | 2 | 1 |
| **Total** | **8** | **7** | **1** |

---

## Bug report

| Defect ID | Title | Severity | Status |
|------------|-------|----------|--------|
| BUG-RDV-001 | Cancellation allowed less than 24h before appointment | High | Open |


## Risk Assessment

The identified defect impacts business rules related to appointment management.

Allowing late cancellation may lead to:
- practitioner scheduling disruption
- operational inefficiencies
- reduced service reliability

Risk level: **Medium to High**
