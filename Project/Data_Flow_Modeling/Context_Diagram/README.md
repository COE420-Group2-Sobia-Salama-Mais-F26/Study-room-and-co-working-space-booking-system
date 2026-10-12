# Context Diagram

The Context Diagram shows the whole **Study Room and Co-working Space Booking System** as one process (Process 0). It exchanges data with three external entities: **User**, **Administrator**, and **Third-Party Space Provider**.

Editable diagram (Creately): https://app.creately.com/d/lNShtZgzeFY/edit

![Context Diagram](Context_Diagram.png)

## External Entities

| Entity | Corresponds to Use Case actor |
|---|---|
| User | User (student / booker) |
| Administrator | Administrator |
| Third-Party Space Provider | Not in the Lab 3 Use Case Diagram |

## Data Flows

| Direction | Data flow |
|---|---|
| User → System | Registration Information, Login Information, Profile Information, Search Criteria, Facility Filters, Space Details Request, Booking Request, Group Booking Information, Booking Modification Request, Booking Cancellation Request, Booking History Request, Availability Request |
| System → User | Registration Confirmation, Login Confirmation, Profile Information, Available Spaces, Space Details, Facility / Location / Availability Information, Booking Confirmation, Updated Booking Information, Cancellation Confirmation, Upcoming / Previous Booking Information, Booking Reminder, Booking Notification, Availability Notification |
| Administrator → System | User Management Request, Space Management Information, Availability Management Information, Reservation Management Request, Room Status Request, Report Request |
| System → Administrator | User Information, Space Information, Availability Information, Reservation Information, Room Status, Booking Reports, Usage Reports, Management Confirmation |
| Third-Party Space Provider → System | External Search Request |
| System → Third-Party Space Provider | External Space Information, External Availability Information |
