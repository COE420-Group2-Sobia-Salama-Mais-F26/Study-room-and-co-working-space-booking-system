# Class Inventory

Classes identified for the Study Room and Co-working Space Booking System, with the use cases each one supports and the member who identified it.

| Class ID | Class Name | Purpose / Responsibility | Related Use Case(s) | Contributor |
|---|---|---|---|---|
| C01 | User | Represents a person using the platform, including their account details and profile. A user can search for spaces, make bookings, and receive notifications. | UC-01, UC-02, UC-03, UC-04, UC-05, UC-06, UC-07, UC-08, UC-10, UC-11, UC-12 | Sobia Adnan – g00100257 |
| C02 | PlatformAdmin | Represents a website administrator who manages platform accounts, reservations, and platform activity. This class does not represent the owner of every listed physical meeting space and does not directly manage external providers' source listings or availability. | UC-09, UC-13, UC-14, UC-15 | Sobia Adnan – g00100257 |
| C03 | Space | Represents a bookable study room, meeting room, private room, desk, or co-working space. Stores information such as its name, capacity, and description. | UC-01, UC-02, UC-03, UC-04, UC-16, UC-17 | Sobia Adnan – g00100257 |
| C04 | Location | Represents where a space is located, including location details used when searching for and viewing spaces. | UC-01, UC-03, UC-16 | Sobia Adnan – g00100257 |
| C05 | Facility | Represents a facility offered by different spaces, such as Wi-Fi, power outlets, whiteboards, or projectors. Supports facility-based filtering and viewing space details. | UC-02, UC-03 | Sobia Adnan – g00100257 |
| C06 | SearchCriteria | Stores the criteria entered by a user, including location, date, time, duration, capacity, and selected facilities. These criteria are used to find matching spaces through the platform and supported DeskOS API operations. | UC-01, UC-02, UC-16, UC-17 | Sobia Adnan – g00100257 |
| C07 | Booking | Represents a booking record available to the platform. Stores the user, selected space, date, start and end times, and booking status. Its status can be updated when a valid booking-status callback is received from DeskOS. | UC-04, UC-05, UC-06, UC-07, UC-10, UC-12, UC-13 | Salama Alsuwaidi – g00099875 |
| C08 | Availability | Represents availability information for a space and time slot. The platform uses information returned by DeskOS, when available, to display availability. It must not assume it can directly change external availability. | UC-01, UC-04, UC-05, UC-06, UC-08, UC-17 | Salama Alsuwaidi – g00099875 |
| C09 | AvailabilityNotificationRequest | Records a user's request to receive a notification if a particular space and time slot become available. It stores the requested space, time slot, requesting user, and request status. Notifications depend on availability updates accessible to the platform. | UC-08 | Salama Alsuwaidi – g00099875 |
| C10 | Notification | Represents a notification sent to a user, such as an upcoming booking reminder or an alert that a requested space has become available. | UC-07, UC-08 | Salama Alsuwaidi – g00099875 |
| C11 | SpaceProvider | Represents external space providers who have agreed to work with the platform. Stores their identifying details, such as provider name, contact information, and provider ID, when available. Allows the platform to display the identity and relevant details of participating providers alongside their space information retrieved through the DeskOS API. | UC-16, UC-17 | Mais Abudaqqa – g00099729 |
| C12 | SpaceSearchService | Coordinates space searches and filtering using the user's criteria and the space information returned by providers through the DeskOS API. | UC-01, UC-02, UC-16, UC-17 | Mais Abudaqqa – g00099729 |
| C13 | BookingService | Coordinates booking creation, cancellation, and modification for operations the platform is authorized to manage, and processes booking-status callbacks to update the corresponding booking record safely. | UC-04, UC-05, UC-06, UC-13, UC-18 | Mais Abudaqqa – g00099729 |
| C14 | DeskOSAPI | Represents the external API that provides space information and availability from the external space providers. It handles communication between the booking platform and the external space providers, including sending search criteria and returning booking-status callbacks to the platform when supported booking operations reach a final state. | UC-01, UC-16, UC-17, UC-18 | Mais Abudaqqa – g00099729 |

## Classes per Member

| Member | Classes identified | Individual diagram |
|---|---|---|
| Sobia Adnan – g00100257 | C01–C06 (User, PlatformAdmin, Space, Location, Facility, SearchCriteria) | [Sobia_Adnan_Class_Diagram.png](Individual_Models/Sobia_Adnan_Class_Diagram.png) |
| Salama Alsuwaidi – g00099875 | C07–C10 (Booking, Availability, AvailabilityNotificationRequest, Notification) | [Salama_Alsuwaidi_Class_Diagram.png](Individual_Models/Salama_Alsuwaidi_Class_Diagram.png) |
| Mais Abudaqqa – g00099729 | C11–C14 (SpaceProvider, SpaceSearchService, BookingService, DeskOSAPI) | [Mais_Abudaqqa_Class_Diagram.png](Individual_Models/Mais_Abudaqqa_Class_Diagram.png) |
