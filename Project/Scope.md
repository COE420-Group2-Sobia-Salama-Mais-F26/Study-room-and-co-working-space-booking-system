# Project Scope

## 1.2. Target Users

The main users and beneficiaries of the system are:

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

## 1.3. In-Scope and Out-Scope Features

**In-Scope Features**

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

**Out-of-Scope Features**

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
