# Task Manager

Web application for managing tasks, built with Jakarta EE and PostgreSQL.

The system supports task registration, editing, filtering, completion tracking, and persistence through JPA.

## Features

- Create tasks with:
  - Number
  - Title
  - Description
  - Assignee
  - Priority
  - Status
  - Deadline
- List registered tasks.
- Edit and delete tasks.
- Mark tasks as completed.
- Filter tasks by:
  - Task number
  - Title
  - Description
  - Assignee
  - Priority
  - Status
- Clear tasks by status.
- Form validation and user-facing error messages.
- Layered separation between model, service/controller, and view.
- Dependency injection with CDI.
- Persistence with JPA and PostgreSQL.

## Tech Stack

- Java 21
- Jakarta EE
- JSF (JavaServer Faces)
- CDI
- JPA / Hibernate
- PostgreSQL
- Maven
- Apache Tomcat 11
- CSS

## Requirements

Before running the project, install:

- JDK 21
- PostgreSQL
- Maven
- Apache Tomcat 11
- An IDE with Jakarta EE support, such as IntelliJ IDEA

## Installation

Clone the repository:

```bash
git clone https://github.com/WendersonGomes/TaskManager.git
cd TaskManager
```

## Database Setup

Create a PostgreSQL database, for example:

```text
TaskManagerDB
```

Then edit:

```text
src/main/resources/META-INF/persistence.xml
```

Configure the JDBC connection for your local environment:

```xml
<property
    name="jakarta.persistence.jdbc.url"
    value="jdbc:postgresql://localhost:5432/TaskManagerDB"
/>

<property
    name="jakarta.persistence.jdbc.user"
    value="postgres"
/>

<property
    name="jakarta.persistence.jdbc.password"
    value="your-password"
/>
```

Do not commit real production credentials.

## Build

Using the Maven Wrapper:

### Linux / macOS

```bash
./mvnw clean package
```

### Windows

```powershell
mvnw.cmd clean package
```

Or, with Maven installed globally:

```bash
mvn clean package
```

## Deployment

1. Configure Apache Tomcat 11 in your IDE or local environment.
2. Deploy the generated WAR artifact.
3. Start Tomcat.
4. Open the application URL configured by your server.

## Project Structure

```text
src/main/
├── java/        # Java source code
├── resources/   # JPA configuration and resources
└── webapp/      # JSF pages and web resources
```

## Notes

The UI intentionally uses JSF and custom CSS rather than PrimeFaces.
