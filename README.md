# Lawyer Management System

## Project Overview

The Lawyer Management System is a robust software solution designed to manage legal cases, track issues, and archive important documents. The system focuses on simplifying administrative tasks for lawyers, providing an intuitive interface for managing their daily operations efficiently and securely.

---

## Objective

- Streamline the process of managing legal cases and issues.
- Provide a secure archiving system for storing and retrieving case-related data.
- Ensure all operations are accessible to authorized users via a single-role system.
- Utilize modern technologies for scalability and maintainability.

---

## Features

### Core Functionalities
1. **Case Management**
   - Add, edit, delete, and retrieve case details.
   - Maintain a history of changes and updates.
   - Categorize cases by status (Open, Resolved, Archived).

2. **Issue Tracking**
   - Add issues independently or link them to specific cases.
   - Archive standalone issues for future reference.
   - Maintain detailed issue logs with timestamps.

3. **Archiving**
   - Archive sensitive or completed issues and cases securely.
   - Provide efficient search and retrieval for archived data.

4. **User Role Access**
   - Single-role system: Only authorized users (lawyers) can access the platform.

5. **Authentication and Authorization**
   - Secure login and session handling with JWT.
   - Password encryption for user data protection.

---

## Functional Requirements

### Users and Roles
- **Single Role: Lawyer**
  - Access to the entire platform.
  - Manage cases, issues, and archives.
  - Ensure sensitive data is securely handled.

### Modules
#### 1. Case Management
- **Create Cases**: Add case details such as title, description, and status.
- **Update Cases**: Modify existing case details.
- **View Cases**: Retrieve case details with sorting and filtering.
- **Delete Cases**: Remove cases from the active database.

#### 2. Issue Tracking
- **Create Issues**: Add new issues with descriptions and links to cases (if applicable).
- **Update Issues**: Edit issue details, status, or associated cases.
- **Archive Issues**: Move resolved or inactive issues to the archive.

#### 3. Archiving
- **Manage Archives**: Store and retrieve archived cases and issues.
- **Search Archives**: Enable keyword-based search for archived data.

#### 4. Authentication and Security
- **Login System**: Authenticate lawyers using username and password.
- **Secure Access**: Ensure data protection through role-based permissions and JWT.

---

## Technical Specifications

### Backend
- **Language**: Java 17
- **Framework**: Spring Boot 3.x
- **Database**: PostgreSQL or H2 for development
- **Authentication**: Spring Security with JWT
- **Build Tool**: Maven

### Frontend
- **Language**: TypeScript
- **Framework**: Angular 17
- **Styling**: Bootstrap or Tailwind CSS
- **Build Tool**: npm

---

## Project Structure

### Backend
The backend follows a layered architecture for clean code separation:
```plaintext
src/
└── main/
    ├── java/com/example/lawyerplatform/
    │   ├── config/         # Configuration files
    │   ├── controller/     # REST APIs
    │   ├── dto/            # Data Transfer Objects
    │   ├── exception/      # Exception handling
    │   ├── model/          # JPA entities
    │   ├── repository/     # Database interactions
    │   ├── service/        # Business logic
    │   └── util/           # Utility classes
    ├── resources/
    │   ├── application.yml # Configuration file
    │   ├── data.sql        # Test data
    │   └── schema.sql      # Database schema
