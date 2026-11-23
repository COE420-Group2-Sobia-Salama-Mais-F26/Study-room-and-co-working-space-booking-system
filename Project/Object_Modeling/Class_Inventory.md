# 6. Object Model

Figure 6.1 shows the final consolidated UML class diagram of the whole
system. It combines the individual class models into one diagram with 14
classes, their attributes, methods, and relationships. Table 6.1
summarizes the responsibility of each class.

Class diagram: [Consolidated_Class_Diagram.png](Class_Diagram/Consolidated_Class_Diagram.png)

| **ID** | **Class**                       | **Responsibility**                                                                                                                                                                                                 |
|--------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C01    | User                            | Represents a person using the platform, including their account details and profile. A user can search for spaces, make bookings, and receive notifications.                                                       |
| C02    | PlatformAdmin                   | Represents a website administrator who manages platform accounts, reservations, and platform activity. It does not manage external providers' source listings or availability.                                     |
| C03    | Space                           | Represents a bookable DeskOS space or desk day pass. Stores information such as the DeskOS ID, campus name, and description.                                                                                       |
| C04    | Location                        | Represents where a DeskOS campus is located, including the campus ID, city, and address used when searching for and viewing spaces.                                                                                |
| C05    | Facility                        | Represents a facility offered by a space, such as Wi-Fi, power outlets, whiteboards, or projectors. Supports facility-based filtering and viewing space details.                                                   |
| C06    | SearchCriteria                  | Stores the criteria entered by a user, including location, date, time, duration, capacity, and selected facilities.                                                                                                |
| C07    | Booking                         | Represents a booking. Stores the user, space, date, times, the booking reference sent to DeskOS, and the status (confirmed, pending_approval, rejected, cancelled, or failed). DeskOS callbacks update the status. |
| C08    | Availability                    | Represents availability information for a space and time slot, based on information returned by DeskOS. The platform cannot change external availability.                                                          |
| C09    | AvailabilityNotificationRequest | Records a user's request to be notified when a particular space and time slot become available. The platform regularly re-checks DeskOS to see if the slot is free.                                                |
| C10    | Notification                    | Represents a notification sent to a user, such as an upcoming booking reminder or an alert that a requested space has become available.                                                                            |
| C11    | SpaceProvider                   | Represents a DeskOS operator whose spaces are shown on the platform. Allows the platform to display the operator's identity alongside its spaces.                                                                  |
| C12    | SpaceSearchService              | Coordinates space searches and filtering using the user's criteria and the space information returned by the DeskOS API.                                                                                           |
| C13    | BookingService                  | Coordinates booking creation and cancellation and processes booking-status callbacks to update the corresponding booking record safely.                                                                            |
| C14    | DeskOSAPI                       | Handles communication between the platform and the DeskOS API: retrieving space information and availability, creating and cancelling bookings, and receiving booking-status callbacks.                            |

**Table 6.1** Classes in the object model
