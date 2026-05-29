# MathLMS Backend

MathLMS is a production-grade backend for an online mathematics learning platform.

## Technology

- ASP.NET Core Web API
- Modular Monolith
- Clean Architecture principles
- Testing-first production practices

Planned for later tasks:

- SQL Server persistence
- Role, permission and ownership-based authorization

## Solution Structure

- `src/piLMS.Api` - Web API entry point
- `src/piLMS.Application` - Application logic and use cases
- `src/piLMS.Domain` - Domain model and business rules
- `src/piLMS.Infrastructure` - Infrastructure integrations
- `tests/piLMS.Tests` - Automated tests
