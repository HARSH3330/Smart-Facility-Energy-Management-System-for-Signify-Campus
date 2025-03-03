 Smart Facility & Energy Management System

Overview
This is a backend project built with Java Spring Boot  and  MySQL   to manage facility bookings, event scheduling, and user feedback in a corporate environment. The system features role-based access control and supports CRUD operations through REST APIs, which can be tested using Postman.

 Features
- User Management:   Register and view users.
- Facility Management:   Add, view, and manage facility availability.
- Booking System:   Create, view, and manage bookings with conflict detection.
- Feedback Collection:   Collect and view feedback for facilities.

## Project Structure
```
smart-facility/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/signify/smartfacility/
│   │   │       ├── SmartFacilityApplication.java
│   │   │       ├── controller/
│   │   │       ├── model/
│   │   │       └── repository/
│   │   └── resources/
│   │       └── application.properties
├── pom.xml
└── README.md
```

## Installation & Setup

1.   Clone the repository:  
```bash
git clone <repository-url>
cd smart-facility
```

2.   Configure the database:  
- Start MySQL using XAMPP.
- Create a database named `smart_facility`.
- Update `application.properties` with your database credentials:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/smart_facility
spring.datasource.username=root
spring.datasource.password=
```

3.   Build and run the application:  
```bash
mvn clean install
mvn spring-boot:run
```

## API Endpoints

### User APIs
- `POST /api/register`: Register a new user.
- `GET /api/users`: Get all users.

### Facility APIs
- `POST /api/facilities`: Add a new facility.
- `GET /api/facilities`: List all facilities.

### Booking APIs
- `POST /api/bookings`: Create a new booking.
- `GET /api/bookings`: List all bookings.

### Feedback APIs
- `POST /api/feedback`: Submit feedback.
- `GET /api/feedback`: View all feedback.

## Testing the APIs
1. Use   Postman   or any API client.
2. Send requests to `http://localhost:8080/api/`.

Example for registering a user:
```json
{
    "fullName": "John Doe",
    "email": "john@example.com",
    "password": "password123",
    "role": "EMPLOYEE"
}
```

## Tools & Dependencies
-   Java Spring Boot   (Web, Data JPA, Validation)
-   MySQL   (Database)
-   Maven   (Build tool)

## How to Package the Project
1.   Build the project:  
```bash
mvn clean package
```
2.   Create a ZIP file:  
```bash
zip -r smart-facility.zip .
```

You can then import the project directly into   IntelliJ IDEA   or any preferred IDE.



