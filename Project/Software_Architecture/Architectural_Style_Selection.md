# 8.1. Architectural Style

The selected architectural style is the **3-Layer Architectural Style**.
It separates the system into a Presentation Layer, an Application Layer,
and a Data Layer, and each layer communicates with the others through
defined interfaces.

- **Presentation Layer:** provides the user interface through which
  users and administrators register, log in, search and filter spaces,
  view space details and availability, make, change, and cancel
  bookings, and manage platform users and booking records.

- **Application Layer:** handles the business logic: registration and
  login, search and filtering, booking requests and availability
  checks, booking changes (rebook) and cancellations, communication
  with the DeskOS API, validation of API responses and API errors, and
  notifications and administrative operations.

- **Data Layer:** stores and retrieves the platform's internal data,
  such as user accounts and booking records, and relevant space
  information received from DeskOS, while maintaining data consistency
  and supporting backup and recovery.

**Justification:** The platform is web-based and has clearly separable
responsibilities: user interaction, booking and search processing, and
persistent data. The application layer is a suitable place to integrate
the external DeskOS API, so API communication and data validation are
handled by the business logic rather than directly by the user
interface. The style supports the project's design goals of
maintainability (one layer can change without major changes to the
others), security (authentication, authorization, booking validation,
and callback verification are handled centrally), reliability (DeskOS
failures are handled in the application layer and do not directly affect
the other layers), and performance (each layer can be optimized as the
number of users grows).
