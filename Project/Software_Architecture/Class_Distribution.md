# Exercise 3: Identify Components and Distribute Project Classes

## Class Distribution

| ID | Component Name | Layer | Responsibilities | Included Classes |
|---|---|---|---|---|
| CO1 | Web Presentation Component | Presentation | Displays the user interface for users and administrators, collects user input, shows results, errors, and confirmations returned by the application layer. | None (UI pages only; Lab 5 has no UI classes) |
| CO2 | Space Search Component | Application | Validates search criteria, lists campuses and inventory from DeskOS and filters spaces, validates returned spaces, checks facilities and availability per inventory item. | SpaceSearchService, SearchCriteria |
| CO3 | Booking Management Component | Application | Creates and cancels bookings through DeskOS (a change is a new booking plus a cancel of the original), applies booking statuses from DeskOS responses and callbacks, lets administrators view and cancel booking records. | BookingService |
| CO4 | DeskOS Integration Component | Application | The only part that talks to the DeskOS API: obtains and renews OAuth tokens, sends discovery, availability, booking, and cancellation requests with idempotency keys, receives webhooks and verifies X-DeskOS-Signature, ignores duplicate callbacks, handles DeskOS errors. | DeskOSAPI |
| CO5 | Account & Notification Component | Application | Handles registration, login, profiles, and user administration, generates usage reports, manages availability-notification requests and notifications. | User, PlatformAdmin, AvailabilityNotificationRequest, Notification |
| CO6 | Platform Data Component | Data | Stores the platform's records (users, bookings, notifications) and caches DeskOS data (spaces, campuses, operators, facilities, availability snapshots), and keeps them consistent. | Space, Location, Facility, SpaceProvider, Booking, Availability |

**Table 8.1** Components and their assigned classes
