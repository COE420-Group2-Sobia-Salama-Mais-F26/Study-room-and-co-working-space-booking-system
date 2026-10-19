# Scenarios

## S-01 – Search and Book a Study Room
**Actor/Stakeholder:** User

A user needs a quiet room for group study. The user searches for study rooms based on location, date, time, duration, and capacity. The user filters the available spaces based on facilities such as Wi-Fi and whiteboards. After viewing the space details and availability, the student selects a suitable room and makes a booking.

## S-02 – Cancel an Existing Booking
**Actor/Stakeholder:** User

A user has an existing booking for a study room but no longer needs it. The user views their upcoming bookings, selects the reservation, and cancels it. The system updates the availability of the space after the booking is cancelled.

## S-03 – Modify an Existing Booking
**Actor/Stakeholder:** User

A user has already booked a study room but needs to change their study session. They log into the system and open their upcoming bookings. After choosing the booking they want to adjust, they select a new date, time, or room. The system checks whether the new option is available and updates the booking if it is. The user then gets a confirmation message. If the new time isn't available, the system shows other possible choices.

## S-04 – Manage Workspace Details
**Actor/Stakeholder:** Platform Administrator

A platform administrator wants to add a new study room or update an existing one. They open the admin dashboard and enter details such as the room name, capacity, facilities, and available times. The administrator saves the changes, and the updated room information becomes available in the system. Users can then see the correct details when searching for a space.

## S-05 – Receive a Booking Reminder
**Actor/Stakeholder:** User

A user has an upcoming booking for a study room. Before the scheduled time, the system sends the student a reminder with the booking details, including the room, date, start time, and duration. The user can open their booking to check the details and make sure everything is correct.

## S-06 – Retrieve External Space Information
**Actors:** User; Third-Party Space Provider (via External API)

A user searches for spaces by location, time, capacity, and facilities. The platform requests matching space information and availability from the external provider API, validates the response, and displays suitable spaces. If the API fails or returns invalid information, the platform shows an appropriate message rather than claiming confirmed availability.
