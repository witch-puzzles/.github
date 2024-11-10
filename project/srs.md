# Software Requirements Specification (SRS)

## 1. INTRODUCTION

### Goal
The purpose of this document is to outline the functional and non-functional requirements for a puzzle-solving website. This platform is designed to engage users in solving puzzles, tracking their progress, and interacting with other users through a leaderboard and profile features.

### Contents and Organization
The document is structured as follows:
- System Requirements: Lists both functional and non-functional requirements.
- Use Cases: Outlines the various types of users, scenarios, and use cases, with diagrams illustrating the flow of actions within the system.

## 2. SYSTEM REQUIREMENTS

### Functional Requirements

1. **User Registration and Authentication**
   - The system will provide secure user registration, including a unique email requirement.
   - Users will have access to secure login, logout

2. **Puzzle Display and Solving**
   - Users can view puzzles and select their preferred difficulty level.
   - A timer will start with the puzzle, enabling competitive gameplay on leaderboards.
   - Users will be able to submit solutions to the leaderboard.

3. **Leaderboard and User Progress Tracking**
   - The platform will rank users on a leaderboard based on times achieved in puzzle-solving.
   - Users can view their scores and progress in the profile panel.
   - Scores and rankings will be updated in real-time based on solved puzzles and recorded times.

4. **Profile Panel**
   - Users can track their progress and view past performance.
   - The profile page will display completed puzzles and times, along with current rankings.

### Non-Functional Requirements

1. **Performance**  
   - The system should maintain page load times under 2 seconds under typical load.

2. **Security**  
   - Sensitive data, including passwords, will be encrypted. All sensitive actions (e.g., login, registration) will use HTTPS.

3. **Usability**  
   - The interface should be user-friendly and accessible on both desktop and mobile devices.

4. **Reliability**  
   - The platform aims for 99.9% uptime.

## 3. USE CASES

### 3.1 User Types

1. **Visitor**  
   - Can view available puzzles, view the leaderboard, and register for an account.

2. **Registered User**  
   - Can log in, solve puzzles, track progress, view the leaderboard, and update personal information.

### 3.2 User Scenarios

1. **Persona: Rümeysa, a casual puzzle enthusiast**  
   - Rümeysa logs in and selects an easy puzzle to start. She finishes the puzzle and checks the leaderboard to see where she ranks compared to others.

2. **Persona: Batuhan, a competitive puzzle solver**  
   - Batuhan loves challenging puzzles and tries to reach the top of the leaderboard. He completes multiple puzzles of increasing difficulty, tracking his performance in his profile panel.

### 3.3 Use Case Diagram

- **Overall System Use Case Diagram**  
  The main use case diagram will depict interactions between user types and the core functionalities: Registration and Authentication, Puzzle Display and Solving, Progress Tracking, and Leaderboard Viewing.

- **Additional Use Case Diagrams**  
  - Diagram for Registration and Authentication
  - Diagram for Puzzle Display and Solving
  - Diagram for Leaderboard and User Progress Tracking

### 3.4 Use Cases

#### Use Case 1: User Registration and Login

**Main Flow**
1. User navigates to the registration page.
2. User enters a unique email and password.
3. The system verifies and creates the account.
4. User logs in with credentials, and the system redirects them to the main puzzle page.

