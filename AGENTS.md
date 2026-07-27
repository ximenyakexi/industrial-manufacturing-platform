# Industrial Manufacturing Platform Instructions

## Project purpose

This repository is a personal portfolio project demonstrating
industrial data integration from a simulated PLC through SCADA, SQL databases,
backend APIs, web applications, MQTT/Sparkplug, containers, and Azure.

All equipment and production data are simulated.

## Repository structure

- `plc/` — Rockwell CCW and later Siemens PLC learning files
- `ignition/` — Ignition exports, scripts, and documentation
- `database/` — SQL Server migrations, seed data, and queries
- `backend/` — .NET 10 backend API and Worker Services
- `frontend/` — React and TypeScript application
- `mqtt/` — MQTT and Sparkplug configuration and examples
- `infrastructure/` — Docker, GitHub Actions, and Azure deployment
- `tests/` — integration and system test materials
- `docs/` — architecture, decisions, screenshots, and case studies

## Working rules

1. Inspect relevant files before making changes.
2. Explain the proposed plan before editing.
3. Complete only one task ID at a time.
4. Do not redesign unrelated parts of the project.
5. Make small, reviewable changes.
6. Run relevant builds, tests, formatting, linting, and type checks.
7. Report all commands run and their results.
8. Clearly state assumptions and unresolved risks.

## Security and privacy

Never add or expose:

- Passwords, tokens, API keys, or connection strings
- Employer code or documents
- Real plant names or locations
- Real PLC IP addresses
- Proprietary PLC tag databases
- Employer screenshots
- Database backups containing real information
- Certificates or private keys

Use `.env.example` files containing placeholders only.

## PLC rules

PLC code in this repository is educational, non-safety training code.

- Never claim that generated PLC code is safety-rated.
- Never bypass PLC permissives or interlocks.
- Validate externally written values locally in the PLC.
- Human review and simulator testing are required.
- Generate state tables, pseudocode, and test cases before implementation.

## Backend rules

- Use .NET 10.
- Enable nullable reference types.
- Use dependency injection.
- Use asynchronous methods and cancellation tokens when appropriate.
- Return Problem Details for API errors.
- Use UTC timestamps.
- Do not expose database entities directly from APIs.
- Add tests for business rules and state transitions.

## Frontend rules

- Use React and strict TypeScript.
- Include loading, empty, error, stale, and forbidden states.
- Use accessible labels and keyboard navigation.
- Never store secrets in frontend code.
- The backend remains responsible for authorization.

## Database rules

- Use SQL Server.
- Use numbered migrations.
- Use primary keys, foreign keys, constraints, and justified indexes.
- Preserve alarms, recipe versions, batch records, and audit history.
- Never overwrite an approved recipe version.
- Store timestamps in UTC.

## Definition of done

A task is complete only when:

1. The requested feature is implemented.
2. Relevant tests pass.
3. Build, formatting, linting, and type checks pass.
4. Documentation is updated.
5. No secrets or employer information were added.
6. Changed files and commands are summarized.
7. Remaining assumptions and risks are identified.