# Context Diagram

The Context Diagram shows the whole **Study Room and Co-working Space Booking System** as one process (Process 0). It exchanges data with three external entities: **User**, **Administrator**, and **Third-Party Space Provider**.

Editable diagram (Creately): https://app.creately.com/d/lNShtZgzeFY/edit

![Context Diagram](Context_Diagram.png)

## External Entities

| Entity | Corresponds to Use Case actor |
|---|---|
| User | User (student / booker) |
| Administrator | Administrator |
| Third-Party Space Provider / External API | Not in the Lab 3 Use Case Diagram |

## Data Flows

| Direction | Data flow (as labeled in the diagram) | Detailed flows at Level 0 |
|---|---|---|
| User → System | Account Information | Registration Information, Login Information, Profile Information, Booking History Request |
| User → System | Search Information | Search Criteria (space type, location, date, time, duration, capacity), Facility Filters, Space Details Request |
| User → System | Booking Information | Booking Request, Group Booking Information, Booking Modification Request, Booking Cancellation Request, Upcoming / Previous Booking Request |
| User → System | Availability Requests | Availability Request, Space Status Request |
| System → User | Account Information | Registration Confirmation, Login Confirmation, Profile Information, Booking History |
| System → User | Search Results | Available Spaces, Space Details, Facility Information, Location Information |
| System → User | Booking Information | Booking Confirmation, Updated Booking Information, Cancellation Confirmation, Upcoming / Previous Bookings, Booking Status |
| System → User | Availability Information | Current Space Availability, Space Status |
| System → User | Notifications | Availability Notification, Booking Reminder, Booking Notification |
| Administrator → System | User Management Request, Space Management Information, Availability Management Information, Reservation Management Request, Room Status Request, Report Request | Same flows into P5 |
| System → Administrator | User Information, Space Information, Reservation Information, Availability Information, Room Status, Booking Reports, Usage Reports, Management Confirmation | Same flows out of P5 |
| System → Third-Party Space Provider | External Search Request | From P2 |
| Third-Party Space Provider → System | External Space Information, External Availability Information | Into P2 |
