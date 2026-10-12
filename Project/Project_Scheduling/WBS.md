# Work Breakdown Structure (WBS)

| ID | Task Name | Description | Predecessor(s) | Duration (Days) |
|---|---|---|---|---|
| T1 | Requirements Refinement | Review and finalize the project scope, functional requirements, non-functional requirements, scenarios, and use cases from Labs 2–3. | — | 3 |
| T2 | Database Design | Design the database structure for users, spaces, bookings, availability, and notifications. | T1 | 4 |
| T3 | User Interface Design | Design the main web interfaces for registration/login, space search, space details, booking, user bookings, and administration. | T1 | 4 |
| T4 | User Management Implementation | Implement user registration, login, profile management, and booking-history functionality. | T2, T3 | 5 |
| T5 | Space Search and Selection Implementation | Implement searching, filtering, space details, location information, and availability display for study rooms, private rooms, desks, and co-working spaces. | T2, T3 | 6 |
| T6 | Booking Management Implementation | Implement booking, group booking, booking modification, cancellation, booking confirmation, and upcoming/previous booking functionality. | T4, T5 | 7 |
| T7 | Availability and Notifications Implementation | Implement availability updates, space status, booking reminders, booking notifications, and notifications when occupied spaces become available. | T6 | 5 |
| T8 | Administration Implementation | Implement user management, space management, availability management, reservation management, room-status monitoring, and usage/booking reports. | T4, T5, T6 | 6 |
| T9 | System Integration | Integrate all implemented modules and ensure that user, space, booking, availability, notification, and administration functions work together. | T7, T8 | 4 |
| T10 | System Testing and Bug Fixing | Test the complete system against the functional and non-functional requirements and correct identified problems. | T9 | 6 |
| T11 | Deployment Preparation and Final Documentation | Prepare the web system for deployment, finalize documentation, and prepare the final project deliverables. | T10 | 3 |

Implementation tasks T4–T8 match the Level-0 DFD processes P1–P5.
