# Mars Rover Mission Control

## Mission Brief

Mars Rover Mission Control is a software system for remotely controlling exploration rovers on Mars. The rover communicates with Mission Control through a communication link with limited bandwidth and several minutes of communication delay.

### Engineering Objectives

The system must:
- Send movement commands to rovers.
- Receive rover location and health data.
- Detect communication failures.
- Prevent unauthorized commands.
- Automatically place a rover into a safe state when a critical fault is detected.
- Store mission events for later investigation.

## 1. Functional Requirements

| ID | Requirement |
|---|---|
| FR-01 | The system shall allow authenticated Mission Control operators to send movement commands to the rover. |
| FR-02 | The rover shall receive and execute valid commands sent from Mission Control. |
| FR-03 | The rover shall report its current position, battery level, temperature, and communication status to Mission Control. |
| FR-04 | The rover shall enter Safe Mode within 3 seconds when battery temperature exceeds the critical threshold or battery capacity falls below the defined emergency level. |
| FR-05 | The system shall reject invalid or unauthorized commands. |
| FR-06 | Mission Control shall receive the execution status of commands sent to the rover. |
| FR-07 | The system shall detect and handle temporary communication interruptions. |
| FR-08 | The system shall record all commands and critical rover events with a timestamp and operator ID. |

## 2. Non-Functional Requirements

| ID | Requirement |
|---|---|
| NFR-01 | The system shall normally complete command processing within 5 seconds after a command is received by the rover. |
| NFR-02 | The system shall require authenticated and role-authorized operators before accepting rover commands. |
| NFR-03 | The system shall continue operating despite temporary communication interruptions. |
| NFR-04 | The system shall support at least 20 simultaneously connected rovers. |
| NFR-05 | The system shall operate within the available communication bandwidth and account for communication delays of several minutes. |

## 3. Change Requests

### CR-01 — Emergency Safety

**Original FR-04:** The rover shall enter Safe Mode when a critical battery or thermal condition is detected.

**Updated FR-04:** The rover shall enter Safe Mode within 3 seconds when battery temperature exceeds the critical threshold or battery capacity falls below the defined emergency level.

**Impact:** Safe Mode response is now time-bound. Battery temperature and capacity must be monitored, and testing must verify activation within 3 seconds.

### CR-02 — Mission Expansion

**Original NFR-04:** The system shall support communication with multiple rovers simultaneously.

**Updated NFR-04:** The system shall support at least 20 simultaneously connected rovers.

**Impact:** The scalability requirement is now measurable. The system must be tested with at least 20 concurrent rover connections.

### CR-03 — Security Upgrade

**Original NFR-02:** Only authenticated Mission Control operators shall be permitted to issue rover commands.

**Updated NFR-02:** The system shall require authenticated and role-authorized operators before accepting rover commands.

**Impact:** Authentication alone is insufficient. The system must verify both operator identity and command authorization before accepting rover commands.

## 4. Requirements Traceability

| Change Request | Requirement | Original | Updated | Main Impact |
|---|---|---|---|---|
| CR-01 | FR-04 | Safe Mode on critical battery/thermal condition | Safe Mode within 3 seconds of threshold violation | Emergency response and testing |
| CR-02 | NFR-04 | Multiple rovers | At least 20 simultaneous rovers | Scalability and load testing |
| CR-03 | NFR-02 | Authentication required | Authentication + role authorization | Access control and security |

## 5. Final Requirements

The requirements shown in the tables above represent the final state after applying CR-01, CR-02, and CR-03.

See the detailed requirement documents in this repository for the complete analysis.
