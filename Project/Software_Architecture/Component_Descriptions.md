# Exercise 3: Identify Components and Distribute Project Classes

## Component Description

| ID | Component | Layer | Responsibilities | Supported functionality (Lab 3) |
|---|---|---|---|---|
| CO1 | Web Presentation Component | Presentation | Displays the user interface for users and administrators; collects user input; shows results, errors and confirmations returned by the application layer. | User-interface side of UC-01 – UC-15 |
| CO2 | Space Search Component | Application | Validates search criteria; searches and filters spaces; requests space and availability data from DeskOS; validates returned spaces; checks facilities and availability. | UC-01 Search for Spaces, UC-02 Filter Spaces, UC-03 View Space Details (FR-01, FR-02, FR-03) |
| CO3 | Booking Management Component | Application | Creates, cancels and modifies bookings; submits booking requests to DeskOS; applies valid status callbacks (CONFIRMED / CANCELLED); updates availability; lets administrators view and cancel booking records. | UC-04 Make Booking, UC-05 Cancel Booking, UC-06 Modify Booking, UC-12, UC-13 Manage Reservations (FR-04, FR-05, FR-06, FR-12, FR-13, FR-14) |
| CO4 | DeskOS Integration Component | Application | Only point of communication with the external DeskOS API; sends search, availability, booking and cancellation requests; receives callbacks and verifies their signature; ignores invalid or duplicate callbacks; handles DeskOS being unavailable. | UC-16, UC-17, UC-18 (NFR-16, NFR-19, NFR-20) |
| CO5 | Account & Notification Component | Application | Handles registration, login, profiles and user administration; generates usage reports; manages availability-notification requests and notifications. | UC-07, UC-08, UC-09, UC-10, UC-11, UC-14, UC-15 (FR-07 – FR-11) |
| CO6 | Platform Data Component | Data | Stores and retrieves the platform’s records (users, bookings, spaces, locations, facilities, providers, availability) and keeps them consistent. | Data side of all use cases (NFR-04) |
