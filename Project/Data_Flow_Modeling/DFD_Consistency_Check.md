# DFD Consistency and Balancing Check

The context diagram in Figure 5.1 represents the whole system as one process (0) and shows its data flows with the three external entities identified in the use case model: User, Administrator, and DeskOS. ([Context_Diagram.png](Context_Diagram/Context_Diagram.png))

The Level-0 DFD in Figure 5.2 decomposes the system into five major processes: 1.0 User Management, 2.0 Space Search and Selection, 3.0 Booking Management, 4.0 Availability and Notification Management, and
5.0 Administration. It uses four data stores (D1 User Data, D2 Space Data, D3 Booking Data, and D4 Notification Data) and the same external entities as the context diagram. ([Level_0_DFD.png](Level_0_DFD/Level_0_DFD.png))

## Balancing

Every flow between an external entity and the system in the Context Diagram also appears in the Level-0 DFD.

| External Entity | Flows in Context Diagram | Level-0 Process |
|---|---|---|
| User | Account Information | P1 User Management |
| User | Search Information, Search Results | P2 Space Search and Selection |
| User | Booking Information | P3 Booking Management |
| User | Availability Requests, Availability Information, Notifications | P4 Availability and Notification Management |
| Administrator | Management requests and reports | P5 Administration |
| DeskOS API | Space and Availability Request, External Space Information, External Availability Information | P2 Space Search and Selection |
| DeskOS API | External Availability Information | P4 Availability and Notification Management |
| DeskOS API | Create Booking Request, Cancel Booking Request, Booking Reference, Booking Status Callback | P3 Booking Management |

## Checklist

| Check | Done |
|---|---|
| Context Diagram shows the system as one process | Yes |
| External entities match the Use Case actors (User, Administrator, DeskOS) | Yes |
| Level-0 DFD uses the same external entities | Yes |
| Context Diagram and Level-0 DFD are balanced | Yes |
| Level-0 has at least 5 processes (P1 to P5) | Yes |
| Level-0 has at least 2 data stores (D1 to D4) | Yes |
| Core Processes Matrix has the same processes as the Level-0 DFD | Yes |
| Processes match the Functional Requirements and Use Cases | Yes |
