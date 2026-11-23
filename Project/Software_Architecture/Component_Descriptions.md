# Exercise 3: Identify Components and Distribute Project Classes

## Component Description

| ID | Component | Layer | Responsibilities | Supported functionality (Lab 3) |
|---|---|---|---|---|
| CO1 | Web Presentation Component | Presentation | Displays the user interface for users and administrators, collects user input, shows results, errors, and confirmations returned by the application layer. | User-interface side of UC-01 – UC-15 |
| CO2 | Space Search Component | Application | Validates search criteria, lists campuses and inventory from DeskOS and filters spaces, validates returned spaces, checks facilities and availability per inventory item. | UC-01 Search for Spaces, UC-02 Filter Spaces, UC-03 View Space Details (FR-01, FR-02, FR-03) |
| CO3 | Booking Management Component | Application | Creates and cancels bookings through DeskOS (a change is a new booking plus a cancel of the original), applies booking statuses from DeskOS responses and callbacks, lets administrators view and cancel booking records. | UC-04 Make Booking, UC-05 Cancel Booking, UC-06 Change Booking, UC-12, UC-13 Manage Reservations (FR-04, FR-05, FR-06, FR-12, FR-13, FR-14) |
| CO4 | DeskOS Integration Component | Application | The only part that talks to the DeskOS API: obtains and renews OAuth tokens, sends discovery, availability, booking, and cancellation requests with idempotency keys, receives webhooks and verifies X-DeskOS-Signature, ignores duplicate callbacks, handles DeskOS errors. | UC-16, UC-17, UC-18 (NFR-16, NFR-19, NFR-20) |
| CO5 | Account & Notification Component | Application | Handles registration, login, profiles, and user administration, generates usage reports, manages availability-notification requests and notifications. | UC-07, UC-08, UC-09, UC-10, UC-11, UC-14, UC-15 (FR-07 – FR-11) |
| CO6 | Platform Data Component | Data | Stores the platform's records (users, bookings, notifications) and caches DeskOS data (spaces, campuses, operators, facilities, availability snapshots), and keeps them consistent. | Data side of all use cases (NFR-04) |


## Provided and Required Interfaces

Figure 8.1 shows the UML component diagram. Provided interfaces use lollipop notation and required interfaces use socket notation, the interface definitions with their operations are included in the diagram. Table 8.2 lists the provided and required interfaces of each component.

Component diagram: [Software_Architecture_Component_Diagram.pdf](Component_Diagram/Software_Architecture_Component_Diagram.pdf)

| **Component**              | **Provided Interfaces**                                        | **Required Interfaces**                                                    |
|----------------------------|----------------------------------------------------------------|----------------------------------------------------------------------------|
| CO1 Web Presentation       | None                                                           | ISpaceSearch, IBookingManagement, IAccountManagement, INotificationService |
| CO2 Space Search           | ISpaceSearch                                                   | IExternalSpaceInfo (CO4), ISpaceData (CO6), IAvailabilityData (CO6)        |
| CO3 Booking Management     | IBookingManagement, IBookingStatusUpdate                       | IExternalBooking (CO4), IBookingRecords (CO6), IAvailabilityData (CO6)     |
| CO4 DeskOS Integration     | IExternalSpaceInfo, IExternalBooking, ICallbackEndpoint        | IDeskOSService (external DeskOS), IBookingStatusUpdate (CO3)               |
| CO5 Account & Notification | IAccountManagement, INotificationService                       | IRecordStorage (CO6)                                                       |
| CO6 Platform Data          | ISpaceData, IAvailabilityData, IBookingRecords, IRecordStorage | None                                                                       |
| DeskOS (external system)   | IDeskOSService                                                 | ICallbackEndpoint (CO4)                                                    |

**Table 8.2** Provided and required interfaces
