# Traineeship Management System

A Java Spring Boot web application for managing university traineeships, including student applications, company positions, supervisor assignments, evaluations, and committee decisions.


## Features

### Authentication and Authorization
- User registration and login
- Role-based access control
- Separate dashboards for students, companies, professors, and committee members

### Student Features
- Create and update student profile
- Browse available traineeship positions
- Apply for a traineeship
- Maintain a traineeship logbook

### Company Features
- Create and update company profile
- Announce available traineeship positions
- View advertised and assigned positions
- Delete available positions
- Evaluate assigned students

### Professor Features
- Create and update professor profile
- View supervised traineeships
- Submit student and company evaluations

### Committee Features
- View student applications
- Search positions for students using different strategies
- Assign traineeship positions to students
- Assign supervising professors
- Monitor in-progress traineeships
- Complete traineeships with PASS/FAIL decisions

## Tech Stack

- Java
- Spring Boot
- Spring MVC
- Spring Security
- Spring Data JPA
- Hibernate
- Thymeleaf
- Maven
- MySQL
- JUnit
- Mockito

## Architecture

The application follows a layered MVC architecture:

- `controllers` handle HTTP requests and user interaction.
- `services` contain the business logic.
- `mappers` / repositories handle database access through Spring Data JPA.
- `domainmodel` contains the main domain entities.
- `config` contains Spring MVC and Spring Security configuration.
- `templates` contain Thymeleaf views.

This separation improves maintainability, testability, and extensibility.

## User Roles

The system supports four user roles:

- `STUDENT`
- `COMPANY`
- `PROFESSOR`
- `COMMITTEE`

Each role has access to a different dashboard and different application features.

## Design Patterns and Design Principles

The application applies several software design principles and patterns:

- Model-View-Controller (MVC)
- Service Layer pattern
- Data Mapper / Repository pattern
- Strategy pattern for traineeship position search
- Strategy pattern for supervisor assignment
- Factory pattern for selecting the appropriate strategy
- Role-based access control with Spring Security

The Strategy pattern is used to make the position search and supervisor assignment logic extensible. For example, positions can be searched based on student interests, preferred location, or both. Supervisors can be assigned based on professor interests or supervision load.

