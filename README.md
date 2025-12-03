Hotel Reservation System

Team Pour ideots- IT 2110

Bacay, Gian B.

Delgado, James Carl R.

Espino, Joshua Rei P.

Salazar, James Lander A.

  📌 Project Overview

The Hotel Reservation System is a console-based Java application designed to simulate an organized, efficient, and user-friendly hotel booking and management process. 
It models real-world hotel operations and integrates software principles such as data accuracy, transparency, and user-centered interaction.

The project is inspired by recent research on digital reservation technologies.
Al-Kasasbeh, M.; Kaur, M. (2017) emphasize the importance of automated booking platforms, real-time room availability monitoring, and secure data handling in improving hotel operations, 
while Lee, S.-H.; Yoo, C. (2015) highlight structured system design and database-driven workflows to simplify reservation management. These studies guided the development of the system’s 
simulated booking and room-tracking features.

The application allows users to manage rooms, record guest information, create and update reservations, and view availability using object-oriented programming concepts.

  🧠 OOP Concepts Used

Encapsulation

Encapsulation is used to protect data within classes such as Room, Reservation, and Guest.

Attributes (e.g., room number, guest name, reservation dates) are kept private, and accessed or modified only through public getter and setter methods.

This ensures data safety and prevents unauthorized or accidental modification.

Inheritance

Inheritance allows the system to reuse shared behavior.

Common attributes for different user types (e.g., Admin, Staff, Customer) or different room categories (e.g., StandardRoom, DeluxeRoom) can be placed in a base class.

This reduces repetitive code and makes it easier to extend the system.

Polymorphism

Polymorphism is applied when different classes share the same method name but implement their behavior differently.

the system may include methods like calculatePrice() that behave differently depending on room type or applied discounts.

This allows flexible and dynamic processing of objects at runtime.

Abstraction

Abstraction is used by creating classes that represent real-world hotels

such as rooms, guests, and reservations—without exposing unnecessary implementation details.

Only essential behaviors and attributes are defined,

simplifying interaction and improving readability.


  📁 Program Structure

Main Classes

Room (abstract)
Base class containing attributes for room number, room type, price, and availability status.

StandardRoom (subclass)
Represents basic accommodation with standard pricing and amenities.

DeluxeRoom (subclass)
Offers enhanced comfort such as upgraded amenities or larger space.Implements higher pricing and refined room details.


Guest
Stores guest information including name, contact details, and ID reference.

Reservation
Links a guest with a specific room. Stores booking information and is added to the reservations list when a booking is made.

HotelReservationSystem (main system class)
Acts as the controller that manages rooms, reservations, and user input.
Includes functions for viewing rooms, booking rooms, canceling reservations, and searching availability.

  📊 Text-Based Class Diagram

               +----------------------+
                     |     Room (abstract)  |
                     +----------------------+
                     | - roomNumber         |
                     | - booked             |
                     +----------------------+
                     | + bookRoom()         |
                     | + cancelBooking()    |
                     | + getPrice()         |
                     +----------------------+
                             ^
                             |
             ---------------------------------------
             |                                     |
     +----------------------+        +----------------------+
     |    StandardRoom      |        |     DeluxeRoom       |
     +----------------------+        +----------------------+
     | + getPrice() =1500  |        | + getPrice() =3000   |
     +----------------------+        +----------------------+
                            

            +----------------------+        +----------------------+
            |        Guest         |        |     Reservation      |
            +----------------------+        +----------------------+
            | - name               |        | - guest              |
            | - contact            |        | - room               |
            +----------------------+        +----------------------+
                        ^                           ^
                        |                           |
                        -----------         ----------
                                    \       /
                                     \     /
                               +----------------------------+
                               |   HotelReservationSystem   |
                               +----------------------------+
                               | - rooms (List)             |
                               | - reservations (List)      |
                               +----------------------------+
                               | + main program logic       |
                               +----------------------------+
                   +---------------------------------------+

How to Run the Program

1. Save the Java File
Make sure the filename matches the public main class.

2. Open Command Prompt / PowerShell
Navigate to the folder containing your .java file:
cd path\to\your\project

3. Compile
javac HotelReservationSystem.java

4. Run
java HotelReservationSystem

5.Interact with the Menu
The main menu will appear, allowing you to:

View all rooms
Book a room
Cancel reservations
Search available rooms

  🖥️ Sample Output

https://github.com/jmscrldelgado/Hotel-Reservation-System/blob/main/590179238_860335826477651_495100115201283920_n.png

  ✍️ Authors & Acknowledgements

This project was created by Team Pour Ideots:

James Carl R. Delgado – Leader, writer, researcher, documentation

Gian B. Bacay – Writer, researcher, documentation

Joshua Rei P. Espino – Writer, researcher, documentation

James Lander A. Salazar– Console programming, system development

The division of tasks allowed each member to contribute based on their strengths, ensuring efficient workflow and creativity in both writing and system implementation.

Special thanks to:

Ms. Christiana Grace Alib — for providing continuous guidance, feedback, and encouragement.

Families, loved ones, and friends — for their unwavering support.

Each team member — for their dedication, effort, and collaboration that led to the project's success.

  🚀 Future Enhancements

1. Add Room Pricing & Billing System
Automatically compute total cost based on room rate and number of nights.

2. Add Check-in and Check-out Dates
Allows users to book rooms for multiple days and prevent overlapping bookings.

3 .Improve Data Persistence
Replace in-memory storage with file handling or a database (e.g., MySQL) so data is saved permanently.

4. Customer Profile Management
Store guest details such as name, contact number, and booking history.

  📚 References

https://www.emerald.com/insight/content/doi/10.1108/JHTT-06-2016-0039/full/html

https://www.sciencedirect.com/science/article/pii/S0278431915000925
