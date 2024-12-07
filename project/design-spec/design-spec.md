# Design Specification

## 1. INTRODUCTION
The purpose of this document is to provide a detailed design specification for the Puzzles project. This includes the architecture, components, low-level designs, and diagrams to guide the implementation phase. The document is organized into system architecture and low-level design sections.

## 2. SYSTEM ARCHITECTURE

### 2.1 System Architecture
The system is divided into the following key components:

1. **Frontend**:
   - Responsible for user interface (UI) and interactions.
   - Implements pages such as the landing page, login, puzzle-solving interface, leaderboard, and profile page.

2. **Backend**:
   - Handles business logic, user authentication, puzzle management, and leaderboard updates.
   - Exposes REST APIs for frontend interactions.

3. **Database**:
   - Stores user data, puzzles and leaderboard rankings.
   - Uses a relational database for structured data and JSON for semi-structured data.

4. **Services**:
   - **User Service**: Manages user registration, authentication, and profile management.
   - **Puzzle Service**: Handles puzzle fetching, validation, and completion recording.
   - **Leaderboard Service**: Updates and retrieves leaderboard data.
   - **E-Mail Service**: Notifies users when a new record is broken in the leaderboard

### 2.2 Component (Package) Diagram
Below is a description of the inputs, outputs, and services of each component:

- **Frontend**:
  - **Inputs**: User interactions like puzzle selection, solving etc..
  - **Outputs**: Rendered pages, user feedback, and leaderboard updates.
  - **Services**: Consumes REST APIs for all functionalities.

- **Backend**:
  - **Inputs**: API requests from the frontend.
  - **Outputs**: JSON responses with data (e.g., puzzle details, user progress).
  - **Services**: Exposes endpoints for authentication, puzzle handling, and leaderboard management.

- **Database**:
  - **Inputs**: Insert, update, and delete queries from the backend.
  - **Outputs**: Query results (e.g., user data, leaderboard rankings).
  - **Services**: Provides structured and semi-structured data storage.

## 3. LOW LEVEL DESIGN

### 3.1 Class Diagrams

#### User Management
- **User**:
  - Attributes: `id`, `email`, `passwordHash`, `name`, `profileData`
  - Methods: `register()`, `login()`, `updateProfile()`

#### Puzzle Management
- **Puzzle**:
  - Attributes: `id`, `difficulty`, `data`, `solution`
  - Methods: `fetchPuzzle()`, `validateSolution()`

#### Leaderboard Management
- **Leaderboard**:
  - Attributes: `id`, `userId`, `puzzleId`, `completionTime`, `rank`
  - Methods: `updateRankings()`, `getLeaderboard()`

### 3.2 Sequence Diagrams

CREATE DIAGRAMS FOR THESE

#### User Registration
1. User submits registration details.
2. Backend validates data and creates user.
3. Confirmation is sent to the frontend.

#### Puzzle Solving
1. User selects a puzzle.
2. Puzzle data is fetched and displayed.
3. User submits a solution.
4. Backend validates the solution and updates progress.
5. Leaderboard is updated, and feedback is returned.

#### Viewing the Leaderboard

### 3.3 Data Flow Diagram (DFD)
Update and extend your DFDs (if necessary) submitted in the Requirements Analysis documents based on the explanations in Software Design lecture.
