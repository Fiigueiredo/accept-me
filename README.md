# Accept Me™
This repository is where I developed the Accept Me™ product in order to be part of the 100% free AWS RE/START CLOUD program offered by Generation Brasil.

---

<p align="center">
"Accept me™, I promise to help build this story" <br/>
</p>

<p align="center">
  <a href="#about"> About </a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#features"> Feats </a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#technologies-used"> Tech </a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#project-structure"> Structure </a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#deploy"> Deploy </a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#code-of-conduct"> Conduct </a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#license"> License </a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</p>

## About
By separating the frontend from the backend, **Accept Me™** not only improves application maintenance and scalability, but also offers a more agile and secure user experience. This separation allows for faster, more independent updates to each part of the system, ensuring that you always have access to the best functionality and the latest security without compromising application stability.

`frontend` - **The Gateway to Entertainment**
<br>The Accept Me front-end offers an intuitive and visually appealing interface. Its design ensures seamless navigation on both desktop and mobile devices.

`backend` - **The Heart of the Project**
<br>The Accept Me backend handles business logic and data management, ensuring secure and efficient processing and storage of interactions.

## Features
- Records creation and management.
- Data validation.
- Database migrations.
- Automatic documentation.
- Integration with MySQL.
- Management InterfaceInteractive

## Technologies Used
To set up the project, make sure you have Maven installed and configured correctly. You can access the [pom.xml](https://github.com/Fiigueiredo/accept-me/blob/main/backend/pom.xml) and [package.json](https://github.com/Fiigueiredo/accept-me/blob/main/frontend/package.json) file to see the dependencies and plugins you need:

- Axios
- Flyway
- Java 17
- Lombok
- ModelMapper
- MySQL 8.0
- React 18
   - Dom
   - Router Dom
- Spring Boot 3.3.1
   - DevTools
   - Starter Data JPA
   - Starter Test
   - Starter Validation
   - Starter Web
- SpringDoc OpenAPI
- TailwindCSS
   - PostCSS
- Vite

## Project Structure
<details>
<summary>Click to view folder structure</summary>

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
│   ├── HELP.md
│   ├── mvnw
│   ├── mvnw.cmd
│   ├── pom.xml
│   └── README.md
│
│
└── frontend/
    │
    ├── node_modules/
    │   └── (unversioned)
    │
    ├── public/
    │   ├── brand/
    │   │   ├── default/
    │   │   └── special/
    │   │
    │   └── others/
    │
    ├── src/
    │   ├── assets/
    │   │   ├── dist/
    │   │   └── img/
    │   │
    │   ├── components/
    │   │   ├── Button/
    │   │   ├── Footer/
    │   │   ├── Header/
    │   │   ├── PageWrapper/
    │   │   └── TypingEffect/
    │   │
    │   ├── pages/
    │   │   ├── About/
    │   │   │   └── index.jsx
    │   │   │
    │   │   ├── Auth/
    │   │   │   ├── signin/
    │   │   │   └── signup/
    │   │   │
    │   │   ├── Contact/
    │   │   │   └── index.jsx
    │   │   │
    │   │   ├── Error/
    │   │   │   └── index.jsx
    │   │   │
    │   │   ├── FAQ/
    │   │   │   └── index.jsx
    │   │   │
    │   │   └── Home/
    │   │       └── index.jsx
    │   │
    │   ├── routers/
    │   │   └── Router.jsx
    │   │
    │   ├── services/
    │   │   └── api.js
    │   │
    │   ├── App.jsx
    │   └── main.jsx
    │
    ├── index.html
    ├── package-lock.json
    ├── package.json
    ├── postcss.config.cjs
    ├── README.md
    ├── tailwind.config.js
    └── vite.config.js
```
</details>

### 1. Backend
The `backend` folder includes all the code needed to run the project's internal environment. To start the backend:

1. Navigate to the folder `backend`:

   ```bash
   cd accept-me/backend
   ```
2. Refer to the README inside the folder for specific instructions on how to set up and run the server environment.

### 2. Frontend
The `frontend` folder includes all the code needed to run the project's external environment. To start the frontend:

1. Navigate to the folder `frontend`:

   ```bash
   cd accept-me/frontend
   ```
2. Refer to the README inside the folder for specific instructions on how to set up and run the user environment.

## Deploy
> Visit our page! [Click here](https://accept-me-eta.vercel.app/)

## Code of Conduct
This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## License
Copyright (c) Accept Me™. All rights reserved.
This project is licensed under the [**Apache License 2.0**](https://github.com/Fiigueiredo/accept-me/tree/main?tab=Apache-2.0-1-ov-file) See the LICENSE.md file for more details.