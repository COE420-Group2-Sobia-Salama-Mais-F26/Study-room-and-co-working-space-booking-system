# Exercise 2: Functional Requirements

| FR ID | Functional Requirement | Source Scenario/Stakeholder | Contributor |
|---|---|---|---|
| FR-01 | The system shall allow users to search for study rooms, private rooms, desks, and co-working spaces based on location, date, time, duration, and capacity. | Space Search / Use | Sobia adnan- g00100257 |
| FR-02 | The system shall allow users to filter spaces based on facilities such as Wi-Fi, power outlets, whiteboards, and projectors. | Space Search / User | Sobia adnan- g00100257 |
| FR-03 | The system shall allow users to view space details, facilities, and location before selecting a space. | Space Search / User | Sobia adnan- g00100257 |
| FR-04 | The system shall allow users to create bookings for spaces through booking functionality that the platform is authorized to manage. For spaces listed through the DeskOS API, the system shall create a reservation through the API. | Booking Management / User | Sobia adnan- g00100257 |
| FR-05 | The system shall allow customers to cancel an existing booking up to one hour before its scheduled start time. The system shall reject cancellation requests submitted less than one hour before the booking starts and display an explanatory message.cancellation shall be processed only when the DeskOS API has permitted it. | Booking Management / User | Sobia adnan- g00100257 |
| FR-06 | The system shall allow users to modify an existing booking by changing the time, date, or room location. | Booking management/ student | Salama alsuwaidi- g00099875 |
| FR-07 | The system shall send user reminders before their scheduled booking time. | Booking notifications/ student | Salama alsuwaidi- g00099875 |
| FR-08 | The system shall allow customers to request notifications for a specific space and time slot that is currently unavailable. When that space and time slot become available, the system shall notify the customers who requested notifications for that slot. | Availability notifications/ student | Salama alsuwaidi- g00099875 |
| FR-09 | The administrators manage platform-owned listings, while external listings are retrieved from the API and are not directly edited by our platform. | Workspace management/ Administrator | Salama alsuwaidi- g00099875 |
| FR-10 | The system shall allow users to create and update their profiles and view their booking history. | User account management/ student | Salama alsuwaidi- g00099875 |
| FR-11 | The system shall allow users to register for a new account using their name, email address, and password. | User Management / Student | Mais Abudaqqa<br>-g00099729 |
| FR-12 | The system shall prevent users from booking a space that is already reserved for the selected date and time. | Booking Management / Student | Mais Abudaqqa<br>-g00099729 |
| FR-13 | The system shall allow users to view their upcoming and previous bookings, including the space, date, time, and booking status. | Booking Management / Student | Mais Abudaqqa<br>-g00099729 |
| FR-14 | The system shall allow administrators to manage reservations by viewing, updating, or cancelling bookings when necessary. | Reservation Management / Administrator | Mais Abudaqqa<br>-g00099729 |
| FR-15 | The system shall allow administrators to generate reports showing booking and space usage information. | Administration / Administrator | Mais Abudaqqa<br>-g00099729 |
| FR-16 | The system shall send user search criteria to a third-party space provider through an external API and receive matching space information. | S-01 / S-06 / DeskOS API Space Search | Sobia adnan- g00100257 |
| FR-17 | The system shall process space availability information received from the registered third-party provider in DeskOS system and display the relevant availability to users. | S-01 / S-06 / External Space Availability | Sobia adnan- g00100257 |
| FR-18 | The system shall allow the website administrator to view registered user and space provider accounts, activate or deactivate accounts, and manage access to the platform. | Manage Users/ Administrator | Sobia adnan- g00100257 |
| FR-18 | The system shall receive booking-status callbacks from the DeskOS API for confirmed, rejected, and cancelled bookings. The backend shall verify and process each callback, update the corresponding booking record, and make the updated status available to the user | DeskOS API / Booking Management | Sobia Adnan/ g0010257 |
