# 8.3. UML Components Diagram

Figure 8.1 shows the UML component diagram. Provided interfaces use
lollipop notation and required interfaces use socket notation, the
interface definitions with their operations are included in the diagram.
Table 8.2 lists the provided and required interfaces of each component.

Component diagram: [Software_Architecture_Component_Diagram.pdf](Component_Diagram/Software_Architecture_Component_Diagram.pdf)

| **Component**              | **Provided Interfaces**                                        | **Required Interfaces**                                                    |
|----------------------------|----------------------------------------------------------------|----------------------------------------------------------------------------|
| CO1 Web Presentation       | None                                                           | ISpaceSearch, IBookingManagement, IAccountManagement, INotificationService |
| CO2 Space Search           | ISpaceSearch                                                   | IExternalSpaceInfo (CO4), ISpaceData (CO6), IAvailabilityData (CO6)        |
| CO3 Booking Management     | IBookingManagement, IBookingStatusUpdate                       | IExternalBooking (CO4), IBookingRecords (CO6), IAvailabilityData (CO6)     |
| CO4 DeskOS Integration     | IExternalSpaceInfo, IExternalBooking, ICallbackEndpoint        | IDeskOSService (external DeskOS), IBookingStatusUpdate (CO3)               |
| CO5 Account & Notification | IAccountManagement, INotificationService                       | IRecordStorage (CO6)                                                       |
| CO6 Platform Data          | ISpaceData, IAvailabilityData, IBookingRecords, IRecordStorage | None                                                                       |
| DeskOS (external system)   | IDeskOSService                                                 | ICallbackEndpoint (CO4)                                                    |

**Table 8.2** Provided and required interfaces
