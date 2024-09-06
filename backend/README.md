# Accept Me™
Accept Me™ is an API developed as part of the practical programming challenge of the Amazon Web Services (AWS) collaboration and Generation Brasil. Using Spring Boot, JPA, and MySQL, the API offers a robust infrastructure for data management and REST functionality.

---

<p align="center">
"Accept me™, I promise to help build this story" <br/>
</p>

<p align="center">
  <a href="#backend"> Backend </a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#Requirements"> Requisites </a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#development"> Development </a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#contribution"> Contribution </a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#routes"> Routes </a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#documentation"> Doc </a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#deploy"> Deploy </a>
</p>

## Backend
This is the backend, a web application built with Java and booted with Spring and MySQL for data. This document provides instructions on how to set up and run the project locally.

<details>
<summary>CLICK HERE: View Folder Structure</summary>

```markdown
accept-me/
│
├── backend/
│   │
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/
│   │   │   │       └── accept/
│   │   │   │           ├── controllers/
│   │   │   │           │   └── StudentController.java
│   │   │   │           │
│   │   │   │           ├── dto/
│   │   │   │           │   └── StudentDTO.java
│   │   │   │           │
│   │   │   │           ├── entities/
│   │   │   │           │   └── Student.java
│   │   │   │           │
│   │   │   │           ├── repositories/
│   │   │   │           │   └── StudentRepository.java
│   │   │   │           │
│   │   │   │           ├── services/
│   │   │   │           │   └── StudentService.java
│   │   │   │           │
│   │   │   │           ├── Application.java
│   │   │   │           ├── Documentation.java
│   │   │   │           └── GlobalExceptionHandler.java
│   │   │   │
│   │   │   └── resources/
│   │   │       ├── db/
│   │   │       │    └── migration/
│   │   │       │        └── V1__create_students_table.sql
│   │   │       │
│   │   │       ├── application.yml
│   │   │       ├── application-dev.properties (unversioned)
│   │   │       └── application-dev.properties.example
│   │   │
│   │   └── test/
│   │       └── java/
│   │           └── com/
│   │               └── accept/
│   │                   └── ApplicationTests.java
│   │
│   ├── mvnw
│   ├── mvnw.cmd
│   ├── pom.xml
│   └── README.md
```
</details>

## Requisites
Make sure you have the following tools installed in your development environment:

- **Git** `>= 2.46.0` [Download Git](https://git-scm.com/downloads)
- **Java** `= 17.0` [Download JDK](https://www.oracle.com/java/technologies/downloads/)
- **Lombok** `>= 1.18.34` [Download Lombok](https://projectlombok.org/download/)
- **MySQL** `>= 8.0.38` [Download MySQL](https://dev.mysql.com/downloads/installer/)

## Development
Instructions for properly developing and versioning the project

### 1. Clone the Repository
---
Navigate to a location on your device:

```bash
git clone https://github.com/Fiigueiredo/accept-me.git
cd accept-me/backend
```
  > Note: Here we are cloning and changing the directory name to the current project name!

### 2. Check Requisites
---
Before you start, you need to have `Java 17` and `MySQL 8.0` installed on your operating system:

#### Chek JAVA
```bash
java -version
javac -version
```

Environment variables, if they have already been configured:

- ```bash
  echo %JAVA_HOME%
  ```

#### Chek MySQL Server
```bash
mysql -version
```

Environment variables, if they have already been configured:

- ```bash
  echo %MYSQL_HOME%
  ```

### 3. Install Dependencies
---
Install the dependencies you need to run the project. Using MAVEN (not required):

```bash
mvn clean install
```

### 4. Environment Variables
---
Whereas you're in the `backend` folder, copy the contents of `application-dev.properties.example` to a new file `application-dev.properties`.

```bash
cp src/main/resources/application-dev.properties.example src/main/resources/application-dev.properties
```

Configure the **DATABASE_URL**, **DATABASE_USERNAME**, and **DATABASE_PASSWORD** variables according to your local environment in the `application-dev.properties` file:

```bash
server.port='Your_port'
PROJECT_NAME='Name_of_your_project'

APP_LOCALE='pt_BR'
TIMEZONE='America/Sao_Paulo'

MYSQL_HOST='localhost
MYSQL_PORT='3306
MYSQL_DATABASE='BD_Name'

DATABASE_URL=jdbc:mysql://${MYSQL_HOST}:${MYSQL_PORT}/${MYSQL_DATABASE}?createDatabaseIfNotExist=true&useTimezone=true&serverTimezone=UTC

DATABASE_USERNAME='Your_MySQL_name'
DATABASE_PASSWORD='Your_MySQL_password'
```
> Note: Ignore single quotation marks

### 5. Build and Run
---
Use the following command to establish your application visually via the browser:

```bash
mvn spring-boot:run
```
> After startup, the project will be available at `http://localhost:{your_door}`

## Contribution
Instructions for developers and contributors to this project

### 1. Check Existing Branches
---
List all branches available in the Git repository, both local and remote branches.

```bash
git branch -a
```

### 2. Create a New Branch (if necessary)
---
Create a new branch for your task, replacing `name-surname` with your name and surname or a brief description of the task:

```bash
git checkout -b task/name-surname
```

### 3. Pull The Changes
---
Pull the changes contained in the development branch into your branch created in step 3:
  
```bash
git pull origin develop
```
> **Attention**: Regularly update your local `develop` branch with changes made in the remote repository!
  
### 4. Commit and Push
---
#### 4.1 Develop and Commit
- Implement your code changes, commit incrementally to [convention](https://www.conventionalcommits.org/en/v1.0.0/#specification) as needed, for example:

  ```bash
  git status
  git add .
  git commit -m "feat: add create method to the student controller"
  ```

#### 4.2 Push The Changes
- Verify that your changes work as expected.

  ```bash
  git push origin task/name-surname
  ```

### 5. Pull Request
---
#### 5.1 Create a Pull Request
- Open a Pull Request comparing `task/name-surname` with `develop` in the GitHub interface.

  ```bash
  [feat] Add endpoints for [brief description of added endpoints]
  ```

  Where:
  ```bash
  1. [feat] indicates the type of change. It can be replaced with [fix], [docs], [refactor], etc., depending on the type of change you are implementing.

  2. "Add endpoints for" is a clear description of what is being done in the Pull Request.
  
  3. [brief description of added endpoints] provides additional details about the functionalities or features that the endpoints introduce.
  ```

#### 5.2 Review and Integration

- Select **Reviewers** and have your **PR** reviewed by other team members. Upon approval, your changes will be integrated into the develop branch.

  - `develop`: *Team Leader*
  - `main`: *Supervisor(a)*

  > **PLEASE**: Don't forget to sign your Pull Request (required)

## Routes
`/students` - routes for students operations (Creating a CRUD) REST API.  

## Documentation
The API documentation is available at:

```bash
http://localhost:{your_door}/swagger-ui.html
```

## Deploy
> Visit our page! [Click here](https://accept-me-eta.vercel.app/)

<p align="center">
"Copyright (c) Accept Me™. All rights reserved." <br/>
</p>