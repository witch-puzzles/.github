# Project Notes

## Details

**Group Name:** Witch
**Project Name:** Puzzles

**Project description:**

Our main goal is to create a platform to promote logic puzzles and games that are less-known or created by us, to support this community of puzzle enthusiasts.

We will be creating a repertoire of logic puzzles, where we are creating the algorithms for puzzle creation, solving and categorizing.

For this project, we are only going to be extending the repertoire for Sudoku. We will create a solver, a generator, and a cathegorizer for Sudoku puzzles.

After we have the repertoire ready, we will create a backend server and populate the puzzles and register them to our database. We will create a RestAPI and deploy it on _**(will be decided soon)**_.

Then, we will create a simplistic website to accommodate these puzzles and our leaderboard for the registered users to showcase their time of solving.


**Tech Stack:**
- Design: Figma
- Frontend: Svelte Kit, TypeScript
- Backend: FastAPI, SQLAlchemy, Python3.12
- Database: Alembic, PostgreSQL
- Externel Services: Firebase for Authentication
- Deployment: Vercel (Frontend), _**(will be decided soon)**_ (Backend) (Not decided yet)
- CI/CD: GitHub Actions
- Tests: PyTest (Backend)
- Communication and Project Management: GitHub
- Documentation: In GitHub, using Markdown & Swagger
- API: _**(will be decided soon)**_

**People & Roles:**
- Ertuğrul Şentürk - Backend Development - Project Leader
- Utku Biçer - Frontend Development - Design
- Hüseyin Şimşek - Backend Development - Puzzle Algorithm Developer
- Oğuzhan Altıntaş - DevOps & Backend Engineering
- Oğuz Eren Kacar - Backend Development
- Lucas Holczinger - Frontend Development - Design
- Ata Türköz - Frontend Development


## Tech Notes

*Labels:*
- ``(no code)`` label means that the task is not directly related to coding, but rather planning, designing, or discussing the code
- `(abstract code)` label means that the task is related to coding, but rather abstract and not directly related to the implementation of the project, like creating the structure of the project with all the necessary files, methods but leaving them blank


### Design

- Creating the general user design and user experience in Figma for Sudoku
  - This design should consist of all the themes and colors that will be used in the project and the animations/transitions that will be used for Sudoku's solving user experience
- Approving the design with the team
  - Everyone should be able to see the design and approve it


### Backend

#### *Puzzle Libs*
- Creating a general environment for Sudoku with interfaces and visualizations
- Creating the solver for Sudoku
- Creating the generator for Sudoku
- Creating the cathegorizer for Sudoku, to determine the difficulty
- Isolating the libs for the use in FastAPI and transferring them to the backend repository

#### *FastAPI*
- Creating the endpoint that will be used `(no code)`
- Database schema `(no code)`
- Creating the general structure of the backend (services, models, routers etc) `(abstract code)`
- Creating base unit tests
- SQLAlchemy entities and crud operations
- Alembic for database migrations
- Authentication services for Firebase
- Implementing FastAPI endpoints
- Creating Swagger documentation


### Frontend

#### *Authentication*
- Authenticate users with Firebase Auth
- Research JWT-based auth with Firebase (if necessary)
- Store user data for leaderboard system

#### *Landing Page*
- Login/registration options (using Firebase)
- If already authenticated redirect to puzzle page

#### *Puzzle & Leaderboard Page*
- Simplistic & intuitive design
    - Option to select difficulty (easy, intermediate, hard)
    - Fetch random puzzle and display its unique id
- Easy to use interface / UX when solving the puzzle
    - For Sudoku accept number key inputs (single digit)
- Display leaderboard below/beside the puzzle or hidden behind a toggle button
- Validate if the puzzle is solved on the client-side


### Deployment & DevOps

#### *Backend*
- Deplyoment of the backend on AWS
- Adding unit tests & CI/CD pipeline in GitHub Actions

#### *Frontend*
- Deployment of the frontend on Vercel
- Adding CI/CD pipeline in GitHub Actions
