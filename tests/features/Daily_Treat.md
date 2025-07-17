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
  - 1. Launch the app again on the same date after closing it.
  - 2. Observe whether the Daily Treat popup appears.

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

## Test Case 8: Reward Not Collected → Popup "Daily RTreat" Reappears on Next Launch

- **Preconditions**:
  - User opened the app and saw the Daily Treat popup.
  - Did **not** tap to collect.
  - Closed the app:
    - Closing the app but leaving it in RAM (background),
    - Or force closing the app completely (removed from RAM)

- **Steps**: Reopen the app.

- **Expected Result**:
  - Daily Treat popup is shown again.
  - Reward collection remains pending.

---

## Test Case 9: Daily Treat Works Without Internet Connection

- **Preconditions**:
  - Device is offline.
  - It's the first launch of the day.

- **Steps**:
  1. Open the app.
  2. Tap to collect reward.

- **Expected Result**:
  - Daily Treat is displayed.
  - Reward is collected successfully.
  - Counter is updated.

---

## Test Case 10: Collect Daily Treat Reward After Losing Internet Connection

- **Preconditions**:
  - Launch the app with internet connection.
  - Daily Treat popup is displayed.

- **Steps**:
  1. Disable internet connection (e.g., turn on airplane mode).
  2. Tap anywhere on the Daily Treat popup to collect the reward.

- **Expected Result**:
  - Reward collection animation plays.
  - Diamonds are added to the counter.
  - App handles offline reward collection gracefully.

---

## Test Case 11: Animation of Diamonds Is Triggered on Reward Collect

- **Preconditions**: 
 - User is launching the app for the first time on day.
 - Daily Treat popup is active.

- **Steps**: Tap anywhere on the popup.

- **Expected Result**: Diamonds fly to the top of the screen toward the diamond counter.

---

## Test Case 12: Correct Diamond Count Is Added After Collection

- **Preconditions**:
  - User has a known diamond balance (e.g., 120).
  - Daily reward is known (e.g., +10).

- **Steps**: Tap to collect reward.

- **Expected Result**:
  - New balance should be 130.
  - Animation reflects this change.

---

## Test Case 13: Daily Treat Reward Not Granted Twice on Different Devices Same Day

- **Preconditions**:
  - User is logged into the same account (e.g., +972 54XXXXXXX) on Device A and Device B.
  - Daily Treat reward for today has been collected on Device A.

- **Steps**:
  1. On Device B, launch the app.
  2. Observe if the Daily Treat popup appears.

- **Expected Result**:
  - Daily Treat popup **does NOT** appear on Device B after the reward was collected on Device A.
  - Reward is not granted twice.
  - User is taken directly to the Lobby screen on Device B.

---

## Test Case 14: Daily Treat Reward Collection Synchronizes Across Devices

- **Preconditions**:
  - User is logged into the same account on Device A and Device B.
  - Both devices have internet connectivity.
  - Daily Treat reward for today has NOT been collected on either device.

- **Steps**:
  1. On Device A, open the app and collect the Daily Treat reward.
  2. Immediately, open or refresh the app on Device B.

- **Expected Result**:
- No Daily Treat popup appears on Device B.
- The rewards counter (e.g., diamond count) on Device B matches the updated counter from Device A.

---

## Test Case 15: Streak Progress Consistency Between Devices

- **Preconditions**:
  - User is logged into the same account on Device A and Device B.
  - Internet connection is active on both devices.
  - User has an active streak of N days recorded on Device A.

- **Steps**:
  1. On Device B, open the app.
  2. Verify the displayed streak day on the Daily Treat popup.

- **Expected Result**:
  - Streak day displayed on Device B matches the streak day on Device A.
  - Rewards correspond correctly to the current streak day on both devices.

---

## Test Case 16: Simultaneous Daily Treat Reward Collection on Two Devices

- **Preconditions**:
  - User is logged into the same account on **Device A** and **Device B**.
  - Both devices have an active internet connection.
  - Daily Treat popup is visible **simultaneously** on both devices.
  - Daily Treat reward for today has **not** been collected yet.

- **Steps**:
  1. On **Device A**, tap to collect the Daily Treat reward.
  2. At the **same time**, tap to collect the reward on **Device B**.

- **Expected Result**:
  - **Only one reward** is granted for the current day.
  - The second device shows the reward was already collected or skips the reward animation.
  - No duplicate rewards are added to the player's balance (e.g., coins or diamonds).
  - The **reward counter** and **streak progress** remain synchronized across both devices.
  - Optionally, Device B may display a message:  
    `"Reward already collected today."`

---

## Test Case 17: Offline Device Synchronization After Reconnecting

- **Preconditions**:
  - User is logged into the same account on Device A and Device B.
  - Device A collects the Daily Treat reward online.
  - Device B is offline (no internet).

- **Steps**:
  1. On Device B, open the app (offline).
  2. Observe if Daily Treat popup appears.
  3. Reconnect Device B to the internet.
  4. Refresh or reopen the app on Device B.

- **Expected Result**:
  - Initially, Device B may show the Daily Treat popup.
  - After reconnecting, Device B syncs and recognizes the reward was collected on Device A.
  - Daily Treat popup no longer appears.
  - Streak progress is updated accordingly.

---

## Notes:
- Observed no critical bugs in the flow; app behavior is consistent.

