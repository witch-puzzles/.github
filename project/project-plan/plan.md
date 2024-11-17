# Project Plan

## Details

**Date:** 27/10/2024

**Course:** BLG411E - Software Engineering

**Group Name:** Witch

**Project Name:** Puzzles


**People & Roles:**
- Ertuğrul Şentürk - Backend Development - Project Leader
- Utku Biçer - Frontend Development - Design
- Hüseyin Şimşek - Backend Development - Puzzle Algorithm Developer
- Oğuzhan Altıntaş - DevOps & Backend Engineering
- Oğuz Eren Kacar - Backend Development
- Lucas Holczinger - Frontend Development - Design
- Ata Türköz - Frontend Development


**Project description:**

Our main goal is to create a platform to promote logic puzzles and games that are less-known or created by us, to support this community of puzzle enthusiasts.

We will be creating a repertoire of logic puzzles, where we are creating the algorithms for puzzle creation, solving and categorizing.

For this project, we are only going to be extending the repertoire for Sudoku. We will create a solver, a generator, and a cathegorizer for Sudoku puzzles.

After we have the repertoire ready, we will create a backend server and populate the puzzles and register them to our database. We will create a RestAPI and deploy it on Convex.

Then, we will create a simplistic website to accommodate these puzzles and our leaderboard for the registered users to showcase their time of solving.


**Tech Stack:**
- Design: Figma
- Frontend: Svelte Kit, TypeScript
- Backend: FastAPI, SQLAlchemy, Python3.12
- Database: Alembic, PostgreSQL
- Externel Services: Firebase for Authentication
- Deployment: Vercel (Frontend), Convex (Backend) (Not decided yet)
- CI/CD: GitHub Actions
- Tests: PyTest (Backend)
- Communication and Project Management: GitHub
- Documentation: In GitHub, using Markdown & Swagger
- API: GitHub API


## Technical Deliverables

*Labels:*
- `(no code)` label means that the task is not directly related to coding, but rather planning, designing, or discussing the code
- `(abstract code)` label means that the task is related to coding, but rather abstract and not directly related to the implementation of the project, like creating the structure of the project with all the necessary files, methods but leaving them blank
- `(X)` X being an number, means X man.weeks of work
- `(SIZE)` SIZE being the size value, means the size of the task, could be XS, S, M, L, XL

### Design


#### *General Design* `(4)`

_Note: Everyone should be able to see the design and approve it_

- Deciding color palette and themes for the project `(S)`
- Creating the general user design and user experience in Figma for landing page `(L)`
- User experience of the Sudoku page, this design should consist of all the animations/transitions that will be used for Sudoku's solving user experience ``(XL)`
- Designing the leaderboard page `(L)`

### Backend

#### *Puzzle Libs* `(4)`
- Creating a general environment for Sudoku with interfaces and visualizations `(M)`
- Creating the solver for Sudoku `(M)`
- Creating the generator for Sudoku `(XL)`
- Creating the cathegorizer for Sudoku, to determine the difficulty `(L)`
- Isolating the libs for the use in FastAPI and transferring them to the backend repository `(XS)`

#### *FastAPI* `(6)`
- Creating the endpoint documents that will be used, deciding the enpoints, request and response type `(no code)` `(M)`
- Database schema `(no code)` `(M)`
- Creating the general structure of the backend (services, models, routers etc) `(abstract code)` `(M)`
- Creating base unit tests `(XL)`
- SQLAlchemy entities and crud operations `(XL)`
- Alembic for database migrations `(L)`
- Authentication services for Firebase `(L)`
- Implementing FastAPI endpoints `(L)`
- Creating Swagger documentation `(M)`


### Frontend

#### *Authentication* `(2)`
- Authenticate users with Firebase Auth `(M)`
- Research JWT-based auth with Firebase (if necessary) `(S)`
- Store user data for leaderboard system `(L)`

#### *Landing Page* `(2)`
- Implementing the design from Figma to Svelte `(L)`
- Login/registration options (using Firebase) `(L)`
- If already authenticated redirect to puzzle page `(XS)`

