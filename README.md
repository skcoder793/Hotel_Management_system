🏨 Hotel Management System
A comprehensive console-based Hotel Management System built with Core Java that streamlines hotel operations including room booking, customer management, food ordering, and billing.

📋 Table of Contents
Features

Technologies Used

System Architecture

Installation

Usage

Class Structure

Key Functionalities

Future Enhancements

✨ Features

🏠 Room Management

4 Room Types: Luxury Double, Deluxe Double, Luxury Single, Deluxe Single

Real-time Availability: Check room availability instantly

Room Allocation: Smart room numbering system (1-60)

Pricing: Different rates for each room category

👥 Customer Management
Customer registration with personal details

Support for single and double occupancy

Contact information and gender tracking

Customer history persistence

🍽️ Food Service
Integrated food ordering system

Menu with 4 items: Sandwich, Pasta, Noodles, Coke

Dynamic pricing and quantity management

Itemized billing

💰 Billing System
Automated bill generation

Room charges + food charges calculation

Detailed receipt printing

Checkout processing

💾 Data Management
Automatic data persistence using serialization

Multi-threaded backup system

Data recovery on application restart

Exception handling for data integrity

🛠 Technologies Used
Language: Java

Concepts: OOP, File I/O, Serialization, Multi-threading, Exception Handling

Data Structures: Arrays, ArrayList

Storage: Object Serialization

🏗 System Architecture
text
Main (Entry Point)
    ->
Hotel (Business Logic Layer)
    ->
Entities: Singleroom, Doubleroom, Food, holder
    ->
Services: write (Backup Thread), NotAvailable (Custom Exception)


📥 Installation
Prerequisites
Java JDK 8 or higher

Any Java IDE (Eclipse, IntelliJ, VS Code) or command line

Steps
Clone or Download the project file

Compile Java files:

terminal:- 
javac *.java

Run the application:

terminal:-
java main

🚀 Usage

Main Menu Options

Display Room Details - View features and pricing for each room type

Display Room Availability - Check available rooms by category

Book Room - Reserve a room with customer details

Order Food - Add food items to room service

Checkout - Process checkout and generate bill

Exit - Close application with automatic backup

Room Numbering System

1-10: Luxury Double Rooms

11-30: Deluxe Double Rooms

31-40: Luxury Single Rooms

41-60: Deluxe Single Rooms

Sample Workflow

Check room availability (Option 2)

Book a room (Option 3)

Order food items (Option 4)

Checkout and pay bill (Option 5)

🏛 Class Structure

Core Classes

main: Application entry point with menu-driven interface

Hotel: Main business logic containing all operations

Singleroom: Single room entity with customer details

Doubleroom: Double room entity (extends Singleroom)

Food: Food item with pricing logic

holder: Data container for all rooms

write: Runnable class for backup operations

NotAvailable: Custom exception for booking errors

Key Methods

bookroom(): Room booking with validation

order(): Food ordering system

bill(): Bill generation and calculation

deallocate(): Checkout processing

availability(): Room availability check

🔧 Key Functionalities

Object-Oriented Programming

Inheritance: Doubleroom extends Singleroom

Encapsulation: Private fields with public methods

Polymorphism: Method overriding in exception handling

Abstraction: Clean separation of concerns

File Handling & Serialization

java

// Automatic backup

FileOutputStream fout = new FileOutputStream("backup");

ObjectOutputStream oos = new ObjectOutputStream(fout);

oos.writeObject(hotel_ob);

Exception Handling

Custom NotAvailable exception for booking conflicts

Comprehensive try-catch blocks for robust error management

Null pointer exception handling for data integrity

Multi-threading
java
// Background backup
Thread t = new Thread(new write(Hotel.hotel_ob));
t.start();


📊 Room Specifications

Room Type	Beds	AC	Breakfast	Price/Day

Luxury Double	1 Double	Yes	Yes	₹4000

Deluxe Double	1 Double	No	Yes	₹3000

Luxury Single	1 Single	Yes	Yes	₹2200

Deluxe Single	1 Single	No	Yes	₹1200

🍕 Menu Items

Item	Price

Sandwich	₹50

Pasta	₹60

Noodles	₹70

Coke	₹30

🔮 Future Enhancements

Database integration (MySQL/PostgreSQL)

Web-based GUI using Spring Boot

User authentication and authorization

Payment gateway integration

Reporting and analytics dashboard

Email notifications

Inventory management

Staff management module

🐛 Known Issues

Console-based interface limitations

No input validation for special characters

Basic error messages

No database persistence (file-based only)

👥 Contributing

Fork the project

Create your feature branch (git checkout -b feature/AmazingFeature)

Commit your changes (git commit -m 'Add some AmazingFeature')

Push to the branch (git push origin feature/AmazingFeature)

Open a Pull Request

📝 License

This project is open source and available under the MIT License.

🎯 Skills Demonstrated

This project showcases strong fundamentals in:

Core Java Programming

Object-Oriented Design Principles

File I/O and Serialization

Exception Handling

Multi-threading

Data Structures and Algorithms

Software Architecture Design

⭐ Star this repo if you find it helpful!
