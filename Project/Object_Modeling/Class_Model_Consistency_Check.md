# Class Model Consistency and Traceability Check

## Use Cases → Classes

| Use Case | Supporting classes |
|---|---|
| UC-01 Search for Spaces | User, SearchCriteria, SpaceSearchService, Space, Location, DeskOSAPI |
| UC-02 Filter Spaces | SearchCriteria, Facility, SpaceSearchService |
| UC-03 View Space Details | Space, Location, Facility |
| UC-04 Make Booking | User, Booking, BookingService, Space, Availability |
| UC-05 Cancel Booking | Booking, BookingService, DeskOSAPI |
| UC-06 Modify Booking | Booking, BookingService, Availability |
| UC-07 Receive Booking Reminder | Notification, Booking, User |
| UC-08 Request Space-Availability Notification | AvailabilityNotificationRequest, Notification, Space |
| UC-09 Manage Platform Information | PlatformAdmin |
| UC-10 View Profile and History | User, Booking |
| UC-11 Register Account | User |
| UC-12 View Upcoming and Previous Bookings | User, Booking |
| UC-13 Manage Reservations | PlatformAdmin, Booking, BookingService |
| UC-14 Generate Usage Reports | PlatformAdmin (`generateUsageReport()`) |
| UC-15 Manage Users | PlatformAdmin, User |
| UC-16 Retrieve External Space Information | SpaceSearchService, DeskOSAPI, SpaceProvider, Space |
| UC-17 Retrieve External Availability | DeskOSAPI, Availability, SpaceProvider |
| UC-18 Process Booking Status Callback | BookingService, DeskOSAPI, Booking |

Every use case from Lab 3 is supported by at least one class.

## DFD Data Stores → Classes

| Data store (Level-0 DFD) | Classes |
|---|---|
| D1 User Data | User, PlatformAdmin |
| D2 Space Data | Space, Location, Facility, Availability, SpaceProvider |
| D3 Booking Data | Booking |
| D4 Notification Data | Notification, AvailabilityNotificationRequest |

## DFD Processes → Classes

| Level-0 process | Classes |
|---|---|
| P1 User Management | User |
| P2 Space Search and Selection | SpaceSearchService, SearchCriteria, Space, Location, Facility, DeskOSAPI, SpaceProvider |
| P3 Booking Management | BookingService, Booking |
| P4 Availability and Notification Management | Availability, AvailabilityNotificationRequest, Notification |
| P5 Administration | PlatformAdmin |

## Checklist

| Check | Status |
|---|---|
| Consolidated diagram includes the approved classes from the individual models | ✅ (14 classes; Report removed, see [Integration Notes](Integration_Notes.md)) |
| Attributes and methods shown with visibility | ✅ |
| Data types, parameters, and return types shown | ✅ |
| Associations named | ✅ |
| Multiplicities on every association | ✅ |
| Helpful UML notes included | ✅ |
| Consistent with the Lab 3 actors (User, Administrator, DeskOS / External API) | ✅ |
| Consistent with the Lab 4 DFD data stores and processes | ✅ |
| Inheritance relationships included where a real generalization exists | ⚠️ None shown. User and PlatformAdmin share `name` and `email`, which could be generalized into an abstract `Account` class. |
