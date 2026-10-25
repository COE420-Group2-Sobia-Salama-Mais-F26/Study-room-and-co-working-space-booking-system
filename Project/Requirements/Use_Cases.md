# Exercise 4: Use Case Identification and Modeling

| UC ID | Use Case Name | Primary Actor | Short Description | Contributor |
|---|---|---|---|---|
| UC-01 | Search for Spaces | User | The user searches for study rooms, private rooms, desks, and co-working spaces based on location, date, time, duration, and capacity. | Sobia adnan- g00100257 |
| UC-02 | Filter Spaces | User | The user filters available spaces based on facilities such as Wi-Fi, power outlets, whiteboards, and projectors. | Sobia adnan- g00100257 |
| UC-03 | View Space Details | User | The user views the details, facilities, and location of a selected space. | Sobia adnan- g00100257 |
| UC-04 | Make Booking | User | The user reserves an available study room or co-working space. | Sobia adnan- g00100257 |
| UC-05 | Cancel Booking | User | The user cancels an existing booking and the system updates space availability. | Sobia adnan- g00100257 |
| UC-06 | Modify booking | User | The user changes the date, time, or room of an existing booking. | Salama alsuwaidi- g00099875 |
| UC-07 | Receive booking reminder | User | The system sends a reminder before the scheduled booking time. | Salama alsuwaidi- g00099875 |
| UC-08 | notify space availability | User | The system alerts users when a previously occupied space becomes available. | Salama alsuwaidi- g00099875 |
| UC-09 | Manage Platform<br>information | Adminstrator | The administrator manages platform users, access permissions, platform activity, reported issues, authorized booking records, and usage reports. The administrator does not directly modify the source listings or availability of external spaces provided through DeskOS. | Salama alsuwaidi- g00099875 |
| UC-10 | View profile and history | User | The user views and updates their profile and checks past bookings. | Salama alsuwaidi- g00099875 |
| UC-11 | Register Account | User | The user creates a new account by entering their name, email address, and password. | Mais Abudaqqa<br>g00099729 |
| UC-12 | View Upcoming and Previous Bookings | User | The student views their upcoming and previous bookings, including the space, date, time, and booking status. | Mais Abudaqqa<br>g00099729 |
| UC-13 | Manage Reservations | Administrator | The administrator views and manages booking records the platform is authorized to control. External reservation changes are performed only if supported and authorized through the DeskOS API. | Mais Abudaqqa<br>g00099729 |
| UC-14 | Generate Usage Reports | Administrator | The administrator generates reports using platform activity and available booking data, including external information only when returned by the supported integration. | Mais Abudaqqa<br>g00099729 |
| UC-15 | Manage Users | Administrator | The administrator views and manages registered user accounts when necessary, such as updating or disabling an account. | Mais Abudaqqa<br>g00099729 |
| UC-16 | Retrieve External Space Information | DeskOS | The system retrieves information about spaces offered by external space providers who have agreed to participate in the platform. It sends supported search criteria to the DeskOS API and receives matching space information. When available and authorized, the system also retrieves and displays the participating provider’s identity and relevant details, such as provider name and contact information | Sobia Adnan-g00102057 |
| UC-17 | Retrieve External Availability | Third-Party Space Provider / External API | The system retrieves availability information for spaces offered by participating external providers. It requests availability for the relevant date and time, processes the returned information, and displays the availability status alongside the space details and participating provider’s identity when available. | Sobia Adnan-g00102057 |
| UC-18 | Process Booking Status Callback<br>I | DeskOS API | DeskOS sends a callback when a booking reaches a final status, such as confirmed, rejected, or cancelled. The platform backend verifies the callback signature, identifies the corresponding booking, processes the status update without duplicating it, and updates the booking record so the latest status can be displayed to the user. | Sobia Adnan-g00102057 |

## Use Case Relationships

| Relationship ID | Base Use Case | Related Use Case | Relationship | Justification |
|---|---|---|---|---|
| R-01 | Make Booking | Search for Spaces | <<include>> | The user needs to search for available spaces as part of making a booking. |
| R-02 | Search for Spaces | Filter spaces | <<extend>> | Filtering is optional and extends the search functionality when the user wants to narrow the results. |
| R-03 | Modify Booking | View upcoming and previous bookings | <<include>> | The user must view their existing bookings before modifying one. |
| R-04 | Manage Platform Information | View space details | <<include>> | The admin needs to see room details before updating them. |
| R-05 | Search for spaces | Request Space-availability notification | <<extend>> | The system optionally alerts users when a searched space becomes available. |
| R-06 | Search for Spaces | Retrieve External Space Information | <<include>> | The system needs to retrieve matching external space information when searching for spaces provided through third-party providers. |
| R-07 | Search for Spaces | Retrieve External Availability | <<include>> | The system needs availability information to show users which externally provided spaces can be booked for the requested time. |
