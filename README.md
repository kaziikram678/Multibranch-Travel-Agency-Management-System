# Multi-branch Travel Agency Management System

This repository contains the database schema and queries for a multi-branch travel agency management system. The project leverages a database management system (DBMS) to optimize operations such as booking management, customer relationship management (CRM), and financial transactions.

## Features

- Centralized Employee Management: Store and retrieve employee details such as ID, name, salary, and address.
- Customer Management: Maintain customer data, including contact information and linked employees.
- Branch Management: Manage branch-specific data, including location and employee count.
- Booking and Payment Systems: Handle bookings, track payment details, and manage tour packages, hotel reservations, and vehicle rentals.
- Hotel and Vehicle Records: Record information about hotels and vehicles associated with bookings.

## Files

- DDL.sql: Contains the Data Definition Language (DDL) scripts to create the database schema.
- DML.sql: Contains the Data Manipulation Language (DML) scripts to insert, update, and retrieve data.

## Schema Overview

The schema includes the following tables:

- EMPLOYEE: Details of employees working in the travel agency.
- CUSTOMER: Information about customers and their linked employees.
- BRANCH: Records of different branches.
- PAYMENT: Details of transactions.
- BOOKING: Information about bookings and reservations.
- OWN: Links employees to branches.
- CHOOSE: Maps customers to hotels.
- MANAGE: Links employees, customers, payments, and bookings.
- PROVIDE: Records bookings and associated hotels and vehicles.
- HOTEL: Hotel details.
- VEHICLE: Vehicle details.

## How to Use

1. Clone this repository.
2. Use `DDL.sql` to create the database schema.
3. Use `DML.sql` to insert and retrieve data as needed.

## Example Queries

- Retrieve all employee data:
  ```sql
  SELECT * FROM EMPLOYEE;
  ```
- Find the average salary of employees:
  ```sql
  SELECT AVG(SALARY) AS "AVERAGE SALARY" FROM EMPLOYEE;
  ```
- List customers and their hotel preferences:
  ```sql
  SELECT C.C_NAME, H.H_NAME FROM CUSTOMER C, CHOOSE CH, HOTEL H WHERE C.C_ID = CH.C_ID AND H.H_ID = CH.H_ID;
  ```

## Conclusion

The multi-branch travel agency management system improves operational efficiency and customer satisfaction by centralizing data and automating key processes. This repository provides a robust foundation for implementing the system in a real-world travel agency.

