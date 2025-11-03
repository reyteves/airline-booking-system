![Airline Booking System Banner](Banner.png)

# Technical Specifications Document

## 1. Title Page

- **Project Name**: Airline Booking System 
- **Version**: 1.0
- **Date**: November 3, 2025
- **Author(s)**: Group 2 Members


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
The MVP includes flight search, booking, ticket management, and payment processing. It excludes advanced features such as seat selection, loyalty programs, or multi-city bookings.
- **Definitions, Acronyms, and Abbreviations**:
    - **PNR**: Passenger Name Record
    - **API**: Application Programming Interface

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

- To be provided as design wireframes/screenshots linking to flight search, booking pages, and user profile.


## 6. Features

- **Flight Search**: Allows users to find available flights by origin, destination, and date.
- **User Registration and Login**: Users create accounts and log in to manage bookings.
- **Booking Creation**: Users can select flights, provide passenger details, and book tickets.
- **Payment Processing**: Secure online payment integration to complete booking.
- **Booking Management**: Users can view booking details and cancel bookings if needed.


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

- User Registration and Login
- Flight Search Functionality
- Booking Processing
- Payment Gateway Integration
- Booking Management Interface


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
- **Database Requirements**: NoSQL, MongoDB Atlas
- **Data Storage and Retrieval**: Efficient retrieval of flight schedules and user bookings for smooth UX.


## 10. External Interface Requirements

- **User Interfaces**: Registration/login pages, flight search page, booking page, user account dashboard.
- **API Interfaces**: Payment gateway API for processing transactions. Flight data API if integrated with external flight data providers (optional).
- **Hardware Interfaces**: None required.
- **Software Interfaces**: Database system, payment gateway integration, optional third-party APIs.


## 11. Glossary

- **PNR**: Passenger Name Record, unique booking identifier.
- **API**: Application Programming Interface, allows systems to communicate.


## 12. Appendices

- **Supporting Information**: User journey diagrams, wireframes (to be attached).
- **Revision History**:
    - **v1.0**: Initial version created November 3, 2025.

