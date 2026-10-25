# DFD Consistency and Balancing Check

## Balancing: Context Diagram vs. Level-0 DFD

Every flow between an external entity and the system in the Context Diagram enters or leaves a specific Level-0 process.

| External entity | Context Diagram flow | Level-0 process |
|---|---|---|
| User → | Registration Information, Login Information, Profile Information | P1 User Management |
| User → | Booking History Request | P1 User Management / P3 Booking Management |
| User → | Search Criteria, Facility Filters, Space Details Request | P2 Space Search and Selection |
| User → | Booking Request, Group Booking Information, Booking Modification Request, Booking Cancellation Request | P3 Booking Management |
| User → | Availability Request | P4 Availability and Notifications |
| → User | Registration Confirmation, Login Confirmation, Profile Information, Booking History | P1 User Management |
| → User | Available Spaces, Space Details, Facility / Location Information | P2 Space Search and Selection |
| → User | Booking Confirmation, Updated Booking Information, Cancellation Confirmation, Upcoming / Previous Booking Information | P3 Booking Management |
| → User | Availability Information, Booking Reminder, Booking Notification, Availability Notification | P4 Availability and Notifications |
| Administrator → | User Management Request, Space Management Information, Availability Management Information, Reservation Management Request, Room Status Request, Report Request | P5 Administration |
| → Administrator | User Information, Space Information, Availability Information, Reservation Information, Room Status, Booking Reports, Usage Reports, Management Confirmation | P5 Administration |
| → Third-Party Space Provider | External Search Request | P2 Space Search and Selection (correct direction in documentation; verify image separately) |
| Third-Party Space Provider → | External Space Information, External Availability Information | P2 Space Search and Selection (correct direction in documentation; verify image separately) |

All Context Diagram flows appear at Level 0, and no new external flows are added. The User flows in the Context Diagram are grouped labels (for example, *Account Information*) that are split into their detailed flows at Level 0.

## Checklist

| Check | Status |
|---|---|
| The Context Diagram represents the whole system as one process | ✅ |
| External entities match the Use Case actors from Lab 3 | ⚠️ User and Administrator match; UC-16 and UC-17 document provider integration; verify the actual Lab 3 use case diagram separately |
| The Level-0 DFD uses the same external entities | ✅ |
| The Context Diagram and Level-0 DFD are balanced (table above) | Textual flow tables now match; actual diagram images still require verification |
| Level-0 contains at least five meaningful processes (P1–P5) | ✅ |
| Level-0 contains at least two relevant data stores (D1 User Data, D2 Space Data, D3 Booking Data, D4 Notification Data) | ✅ |
| The Core Processes Matrix contains the same processes as the Level-0 DFD | ✅ |
| The DFD processes are consistent with the Functional Requirements and Use Cases | ✅ (see mapping below) |

## Process ↔ Functional Requirement Mapping

| Process | Functional Requirements |
|---|---|
| P1 User Management | FR-10, FR-11, FR-13 |
| P2 Space Search and Selection | FR-01, FR-02, FR-03, FR-16, FR-17 |
| P3 Booking Management | FR-04, FR-05, FR-06, FR-12, FR-13 |
| P4 Availability and Notifications | FR-05, FR-07, FR-08 |
| P5 Administration | FR-09, FR-14, FR-15 |

Functional requirements FR-01 through FR-17 are covered by the process mapping, including external provider integration under P2.
