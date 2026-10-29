# FestPass — Campus Event Booking System

A Java-based CLI application for managing campus events, student registrations, seat availability, and booking cancellations. This project also demonstrates automated testing and CI/CD using Jenkins.

## Features
- Event creation and seat management
- Student booking and cancellation
- File-based data persistence
- Input validation and error handling
- Automated testing and JAR packaging with Jenkins

## Tech Stack
Java 21 · Git · Jenkins · TSV File Storage

## Getting Started

**Run tests and build the JAR:**
```bash
java ci/Build.java verify
```

**Run the application:**
```bash
java -jar build/festpass.jar help
```

**Run smoke tests:**
```bash
java ci/SmokeTest.java
```

## Jenkins Pipeline

The Jenkins pipeline automates:
1. Source code checkout
2. Automated testing
3. JAR packaging
4. Smoke testing
5. Build artifact and evidence archival

SCM polling is configured to check for repository changes every minute.

## Results
- **28 automated tests passed**
- **7 JAR smoke checks passed**
- Fixed booking cancellation and persistence behavior

## Project Structure
- `src/` — Application and test code
- `ci/` — Build, smoke test, and evidence scripts
- `Jenkinsfile` — Jenkins pipeline
- `submission/` — Assessment evidence and final JAR

## Author
**Riddhi Sharma**
