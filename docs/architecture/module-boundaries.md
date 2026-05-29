# Module Boundaries

MathLMS/PiLMS is designed as a Modular Monolith using Clean Architecture principles.

The goal is to keep the system modular, testable, maintainable, and ready for production usage.

## Core Architectural Rules

1. Domain must remain independent.
2. Application contains use cases, contracts, DTOs, validation rules, and orchestration.
3. Infrastructure implements technical details such as persistence, external services, email, storage, and database access.
4. API exposes HTTP endpoints and wires dependencies.
5. Modules should communicate through Application-level contracts, not direct database access.
6. Controllers must not contain business logic.
7. Infrastructure must not leak into Domain.
8. Admin/Backoffice and Learning Portal can share backend modules, but authorization rules must clearly separate access.

## Planned Modules

### Identity & Access

Responsible for:
- Users
- Roles
- Permissions
- Authentication
- Authorization
- Ownership/resource-based access

Expected actors:
- Student
- Teacher
- Admin/Staff

### Learning

Responsible for:
- Courses
- Lessons
- Learning materials
- Course enrollment
- Progress tracking

### Assignments

Responsible for:
- Homework
- Submissions
- Teacher review
- Grades/feedback

### Questions & Discussions

Responsible for:
- Student questions
- Teacher answers
- Lesson/course discussions

### Admin/Backoffice

Responsible for:
- Managing users
- Managing courses
- Managing teachers
- Operational views
- Administrative actions

### Audit Logs

Responsible for:
- Tracking important system actions
- Recording actor, action, resource, timestamp, and metadata
- Supporting accountability and production troubleshooting

## Clean Architecture Dependency Direction

Allowed dependency direction:

```text
Api -> Application
Api -> Infrastructure

Infrastructure -> Application
Infrastructure -> Domain

Application -> Domain

Domain -> no project dependencies
