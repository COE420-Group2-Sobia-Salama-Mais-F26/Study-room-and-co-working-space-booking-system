## Exercise 2: Define the Project Scope done by *Mais Abudaqqa g00099729*

Define the initial scope of your software project.

Your project scope should include:

1.  **Project Objective**

**The main objectives of the project are to:**

1.  Provide one web-based platform where students, professionals,
    freelancers, remote workers, and other individuals can find and
    reserve suitable spaces for studying, working, meetings, or
    collaboration.

2.  Allow users to search for spaces based on location, date, time,
    duration, capacity, and available facilities.

3.  Allow users to make, view, change, and cancel bookings, and to
    receive booking reminders and availability notifications.

4.  Get spaces and their availability from DeskOS operators through the
    DeskOS API, so users can search external spaces in one place.

5.  Allow the website administrator to manage platform users, access
    permissions, platform activity, authorized booking records,
    reported issues, and usage reports.

The platform manages its own user accounts, access permissions, booking records, and notifications. It does not create or edit the operators' space listings or availability, and the administrator does not manage the physical facilities, source listings, or source availability of external providers.

2.  **Target Users**

Identify the main users or beneficiaries of the proposed system.

**ANS:**

- **Students:** users who need quiet spaces for individual or group
  study.

- **Freelancers and remote workers:** users who need suitable
  workspaces, meeting spaces, or desks.

- **Professionals and other individuals:** users who need spaces for
  meetings, work, collaboration, or other activities.

- **Platform administrators:** personnel responsible for managing user
  accounts, access permissions, platform activity, authorized booking
  records, reported issues, platform settings, and usage reports.

- **Third-party space providers:** coworking companies that join DeskOS.
  They choose which campuses to share and approve bookings in their
  own DeskOS dashboard. They do not use the platform directly.

3.  **In-Scope Features**

List the major features and functionalities that will be included in the project.

**ANS:**

Table 1.1 lists the major features and functionalities included in the
project.

| **Feature Area**                        | **Included Functionality**                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| User Management                         | User registration and login, user profile, viewing booking history.                                                                                                                                                                                                                                                                                                                               |
| Space Search and Selection              | Search for meeting rooms and desks (day passes) by location, date, time, duration, and capacity, filter spaces by facilities such as Wi-Fi, power outlets, whiteboards, and projectors, view space details, facilities, and location.                                                                                                                                                             |
| Third-Party Space Integration           | Connect the platform backend to the DeskOS API using a client ID and secret, retrieve and process external space information, retrieve and display availability, validate returned information before displaying it, handle API errors, unavailable responses, and incomplete data.                                                                                                               |
| Platform Booking and Booking Management | View booking records, create, change, or cancel bookings, make and cancel DeskOS bookings through the API, where a change is done by booking the new time and cancelling the old booking, show the booking status returned by DeskOS (confirmed, pending, rejected, or cancelled), check for overlapping bookings.                                                                                |
| Availability and Notifications          | Display external space availability returned by the DeskOS API, send booking reminders, notify users when a booked-out space becomes free by checking DeskOS regularly, avoid presenting external availability as confirmed when the API has not supplied it.                                                                                                                                     |
| Administration                          | View and manage user accounts, activate or deactivate accounts and manage access permissions, monitor platform activity, reported problems, and API integration errors, view and manage authorized booking records, generate usage and booking reports, manage platform settings and notification rules, manage only platform-owned data, not the listings or availability of external providers. |

**Table 1.1** In-scope features

4.  **Out-of-Scope Features**

> Identify features or functionalities that will **not** be included in the current version of the project.
>
> **ANS:**

- Online payment processing or integration with payment gateways.

- Real-time IoT integration, such as detecting whether a room is
  physically occupied using sensors.

- Smart access control, such as unlocking doors using QR codes, NFC, or
  biometric authentication.

- Food and beverage ordering.

- Advanced AI-based recommendations for selecting the best workspace.

- Integration with external calendar applications such as Google
  Calendar or Microsoft Outlook.

- Video conferencing within the booking system.

- Native mobile applications for Android and iOS, the initial version
  focuses on a web-based system.

- Managing or controlling the physical facilities, rooms, or operations
  of third-party providers, or directly owning or operating their
  workspace locations.

- Directly creating, editing, deleting, or maintaining external
  providers' space listings, availability, or inventory in DeskOS.

- Developing a separate provider-management system that duplicates the
  functions already supplied by DeskOS.

- Implementing unsupported DeskOS API operations or assuming access to
  data that the API does not provide.

- Booking changes inside DeskOS (the API has no change option, the
  platform cancels and books again).

- Operator settings (joining DeskOS, shared campuses, approval mode, and
  commission), which operators set in their DeskOS dashboard.

- Booking virtual offices, which the API only lists.

5.  **Major Deliverables**

> Identify the main expected deliverables of the project, such as software components, documentation, prototypes, or other project artifacts.
>
> ANS:

- Requirements Specification describing system requirements and user needs.

- System Design including use case diagrams, class diagrams, database design, and system architecture.

- User Interface Prototype showing the main screens and user interactions.

- DeskOS API integration component for retrieving, validating, and processing supported external space information and availability.

- Platform booking and booking record management functionality for operations the system is authorized to handle.

- Platform administration functionality for user access, activity monitoring, authorized booking records, issue handling, and usage reports.

- Testing documentation covering API responses, error handling, data validation, and the supported platform booking workflows.

- A web-based space search and booking platform.

- Search and filtering functionality.

- DeskOS API integration for supported external space information and availability.

- Display of participating provider identity and relevant information when available.

- Platform booking records and authorized booking functions.

- User notifications and platform administration features.

- API error handling, testing, and project documentation.
