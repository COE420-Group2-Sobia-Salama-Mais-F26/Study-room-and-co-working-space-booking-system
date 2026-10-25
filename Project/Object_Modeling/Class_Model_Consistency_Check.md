# Class Model Consistency Check

## Use Cases and Classes

| Use Cases | Classes |
|---|---|
| UC-01, UC-02, UC-03 (search, filter, view details) | User, SearchCriteria, SpaceSearchService, Space, Location, Facility |
| UC-04, UC-05, UC-06 (make, cancel, modify booking) | Booking, BookingService, Space, Availability |
| UC-07, UC-08 (reminder, availability notification) | Notification, AvailabilityNotificationRequest |
| UC-09, UC-13, UC-14, UC-15 (administration) | PlatformAdmin |
| UC-10, UC-11, UC-12 (profile, register, view bookings) | User, Booking |
| UC-16, UC-17, UC-18 (DeskOS integration) | DeskOSAPI, SpaceProvider, SpaceSearchService, BookingService |

## Data Stores and Classes

| Data Store | Classes |
|---|---|
| D1 User Data | User, PlatformAdmin |
| D2 Space Data | Space, Location, Facility, Availability |
| D3 Booking Data | Booking |
| D4 Notification Data | Notification, AvailabilityNotificationRequest |

## Checklist

| Check | Done |
|---|---|
| All approved classes are in the team diagram | Yes |
| Attributes and methods have visibility and data types | Yes |
| Associations have names and multiplicities | Yes |
| Classes match the use cases | Yes |
| Classes match the DFD data stores | Yes |
