## Exercise 2: Define the Project Scope done by *Mais Abudaqqa g00099729*

Define the initial scope of your software project.

Your project scope should include:

1.  **Project Objective**

Existing UAE workspace booking systems are often limited to specific institutions or particular types of users. The proposed Study Room and Co-Working Space Booking System aims to provide a unified web-based platform where students, professionals, freelancers, remote workers, and other individuals can find and reserve suitable spaces for studying, working, meetings, or collaboration.

The system will allow users to search for spaces based on location, date, time, duration, capacity, and available facilities. Users will be able to make, view, modify, and cancel bookings.

The platform will integrate with the DeskOS API to retrieve and display space information and availability when supported by the API and available access permissions. This will allow users to search for relevant external spaces through one platform. The platform will not independently create or maintain the source listings or availability of external spaces.

The platform will manage its own user accounts, access permissions, and the booking records and notifications it is authorized to handle. External booking, modification, and cancellation operations will be supported only if the DeskOS API provides the required functionality and access.

The website administrator will manage platform users, access permissions, platform activity, authorized booking records, reported issues, and usage reports. The administrator will not manage the physical facilities, source listings, or source availability of external providers.

2.  **Target Users**

Identify the main users or beneficiaries of the proposed system.

**ANS:**

- **Students:** Users who need quiet spaces for individual or group study.

- **Freelancers and remote workers:** Users who need suitable workspaces, meeting spaces, or desks.

- **Professionals and other individuals:** Users who need spaces for meetings, work, collaboration, or other activities.

- **Platform administrators:** Personnel responsible for managing user accounts, access permissions, platform activity, authorized booking records, reported issues, platform settings, and usage reports.

- **Third-party space providers:** External parties responsible for the space information and provider-side operations made available through the DeskOS platform and API. Their exact responsibilities and supported operations depend on the integration arrangement.

3.  **In-Scope Features**

List the major features and functionalities that will be included in the project.

**ANS:**

#### **1. User Management**

- User registration and login

- User profile

- View booking history

#### **2. Space Search and Selection**

- Search for study rooms, meeting rooms, private rooms, desks, and co-working spaces

- Search by location, date, time, duration, and capacity

- Filter spaces based on facilities such as Wi-Fi, power outlets, whiteboards, and projectors

- View space details, facilities, and location

#### **3. Third-Party Space Integration**

- Connect the platform backend to the DeskOS API, subject to access and authentication requirements.

- Send user search criteria to supported API endpoints.

- Retrieve and process external space information returned by the API.

- Retrieve and display availability information when supported by the API.

- Validate returned information before displaying it.

- Handle API errors, unavailable responses, and incomplete data.

- Support external booking operations only if the API provides the required functionality and access.

#### **4. Platform Booking and Booking Management**

- Allow users to view booking records available to the platform.

- Allow users to create, modify, or cancel bookings that the platform is authorized to manage.

- Display booking confirmations and status information when available.

- Check for overlapping bookings within the booking records the platform controls.

- Support booking, modification, and cancellation of DeskOS-listed spaces only if the API explicitly supports these operations and the platform has permission to use them.

#### **5. Availability and Notifications**

- Display external space availability based on information returned by the DeskOS API.

- Display the time and availability information supplied by the API, where available.

- Send booking reminders for bookings whose details and status are available to the platform.

- Notify users about changes in external space availability only when the required updates or availability information are provided to the platform.

- Avoid presenting external availability as confirmed when the API has not supplied the necessary information.

#### **6. Administration**

- View and manage user accounts.

- Activate or deactivate accounts and manage platform access permissions.

- Monitor platform activity and review reported problems.

- View and manage booking records that the platform is authorized to control.

- Generate reports using available platform usage and booking data.

- Manage platform settings and notification rules, if implemented.

- Monitor API integration errors and the status of requests made by the platform.

- Manage only platform-owned data and authorized records, not the source listings or availability of external providers.

4.  **Out-of-Scope Features**

> Identify features or functionalities that will **not** be included in the current version of the project.
>
> **ANS:**

- Online payment processing or integration with payment gateways.

- Real-time IoT integration, such as detecting whether a room is physically occupied using sensors.

- Smart access control, such as unlocking doors using QR codes, NFC, or biometric authentication.

- Food and beverage ordering.

- Advanced AI-based recommendations for selecting the best workspace.

- Integration with external calendar applications such as Google Calendar or Microsoft Outlook.

- Video conferencing within the booking system.

- Native mobile applications for Android and iOS; the initial version will focus on a web-based system.

- Managing or controlling the physical facilities of third-party providers.

- Direct ownership or operation of third-party workspace locations.

- Direct creation, editing, deletion, or maintenance of external providers' source space listings in DeskOS.

- Direct management or modification of external providers' source availability and inventory.

- Direct management of external providers' physical rooms, facilities, or operations.

- Developing a separate provider-management system that duplicates the provider or inventory management functions already supplied by DeskOS.

- Implementing unsupported DeskOS API operations or assuming access to data that the API does not provide.

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
