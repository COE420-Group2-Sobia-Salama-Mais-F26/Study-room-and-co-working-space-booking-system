# Exercise 3: Non-Functional Requirements

| NFR ID | Category | Non-Functional Requirement | Contributor |
|---|---|---|---|
| NFR-01 | Performance | The system shall display space search results within 3 seconds under normal operating conditions | Sobia adnan- g00100257 |
| NFR-02 | Security | The system shall require users to log in before making or cancelling a booking. | Sobia adnan- g00100257 |
| NFR-03 | Usability | The system shall display space details, including facilities and location, in a clear and understandable format. | Sobia adnan- g00100257 |
| NFR-04 | Reliability | The system shall update space availability after a booking is made or cancelled, ensuring that the displayed availability reflects the latest booking status. | Sobia adnan- g00100257 |
| NFR-05 | Portability | The web-based system shall support access through Google Chrome, Microsoft Edge, and Mozilla Firefox. | Sobia adnan- g00100257 |
| NFR- 06 | Maintainability | The system shall let administrators update room details and booking rules from the dashboard without editing the code. | Salama alsuwaidi- g00099875 |
| NFR-07 | Scalability | The system shall support 500 simultaneous users and finish search or booking actions within few seconds. | Salama alsuwaidi- g00099875 |
| NFR-<br>08 | Responsiveness | The system shall adjust its layout to fit desktop, tablet, and mobile screens without horizontal scrolling. | Salama alsuwaidi- g00099875 |
| NFR-09 | Robustness | The system shall show an error message when users enter invalid data or try to book an unavailable room. | Salama alsuwaidi- g00099875 |
| NFR-<br>10 | Accessibility | The system shall allow users to search for rooms and manage their bookings using only a keyboard. | Salama alsuwaidi- g00099875 |
| NFR-<br>11 | Availability | The system shall be available at least 99% of the time during normal operating hours, excluding planned maintenance. | Mais Abudaqqa<br>g00099729 |
| NFR-<br>12 | Security | The system shall lock a user account for 5 minutes after 5 consecutive unsuccessful login attempts. | Mais Abudaqqa<br>g00099729 |
| NFR-<br>13 | Recoverability | The system shall create a backup of user and booking data at least once every 24 hours so that the data can be restored in case of system failure. | Mais Abudaqqa<br>g00099729 |
| NFR-<br>14 | Privacy | The system shall restrict access to users' personal information and booking history to the user and authorized administrators. | Mais Abudaqqa<br>g00099729 |
| NFR-<br>15 | Data Integrity | The system shall ensure that two users cannot successfully book the same space for overlapping date and time periods. | Mais Abudaqqa<br>g00099729 |
| NFR-16 | Reliability | The system shall handle unavailable or unresponsive DeskOS API responses without causing the booking platform to crash | Sobia Adnan- g00100257 |
| NFR-17 | Data Integrity | Requirement: The system shall validate space information and any availability information received from the DeskOS API before displaying it to users. | Sobia Adnan- g00100257 |
| NFR-18 | Performance | The system shall process a successful response from the DeskOS API and display the corresponding space information within 5 seconds under normal operating conditions, excluding delays outside the system's control. | Sobia Adnan- g00100257 |
| NFR-19 | Security | The system shall verify the signature of each incoming DeskOS callback before accepting and processing its booking-status update | Sobia Adnan- g00100257 |
| NFR-20 | Realibility | The system shall process duplicate deliveries of the same DeskOS callback so booking-status should not update more than once. | Sobia Adnan - g00100257 |
