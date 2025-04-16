1.	Introduction

Project Title: Car Rental System
Objective:
The "Car Rental System" is a Java-based desktop application designed to manage car reservations in a streamlined and user-friendly manner. The primary goal is to provide an interactive platform where users can view available cars, book them, and process payments efficiently. The system supports different car types, handles booking validations, and maintains a persistent record of all reservations.
Technology Stack:
• Programming Language: Java
• GUI Framework: Swing (javax.swing)
• Collection Framework: java.util
• File Handling: java.io
• Exception Handling: Custom Exceptions (BookingException, PaymentException)
• Threading: javax.swing.SwingUtilities (for safe GUI updates)

2.	Project Overview
System Architecture:
The application is designed around a single main class that integrates both the graphical user interface and the core business logic. It utilizes abstract classes, inheritance, inner classes, and basic multi-threading concepts to ensure smooth operation and modularity. Key components include:
• GUI interface (Swing)
• Car inventory and booking system (data model)
• Payment processing and validation
• File I/O for reservation logging
Features:
• View all available cars
• Book a car by entering details and payment
• Categorization of cars using inheritance (SUV, Sedan)
• Custom exception handling for booking and payment errors
• Save reservation records to a file
• GUI-based, event-driven interaction
Modules:
1.	Main Frame (CarRentalSystem): Manages the user interface, event handling, and overall system workflow
2.	Car Class Hierarchy: Abstract Car class with derived SUV and Sedan types
3.	Payment Module: Inner class handling payment validation and simulation
4.	Reservation Manager: Handles booking logic, availability checks, and file storage using the Collection and I/O APIs


a.	Implementation Details

I.	Inheritance and Polymorphism:
• Car is an abstract class with SUV and Sedan as concrete subclasses.
• The toString() method is overridden to display car details, and polymorphism is used to manage different car types uniformly.

II.	Inner Classes:
• The Payment module is implemented as an inner class within CarRentalSystem to encapsulate payment-specific logic.

III.	Exception Handling:
• Custom exceptions (BookingException, PaymentException) are used to handle specific error conditions like unavailable cars or failed payments.
• Try-catch blocks are used for validating user input and handling file I/O errors.

IV.	Threading:
• The GUI is initialized using SwingUtilities.invokeLater() to ensure thread-safe operations on the Swing UI thread.

V.	Collection API:
• A HashMap is used to store the inventory of cars with their IDs.
• An ArrayList is used to maintain a list of all reservations.

VI.	File Handling:
• BufferedWriter and FileWriter are used to append reservation details to a file (reservations.txt) for record-keeping.


	Key Functionalities
• View Available Cars
• View All Cars in Inventory
• Book a Car with Customer Name and Payment
• Validate Availability and Payment Status
• Log and Store Booking Details in a File

	User Interface
• Inputs: TextFields for Car ID, Customer Name, and Payment Amount
• Output: JTextArea to display car lists, booking confirmations, and error messages
• Buttons:
  – Show Available Cars
  – Show All Cars
  – Book a Car
  – Exit
• UI Layout: Grid and Border layouts used for clean arrangement
• Visual Design: Simple and intuitive layout with labeled sections for easy navigation

	Development Challenges:
• Managing thread-safe updates to the car inventory and reservation list
• Maintaining UI responsiveness during file write operations and booking processes
• Validating user inputs (e.g., payment amount, car ID) and handling exceptions gracefully

	Solutions Implemented:
• Used synchronized methods and thread-safe collections to ensure data consistency
• Performed UI updates and operations on the Event Dispatch Thread using SwingUtilities.invokeLater
• Implemented custom exceptions (BookingException, PaymentException) and input validation to improve error handling

Screenshot:-

![image](https://github.com/user-attachments/assets/f9a71c9c-d9fe-435f-84be-9a64d10dba6e)

![image](https://github.com/user-attachments/assets/c2d0cef4-49ac-45d8-8446-7a9d0cd8dcd3)

![image](https://github.com/user-attachments/assets/a059d217-7dbc-46bc-b7aa-7f29a19e54c3)
