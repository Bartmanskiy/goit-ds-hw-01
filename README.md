## Description

This repository contains a Python-based command-line address book application designed to manage contacts, phone numbers, and birthdays.

The project demonstrates object-oriented programming, data validation, custom error handling, persistent data storage, and containerization with Docker. The application allows users to manage contact information through an interactive command-line interface and automatically saves the address book data between sessions.

## Technologies

* Python 3.11
* Object-Oriented Programming (OOP)
* `collections.UserDict`
* `datetime`
* `pickle`
* Custom exceptions
* Decorators
* Data validation
* Command-line interface (CLI)
* Docker

## Functionality

### Contact Management

The application provides an interactive assistant for managing contacts.
It supports:
* adding new contacts;
* adding and editing phone numbers;
* searching for contact phone numbers;
* displaying all contacts;
* deleting contacts;
* handling invalid commands and missing arguments.

### Birthday Management

The address book supports storing and managing birthdays.
The application allows users to:
* add a birthday to a contact;
* display a contact's birthday;
* find upcoming birthdays within a specified number of days;
* automatically move birthdays falling on weekends to the nearest working day.

### Data Validation

The application validates user input before storing it.
It validates:
* phone numbers using a 10-digit format;
* birthdays using the `DD.MM.YYYY` format;
* command arguments and required input parameters.

### Persistent Data Storage

Contact information is stored using Python's `pickle` module.
The application:
* saves the address book to a `.pkl` file;
* loads previously saved contacts when the application starts;
* preserves contacts, phone numbers, and birthdays between sessions.

### Object-Oriented Design

The application uses a structured class hierarchy:
* `Field` — base class for contact fields;
* `Name` — represents a contact name;
* `Phone` — validates and stores phone numbers;
* `Birthday` — validates and stores birthdays;
* `Record` — represents an individual contact;
* `AddressBook` — manages the collection of contact records.

### Error Handling

The project uses custom exceptions and an `input_error` decorator to handle invalid operations and user input without terminating the application.

### Docker Support

The project includes a Docker configuration based on Python 3.11 Slim, allowing the application to be packaged and executed in an isolated container environment.

## Links

GitHub: https://github.com/Bartmanskiy/goit-ds-hw-01
