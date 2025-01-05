# Test Specification Document

## Introduction

### Goal

The goal of our testing is to ensure that our Puzzles website functions correctly, reliably, and securely, meeting both user expectations and project requirements. Through testing, we aim to identify and eliminate potential issues in functionality and usability before deploying the system to users.

Our testing strategy includes both black-box testing and white-box testing. Black-box testing focuses on validating the system’s behavior by testing inputs and outputs against expected results without considering the internal code structure. White-box testing, on the other hand, involves examining the internal logic, structure, and individual components of the code to verify their correctness and robustness.

By adopting a systematic and comprehensive testing process, we aim to deliver a high-quality product that is reliable under all expected conditions.

### Contents and Organization
The document is structured as follows:
- Test Plan: Outline the overall strategy, subjects and methods used for testing
- Test Results: Results and analysis of information gathered from our tests


## Test Plan
### Testing Strategy
    For unit testing, we used the Python pytest module and created some unit test files.
    For module integration tests, we have used the bottom up approach as our project was slowly built from the tinier parts first.
    For the system testing, we used the black box testing method to track down the bugs that would cause the website to generate incorrect results from the specified inputs.

### Test Subjects
#### Backend Testing Subjects

##### User Authentication:

- Ensure that the user registration, login, and authentication flow works correctly with external services like Firebase Authentication.
- Validate the session management and token-based authentication (if implemented).
- Check that invalid or unauthorized users are properly blocked.

##### Puzzle Management:

- Ensure that puzzles are fetched correctly based on user selection (e.g., easy, medium, hard).
- Test the puzzle validation logic: Ensure that puzzle solutions are correctly validated (including checking for time limits and duplication).
- Ensure that puzzle completion records are updated correctly in the database.

##### Leaderboard Management:

Validate that the leaderboard correctly updates when a new puzzle is solved and that rankings are recalculated based on new completion times.
Ensure that the system retrieves and displays the leaderboard data for specific categories (easy, medium, hard).

3. Database Testing

The database stores user data, puzzle data, leaderboard rankings, and completion records. The tests here should focus on ensuring data integrity, retrieval, and storage efficiency.
Test Subjects:

    User Data Storage:
        Validate the correct storage of user data (e.g., name, email, password hash).
        Test user data retrieval (e.g., after login) to ensure correct information is returned.
    Puzzle Data Storage:
        Ensure puzzle data (metadata, difficulty, etc.) is correctly stored and retrieved for each puzzle.
    Leaderboard Data Storage:
        Validate that leaderboard rankings are stored correctly, and that updates are performed when new solutions are logged.
        Test for data consistency and accuracy in the leaderboard records (e.g., rank order, timestamps).

4. API Testing

Since the frontend communicates with the backend via REST APIs, thorough API testing is required to ensure data flows correctly between these components.
Test Subjects:

    User API:
        Test registration and login endpoints to ensure proper authentication and error handling.
        Ensure that profile management APIs work correctly (e.g., updating user details).
    Puzzle API:
        Test endpoints for fetching puzzle data, submitting solutions, and validating answers.
        Ensure the API correctly handles edge cases such as invalid solutions or time limits.
    Leaderboard API:
        Test endpoints for fetching leaderboard data, filtering by difficulty, and updating rankings.
        Ensure the API returns accurate and correctly formatted leaderboard data.

5. Functional Testing

Ensure that all the system components interact correctly and that the application functions as intended.
Test Subjects:

    Puzzle Solving Flow:
        Test the entire process of puzzle solving, including selecting a puzzle, submitting a solution, validating the solution, and updating the leaderboard.
    Leaderboard Viewing:
        Test the process of viewing the leaderboard, selecting difficulty levels (easy, medium, hard), and confirming the correct leaderboard is displayed.
    Profile Updates:
        Ensure that the user can view and update their profile information and that changes are reflected correctly.

6. Integration Testing

Test the interactions between different system components, ensuring they work together as expected.
Test Subjects:

    Frontend and Backend:
        Ensure that the frontend correctly interacts with the backend via the APIs. For example, a user logs in, selects a puzzle, submits a solution, and sees the leaderboard update in real time.
    Backend and Database:
        Test that the backend properly interacts with the database, particularly when saving and retrieving user data, puzzle completions, and leaderboard data.

7. Security Testing

Since the system handles user data and authentication, security is a key area of testing.
Test Subjects:

    Authentication and Authorization:
        Ensure that unauthorized access is blocked and that sensitive data (like passwords) is securely hashed and stored.

    Data Privacy:
        Ensure that user data is handled and transmitted securely (e.g., over HTTPS, data encryption).

    API Security:
        Test for common security vulnerabilities such as SQL injection, XSS, CSRF, and rate-limiting issues in the APIs.

8. Performance Testing

Evaluate the system's performance under normal and peak loads to ensure it can handle traffic efficiently.
Test Subjects:

    Load Testing:
        Simulate high traffic, such as multiple users logging in, solving puzzles, and updating leaderboards simultaneously.
    Response Time Testing:
        Measure how quickly API endpoints respond under varying load conditions.

9. Usability Testing

Ensure the user experience is smooth and intuitive.
Test Subjects:

    UI/UX:
        Test that the UI is user-friendly, intuitive, and easy to navigate.
        Ensure consistency in the layout and design across all pages (landing page, puzzle-solving interface, leaderboard, profile page).

Conclusion

Your testing specification should cover all these areas to ensure that each component of the system is thoroughly validated. The goal is to ensure that the entire system—frontend, backend, database, services, and APIs—works seamlessly together, while also focusing on edge cases, security, and performance to ensure a robust user experience.

## Test Results
### Analysis
### Logs
