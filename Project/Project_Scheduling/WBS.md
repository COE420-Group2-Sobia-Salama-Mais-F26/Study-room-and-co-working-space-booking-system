# Work Breakdown Structure (WBS)

| ID | Task Name | Description | Predecessor(s) | Duration (Days) |
|---|---|---|---|---|
| T1 | Requirements Refinement | Review and finalize the project scope, scenarios, functional requirements, non-functional requirements, actors, and use cases from Labs 1–3. Resolve inconsistencies before implementation. | — | 3 |
| T2 | Database Design | Design the data structures required for user accounts, spaces, bookings, availability, and notifications, including the relationships between the data. | T1 | 4 |
| T3 | User Interface Design | Design interfaces for account registration, login, profile management, space search, filtering, space details, booking management, notifications, and administration. | T1 | 4 |
| T4 | User Management Implementation | Implement account registration, authentication, login, profile management, user information, and access to booking history. | T2, T3 | 5 |
| T5 | Space Search and Selection Implementation | Implement space searching and filtering based on location, date, time, duration, capacity, space type, and facilities. Implement space-detail viewing and integration with the third-party space provider. | T2, T3 | 6 |
| T6 | Booking Management Implementation | Implement booking creation, booking confirmation, booking modification, booking cancellation, and viewing of upcoming and previous bookings. | T4, T5 | 7 |
| T7 | Availability and Notification Implementation | Implement availability checking and updates, booking reminders, booking notifications, and notifications when a previously unavailable space becomes available. | T6 | 5 |
| T8 | Administration Implementation | Implement administrator functions for managing users, spaces, facilities, availability, reservations, room status, and booking/usage reports. | T4, T5, T6 | 6 |
| T9 | System Integration | Integrate user management, space search, booking management, availability and notification management, and administration. Verify communication with the third-party space provider and ensure the components work together correctly. | T7, T8 | 4 |
| T10 | System Testing and Bug Fixing | Test registration, authentication, space search, filtering, external space information, booking operations, modifications, cancellations, availability updates, notifications, administration, data consistency, and system integration. Fix identified defects. | T9 | 6 |
| T11 | Deployment Preparation and Final Documentation | Prepare the system for deployment, finalize system documentation, verify the final functionality, and organize the project deliverables and repository. | T10 | 3 |

Implementation tasks T4–T8 match the Level-0 DFD processes P1–P5.
