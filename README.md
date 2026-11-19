# Student Management REST API

A Java-based Student Management REST API developed using Spring Boot and Maven. The application provides REST endpoints to manage student academic information through JSON requests and responses.

## Project Overview

This project represents a basic Student Academic Management System. It allows users to create, retrieve, update, delete, and search student records.

Each student record contains:

- Student ID
- Name
- Email
- Branch
- Academic Year
- CGPA

Student records are maintained using an in-memory Java `List`. A database is not required for this project.

## Technologies Used

- Java
- Spring Boot
- Spring Web
- Maven
- REST APIs
- JSON
- Eclipse IDE
- Postman

## Features

- Retrieve all student records
- Retrieve a student using their ID
- Add a new student
- Update existing student details
- Delete a student record
- Search students by branch and academic year
- Find students whose CGPA is greater than or equal to a given value

## REST API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/students` | Retrieve all students |
| GET | `/students/{studentId}` | Retrieve a student by ID |
| POST | `/students` | Add a new student |
| PUT | `/students/{studentId}` | Update student details |
| DELETE | `/students/{studentId}` | Delete a student |
| GET | `/students/search?branch=CSE&year=2` | Search by branch and year |
| GET | `/students/topper?cgpa=9.0` | Find students meeting the minimum CGPA |

The exact response format and behaviour depend on the implementation in the source code.

## Example JSON

Example student object:

```json
{
  "studentId": 101,
  "name": "Rahul Sharma",
  "email": "rahul@kiet.edu",
  "branch": "CSE(AI & ML)",
  "year": 2,
  "cgpa": 8.65
}
```

## Requirements

Make sure the following software is installed:

- Java Development Kit (JDK)
- Eclipse IDE
- Maven (or Eclipse Maven integration)
- Postman for API testing

## How to Run in Eclipse

1. Download or clone this repository.
2. If the project is provided as a ZIP file, extract it first.
3. Open Eclipse.
4. Select **File → Import → Maven → Existing Maven Projects**.
5. Browse to the extracted project folder.
6. Select the project and click **Finish**.
7. Allow Maven to download and configure the required dependencies.
8. Locate the Spring Boot main application class (the class containing `@SpringBootApplication`).
9. Right-click the class and select **Run As → Java Application** or **Spring Boot App**, if available.
10. Wait until the application starts successfully. The default port for this project is `8080`, if configured as specified.

## Testing with Postman

1. Start the Spring Boot application in Eclipse.
2. Open Postman.
3. Send requests to `http://localhost:8080` followed by the required endpoint.
4. Select the appropriate HTTP method: GET, POST, PUT, or DELETE.
5. For POST and PUT requests, select **Body → raw → JSON** and provide the JSON data.
6. Click **Send** and inspect the response.

Example POST URL:

```text
http://localhost:8080/students
```

Example search URL:

```text
http://localhost:8080/students/search?branch=CSE&year=2
```

Example CGPA URL:

```text
http://localhost:8080/students/topper?cgpa=9.0
```

## Important Note

This project uses an in-memory list for storing student data. Therefore, records added or modified while the application is running are not permanently stored and may be lost when the application restarts.

## Author

Developed as part of B.Tech academic practical work.
