## Review and Validate the Activity Diagrams:

Each team must review its diagrams to ensure that they correctly represent the selected use cases. The review must address the following questions:

**Does each Activity Diagram correspond to one of the use cases selected in Lab 6?**

Yes, All three Activity Diagrams correspond to the same use cases selected in Lab 6:

- UC01 – Search for Spaces (Lab 3: UC-01).

- UC02 – Make Booking (Lab 3: UC-04).

- UC03 – Manage Platform Booking Records (Lab 3: UC-13).

Each diagram represents a different major function of the system and follows its corresponding use case.

**Is the workflow consistent with the relevant functional requirements and use case description?**

The workflows follow the expected system behavior:

- UC01 – Search for Spaces: The user enters search criteria, and the system validates them before sending a search request to the DeskOS API. The returned space information is validated, and the system checks the selected facilities and availability before displaying matching spaces.

- UC02 – Make Booking: The user selects a space and enters booking details. The system checks availability before creating a booking record and submitting the booking request to DeskOS. The booking status is updated according to the response and callback received.

- UC03 – Manage Platform Booking Records: The administrator views booking records, selects a booking, and reviews its details. If cancellation is requested, the system checks the booking status and sends the cancellation request to DeskOS. The booking is updated to cancelled only after receiving an authorized confirmation.

**Does the diagram contain a clearly identifiable initial node and final node?**

All three diagrams contain identifiable initial nodes and final nodes. The initial nodes indicate where each workflow begins, while the final nodes represent the completion of the relevant workflow or alternative outcome.

**Are the actions named clearly and arranged in a logical order?**

The actions are clearly named and arranged in a logical sequence. For example, search criteria are validated before searching, availability is checked before booking, and booking status is checked before cancellation.

**Are control-flow arrows used correctly?**

Yes. The arrows connect the activities in the correct sequence and show how the process moves between the user, system services, and external DeskOS API.

**Are decision branches labeled with meaningful guard conditions?**

Yes. Decision nodes represent important conditions, such as whether search criteria are valid, whether a space is available, and whether a booking request or cancellation is accepted.

**Do alternative paths lead to appropriate outcomes?**

Yes. The diagrams include alternative paths for invalid search criteria, unavailable spaces, rejected booking requests, and unsuccessful cancellation requests.

**Are merge nodes used appropriately when alternative paths rejoin?**

Yes. Merge nodes bring alternative paths back together.

**Are fork and join nodes used correctly when parallel activities exist?**

Yes. fork and join nodes represent activities that can happen in parallel, such as checking space facilities and availability in the search process.

**Are swimlanes used appropriately to distinguish responsibilities, where needed?**

Yes. Each activity is placed in the appropriate swimlane according to the responsible actor or system component, including User, PlatformAdmin, BookingService, SpaceSearchService, and DeskOSAPI.

**Are the modeled activities consistent with the system's intended behavior and the other project models?**

Yes. The diagrams represent the expected behaviour of the Study Room and Co-Working Space Booking System, including searching for spaces, making bookings, and managing booking records.

**Are there any missing activities, unnecessary steps, contradictory paths, or unreachable actions?**

No major missing, unnecessary, or contradictory activities were identified. The activities support the main purpose of each use case and follow the expected system workflow.

## Consistency with Previous Labs:

Teams must pay particular attention to the following relationships:

- **Lab 3 – Requirements and Use Case Modeling:** Each Activity Diagram must reflect the relevant functional requirements and the corresponding use case behavior.

The activity diagrams are consistent with the requirements and use cases developed in Lab 3.

- UC-01 Search for Spaces: Matches the search spaces use case (UC-01), where users enter search criteria and view matching available spaces.

- UC-02 Make Booking: Matches the make booking use case (UC-04), where users select a space, submit booking details, and receive a booking result.

- UC-03 Manage Platform Booking Records: Matches the manage reservations use case (UC-13), where the administrator views booking records, checks booking details, and handles cancellation requests.

All three diagrams follow the expected use-case flows and do not introduce unrelated functionality.

- **Lab 5 – Object Modeling and Class Diagrams:** Actions that correspond to system operations should be compatible with the responsibilities of the identified classes, where applicable.

The activity diagrams use the same main classes and system components identified in the Lab 5 class diagram.

- UC-01: Uses SpaceSearchService, SearchCriteria, Space, and Availability to handle search requests and retrieve matching spaces.

- UC-02: Uses BookingService, Booking, and Availability to check availability and create booking records.

- UC-03: Uses BookingService and Booking to retrieve booking records, view booking details, and update booking status.

- **Lab 6 – Sequence Diagram Modeling:** Each Activity Diagram must represent the same use case as its corresponding Sequence Diagram. The two diagrams should provide complementary views of the same behavior without contradicting one another.

The activity diagrams are consistent with the sequence diagrams developed in Lab 6. They represent the same interactions between the actors, system components, and external DeskOS API.

- The search process includes validating search criteria and retrieving space information from DeskOS API.

- The booking process includes checking availability, creating a booking request, and receiving the booking response.

- The booking management process includes retrieving booking records, viewing details, and processing cancellation requests through DeskOS API.

The same system components, responsibilities, and overall workflows are maintained across both diagram types.

The diagrams do not need to have identical structures. Activity Diagrams emphasize workflow and control flow, while Sequence Diagrams emphasize interactions and message exchanges.

Each team must confirm, **in writing within the report**, that all of the listed consistency checks have been performed and verified. **Any mismatch will result in point deductions from the grade of this lab.**
