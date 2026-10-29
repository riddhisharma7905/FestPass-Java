# FestPass: Campus Event Booking System with Jenkins CI/CD

FestPass is a Java-based command-line application for managing campus events, student registrations, seat availability, and booking cancellations. The project integrates Jenkins to demonstrate automated testing, build validation, and continuous integration.

## Features

- **Event Management:** Create events with unique IDs, titles, and seat capacities.
- **Student Registration:** Book event seats while preventing duplicate registrations and overbooking.
- **Booking Cancellation:** Cancel existing bookings and release available seats.
- **Data Persistence:** Store event and booking information in local TSV files.
- **Input Validation:** Handle invalid commands, missing bookings, and capacity restrictions.
- **Automated CI Pipeline:** Use Jenkins to run tests, package the application, execute smoke tests, and archive build artifacts.

## Tech Stack

- **Language:** Java 21
- **Version Control:** Git
- **CI/CD:** Jenkins
- **Storage:** TSV-based file persistence

## Project Structure

```text
festpass-java/
├── src/                  # Application and test source code
├── ci/                   # Build, testing, and evidence scripts
├── data/                 # Local application data
├── Jenkinsfile           # Jenkins pipeline configuration
├── submission.properties # Assessment configuration
├── submission/            # Evidence files and final JAR
└── README.md
```

## Getting Started

Make sure Java 21 is installed, then run the following commands from the project directory.

**Run tests and build the application:**

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

## Jenkins CI Pipeline

The Jenkins pipeline automates the following stages:

1. Source code checkout
2. Submission setup and evidence preparation
3. Automated testing
4. JAR packaging after successful tests
5. Smoke testing of the packaged application
6. Artifact and build evidence archival

SCM polling is configured to check for repository changes every minute.

## Test Results

- **28 automated tests passed**
- **7 JAR smoke checks passed**
- Booking cancellation and persistence behavior corrected and verified

## Learning Outcomes

This project demonstrates Java application development, file-based persistence, business-rule validation, automated testing, debugging, Git version control, and Jenkins pipeline configuration.

## Author

**Riddhi Sharma**
