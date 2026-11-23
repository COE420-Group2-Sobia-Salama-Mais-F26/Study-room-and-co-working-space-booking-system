## Exercise 2: Select and Justify an Architectural Style

Each team must select an appropriate architectural style based on its design goals.

Teams must document:

1.  The selected architectural style.

2.  Its main characteristics.

3.  Why it is appropriate for the project.

4.  How it supports the identified design goals.

5.  Its main advantages and potential limitations.

**Deliverable:** Architectural_Style_Selection.md

## ANS: 

## 1. Selected Architectural Style

The selected architectural style for the Study Room and Co-Working Space Booking System is the **3-Layer Architectural Style**.

This architecture separates the system into three main layers: Presentation Layer, Application Layer, and Data Layer. Each layer has its own responsibilities and communicates with the other layers through defined interfaces.

## 2. Main Characteristics

The 3-Layer Architectural Style consists of the following layers:

### **2.1 Presentation Layer**

This layer provides the user interface through which users and administrators interact with the system.

Its responsibilities include:

- Allowing users to register and log in.

- Providing space search and filtering interfaces.

- Displaying space details, facilities, and availability.

- Allowing users to make, change, and cancel bookings.

- Providing administrators with interfaces to manage platform users and booking records.

### **2.2 Application Layer**

This layer handles the main business logic and processes requests received from the presentation layer.

Its responsibilities include:

- Processing user registration and login requests.

- Handling space search and filtering operations.

- Managing booking requests and checking availability.

- Processing booking changes (rebook) and cancellations.

- Communicating with the external DeskOS API to retrieve space and availability information.

- Validating external API responses and handling API errors.

- Managing notifications and administrative operations.

### **2.3 Data Layer**

This layer manages the storage and retrieval of the platform's internal data such as user information and booking records, through the system's data-access functionality.

Its responsibilities include:

- Storing user account information.

- Maintaining platform booking records.

- Storing relevant space information received from DeskOS.

- Retrieving and updating stored records.

- Maintaining data consistency and supporting backup and recovery operations.

The external DeskOS API remains a separate external service. The application layer communicates with it to retrieve supported space and availability information.

## 3. Why This Architectural Style Is Appropriate

The 3-Layer Architectural Style is appropriate for the proposed system because the platform itself is web based and needs a clear seperate different responsibilities that can be separated into independent layers.

The presentation layer handles user interaction, the application layer processes booking and search operations, and the data layer manages persistent information.

This separation is particularly useful because the system supports several types of users, including students, professionals, freelancers, remote workers, and administrators.

Additionally, the application layer provides a suitable location for integrating the external DeskOS API, which is in the application layer. This ensures that external API communication and data validation are handled by the system's business logic rather than directly by the user interface.

The architecture also allows the user interface and database to be modified independently without requiring major changes to the entire application.

## 4. How the Architecture Supports the Design Goals

The selected architecture supports the architectural design goals identified in Exercise 1.

**Maintainability:**

Separating the system into three layers makes it easier to modify individual parts of the application. For example, changes to the user interface can be implemented without directly modifying the database or booking logic.

**Security:**

The application layer processes requests and controls access to the system's data. Authentication, authorization, booking validation, and external API callback verification can be handled centrally rather than allowing direct access to stored information from the presentation layer.

**Reliability:**

The application layer manages booking operations, validates external API responses, and handles communication failures. Separating these responsibilities helps prevent external API problems from directly affecting the presentation and data layers.

**Performance:**

The separation of responsibilities allows individual layers to be optimized as the number of users and requests increases. The application layer can handle search and booking requests while the data layer manages the required database operations.

## 5. Advantages and Potential Limitations

### **Advantages**

1.  **Separation of Responsibilities:** Each layer has clearly defined responsibilities, making the system easier to understand and manage.

2.  **Maintainability:** Changes to one layer can be implemented without requiring major modifications to other layers.

3.  **Scalability:** Individual layers can be optimized as the system grows and supports more users.

4.  **Easier testing**: The application logic, user interface, and data-access functionality can be tested as separate parts.

### **Potential Limitations**

1.  **Performance Overhead:** Requests must pass through multiple layers, which may introduce additional processing time.

2.  **Dependency Between Layers:** Changes to lower layers may affect the layers that depend on their services.

3.  **Additional Development Effort:** Separating the application into layers requires additional planning, interface design, and testing.

4.  **External API Dependency:** The platform still depends on the availability and supported functionality of the DeskOS API when retrieving external space and availability information.

These limitations can be managed through efficient interface design, proper testing, error handling, and clear separation of responsibilities.

## 6. Conclusion

The 3-Layer Architectural Style is selected because it provides a clear separation between user interaction, business logic, and data management.

It supports the project's main architectural design goals, particularly maintainability, security, reliability, and scalability.

It also provides a suitable structure for integrating the external DeskOS API while maintaining control over the platform's internal booking operations and user information.
