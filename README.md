![Airline Booking System Banner](Banner.png)

# Technical Specifications Document

## 1. Title Page

- **Project Name**: Airline Booking System
- **Version**: 1.1 (Updated)
- **Date**: November 5, 2025
- **Author(s)**:
    * Rey Jesus M. Teves
    * Jan Chelsea Lavaro
    * Darwin Besorio
    * Rex Bugcalao
    * Cristino France Madali
    * Manuel P Buenviaje II

## 2. Table of Contents

1. [Introduction](#3-introduction)
2. [Overall Description](#4-overall-description)
3. [Visual Mockup Reference](#5-visual-mockup-reference)
4. [Features](#6-features)
5. [Functional Requirements](#7-functional-requirements)
6. [Non-Functional Requirements](#8-non-functional-requirements)
7. [Data Requirements](#9-data-requirements)
8. [External Interface Requirements](#10-external-interface-requirements)
9. [Glossary](#11-glossary)
10. [Appendices](#12-appendices)

## 3. Introduction

- **Purpose**:
To develop a basic airline booking system that enables users to search for flights, book tickets, and manage their bookings efficiently.
- **Scope**:
**The Airline Booking System** includes flight search, booking, ticket management, and payment processing. It excludes advanced features such as seat selection, loyalty programs, or multi-city bookings.
- **Definitions, Acronyms, and Abbreviations**:
    - **PNR**: Passenger Name Record
    - **API**: Application Programming Interface
    - **MVP**: Minimum Viable Product

## 4. Overall Description

- **Product Perspective**:
The system is a standalone web application aimed at customers and airline staff to manage flight bookings.
- **Product Functions**:
    - Flight search by date, origin, and destination
    - Booking creation and confirmation
    - User registration and login
    - Payment gateway integration for ticket purchase
    - Booking viewing and cancellation
- **User Classes and Characteristics**:
    - **End Users**: Customers searching and booking flights.
    - **Admin Users**: Airline staff managing flight schedules and bookings in backend.
- **Operating Environment**:
    - Client: Modern web browsers (Chrome, Firefox, Safari)
    - Server: Web backend (e.g., Node.js, Python) with relational or NoSQL database
- **Assumptions and Dependencies**:
    - Reliable internet connectivity for users.
    - Availability of a payment gateway API (e.g., Stripe, PayPal).

## 5. Visual Mockup Reference

- **Link or Screenshot**: To be provided as design wireframes/screenshots linking to flight search, booking pages, and user profile. (Refer to the attached mobile mockups: Landing/Home, Search Results, Book a Flight/Confirmation, My Bookings, User Profile).

## 6. Features

**The Airline Booking System** is structured around the following core features and corresponding UI pages:

- **FEAT01: Landing/Home**: Provides the initial entry point and search interface.
- **FEAT02: User Registration and Login**: Allows users to create accounts and log in to manage bookings.
- **FEAT03: Flight Search & Results**: Allows users to find and view available flights by origin, destination, and date.
- **FEAT04: Flight Selection/Details**: Allows users to choose a specific flight and view full details before booking.
- **FEAT05: Booking Creation (Input Forms)**: Users can select flights, provide passenger details, and finalize the booking inputs.
- **FEAT06: Payment & Booking Confirmation**: Secure online payment integration to complete the booking, leading to a confirmation.
- **FEAT07: Booking Management (My Bookings)**: Users can view their upcoming, past, and cancelled bookings.
- **FEAT08: User Profile/Account**: Allows users to manage personal information and security settings.

- **Figma UI Kit**: Figma Design is available here: https://www.figma.com/design/HxhnSgMzAq0FQLGGGmckLR/Airify---Flight-Booking-App-UI-Kit---Travel-App----Preview-?node-id=4027-51417&p=f&t=ln5cW6WjYXD9etvC-0

## 7. Functional Requirements

### Use Cases

- **Use Case 1: User Registration and Login**
    - **Description**: New users can register and existing ones can log in securely.
    - **Actors**: End User
    - **Preconditions**: User accesses registration or login page
    - **Postconditions**: User account created or user authenticated
    - **Main Flow**: User inputs email and password > System validates and registers/authenticates user > User accesses account dashboard
    - **Alternate Flow**: Invalid input leads to error messages
- **Use Case 2: Flight Search**
    - **Description**: User searches for flights by origin, destination, and date.
    - **Actors**: End User
    - **Preconditions**: User is on flight search page
    - **Postconditions**: System displays available flights matching criteria
    - **Main Flow**: User inputs search parameters > System queries flights database > Results displayed
    - **Alternate Flow**: No flights found message if no matches
- **Use Case 3: Booking a Flight**
    - **Description**: User books a selected flight by providing passenger details and payment.
    - **Actors**: End User
    - **Preconditions**: User is logged in and has searched flights
    - **Postconditions**: Booking confirmed, ticket issued
    - **Main Flow**: User selects flight > enters passenger info > makes payment > confirms booking
    - **Alternate Flow**: Payment failure triggers error and retry option
- **Use Case 4: Managing Bookings**
    - **Description**: Users can view and cancel their bookings.
    - **Actors**: End User
    - **Preconditions**: User is logged in
    - **Postconditions**: Booking cancelled or displayed correctly
    - **Main Flow**: User selects "My Bookings" > chooses booking > views or cancels booking
    - **Alternate Flow**: Cancellation not allowed if deadline passed

### System Features

- **FEAT01/02:** User Registration and Login
- **FEAT03/04:** Flight Search and Selection Functionality
- **FEAT05/06:** Booking and Payment Processing
- **FEAT07:** Booking Management Interface
- **FEAT08:** User Profile Management Interface

## 8. Non-Functional Requirements

- **Performance**: Search results within 3 seconds, page load under 2 seconds.
- **Security**: Passwords hashed, sessions secured, HTTPS for all transactions.
- **Usability**: Intuitive user interface with responsive design for desktop and mobile.
- **Reliability**: 99.5% uptime with backup and recovery plans.
- **Supportability**: Codebase well-documented, modular for easy maintenance.

## 9. Data Requirements

- **Data Models**:
    - **User**: { user_id, email, password_hash, name }
    - **Flight**: { flight_id, airline, origin, destination, departure_time, arrival_time, available_seats }
    - **Booking**: { booking_id, user_id, flight_id, passenger_details, booking_status, payment_status }
    - ***ERD Entities to be modeled***: User, Flight, Airport, Booking, Passenger, Payment, Ticket (as previously discussed).
- **Database Requirements**: NoSQL, MongoDB Atlas
- **Data Storage and Retrieval**: Efficient retrieval of flight schedules and user bookings for smooth UX.
- **ERD**: Add the ERD for the database models based on Specifications. (To be attached)

## 10. External Interface Requirements

- **User Interfaces**: Registration/login pages, flight search page, booking page, user account dashboard. (Specifically: Landing/Home, Search Results, Flight Selection, Book a Flight, My Bookings, User Profile).
- **API Interfaces**: Payment gateway API for processing transactions. Flight data API if integrated with external flight data providers (optional).
- **Hardware Interfaces**: None required.
- **Software Interfaces**: Database system, payment gateway integration, optional third-party APIs.

## 11. Glossary

- **PNR**: Passenger Name Record, unique booking identifier.
- **API**: Application Programming Interface, allows systems to communicate.
- **MVP**: Minimum Viable Product, a version of a product with just enough features to satisfy early customers.

## 12. Appendices

- **Supporting Information**: User journey diagrams, wireframes (to be attached).
- **Revision History**:
    - **v1.0**: Initial version created November 3, 2025.
    - **v1.1**: Updated November 5, 2025. Incorporated all core UI pages (FEAT01-FEAT08) and enhanced Data Requirements based on MVP discussion.

