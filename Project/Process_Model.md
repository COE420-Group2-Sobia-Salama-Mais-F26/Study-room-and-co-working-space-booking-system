**Exercise 1: Selection of a Software Process Model done by *sobia adnan g00100257***

Based on the characteristics of your proposed project, select the **most appropriate software process model**.

Your team should:

1.  Identify the selected software process model.

2.  Justify why this model is appropriate for your project.

3.  Identify the major overheads/drawbacks associated with the selected model, and explain how your team will manage or reduce these overheads/drawbacks.

ANS:

**1. Selected Software Process Model**

The **Incremental Model** has been selected as the most appropriate software process model for the proposed **Study Room and Co-Working Space Booking System**.

#### **Reason**

The proposed system contains several major feature categories that can be developed as separate increments:

1.  **User Management**

    - User registration and login

    - User profile

    - Booking history

2.  **Space Search and Selection**

    - Search for study rooms, meeting rooms, private rooms, desks, and co-working spaces

    - Search by location, date, time, duration, and capacity

    - Filter spaces based on facilities such as Wi-Fi, power outlets, whiteboards, and projectors

    - View space details and location

3.  **Third-Party Space Integration/ Providers**

    - Receive space information from external providers through external APIs

    - Receive available locations and space information

    - Process external availability information

    - Provide relevant space information to the platform based on user location criteria

4.  **Booking Management**

    - Make a booking

    - Modify a booking

    - Cancel a booking

    - Group booking

    - View upcoming and previous bookings

    - Booking confirmation

    - Support external booking operations only if the DeskOS API permits them

5.  **Real-Time Availability and Notifications**

    - View the availability status of spaces

    - Update availability when a space becomes free

    - Notify users when a previously occupied space becomes available

    - Send booking reminders and notifications

6.  **Administration**

    - Manage users and access.

    - Monitor platform activity and reported issues.

    - View authorized booking records.

    - Generate platform usage reports.

    - Manage platform settings and notification rules, if implemented.

The Incremental Model is appropriate because these features can be divided into separate increments and developed progressively. For example, the first increment can focus on User Management, followed by Space Search, Third-Party API Integration, Booking Management, Availability and Notifications, and finally Administration.

The DeskOS API integration will be developed as a separate increment after the basic space search functionality is established. The team will review the API documentation, verify access and supported functionality, and test integration before incorporating external space information into the platform

Each increment can be designed, implemented, tested, and delivered before the next increment is developed. The completed functionality remains part of the final system while each new increment adds additional functionality. This allows the team to develop the platform piece by piece while obtaining a working system at an earlier stage.

### **3. Major Overheads/Drawbacks and How We Will Manage Them**

**Integration:  
** The DeskOS API may provide information in a format that differs from the platform's internal data format. New increments may also cause integration problems with existing features. The team will test API integration with the existing system and ensure that external space information is correctly processed before displaying it to users.

**Planning:  
** Deciding which features should be developed in each increment can be difficult. The team will prioritize the core features and develop them in a logical order, starting with user management and search before implementing booking and external API integration.

**Testing:  
**Each increment needs to be tested, including the communication between the platform and DeskOS APIs. This increases the testing effort. The team will test each increment before moving to the next one and verify that external data is handled correctly. The team will test the DeskOS API integration, validate returned space information, and verify that API failures do not cause the platform to crash.

**Management:  
**Managing multiple increments and coordinating with external API requirements can require additional coordination between team members. The team will assign clear responsibilities, maintain a development schedule, and document the API requirements.

Overall, these drawbacks can be managed through proper planning, regular testing, clear coordination, and careful integration of the third-party services.
