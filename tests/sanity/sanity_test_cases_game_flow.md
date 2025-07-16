# Sanity Test Cases for Game Flows and New User Experience

## Preconditions
- Clean install of the app via APK file.
- User has stable internet connection.

## TC 1: App Installation and Permissions
**Steps:**
- Verify APK installs successfully.
- Verify notification permission prompt appears on first launch.
- Verify app proceeds to home screen after permission is granted.

**Expected Results:**
- App installs without errors.
- Permission prompt appears on first launch.
- Home screen loads successfully after permission approval.

## TC 2: Initial Registration Screen (Choose Your Avatar)
**Steps:**
- Verify user can select or upload avatar.
- Verify username is autofilled and editable.
- Verify phone number sign-in flow works correctly and is available only in supported countries.
- Verify pressing Next advances to tutorial.

**Expected Results:**
- Avatar selection and upload functions correctly.
- Username appears and can be edited.
- Phone number sign-in works in supported countries.
- Pressing Next navigates to tutorial.


## TC 3: Tutorial Mode
**Steps:**
- Verify tutorial enforces required user actions (cannot skip confirmation dialogs).
- Verify visual pointer guides user to perform required actions that advance the tutorial.
- Verify that pressing the Next button ends the tutorial game session immediately and navigates to the Game Over screen.
- Verify tutorial session resumes from last step if app is closed or removed from memory mid-tutorial.

**Expected Results:**
- Tutorial responds only after user completes guided actions.
- Visual pointer leads user to next step.
- Next button ends session and transitions to score summary.
- Tutorial resumes from same point after relaunch.

## TC 4: End Game Prompt
**Steps:**
- Verify "End Game" screen shows confirmation dialog.
- Verify screen is dimmed except "Submit" button spotlight.
- Verify user cannot continue tutorial without selecting either Submit or Play On.
- Verify "Submit" button confirms and ends tutorial game.

**Expected Results:**
- Confirmation dialog opens on End Game.
- Spotlight effect highlights Submit.
- User forced to choose "Submit" to proceed.
- Submit ends the tutorial and moves to Game Over.

## TC 5: Game Over Screen
**Steps:**
- Verify Game Over screen loads successfully without errors.
- Verify score, time bonus, and total score are displayed correctly.
- Verify "OK"/close (X) button dismisses the score screen without issues.

**Expected Results:**
- Game Over screen loads without crashes or freezes.
- Score, Time Bonus, and Total Score are calculated and displayed correctly.
- Pressing "OK" or close (X) exits the screen smoothly and transitions to the Leaderboard.

## TC 6: Leaderboard Screen
**Steps:**
- Verify leaderboard screen loads without errors.
- Verify all players are listed sorted by total score descending.
- Verify each entry shows player avatar, name, and score.
- Verify "CLAIM" button successfully collects reward.
- Verify user is taken to Game Lobby after claiming reward.

**Expected Results:**
- Leaderboard loads properly.
- Players sorted by score.
- Entries include full player info.
- CLAIM works and shows animation.
- User lands in Game Lobby after.

## TC 7: First Real Game
**Steps:**
- Verify tapping Play deducts X diamonds and starts the game.
- Verify game starts in standard mode without tutorial assistance.

**Expected Results:**
- Diamonds deducted accurately.
- Game launches in standard mode (non-tutorial), stable and fully functional.

## TC 8: Daily Login Reward Screen
**Steps:**
- Verify Daily Login Reward screen appears automatically.
- Verify current login streak day is displayed correctly.
- Verify Collect button adds reward to inventory.
- Verify screen transitions to main lobby after collection.

**Expected Results:**
- Bonus screen appears once daily.
- Login streak is accurate.
- Collect button works.
- App navigates to main lobby.

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
