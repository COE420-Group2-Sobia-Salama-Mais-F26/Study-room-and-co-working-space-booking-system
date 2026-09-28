# Use Cases

## Sobia Adnan – g00100257

**UC-01 – Search for Spaces:** The user searches for study rooms, private rooms, desks, and co-working spaces based on location, date, time, duration, and capacity.

**UC-02 – Filter Spaces:** The user filters available spaces based on facilities such as Wi-Fi, power outlets, whiteboards, and projectors.

**UC-03 – View Space Details:** The user views the details, facilities, and location of a selected space.

**UC-04 – Make Booking:** The user reserves an available study room or co-working space.

**UC-05 – Cancel Booking:** The user cancels an existing booking and the system updates space availability.

## Salama Alsuwaidi – g00099875

**UC-06 – Modify Booking:** The user changes the date, time, or room of an existing booking.

**UC-07 – Receive Booking Reminder:** The system sends a reminder before the scheduled booking time.

**UC-08 – Notify Space Availability:** The system alerts users when a previously occupied space becomes available.

**UC-09 – Manage Room Information:** The administrator adds or updates study room details such as capacity, facilities, and availability.

**UC-10 – View Profile and History:** The user views and updates their profile and checks past bookings.

## Mais Abudaqqa – g00099729

**UC-11 – Register Account:** The user creates a new account by entering their name, email address, and password.

**UC-12 – View Upcoming and Previous Bookings:** The student views their upcoming and previous bookings, including the space, date, time, and booking status.

**UC-13 – Manage Reservations:** The administrator views, updates, or cancels reservations when necessary.

**UC-14 – Generate Usage Reports:** The administrator generates reports showing booking and space usage information.

**UC-15 – Manage Users:** The administrator views and manages registered user accounts when necessary, such as updating or disabling an account.

# Use Case Relationships

**R-01:** Make Booking → Search for Spaces — `<<include>>`  
The user needs to search for available spaces as part of making a booking.

**R-02:** Filter Spaces → Search for Spaces — `<<extend>>`  
Filtering is optional and extends the search functionality when the user wants to narrow the results.

**R-03:** Modify Booking → View Profile/History — `<<include>>`  
The user must view their existing bookings before modifying one.

**R-04:** Manage Room Information → View Space Details — `<<include>>`  
The admin needs to see room details before updating them.

**R-05:** Notify Space Availability → Search for Spaces — `<<extend>>`  
The system optionally alerts users when a searched space becomes available.
