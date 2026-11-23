# 2.4. Feasibility Study

**Technical feasibility:** The system can be developed using the
technologies, software, and resources available for a web-based project.
The main functions are user registration and login, searching and
filtering spaces, viewing space details and availability, making and
managing bookings, notifications, and an admin dashboard, supported by a
database for users, spaces, availability, and reservations. No special
hardware is required because IoT sensors and smart access are outside
the scope, and the system is web-based rather than separate Android and
iOS applications. The DeskOS API gives the platform a login token using
a client ID and secret, with this token, the platform can get spaces and
availability and make and cancel bookings. DeskOS does not allow
changing a booking, so the platform cancels and books again instead. The
team will test everything on the DeskOS test (staging) server.

**Economic feasibility:** The expected costs are reasonable because the
current version is a web-based booking system, and features that need
additional resources, such as online payments, IoT sensors, smart
access, and native mobile applications, are not included. The main
resources are development software and tools and the team's time and
effort. The DeskOS documentation does not list a subscription fee, it
has request limits, and higher limits can be requested. Users do not pay
through DeskOS: DeskOS bills the operators and records a commission for
each booking. The team will contact DeskOS sales to get access.

**Operational feasibility:** The system solves a real problem because
existing workspace booking systems in the UAE are usually limited to
certain institutions or mainly serve professional users. The platform
gives students, freelancers, remote workers, and other users one place
to find and book a suitable space by location, date, time, capacity, and
facilities, and to make, change, or cancel bookings. Platform
administrators manage users and bookings, while operators manage their
spaces in DeskOS. The DeskOS integration is useful only if DeskOS
operators share spaces in the cities the users need, so the team will
check the list of cities the API returns before relying on it.

**Schedule feasibility:** The project can be completed within the course
duration because the work is divided into increments: User Management,
Space Search and Selection, DeskOS Integration, Booking Management,
Availability and Notifications, and Administration. Since the
Incremental Model is used, each part can be finished and tested before
moving to the next. The project schedule in Chapter 3 gives a total
duration of 39 days (5 October to 12 November 2026). The DeskOS
integration may need time to review documentation, obtain access, test
endpoints, validate responses, and handle errors, so the team will
investigate these early and prioritize the core platform features.

**Overall feasibility:** The Study Room and Co-Working Space Booking
System is feasible within the course duration because its main features
(user management, space search, DeskOS API integration, platform
administration, and booking) can be developed incrementally. The DeskOS
integration depends on getting access from DeskOS and on operators
sharing spaces in the users' cities. By finishing core features first,
testing each increment, and testing the integration on the DeskOS
staging server, the team aims to deliver a working system within the
available time.
