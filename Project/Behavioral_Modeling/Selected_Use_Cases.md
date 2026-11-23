# Exercise 1: Select Three Major Use Cases

| Use Case ID | Use Case Name | Primary Actor | Purpose | Reason for Selection |
|---|---|---|---|---|
| UC01 | Search for Spaces | User | Find meeting rooms or day-pass desks that match the user's criteria. | This is a core system function and demonstrates interactions between the User, SpaceSearch, Space, Location, Facility, and the external DeskOS API. It is suitable for modeling how search criteria are submitted, external results are processed, and matching spaces are displayed. |
| UC02 | Make Booking | User | Reserve an available meeting room or day-pass desk for a selected date and time. | Booking is a major system function that involves interactions among the User, Space, Availability, Booking, and BookingService classes. The sequence diagram can demonstrate request validation, availability checking, communication with the external system when supported, and the handling of the booking result. |
| UC03 | Manage Platform Booking Records | Administrator | Review the booking records the platform is authorized to control and cancel a booking when needed. | This use case demonstrates administrative functionality and interactions among the PlatformAdmin, Booking, BookingService, and relevant external integration components. It also shows the distinction between managing platform booking records and directly controlling external providers' bookings or source availability. |


## Use Case Descriptions

The three major use cases below are the same ones modeled in the
sequence and activity diagrams: Search for Spaces (UC-01), Make Booking
(UC-04), and Manage Reservations (UC-13).

| **Field** | **Description** |
|---|---|
| Use Case | UC-01 Search for Spaces |
| Primary Actor | User |
| Secondary Actor | DeskOS |
| Goal | Find meeting rooms or day-pass desks that match the user's criteria. |
| Precondition | The user has opened the platform's search page. |
| Main Flow | 1. The user enters the search criteria: city, date, time, duration, and number of seats.<br>2. The system validates the search criteria.<br>3. The system requests the campuses in the city and the inventory (availability) of each campus from the DeskOS API (includes UC-16 Retrieve External Space Information).<br>4. The system validates the returned space information.<br>5. For each space, the system checks the selected facilities and the availability for the requested time (includes UC-17 Retrieve External Availability).<br>6. The system displays the matching spaces with their details, availability, and the operator's name and campus. |
| Alternative Flows | Invalid criteria: the system shows an error message and the user corrects the criteria.<br>DeskOS API unavailable or data incomplete: the system shows an error message without crashing.<br>No matching spaces: the system informs the user that no results were found. |
| Extensions | The user may filter the results (UC-02 Filter Spaces) or request an availability notification (UC-08). |
| Postcondition | A list of matching spaces is displayed to the user. |
| Related Requirements | FR-01, FR-02, FR-03, FR-16, FR-17, NFR-01, NFR-16, NFR-17, NFR-18 |

**Table 4.3** Use case description – UC-01 Search for Spaces

| **Field** | **Description** |
|---|---|
| Use Case | UC-04 Make Booking |
| Primary Actor | User |
| Secondary Actor | DeskOS |
| Goal | Reserve an available meeting room or day-pass desk for a selected date and time. |
| Precondition | The user is logged in and has found a space through Search for Spaces (UC-01, included). |
| Main Flow | 1. The user selects a space and enters the booking details: date, time, duration, and number of people.<br>2. The system checks that the space is available.<br>3. The system creates a booking record with a platform-generated external_ref and idempotency key and submits the booking request to the DeskOS API.<br>4. DeskOS returns the booking status: confirmed, or pending_approval when the operator approves bookings manually.<br>5. The system displays the booking confirmation or pending status, and the booking appears in the user's upcoming bookings.<br>6. For a pending booking, DeskOS later sends a booking-status callback, the system verifies its signature and updates the booking record (UC-18). |
| Alternative Flows | Space unavailable: the system informs the user, who may request an availability notification.<br>Booking rejected by DeskOS (for example, the slot is taken): the booking status is set to rejected and the user is informed.<br>No response from DeskOS: the system retries with the same idempotency key, then shows an error message without crashing. |
| Postcondition | The booking is stored with its latest status (confirmed, pending, or rejected). |
| Related Requirements | FR-04, FR-12, FR-19, NFR-02, NFR-15, NFR-19, NFR-20, NFR-21 |

**Table 4.4** Use case description – UC-04 Make Booking

| **Field** | **Description** |
|---|---|
| Use Case | UC-13 Manage Reservations (Manage Platform Booking Records) |
| Primary Actor | Administrator |
| Secondary Actor | DeskOS |
| Goal | Review the booking records the platform is authorized to control and cancel a booking when needed. |
| Precondition | The administrator is logged in with administrator permissions. |
| Main Flow | 1. The administrator opens the booking records.<br>2. The system retrieves the booking records the platform is authorized to control using GET /bookings/{external_ref}, GET /bookings.<br>3. The administrator selects a booking and views its details.<br>4. If a cancellation is needed, the administrator requests it and the system checks that the booking status is confirmed or pending_approval.<br>5. The system sends the cancellation request to the DeskOS API.<br>6. DeskOS returns the cancelled status, the system updates the booking status to cancelled and displays a confirmation. |
| Alternative Flows | Booking already closed (cancelled or rejected): the system shows a message and no cancellation is made.<br>Cancellation fails (DeskOS error or no response): the booking status stays unchanged and the administrator is informed. |
| Postcondition | Booking records show the latest status. Bookings cannot be modified, and the administrator does not change the operators' listings or availability. |
| Related Requirements | FR-14, FR-19, NFR-14 |

**Table 4.5** Use case description – UC-13 Manage Reservations


## Dynamic Model

The dynamic models cover the three major use cases: UC-01 Search for Spaces, UC-04 Make Booking, and UC-13 Manage Reservations (Manage Platform Booking Records). Each use case has a UML sequence diagram, which shows the messages exchanged between actors and objects, and a UML activity diagram, which shows the workflow and decision points.

- Figure 7.1 shows how the search criteria are validated and how campuses, spaces, and availability are retrieved from DeskOS before the matching spaces are displayed. ([Sequence_Diagrams/UC01_Search_for_Spaces.png](Sequence_Diagrams/UC01_Search_for_Spaces.png))
- Figure 7.2 shows how availability is checked, how the booking is submitted to DeskOS, and how the booking status is updated. ([Sequence_Diagrams/UC02_Make_Booking.png](Sequence_Diagrams/UC02_Make_Booking.png))
- Figure 7.3 shows how the administrator retrieves booking records, views booking details, and cancels a booking through DeskOS. ([Sequence_Diagrams/UC03_Manage_Platform_Booking_Records.png](Sequence_Diagrams/UC03_Manage_Platform_Booking_Records.png))

The activity diagrams use swimlanes for the User, PlatformAdmin, SpaceSearchService, BookingService, and DeskOSAPI, and show the decision points, guard conditions, and parallel steps of each use case.

- Figure 7.4 Activity diagram for UC-01 Search for Spaces: [AD_UC01_Search_for_Spaces.pdf](Activity_Diagrams/AD_UC01_Search_for_Spaces.pdf)
- Figure 7.5 Activity diagram for UC-04 Make Booking: [AD_UC02_Make_Booking.pdf](Activity_Diagrams/AD_UC02_Make_Booking.pdf)
- Figure 7.6 Activity diagram for UC-13 Manage Reservations: [AD_UC03_Manage_Platform_Booking_Records.pdf](Activity_Diagrams/AD_UC03_Manage_Platform_Booking_Records.pdf)
