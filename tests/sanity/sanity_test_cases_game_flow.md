# Sanity Test Cases for Game Flows and New User Experience

## TC 1: App Installation and Permissions
### Preconditions
- The user has a stable internet connection.
- Clean install of the app via APK file.
  
**Step 1:** Install the APK.  
**Expected:** APK installs successfully without errors.

**Step 2:** Launch the app and check if the notification permission prompt appears.  
**Expected:** The notification permission prompt will appear on the first launch.

**Step 3:** Grant Notification permission.  
**Expected:** App proceeds to the Home screen smoothly.

## TC 2: Initial Registration Screen (Choose Your Avatar)
### Preconditions
- The app was installed via clean APK installation (already completed in TC 1).
- User is launching the app for the **first time** after installation.
- User has a stable internet connection.

### Test Steps and Expected Results
**Step 1:** Select an avatar or upload a custom image.  
**Expected Result:** Avatar is selected or uploaded successfully without errors.

**Step 2:** Check that the username field is autofilled.  
**Expected Result:** Username appears automatically and is editable by the user.

**Step 3:** Tap on "Sign In" and enter a valid phone number.  
**Expected Result:** Phone number sign-in is completed successfully, **only if the country is supported**.

**Step 4:** Tap the "Next" button.  
**Expected Result:** App navigates to the tutorial screen.

## TC 3: Tutorial Mode
### Preconditions
- User has completed the registration flow.
- App navigated to tutorial mode for the first time.
- The device is connected to a stable internet connection.

### Test Steps and Expected Results
**Step 1:** Try to interact with elements allowed by the tutorial, elements **not** allowed by the tutorial, and press the "Next" button to finish the tutorial at any time.  
**Expected Result:** Interactions with tutorial-allowed elements and the "Next" button succeed. interactions with non-allowed elements are blocked or ignored.

**Step 2:** Observe the visual pointer guiding the user during the tutorial.  
**Expected Result:** The visual pointer clearly indicates the next required action to advance the tutorial.

**Step 3:** Press the "Next" button during the tutorial.  
**Expected Result:** The tutorial session ends immediately and navigates to the Game Over screen.

**Step 4:** Close or remove the app from memory during the tutorial, then relaunch the app.  
**Expected Result:** The tutorial resumes from the step where it was interrupted.

## TC 4: End Game Prompt
### Preconditions
- User is in tutorial mode and reaches the End Game prompt.

### Test Steps and Expected Results
**Step 1:** Press the "End" button to trigger the end game flow.  
**Expected Result:** The "End Game" confirmation dialog appears.

**Step 2:** Try to press the "Play On" button and the "Submit" button.  
**Expected Result:** The "Play On" button is present but disabled and does not respond. the "Submit" button is highlighted, enabled, and responds to the press. Press "Submit" leading the user to the "Game over" screen.

## TC 5: Game Over Screen
### Preconditions
- The game session has ended and the Game Over screen is triggered.

### Test Steps and Expected Results
**Step 1:** Wait for the Game Over screen to appear.  
**Expected Result:** The Game Over screen loads successfully without crashes or freezes.

**Step 2:** Check the displayed score, time bonus, and total score on the Game Over screen.  
**Expected Result:** Score, Time Bonus, and Total Score are calculated and displayed correctly.

**Step 3:** Press the "OK" or close (X) button to dismiss the Game Over screen.  
**Expected Result:** The screen exits smoothly and the app transitions to the "Leaderboard" screen.

## TC 6: Leaderboard Screen
### Preconditions
- User has completed a game session and arrived at the Leaderboard screen.

### Test Steps and Expected Results
**Step 1:** Wait for the Leaderboard screen to load.  
**Expected Result:** The Leaderboard screen loads without errors.

**Step 2:** Review the list of players displayed on the Leaderboard.  
**Expected Result:** Players are listed with the highest total score at the top, descending to the lowest.

**Step 3:** Check each player's entry for avatar, name, and score.  
**Expected Result:** Each entry shows the correct player avatar, name, and score.

**Step 4:** Press the "CLAIM" button next to your player entry to collect the reward.  
**Expected Result:** Reward is successfully collected and an animation plays.

**Step 5:** Observe the screen transition after claiming the reward.  
**Expected Result:** User is taken to the Game Lobby screen.

## TC 7: First Real Game
### Preconditions
- User is logged in and on the Game Lobby screen.
- User has sufficient diamonds to play.

### Test Steps and Expected Results
**Step 1:** Tap the "Play" button to start the game.  
**Expected Result:** The correct amount of diamonds (X) is deducted from the user's balance.

**Step 2:** Observe the game launch after tapping "Play".  
**Expected Result:** The game starts in standard (non-tutorial) mode, stable and fully functional.

**Step 3:** Attempt to interact with all standard game functions (e.g., move cards, click "Undo" button).  
**Expected Result:** All game functionalities respond normally without tutorial restrictions. The user is no longer in tutorial mode.

## TC 8: Daily Login Reward Screen
### Preconditions
- User has completed the tutorial and first real game.
- User is entering the main lobby for the first time (not in tutorial mode).

### Test Steps and Expected Results
**Step 1:** Wait on the main lobby screen after the first real game.  
**Expected Result:** The Daily Login Reward screen appears automatically without user action.

**Step 2:** Check the displayed login streak day on the reward screen.  
**Expected Result:** The current login streak day is displayed correctly.

**Step 3:** Tap the "Collect" button to claim the daily reward.  
**Expected Result:** The reward is added to the user's inventory.

**Step 4:** Observe the screen transition after collecting the reward.  
**Expected Result:** The app navigates automatically to the main lobby screen.

## TC 9: First Time Game Lobby Entry
**Steps:**
- Verify lobby screen loads without crashes or critical errors.
- Verify available game entry options are displayed.
- Verify tapping Play starts the game.
- Verify navigation between screens via bottom bar works without crashes.

**Expected Results:**
- Lobby loads with no errors.
- Game options are visible.
- Play works correctly.
- Navigation bar works stably.
