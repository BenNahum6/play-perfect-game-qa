# Sanity Test Cases for Game Flows and New User Experience

## Preconditions
- Clean install of the app via APK file.
- User has stable internet connection.

## TC 1: App Installation and Permissions
- Verify APK installs successfully.
- Verify notification permission prompt appears on first launch.
- Verify app proceeds to home screen after permission is granted.

## TC 2: Initial Registration Screen (Choose Your Avatar)
- Verify background music plays.
- Verify user can select or upload avatar.
- Verify username is autofilled and editable.
- Verify phone number sign-in flow works correctly and is available only in supported countries.
- Verify pressing Next advances to tutorial.


## TC 3: Tutorial Mode
- Verify tutorial enforces required user actions (cannot skip confirmation dialogs).
- Verify visual pointer guides user to perform required actions that advance the tutorial.
- Verify that pressing the Next button ends the tutorial game session immediately and navigates to the Game Over screen.
- Verify tutorial session resumes from last step if app is closed or removed from memory mid-tutorial.

## TC 4: End Game Prompt
- Verify End Game button shows confirmation dialog.
- Verify "Submit" button confirms and ends tutorial game.
- Verify screen is dimmed except Submit button spotlight.
- Verify user cannot continue tutorial without selecting either Submit or Play On.

## TC 5: Game Over Screen
- Verify Game Over screen loads successfully without errors.
- Verify score, time bonus, and total score are displayed correctly.
- Verify Close (X) button dismisses the score screen without issues.
- Verify "OK" button proceeds correctly to the Leaderboard screen.

## TC 6: Leaderboard Screen
- Verify leaderboard screen loads without errors.
- Verify all players are listed sorted by total score descending.
- Verify each entry shows player avatar, name, and score.
- Verify "CLAIM" button successfully collects reward.
- Verify user is taken to Game Lobby after claiming reward.

## TC 7: First Real Game
- Verify tapping Play deducts X diamonds and starts the game.
- Verify game starts in standard mode without tutorial assistance.

## TC 8: Daily Login Reward Screen
- Verify Daily Login Reward screen appears once per day.
- Verify current login streak day is displayed correctly.
- Verify Collect button adds reward to inventory.
- Verify screen transitions to main lobby after collection.

## TC 9: First Time Game Lobby Entry
- Verify lobby screen loads without crashes or critical errors.
- Verify available game entry options are displayed.
- Verify tapping Play starts the game.
- Verify navigation between screens via bottom bar works without crashes.



