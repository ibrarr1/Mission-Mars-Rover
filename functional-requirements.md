# Functional Requirements — Mars Rover Mission Control

| ID | Functional Requirement |
|---|---|
| FR-01 | The system shall allow authenticated Mission Control operators to send movement commands to the rover. |
| FR-02 | The rover shall receive and execute valid commands sent from Mission Control. |
| FR-03 | The rover shall report its current position, battery level, temperature, and communication status to Mission Control. |
| FR-04 | The rover shall enter Safe Mode within 3 seconds when battery temperature exceeds the critical threshold or battery capacity falls below the defined emergency level. |
| FR-05 | The system shall reject invalid or unauthorized commands. |
| FR-06 | Mission Control shall receive the execution status of commands sent to the rover. |
| FR-07 | The system shall detect and handle temporary communication interruptions. |
| FR-08 | The system shall record all commands and critical rover events with a timestamp and operator ID. |

## Original FR-04
The rover shall enter Safe Mode when a critical battery or thermal condition is detected.

## Change applied by CR-01
The requirement now specifies a 3-second response time and explicit battery temperature/capacity threshold conditions.
