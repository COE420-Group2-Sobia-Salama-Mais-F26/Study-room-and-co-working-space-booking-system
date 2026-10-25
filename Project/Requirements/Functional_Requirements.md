# Functional Requirements

Each member contributed at least five FRs. The contributor of every requirement is kept in the consolidated list below so individual work stays traceable.

## Individual Contributions

### Sobia Adnan – g00100257
FR-01, FR-02, FR-03, FR-04, FR-05, FR-16, FR-17, FR-18, FR-19

### Salama Alsuwaidi – g00099875
FR-06, FR-07, FR-08, FR-09, FR-10

### Mais Abudaqqa – g00099729
FR-11, FR-12, FR-13, FR-14, FR-15

## Team Consolidated Requirements

| FR ID | Functional Requirement | Source Scenario / Stakeholder | Contributor |
|---|---|---|---|
| FR-01 | The system shall allow users to search for study rooms, private rooms, desks, and co-working spaces based on location, date, time, duration, and capacity. | Space Search / User | Sobia Adnan – g00100257 |
| FR-02 | The system shall allow users to filter spaces based on facilities such as Wi-Fi, power outlets, whiteboards, and projectors. | Space Search / User | Sobia Adnan – g00100257 |
| FR-03 | The system shall allow users to view space details, facilities, and location before selecting a space. | Space Search / User | Sobia Adnan – g00100257 |
| FR-04 | The system shall allow users to create bookings for spaces through booking functionality that the platform is authorized to manage. For spaces listed through the DeskOS API, the system shall create a reservation through the API. | Booking Management / User | Sobia Adnan – g00100257 |
| FR-05 | The system shall allow customers to cancel an existing booking up to one hour before its scheduled start time. The system shall reject cancellation requests submitted less than one hour before the booking starts and display an explanatory message. Cancellation shall be processed only when the DeskOS API has permitted it. | Booking Management / User | Sobia Adnan – g00100257 |
| FR-06 | The system shall allow users to modify an existing booking by changing the time, date, or room location. | Booking Management / Student | Salama Alsuwaidi – g00099875 |
| FR-07 | The system shall send users reminders before their scheduled booking time. | Booking Notifications / Student | Salama Alsuwaidi – g00099875 |
| FR-08 | The system shall allow customers to request notifications for a specific space and time slot that is currently unavailable. When that space and time slot become available, the system shall notify the customers who requested notifications for that slot. | Availability Notifications / Student | Salama Alsuwaidi – g00099875 |
| FR-09 | The administrators manage platform-owned listings, while external listings are retrieved from the API and are not directly edited by our platform. | Workspace Management / Administrator | Salama Alsuwaidi – g00099875 |
| FR-10 | The system shall allow users to create and update their profiles and view their booking history. | User Account Management / Student | Salama Alsuwaidi – g00099875 |
| FR-11 | The system shall allow users to register for a new account using their name, email address, and password. | User Management / Student | Mais Abudaqqa – g00099729 |
| FR-12 | The system shall prevent users from booking a space that is already reserved for the selected date and time. | Booking Management / Student | Mais Abudaqqa – g00099729 |
| FR-13 | The system shall allow users to view their upcoming and previous bookings, including the space, date, time, and booking status. | Booking Management / Student | Mais Abudaqqa – g00099729 |
| FR-14 | The system shall allow administrators to manage reservations by viewing, updating, or cancelling bookings when necessary. | Reservation Management / Administrator | Mais Abudaqqa – g00099729 |
| FR-15 | The system shall allow administrators to generate reports showing booking and space usage information. | Administration / Administrator | Mais Abudaqqa – g00099729 |
| FR-16 | The system shall send user search criteria to a third-party space provider through an external API and receive matching space information. | S-01 / S-06 / DeskOS API Space Search | Sobia Adnan – g00100257 |
| FR-17 | The system shall process space availability information received from the registered third-party provider in the DeskOS system and display the relevant availability to users. | S-01 / S-06 / External Space Availability | Sobia Adnan – g00100257 |
| FR-18 | The system shall allow the website administrator to view registered user and space provider accounts, activate or deactivate accounts, and manage access to the platform. | Manage Users / Administrator | Sobia Adnan – g00100257 |
| FR-19 | The system shall receive booking-status callbacks from the DeskOS API for confirmed, rejected, and cancelled bookings. The backend shall verify and process each callback, update the corresponding booking record, and make the updated status available to the user. | DeskOS API / Booking Management | Sobia Adnan – g00100257 |

## Consolidation Notes

- The Lab 3 report numbers the last two requirements as FR-18 twice. They are numbered **FR-18** (account administration) and **FR-19** (DeskOS booking-status callbacks) here so every ID is unique.
- FR-04, FR-05, and FR-09 were revised so that external bookings and listings are handled only through the DeskOS API, consistent with the external-provider scope.
