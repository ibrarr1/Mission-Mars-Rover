# Change Requests — Mars Rover Mission Control

## CR-01 — Emergency Safety

### Original
**FR-04:** The rover shall enter Safe Mode when a critical battery or thermal condition is detected.

### New Requirement
**FR-04:** The rover shall enter Safe Mode within 3 seconds when battery temperature exceeds the critical threshold or battery capacity falls below the defined emergency level.

### Impact
- Safe Mode response is time-bound.
- Battery temperature and capacity must be monitored.
- Safe Mode must be triggered automatically.
- Testing must verify activation within 3 seconds.

---

## CR-02 — Mission Expansion

### Original
**NFR-04:** The system shall support communication with multiple rovers simultaneously.

### New Requirement
**NFR-04:** The system shall support at least 20 simultaneously connected rovers.

### Impact
- The scalability requirement is measurable.
- The communication architecture must support at least 20 concurrent rovers.
- Load and scalability testing should include 20 connected rovers.

---

## CR-03 — Security Upgrade

### Original
**NFR-02:** Only authenticated Mission Control operators shall be permitted to issue rover commands.

### New Requirement
**NFR-02:** The system shall require authenticated and role-authorized operators before accepting rover commands.

### Impact
- Authentication alone is no longer sufficient.
- Operators must have an appropriate role/permission.
- Unauthorized roles must be prevented from issuing commands.
- Testing must include unauthorized-role scenarios.

## Traceability Summary

| Change Request | Requirement | Main Change |
|---|---|---|
| CR-01 | FR-04 | Adds a 3-second Safe Mode response requirement and explicit emergency thresholds. |
| CR-02 | NFR-04 | Changes vague multi-rover support to at least 20 simultaneously connected rovers. |
| CR-03 | NFR-02 | Adds role authorization to authentication before accepting commands. |
