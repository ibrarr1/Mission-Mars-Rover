# Non-Functional Requirements — Mars Rover Mission Control

| ID | Non-Functional Requirement |
|---|---|
| NFR-01 | The system shall normally complete command processing within 5 seconds after a command is received by the rover. |
| NFR-02 | The system shall require authenticated and role-authorized operators before accepting rover commands. |
| NFR-03 | The system shall continue operating despite temporary communication interruptions. |
| NFR-04 | The system shall support at least 20 simultaneously connected rovers. |
| NFR-05 | The system shall operate within the available communication bandwidth and account for communication delays of several minutes. |

## Original Requirements Changed

**NFR-02 original:** Only authenticated Mission Control operators shall be permitted to issue rover commands.

**NFR-02 updated by CR-03:** The system shall require authenticated and role-authorized operators before accepting rover commands.

**NFR-04 original:** The system shall support communication with multiple rovers simultaneously.

**NFR-04 updated by CR-02:** The system shall support at least 20 simultaneously connected rovers.
