# FestPass Java — Jenkins CI Evidence

## Project
FestPass campus event booking and registration application.

## Build Results

| Build | Commit | Result | Evidence |
|---|---|---|---|
| #2 | ea506f9 | FAILED | Initial starter build; 3 test failures |
| #4 | d7a1a10 | FAILED | Help introduction change; 3 test failures |
| #5 | 5cef727 | SUCCESS | 28 tests passed; JAR smoke test passed |

Build #4 was manually started. Automatic SCM triggering was configured later in commit e06eaf9.

## Failure and Fix
The cancellation implementation did not remove a cancelled student from the event's student set. This caused cancellation and persistence tests to fail.

The fix removes the student from the event after validating the booking. The corrected build passed all 28 tests.

## Successful Artifact
Artifact: festpass.jar

The JAR help command was verified locally. Jenkins' successful smoke test passed 7 checks.

## Included Evidence
- build-2-evidence.csv
- build-4-evidence.csv
- build-5-evidence.csv
- festpass.jar

The CSV files contain the recorded Jenkins build evidence.
