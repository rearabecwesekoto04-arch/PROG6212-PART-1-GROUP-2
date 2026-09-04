# RaceDay - Part 1: System Planning and Database

**Author:** Tlhologelo Rearabecwe Sekoto
**Module:** PROG (Programming) - Portfolio of Evidence
**Institution:** The Independent Institute of Education (IIE)

## System Description

RaceDay is a full-stack, web-based event management system built for the South African
road running, walking, and cycling community. It replaces the paper-based registration
and disconnected spreadsheets many local road events still rely on.

Event Organisers can create and manage events, define categories (e.g. 5km, 10km, half
marathon), and capture participant results. Participants can browse upcoming events,
enrol in a category, track their personal enrolment and results history, and prepare
for race day using event route and location details.

This repository covers **Part 1** of the Portfolio of Evidence: planning the system
before any application code is written. It contains the Entity Relationship Diagram,
the API endpoint plan, and the SQL database script for RaceDay.

## User Roles

- **Organiser** - can create, edit, and delete events; manage event categories; capture
  participant results; and view all enrolments for their own events.
- **Participant** - can create an account, browse events, enrol in an event by selecting
  a category, view their own enrolments, and track their personal results.

Role-based access is planned at the API level here in Part 1, enforced in the API in
Part 2, and reflected in the MVC interface in Part 3.

## Repository Structure

/docs
  ├── RaceDay_ERD.png                    # Entity Relationship Diagram
  ├── RaceDay_API_Endpoint_Plan.md       # Full API endpoint plan
  └── RaceDay_Database.sql               # Database creation + seed script
.github/workflows/validate-docs.yml      # CI/CD workflow (validates repo structure)
README.md                                # This file


## Setup Instructions (Part 1)

1. Clone the repository:
   ```
   git clone <https://github.com/rearabecwesekoto04-arch/PROG6212-PART-1-GROUP-2.git>
   cd <PROG6212 PART 1 Tlhologelo Rearabecwe Sekoto>
   ```
2. Open SQL Server Management Studio (SSMS) and connect to a local or clean SQL Server
   instance.
3. Open `/docs/RaceDay_Database.sql` and execute the script. This will:
   - Create the `RaceDayDB` database
   - Create all six tables (Roles, Users, Events, Categories, Enrolments, Results)
   - Seed the database with sample Organisers, Participants, Events, Categories,
     Enrolments, and Results
4. Review `/docs/RaceDay_ERD.png` for the full data model.
5. Review `/docs/RaceDay_API_Endpoint_Plan.md` for the planned API surface that Part 2
   will implement.

## CI/CD

A GitHub Actions workflow (`.github/workflows/validate-docs.yml`) runs on every push and
pull request to `main`. It checks that:
- the `/docs` folder exists,
- it contains an ERD file, an API endpoint plan, and a `.sql` script,
- a `README.md` exists at the repository root.

**Screenshot of successful green build:**

`[INSERT SCREENSHOT HERE - Actions tab, showing a green checkmark on the latest run]`

## Video Walkthrough

**YouTube (unlisted) link:** `[INSERT YOUTUBE LINK HERE]`

The video covers:
- The planning documents and how the repository is structured
- ERD design decisions (why each entity and relationship was chosen)
- API endpoint plan choices (routes, roles, request/response design)
- A live run-through of the SQL script in SSMS