#### *Puzzle & Leaderboard Page* `(4)`
- Implementing the design from Figma to Svelte `(XL)`
    - Option to select difficulty (easy, intermediate, hard)
    - Fetch random puzzle and display its unique id
- Easy to use interface / UX when solving the puzzle `(L)`
    - For Sudoku accept number key inputs (single digit)
- Implementing the design for our leaderboard, displaying it below/beside the puzzle or with hidden behind a toggle button `(XL)`
- Validate if the puzzle is solved on the client-side `(M)`
- Get the repository star count information from GitHub API and display it `(M)`


### Deployment & DevOps

#### *Backend* `(3)`
- Deployment of the backend on Convex `(XL)`
- Adding unit tests to automatically run everytime a new push comes `(L)`
- Continues Deployment pipeline in GitHub Actions for the backend `(M)`

#### *Frontend* `(3)`
- Deployment of the frontend on Vercel `(L)`
- Adding CI/CD pipeline in GitHub Actions `(L)`


## Charts & Timeline

All the charts here are created by the Mermaid library, you can see the code for the charts [here](https://github.com/witch-puzzles/.github/blob/main/project/project-plan/charts).

Gantt Chart below is the graphical representation of the project plan. It shows the tasks, their start and end dates, and the dependencies between them.

[![](https://mermaid.ink/img/pako:eNqNlttu4zYQhl-FELCLXcAniZJs6y61m-0WCZo2DXpAbmhpLLORRYGknE2CvHuHOtIHtasrSeR8nPk5M-SbE4sEnMhJWa71Y07w0VxnQO6k-AdiTb6YAbLaMYnD9YQPH8gatjwHnLoHUuZcK_LpGeBJfa5nJEzDtZB7pgn5C5_x7e14va7HFFK5yBGheNoQVyITkhQsA62BsDwhegd7UOToiRJQ7oh4M88fu7MxnY3IbBI814gvkINkGcnQmucpwlIgSbXGCcJrEe54FuJ7A7gvE_FU1nYPf56b9gDaAzz0gTaAG2AJyI1gMhlYvQX4LcBDRu3BsTY_sPgJUIUxuStfX3E3bvhGHbkJ-YFLke8h1-Qj4bkGuWVxp1iU8c2JVO5xnEpkB5Bk6DEAFIptEUxq2AkgrQTXQg4DqAXwzpSOMUlSIfnrZTcMwLcACHO73TZ6EI4xsEqvLXpxzZS-uvt6iggshN8mzJDaDaMe_jFPCoHKkkTEZSV0LKFez16DFXwwKddMsw1TQFSM-cwGksogOq1rXKt165rSsox1KWHQB2oBPBug6golGpRWQ7uNRr4FoNZm_XpzlRnvXzDPVr89rIkozL6jC-oYEFgAvwdcZbDf8JjseXpmdgwILUBgy3jNJVQyXpXYF3LN41oCBfLAu6Q3iLmFCHsV2tyAZkvVoAoLCzC3cv6ZpSn-bVPhbAs6wNICLC7n2zUWrq4T7jigC9FWpd0Id7IWjg6U-M9__D42hISYSUSCAibj3Zm3ONjnXY3rRX9QJl5MYEw-IU0_M1WWWU2ug1Ab0iTfYMg3TYO-Q2QbcIq1oQW5P0CG_Z_vC8yZU5WjrHD7xjvvE-xGpDyfSkg5Vklt8swx7E7H1rzvZ4VVYk2HrTq2hASN4gubi-Z9NzOk_9nYhvrx6FToQ744fBZ3VGRWyB6--8dOmyZutMTzCo2lOFTmXXajfRdzjbpwVGmRppUr54dlkdHe3Goqq4zjMmPFEyAHlvHkYjmgud-b06PDmuufyg0xJTmU3zUg6AEDzXsNRSZemnNwDYdfCoXyN33zuIkm_dRL1Z_AwVLbtVrYQ98_ccWiVLshQCd3DesPrNXX6WpNCl5AZi5On1oFqiDUZwtBLYTXIr4n5jb7mqJqc_E_ozYL-peD_n6PA8tjv_bYGTl7wPsfT_Bu-WaAj051pXt0InzNeLrTj85j_o4TsWmI-5c8diI85GDkSFGmOyfaskzhV1mYy-SaM0ySfTsFyxR70m19da1usCMnEyannejN0S9FdaXFfoD_Y5FveWr-lzLD3zutCxVNp2Z4kmKjKDeTWOynmM3mkrs7LMNp6IUL5lEI55QFlCbxxl0utp7vbpP5zPWY8_4-cgqW_y1E5xN-mkW-ORENJpSGMy_w6GJG53jFc16caB5MluHMX8xpGMw9LwwR8VrZu5MZdf0ldRfhMpiFCxq-_wtMLVme?type=png)](https://mermaid.live/edit#pako:eNqNlttu4zYQhl-FELCLXcAniZJs6y61m-0WCZo2DXpAbmhpLLORRYGknE2CvHuHOtIHtasrSeR8nPk5M-SbE4sEnMhJWa71Y07w0VxnQO6k-AdiTb6YAbLaMYnD9YQPH8gatjwHnLoHUuZcK_LpGeBJfa5nJEzDtZB7pgn5C5_x7e14va7HFFK5yBGheNoQVyITkhQsA62BsDwhegd7UOToiRJQ7oh4M88fu7MxnY3IbBI814gvkINkGcnQmucpwlIgSbXGCcJrEe54FuJ7A7gvE_FU1nYPf56b9gDaAzz0gTaAG2AJyI1gMhlYvQX4LcBDRu3BsTY_sPgJUIUxuStfX3E3bvhGHbkJ-YFLke8h1-Qj4bkGuWVxp1iU8c2JVO5xnEpkB5Bk6DEAFIptEUxq2AkgrQTXQg4DqAXwzpSOMUlSIfnrZTcMwLcACHO73TZ6EI4xsEqvLXpxzZS-uvt6iggshN8mzJDaDaMe_jFPCoHKkkTEZSV0LKFez16DFXwwKddMsw1TQFSM-cwGksogOq1rXKt165rSsox1KWHQB2oBPBug6golGpRWQ7uNRr4FoNZm_XpzlRnvXzDPVr89rIkozL6jC-oYEFgAvwdcZbDf8JjseXpmdgwILUBgy3jNJVQyXpXYF3LN41oCBfLAu6Q3iLmFCHsV2tyAZkvVoAoLCzC3cv6ZpSn-bVPhbAs6wNICLC7n2zUWrq4T7jigC9FWpd0Id7IWjg6U-M9__D42hISYSUSCAibj3Zm3ONjnXY3rRX9QJl5MYEw-IU0_M1WWWU2ug1Ab0iTfYMg3TYO-Q2QbcIq1oQW5P0CG_Z_vC8yZU5WjrHD7xjvvE-xGpDyfSkg5Vklt8swx7E7H1rzvZ4VVYk2HrTq2hASN4gubi-Z9NzOk_9nYhvrx6FToQ744fBZ3VGRWyB6--8dOmyZutMTzCo2lOFTmXXajfRdzjbpwVGmRppUr54dlkdHe3Goqq4zjMmPFEyAHlvHkYjmgud-b06PDmuufyg0xJTmU3zUg6AEDzXsNRSZemnNwDYdfCoXyN33zuIkm_dRL1Z_AwVLbtVrYQ98_ccWiVLshQCd3DesPrNXX6WpNCl5AZi5On1oFqiDUZwtBLYTXIr4n5jb7mqJqc_E_ozYL-peD_n6PA8tjv_bYGTl7wPsfT_Bu-WaAj051pXt0InzNeLrTj85j_o4TsWmI-5c8diI85GDkSFGmOyfaskzhV1mYy-SaM0ySfTsFyxR70m19da1usCMnEyannejN0S9FdaXFfoD_Y5FveWr-lzLD3zutCxVNp2Z4kmKjKDeTWOynmM3mkrs7LMNp6IUL5lEI55QFlCbxxl0utp7vbpP5zPWY8_4-cgqW_y1E5xN-mkW-ORENJpSGMy_w6GJG53jFc16caB5MluHMX8xpGMw9LwwR8VrZu5MZdf0ldRfhMpiFCxq-_wtMLVme)

---

Pert Chart below showing the tasks and their dependencies in a more abstract way. Longest path is also marked with a different color

[![](https://mermaid.ink/img/pako:eNqdVltzozYU_isadjZPdhwQxpeHzqRxs92OZ5qum9mdYj_IcAxqZMQIQdbJ5L_3CCOMHe-0NU9I5zv3cz54dSIZgzN1NkI-RylTmsy_LDOCz8eP5EHJvyHSZKFRsL_N8aowx9AK69PqREr6_Z9IDIV77p7l_Oy94Ovz-FKnKGjDmkHBk4w8pKyA_aXxFN5JIRXJmQCtgbAsJjqFLRQrG4wXfoIMFBNEoJRnCYITMBI0t2oteRZPw0UZy6dyD3v89g5JLdIP58BiUGvJVHzeql9jc9FN5GcWPQHG2ScP5cuLADLn66Kbl6mIDQLfFVMc82llnpUVUlSgDoI28qROWMuOzLeyiGlIpOIvXU3XdsI7eLFX9GDfXvkHs_UVZmN6dzbHe1bo24fP3fzMJIS_oI7kmSaxjMot4EukgGkus5UdFy-cMc3WqEeKCJvKjstrEBZKQ-ux0KqMdKngYK-FUwv3EY5Wy4xroqHQxQGzz2gd8Shubd59HtzNGkgtaSagck_U8GUYLv6Y3woT745ckbsvjzMic9MODKXjZ2gVgvBWwHbNI7LlyTtYYGGj8J4rqItxi5uBBeNRDSYFqIpH0FEaWaVxaMsPTbk7qLFFTcLFM0sSUG0vTuo2-UGX75XM9L7NJzF1u232-Dh4goFAk-uqg2r33gt_-_pn3-Dj-kwUFMBUlHbQXoum4WNhgsdhwfZLZRZxg6QgDtvZ0aNnVrKTyLwhiQdj5ZhsmpXITTYJTqOWZFGBQNrh2xx7eFI4BDYKXjiXCc8GChKO87kv0TPHvGxZWhXrg4YNOdS0oiBGYHRk_F_yaNSvSJejTpOyIaKV8KzC2cQQXWtt6iVpfXa3xEJy4VnDhq1MYZFR0aqSVW23aBUsAVf-qQk_vBMcsf2Cx0AqJnh8HI5l2WH4ietfyzUxE_9-xjbd1fVtW6sfcdgMciF3NTVd4aH6PS-wrpYTjvls3DJCSxpxq95-Dir3f7lqK9vxhUm2GRxKf-RrD2yctB_se57xIoV41XE7l1mC7IczhqNY6J3A_uyF5gCdD_KGCzH9sJlEPZxf-QTTD5TS5r3_zGOdTv38e1fXfJwvU_MuU6OXqfkXqJnRvETrssyqS0Js2v-fNZ2eswW1ZTzG38JXY2np1D9SS2eKr0inOChLp9dI6oMRpCCEJM9SiXjpLLM3tIMkKxe7LHKmGyYK6DlKlknansoctxdmnOFybttbIQ3pONNXR-9y82tqmBKNRTLb8MTcl0rgdap1XkwHAyO-TpBCy_V1JLcDpAbzH5tWk2AQeMGYeRSCEWVDSuNo7U7GG893N_HoxvWY8_bWc3KW_SUlBoD_C1AfjZPvzpQOrykNbryhR8c3dOS6PWfnTEfD60lw449HNBiOPC8I0MRLre9e31DXn1B36HvuZOR6w7d_AFvWraQ?type=png)](https://mermaid.live/edit#pako:eNqdVltzozYU_isadjZPdhwQxpeHzqRxs92OZ5qum9mdYj_IcAxqZMQIQdbJ5L_3CCOMHe-0NU9I5zv3cz54dSIZgzN1NkI-RylTmsy_LDOCz8eP5EHJvyHSZKFRsL_N8aowx9AK69PqREr6_Z9IDIV77p7l_Oy94Ovz-FKnKGjDmkHBk4w8pKyA_aXxFN5JIRXJmQCtgbAsJjqFLRQrG4wXfoIMFBNEoJRnCYITMBI0t2oteRZPw0UZy6dyD3v89g5JLdIP58BiUGvJVHzeql9jc9FN5GcWPQHG2ScP5cuLADLn66Kbl6mIDQLfFVMc82llnpUVUlSgDoI28qROWMuOzLeyiGlIpOIvXU3XdsI7eLFX9GDfXvkHs_UVZmN6dzbHe1bo24fP3fzMJIS_oI7kmSaxjMot4EukgGkus5UdFy-cMc3WqEeKCJvKjstrEBZKQ-ux0KqMdKngYK-FUwv3EY5Wy4xroqHQxQGzz2gd8Shubd59HtzNGkgtaSagck_U8GUYLv6Y3woT745ckbsvjzMic9MODKXjZ2gVgvBWwHbNI7LlyTtYYGGj8J4rqItxi5uBBeNRDSYFqIpH0FEaWaVxaMsPTbk7qLFFTcLFM0sSUG0vTuo2-UGX75XM9L7NJzF1u232-Dh4goFAk-uqg2r33gt_-_pn3-Dj-kwUFMBUlHbQXoum4WNhgsdhwfZLZRZxg6QgDtvZ0aNnVrKTyLwhiQdj5ZhsmpXITTYJTqOWZFGBQNrh2xx7eFI4BDYKXjiXCc8GChKO87kv0TPHvGxZWhXrg4YNOdS0oiBGYHRk_F_yaNSvSJejTpOyIaKV8KzC2cQQXWtt6iVpfXa3xEJy4VnDhq1MYZFR0aqSVW23aBUsAVf-qQk_vBMcsf2Cx0AqJnh8HI5l2WH4ietfyzUxE_9-xjbd1fVtW6sfcdgMciF3NTVd4aH6PS-wrpYTjvls3DJCSxpxq95-Dir3f7lqK9vxhUm2GRxKf-RrD2yctB_se57xIoV41XE7l1mC7IczhqNY6J3A_uyF5gCdD_KGCzH9sJlEPZxf-QTTD5TS5r3_zGOdTv38e1fXfJwvU_MuU6OXqfkXqJnRvETrssyqS0Js2v-fNZ2eswW1ZTzG38JXY2np1D9SS2eKr0inOChLp9dI6oMRpCCEJM9SiXjpLLM3tIMkKxe7LHKmGyYK6DlKlknansoctxdmnOFybttbIQ3pONNXR-9y82tqmBKNRTLb8MTcl0rgdap1XkwHAyO-TpBCy_V1JLcDpAbzH5tWk2AQeMGYeRSCEWVDSuNo7U7GG893N_HoxvWY8_bWc3KW_SUlBoD_C1AfjZPvzpQOrykNbryhR8c3dOS6PWfnTEfD60lw449HNBiOPC8I0MRLre9e31DXn1B36HvuZOR6w7d_AFvWraQ)


## Project Risks

Since this is an open-source project whose main audience is puzzle enthusiasts, we don't expect any major risks. However, we have identified some risks that might affect the project:

- **Lack of communication:** Since we are working remotely, we might face some communication issues. We will have to make sure that we understand each other and communicate effectively.
- **Lack of user feedback:** For the best user experience for a puzzle platform, we need user feedback. During the time of main development, we might not have enough users to give feedback.
- **Lack of funding:** Since this is an open-source project, we might not have enough funding to extend and host the project for a broader audience.