[![](https://mermaid.ink/img/pako:eNpdUtuOmzAQ_RXLz5CACSTw0ItUVaq0WlVb9aENUeXgASwZm9pm02w2_75j6K7S8uQzcy7jwRfaGAG0onEc19pLr6AiX6enJwWOfJx8D1hsuJdGk-8OLPmszKnWM7vFY9Nz68ndQ60Jfs4j2s88M4J2BPXkBEfCx_FA4vgdUaaTemFIRyz8nsB5EKQ1lvB_4wR4LpU7LNazcLYItA8X1_MRRxWSD0aLiCh-BFWRL45MwdxCJ9HYgnh_XQyCLOiff4B7nlG6vzMdQVcEZuAhWKnz4T_6vVnYbP8we9plutGaBpy7YbO36X5hera_2R7c0ObmsguuhdTd_p4_yg5JxJvXGhl5dytKbwU0ogPYgUuB_-0SSDXFqAFqWuERV4k7rWn0tzOD0OhBKUNOxipR01pf0Sfc_NtZN7TydoKIWjN1Pa1arhyiaRQ41ifJO8uHt6oyXICl1YX68xieTtgKejVGt7IL9ckqLPfej65ar0N71UnfT8dVY4a1kyI8mv6xLNYFK3acZVBsM55nmWiOablr2SZtxTZJGafXa0RHrn8aM7zOiDCE_KFVnCX5Ks03eZpsyl2yKcqInmnFWLpK2S7ZMbbNszIpGJo8zQ7papuXRVEkebLZ5mmJrRdGyf1E?type=png)](https://mermaid.live/edit#pako:eNpdUtuOmzAQ_RXLz5CACSTw0ItUVaq0WlVb9aENUeXgASwZm9pm02w2_75j6K7S8uQzcy7jwRfaGAG0onEc19pLr6AiX6enJwWOfJx8D1hsuJdGk-8OLPmszKnWM7vFY9Nz68ndQ60Jfs4j2s88M4J2BPXkBEfCx_FA4vgdUaaTemFIRyz8nsB5EKQ1lvB_4wR4LpU7LNazcLYItA8X1_MRRxWSD0aLiCh-BFWRL45MwdxCJ9HYgnh_XQyCLOiff4B7nlG6vzMdQVcEZuAhWKnz4T_6vVnYbP8we9plutGaBpy7YbO36X5hera_2R7c0ObmsguuhdTd_p4_yg5JxJvXGhl5dytKbwU0ogPYgUuB_-0SSDXFqAFqWuERV4k7rWn0tzOD0OhBKUNOxipR01pf0Sfc_NtZN7TydoKIWjN1Pa1arhyiaRQ41ifJO8uHt6oyXICl1YX68xieTtgKejVGt7IL9ckqLPfej65ar0N71UnfT8dVY4a1kyI8mv6xLNYFK3acZVBsM55nmWiOablr2SZtxTZJGafXa0RHrn8aM7zOiDCE_KFVnCX5Ks03eZpsyl2yKcqInmnFWLpK2S7ZMbbNszIpGJo8zQ7papuXRVEkebLZ5mmJrRdGyf1E)

**Alternative Flow**
- If the email is already in use, the system notifies the user and prompts for a different email.

#### Use Case 2: Puzzle Display and Solving

**Main Flow**  
1. User selects a puzzle from the list based on difficulty.
2. The puzzle interface loads, and the timer starts.
3. User inputs answers.
4. The system validates answers and provides feedback.
5. Upon completion, the system logs the user's time and updates the leaderboard.

[![](https://mermaid.ink/img/pako:eNp9k01v3CAQhv8K4uz9MM56bR_aSo0iVaqiqmkP7TqqMGAbBYMFOOlms_8946-N00P3sjDzzAvzjjlhZrjAGV6tVrn20iuRoW_d87MSDt0Z9Sh1hX46YdGNMk-5HrASlqym1qOv33ON4Oc87A431jRIUc37opZW4h6tVh8Qq41x4vB5-EPtIH4_1o2pBRXOmAUZUPs_TWa6oE5wZDTisiwl65Q_vqsJhyIH_YjDLX2UFfUCeTNGxqsucfKGT_0N3CUYHn7IBjyRbuxc8PsFtziMHAbvhrVDvv6n_ZEZ8a5opJ_wYT3ygHReGj1XDKnJAsEePp1cTVuYGZe0MZoH4H8hVIa-uEspYsZawfzH89wjFPYSL7-Ee0GUMdH6P0AfrqVrFT2i1jjpJXRcCsELyh4C5GrzhJSgXNjCUMsn5nKxN9Fb84K4YEpq8U5UC3D9vajQzHQW3O9n4e0R0YrKWXGhsTAUjcm3Sw85A1xjrLgcZtqh88uI--TkvZv055rF94QDDGNtqOTwIk49lmMYQiNynMGyBNr5HAdTZtj0iVooZdCTsYrnONdn0KGdN3dHzXDmbScCbE1X1TgrqXKw61oOX-C1pJWlzSWqTG8vzk7YH9v-UVbSedBiRpey6uOdVRCuvW9dttn06XUlfd0Va2aajZO8f5X1YxpvYhInlEQi3kd0F0WcFWGalOQqLPl-GxKKz-cAt1T_NqaZ7wjb_pC_OFul0Xa9D5OIkP0uSrcxCfARZySM1hGJtkm6S9N4m0YJiDwPCmQd7_ZRst2F8RUUxgk5vwJYMXVP?type=png)](https://mermaid.live/edit#pako:eNp9k01v3CAQhv8K4uz9MM56bR_aSo0iVaqiqmkP7TqqMGAbBYMFOOlms_8946-N00P3sjDzzAvzjjlhZrjAGV6tVrn20iuRoW_d87MSDt0Z9Sh1hX46YdGNMk-5HrASlqym1qOv33ON4Oc87A431jRIUc37opZW4h6tVh8Qq41x4vB5-EPtIH4_1o2pBRXOmAUZUPs_TWa6oE5wZDTisiwl65Q_vqsJhyIH_YjDLX2UFfUCeTNGxqsucfKGT_0N3CUYHn7IBjyRbuxc8PsFtziMHAbvhrVDvv6n_ZEZ8a5opJ_wYT3ygHReGj1XDKnJAsEePp1cTVuYGZe0MZoH4H8hVIa-uEspYsZawfzH89wjFPYSL7-Ee0GUMdH6P0AfrqVrFT2i1jjpJXRcCsELyh4C5GrzhJSgXNjCUMsn5nKxN9Fb84K4YEpq8U5UC3D9vajQzHQW3O9n4e0R0YrKWXGhsTAUjcm3Sw85A1xjrLgcZtqh88uI--TkvZv055rF94QDDGNtqOTwIk49lmMYQiNynMGyBNr5HAdTZtj0iVooZdCTsYrnONdn0KGdN3dHzXDmbScCbE1X1TgrqXKw61oOX-C1pJWlzSWqTG8vzk7YH9v-UVbSedBiRpey6uOdVRCuvW9dttn06XUlfd0Va2aajZO8f5X1YxpvYhInlEQi3kd0F0WcFWGalOQqLPl-GxKKz-cAt1T_NqaZ7wjb_pC_OFul0Xa9D5OIkP0uSrcxCfARZySM1hGJtkm6S9N4m0YJiDwPCmQd7_ZRst2F8RUUxgk5vwJYMXVP)

**Alternative Flow**  
- If the user submits an incorrect answer, they are given the option to retry.

#### Use Case 3: Leaderboard and Progress Tracking

**Main Flow**  
1. User views the leaderboard to see their rank based on completion times.
2. The system displays rankings in real-time.
3. User checks their progress in their profile panel.

[![](https://mermaid.ink/img/pako:eNp1kk2PmzAQhv-K5UO7K0GCIZiPQ0-rnvawatVLw6py8ABWjY1s05RE-e81hF2xh1qyNO98PGN7fMW15oBLHIZhpZxwEkr0Ml4uEix6BsbBnDQzHH1CL0a3BqxFPywY9FXqc6WWqsabdceMQ8_fKoX8ss6r45IHyoGxyHWA5AY3sBZeURh-2XqPT8IOkk0fMk_MAkdaIS6aRtSjdNPrvcs2ayHxXxYk1Gvnmil017504XrOBrLWkP_ByLHC7yCh7DCTgNXdh1x_PzOhB8V6CNCghXI2QIap38Gm12OF387MyYqPV_xni_RZ3TkP9hEJizrRdtJvB9wX4gD3YHomuB_TdcZU2D9nDxUuvdloPxRX4WCNLGIOdCClRmdtpKdU6uY5bHT6-6RqXDozQoCNHtsOlw2T1qtx4MzBk2CtYf27V-r5sri8YjcN809phXWeVWvViHb2j0Z6d-fcYMv9fg7vWuG68bSrdb-3gs9_o_tT0D2Nac7iBGiWsDRJeH0iRd7EB9LwLCIxw7dbgAemfmrdv53Ry7nJX1yGhyTakfRwyIoijw40z9IAT7gkebYjcR5Rz6A0Iin1lMuCILssLSilcUrTiBQRJbd_KUj3Ww?type=png)](https://mermaid.live/edit#pako:eNp1kk2PmzAQhv-K5UO7K0GCIZiPQ0-rnvawatVLw6py8ABWjY1s05RE-e81hF2xh1qyNO98PGN7fMW15oBLHIZhpZxwEkr0Ml4uEix6BsbBnDQzHH1CL0a3BqxFPywY9FXqc6WWqsabdceMQ8_fKoX8ss6r45IHyoGxyHWA5AY3sBZeURh-2XqPT8IOkk0fMk_MAkdaIS6aRtSjdNPrvcs2ayHxXxYk1Gvnmil017504XrOBrLWkP_ByLHC7yCh7DCTgNXdh1x_PzOhB8V6CNCghXI2QIap38Gm12OF387MyYqPV_xni_RZ3TkP9hEJizrRdtJvB9wX4gD3YHomuB_TdcZU2D9nDxUuvdloPxRX4WCNLGIOdCClRmdtpKdU6uY5bHT6-6RqXDozQoCNHtsOlw2T1qtx4MzBk2CtYf27V-r5sri8YjcN809phXWeVWvViHb2j0Z6d-fcYMv9fg7vWuG68bSrdb-3gs9_o_tT0D2Nac7iBGiWsDRJeH0iRd7EB9LwLCIxw7dbgAemfmrdv53Ry7nJX1yGhyTakfRwyIoijw40z9IAT7gkebYjcR5Rz6A0Iin1lMuCILssLSilcUrTiBQRJbd_KUj3Ww)

**Alternative Flow**  
- If no puzzles are completed, a prompt will encourage the user to try a puzzle.
