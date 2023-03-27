# InBank Internship Assignment

This repository combines the InBank Frontend and Backend services using Git submodules. It provides a loan application service with a Flutter frontend and a Spring Boot backend API.
The submodules can also be separately accessed from these links. ([frontend](https://github.com/boostd/inbank-frontend) and [backend](https://github.com/boostd/inbank-backend))

## Technologies Used

- Flutter (Frontend)
- Dart (Frontend)
- Java 17 (Backend)
- Spring Boot (Backend)
- [estonian-personal-code-validator:1.6](https://github.com/vladislavgoltjajev/java-personal-code) (Backend) (Used for validating the ID code server side)

## Requirements

- Flutter (Frontend)
- Java 17 (Backend)
- Gradle (Backend)

## Installation

To install and run the application, please follow these steps:

1. Clone the repository, including the submodules:

```
git clone --recurse-submodules https://github.com/boostd/inbank-internship-assignment.git
```
2. Install and run the backend:
    1. Navigate to the backend submodule directory:
    ```
    cd ../inbank-backend
    ```
    2. Run `gradle build` to build the application.
    3. Run `java -jar build/libs/inbank-backend-1.0.jar` to start the application. The default port is 8080.

3. Install and run the frontend:
    1. Navigate to the frontend submodule directory:
    ```
    cd inbank-frontend
    ```
    2. Run `flutter pub get` to install the required dependencies.
    3. Run `flutter run` to start the application in debug mode.

## Functionality
The InBank loan application service provides a form for submitting loan applications.
The form consists of two sliders for selecting the loan amount and loan period, and a text field for entering the national ID number.
The application communicates with the backend API to calculate the approved loan amount and loan period, which are displayed to the user.

## Components
The application consists of the following main components:

### Frontend Components
**LoanForm**

The LoanForm component displays the loan application form, including the sliders for selecting the loan amount/period and the text field for entering the national ID number.
It communicates with the backend API to calculate the approved loan amount and loan period based on the form inputs.

**ApiService**

The ApiService component provides methods for making API calls to the backend API.
It sends loan application information to the backend API and receives a response with the approved loan amount and loan period.

### Backend Components
**DecisionEngine**

A service class that provides a method for calculating an approved loan amount and period for a customer.

**DecisionEngineController**

A REST endpoint that handles requests for loan decisions.

## Contributors
This combined repository and its frontend and backend applications were developed by Jürgen Tihanov as a part of the application for an InBank software developer internship.
