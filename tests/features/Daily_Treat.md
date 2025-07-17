# Test Case Document: Daily Treat Feature

## Feature Description
The **Daily Treat** feature rewards users for launching the game each day. On the first app launch of the day, a full-screen popup is displayed **above the Game Lobby screen**, blocking interaction with the underlying UI. The user must tap anywhere on the popup to collect the daily reward (e.g., diamonds). This feature supports user retention and provides visual feedback via reward animations.

## Test Execution Summary

- **Test Type**: Manual Functional and Non-Functional Testing  
- **Device Used**: Samsung Galaxy S23 FE.  
- **OS Version**: Android 15, One UI 7.0  
- **App Version**: APK XX.XXX  
- **Date of Execution**: July 17, 2025.  
- **Tester**: Ben Nahum.  
- **Network Conditions**: Tested under both online and offline modes.
---

## Test Case 1: Daily Treat Appears on First App Launch of the Day

- **Preconditions**:
  - User has not opened the app yet today.
  - Internet connection is active.

- **Steps**: Launch the app.

- **Expected Result**: After launching and loading the app, the **Daily Treat** popup appears, fully covering the **Lobby** screen.

---

## Test Case 2: Daily Treat Requires Tap to Collect Reward

- **Preconditions**:
  - Daily Treat popup is visible.

**Steps**: Tap directly on the reward icon.

**Expected Result**:
  - Reward collection animation plays (e.g., diamonds fly to counter).
  - Daily Treat popup is dismissed.
  - Lobby screen becomes visible.

---

## Test Case 3: Tap Outside Button Still Collects Reward

- **Preconditions**: Daily Treat popup is visible.

- **Steps**: Tap anywhere on the popup (not necessarily a specific button).
  
- **Expected Result**:
  - Reward is collected successfully.
  - Diamonds animation is shown.
  - Lobby screen becomes visible

---

## Test Case 4: Daily Progress Resets If User Skips a Day

- **Preconditions**: User has not opened the app for more than 24 hours.
  
- **Steps**: Open the app.
  
- **Expected Result**: Daily Treat resets to Day 1.

---

## Test Case 5: Daily Treat Progress Continues on Consecutive Days

- **Preconditions**: User opened the app and collected reward yesterday.

- **Steps**: Open the app the next day.
- **Expected Result**:
  - Daily Treat shows next reward (Day 2, Day 3, etc.).
  - User sees visual feedback of progress.

---

## Test Case 6: Daily Treat Does Not Reappear After Collection on the Same Date

- **Preconditions**:
  - User has already collected the Daily Treat reward earlier today.
  - The app was closed after collecting the reward.

- **Steps**:
  1. Launch the app again on the same date after closing it.
  2. Observe whether the Daily Treat popup appears.

- **Expected Result**:
  - The Daily Treat popup **does NOT** appear again on the same day after the reward was collected.
  - User is taken directly to the Lobby screen without interruption.

---


## Test Case 7: Collected Reward Is Persisted After App Close

- **Preconditions**:
  - User taps to collect reward.
  - User closes the app immediately after tapping, either by:
    - Closing the app but leaving it in RAM (background),
    - Or force closing the app completely (removed from RAM

- **Steps**: Reopen the app.

- **Expected Result**:
  - Reward is still marked as collected.
  - Daily Treat popup is no longer shown.
  - Diamond counter is updated accordingly.

---

##need to continue

