# 2.1. Process Model

The team selected the **Incremental Model**. The system contains several
major feature categories, and each can be designed, implemented, tested,
and delivered as a separate increment before the next one is developed.
The increments are developed in this order:

1.  **User Management**

    - User registration and login

    - User profile

    - Booking history

2.  **Space Search and Selection**

    - Search for meeting rooms and day-pass desks (co-working seats),
      view virtual offices as listing-only

    - Search by location, date, time, duration, and capacity

    - Filter meeting rooms by the amenities the operator lists (for
      example whiteboard, TV, video conferencing)

    - View space details and location

3.  **Third-Party Space Integration/ Providers**

    - Connect to the DeskOS API (client ID and secret)

    - Get cities, operators, campuses and spaces from the AP

    - Make and cancel bookings through the API

4.  **Booking Management**

    - Make a booking

    - Change a booking (cancel it and book again)

    - Cancel a booking

    - View upcoming and previous bookings

    - Booking confirmation

5.  **Real-Time Availability and Notifications**

    - View the availability status of spaces

    - Update availability when a space becomes free

    - Notify users when a previously occupied space becomes available

    - Send booking reminders and notifications

    - Refresh availability from DeskOS and

    - Notify users when a requested slot becomes free (the platform
      re-checks availability on a schedule)

6.  **Administration**

    - Manage users and access.

    - Monitor platform activity and reported issues.

    - View authorized booking records.

    - Generate platform usage reports.

    - Manage platform settings and notification rules, if implemented.

**Justification:**

The Incremental Model is appropriate because these features can be
divided into separate increments and developed progressively. For
example, the first increment can focus on User Management, followed by
Space Search, Third-Party API Integration, Booking Management,
Availability and Notifications, and finally Administration.

Each increment can be designed, implemented, tested, and delivered
before the next increment is developed. The completed functionality
remains part of the final system while each new increment adds
additional functionality. This allows the team to develop the platform
piece by piece while obtaining a working system at an earlier stage

The DeskOS API integration will be developed as a separate increment
after the basic space search functionality is established. The team will
review the API documentation, verify access and supported functionality,
and test integration before incorporating external space information
into the platform
