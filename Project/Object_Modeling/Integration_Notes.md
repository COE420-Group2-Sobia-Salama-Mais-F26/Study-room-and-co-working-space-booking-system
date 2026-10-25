# Integration Notes

This record lists the changes made when the three individual class models were merged into the [consolidated class diagram](Class_Diagram/README.md). Each entry compares an individual diagram with the final one.

## Duplicate Classes Resolved

| Class | Appeared in | Version kept in the consolidated diagram |
|---|---|---|
| User | Sobia, Salama | Sobia's version (adds `password`, `phoneNumber`, `register()`, `login()`, `updateProfile()`, `searchSpaces()`). Salama's getter-only version was merged into it. |
| Space | Sobia, Salama, Mais | Sobia's version (`spaceId`, `name`, `capacity`, `description`, `availabilityStatus`; `getSpaceDetails()`, `getCapacity()`, `isAvailable()`). Mais's `spaceName` was unified as `name`. |
| SearchCriteria | Sobia, Mais | Sobia's version, which includes `duration`, `selectedFacilities`, `matchesSpace()`, `addFacility()`, and `removeFacility()`. Mais's getter methods were dropped. |
| Booking | Salama, Mais | Salama's attributes and methods (`create()`, `cancel()`, `modify()`, `getStatus()`, `isActive()`). |
| Availability | Salama, Mais | Salama's version, including `getStartTime()` and `getEndTime()`. |

## Major Integration Decisions

1. **Foreign-key attributes replaced by associations.** `userId` and `spaceId` were removed from Booking, Availability, AvailabilityNotificationRequest, and Notification because the links are now shown as associations (for example, User *makes* Booking, Booking *reserves* Space, Space *has* Availability).
2. **External system marked explicitly.** DeskOSAPI carries the `«External System»` stereotype, and notes state that external booking, cancellation, and modification happen only when DeskOS supports and authorizes them.
3. **Administrator scope kept to the platform.** PlatformAdmin *manages* User, *oversees* Booking, and *monitors* Notification, and does not edit external listings, matching Lab 3 (S-04, UC-09).
4. **Services connected.** BookingService *uses* SpaceSearchService and DeskOSAPI and *manages* Booking. SpaceSearchService *uses* SearchCriteria, *searches* Space, and *requests data from* DeskOSAPI.
5. **External data flows modeled.** DeskOSAPI *returns* space information (Space), availability (Availability), and provider information (SpaceProvider); SpaceProvider *provides* Space.
6. **BookingService simplified.** The `bookingId` attribute was removed from BookingService, since booking IDs belong to Booking.
7. **Report class removed.** Sobia's `Report` class is not in the consolidated diagram, and `PlatformAdmin.generateUsageReport()` now returns `void` instead of `Report`.

## Open Items

- The lab asks for inheritance relationships, but no inheritance appears in the individual or consolidated diagrams. See the [consistency check](Class_Model_Consistency_Check.md).
- UC-14 (Generate Usage Reports) has no dedicated class after Report was removed.
