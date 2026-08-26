# IDS706-Assignment-1
[![Python tests](https://github.com/inmang13/IDS706-Assignment-1/actions/workflows/test.yml/badge.svg)](https://github.com/inmang13/IDS706-Assignment-1/actions/workflows/test.yml)

## Project Description

This project was built and used as a small Python data engineering demonstration. It provides a simple command-line application that welcomes a user by name and includes automated tests, Docker support, and continuous integration with GitHub Actions.

## Project Structure

- `src/main.py` - application code
- `tests/test_main.py` - automated tests
- `Dockerfile` - container configuration
- `Makefile` - common development commands
- `.github/workflows/test.yml` - GitHub Actions workflow

## Installation

Create and activate a virtual environment if desired, then install the project dependencies:

```bash
python -m pip install -r requirements.txt
```

Or use the Makefile:

```bash
make install
```

## Running the Application

Run the application with:

```bash
python src/main.py
```

Or:

```bash
make run
```

The program asks for a name and prints a welcome message.

Example:

```text
Enter your name: Ammy
Ammy, welcome to the Data Engineering course.
```

The main function, `welcome_message(name)`, accepts a name and returns a formatted welcome string.

## Running Tests

Run the tests locally with:

```bash
python -m pytest -q
```

Or:

```bash
make test
```

The GitHub Actions workflow runs the tests, builds the Docker image, and runs the test suite inside Docker for every push and pull request.

## Docker

Make sure Docker Desktop is running, then build and run the application:

```bash
make docker-build
make docker-run
```

To run the tests inside the container:

```bash
make docker-test
```

## Notes and Next Steps

This is intentionally a simple starter project. Potential next steps include adding more application functionality, expanding test coverage, pinning dependency versions, and adding data ingestion or transformation examples.
