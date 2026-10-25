# Exercise 5: Initial Feasibility Study Salama alsuwaidi 99875

1.  **A. Technical Feasibility**

The system can be developed using the technologies, software, and resources available for a web-based project. The main functions we plan to develop are user registration and login, searching and filtering spaces, viewing space details and availability, making and managing bookings, notifications, and an admin dashboard. The system will also need a database to manage information such as users, spaces, availability, and reservations.

The project does not require special hardware because features such as IoT sensors and smart access using QR codes, NFC, or biometric authentication are outside the scope of the current version. We are also focusing on a web-based system rather than developing separate Android and iOS applications. This keeps the technical work within the planned scope and makes the project more manageable for the team.

The technical feasibility of the DeskOS API integration depends on the availability of API access, authentication requirements, and support for the space information and availability operations required by the platform. The team must review the documentation and test the supported endpoints. External space listings and their source availability will be retrieved through the API rather than independently managed by the platform. External booking operations will be implemented only if the required API functionality and access are available. If a required operation is unsupported, it will be excluded from the implementation or replaced with a feasible alternative within the project scope.

2.  **Economic Feasibility**

The expected costs and resources for the project are reasonable because the current version focuses on a web-based booking system. Features that may require additional resources, such as online payment processing, IoT sensors, smart access systems, and native mobile applications, are not included in the current scope. The main resources needed will be the software and tools required to develop the system and the time and effort of the team members. A possible limitation is that adding some of the out-of-scope features in the future may require additional resources and costs.

The team must also verify whether using the DeskOS API involves subscription fees, usage limits, or other costs. The economic feasibility of the integration will depend on the actual access conditions and any associated charges. These costs must be checked before confirming the final implementation plan.

3.  **Operational Feasibility**

The system solves a real problem because existing workspace booking systems in the UAE are usually limited to certain institutions or are mainly made for professional users. Our system gives students, freelancers, remote workers, and other users one place to find and book a suitable space for studying or working. They can search based on things like location, date, time, capacity, and available facilities. They can also make, change, or cancel their bookings. Space administrators can manage the spaces, availability, and reservations. We think users would use the system because it makes finding and booking a suitable space easier and more organized.

The usefulness of the DeskOS integration will also depend on whether it provides relevant space information for the intended users and locations. The team should verify the available provider coverage and returned information before relying on the integration.

The platform will simplify space discovery by displaying external space information returned by the DeskOS API. Its usefulness depends on the relevance and completeness of the returned information and the availability of suitable spaces for the intended users. The platform administrator will manage website operations and authorized records, while external providers remain responsible for their own source listings and physical facilities.

4.  **Schedule Feasibility**

The project can be completed within the course duration because the work is already divided into different parts. We will start with User Management, then Space Search and Selection, Booking Management, Real-Time Availability and Notifications, and finally Administration. Since we are using the Incremental Model, we can finish and test one part before moving to the next. This makes the project easier to manage during the semester. The main limitation could be if some tasks take longer than planned, so we will divide the tasks between the team members and keep track of the deadlines.

The DeskOS API integration may require time to review documentation, obtain access, test supported endpoints, validate responses, and handle errors. The team will investigate these requirements early and prioritize core platform features. The final integration scope will depend on the functionality and access available within the course schedule.

5.  **Overall Feasibility**

Overall, the Study Room and Co-Working Space Booking System is expected to be feasible within the course duration because its main features can be developed incrementally. These features include user management, space search, DeskOS API integration, platform administration, and booking-related functionality that the platform is authorized to handle. The DeskOS integration introduces dependencies involving access, supported operations, possible costs, and the availability of relevant space information. The team will verify these requirements before finalizing the integration scope. By prioritizing core features, testing each increment, and limiting implementation to verified functionality, the team aims to deliver a functional system within the available time.
