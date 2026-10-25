# DFD Consistency and Balancing Check

## Balancing

Every flow between an external entity and the system in the Context Diagram also appears in the Level-0 DFD.

| External Entity | Flows in Context Diagram | Level-0 Process |
|---|---|---|
| User | Account Information | P1 User Management |
| User | Search Information, Search Results | P2 Space Search and Selection |
| User | Booking Information | P3 Booking Management |
| User | Availability Requests, Availability Information, Notifications | P4 Availability and Notification Management |
| Administrator | Management requests and reports | P5 Administration |
| Third-Party Space Provider | External Search Request, External Space Information, External Availability Information | P2 Space Search and Selection |
| Third-Party Space Provider | Space and Availability Updates | P4 Availability and Notification Management |

## Checklist

| Check | Done |
|---|---|
| Context Diagram shows the system as one process | Yes |
| External entities match the Use Case actors (User, Administrator, DeskOS / External API) | Yes |
| Level-0 DFD uses the same external entities | Yes |
| Context Diagram and Level-0 DFD are balanced | Yes |
| Level-0 has at least 5 processes (P1 to P5) | Yes |
| Level-0 has at least 2 data stores (D1 to D4) | Yes |
| Core Processes Matrix has the same processes as the Level-0 DFD | Yes |
| Processes match the Functional Requirements and Use Cases | Yes |
