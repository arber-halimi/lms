# Architecture Notes

MathLMS Backend will be built as a Modular Monolith using Clean Architecture principles.

## Main Principles

- Domain layer must remain clean and independent.
- Application layer contains use cases and contracts.
- Infrastructure implements technical details such as database access.
- API exposes the system through HTTP endpoints.
- Features will be added incrementally through task-based development.

## Initial Modules Planned

- Identity and Access
- Learning
- Assignments
- Questions and Discussions
- Admin/Backoffice
- Audit Logs