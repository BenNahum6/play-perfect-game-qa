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
  1. User has not opened the app yet today.
  2. Internet connection is active.

- **Steps**:
  1. Launch the app.

- **Expected Result**:
  1. After launching and loading the app, the **Daily Treat** popup appears, fully covering the **Lobby** screen.

---

## Test Case 2: Daily Treat Requires Tap to Collect Reward

- **Preconditions**:
  1. Daily Treat popup is visible.

- **Steps**:
  1. Tap directly on the reward icon.

- **Expected Result**:
  1. Reward collection animation plays (e.g., diamonds fly to counter).
  2. Daily Treat popup is dismissed.
  3. Lobby screen becomes visible.

---

## Test Case 3: Tap Outside Button Still Collects Reward

- **Preconditions**:
  1. Daily Treat popup is visible.

- **Steps**:
  1. Tap anywhere on the popup (not necessarily a specific button).
  
- **Expected Result**:
  1. Reward is collected successfully.
  2. Diamonds animation is shown.
  3. Lobby screen becomes visible

---

## Test Case 4: Daily Progress Resets If User Skips a Day

- **Preconditions**:
  1. User has not opened the app for more than 24 hours.
  
- **Steps**:
  1. Open the app.
  
- **Expected Result**:
  1. Daily Treat resets to Day 1.

---

## Test Case 5: Daily Treat Progress Continues on Consecutive Days

- **Preconditions**:
  1. User opened the app and collected reward yesterday.

- **Steps**:
  1. Open the app the next day.

- **Expected Result**:
  1. Daily Treat shows next reward (Day 2, Day 3, etc.).
  2. User sees visual feedback of progress.

---

## Test Case 6: Daily Treat Does Not Reappear After Collection on the Same Date

- **Preconditions**:
  1. User has already collected the Daily Treat reward earlier today.
  2. The app was closed after collecting the reward.

- **Steps**:
  1. Launch the app again on the same date after closing it.
  2. Observe whether the Daily Treat popup appears.

- **Expected Result**:
  1. The Daily Treat popup **does NOT** appear again on the same day after the reward was collected.
  2. User is taken directly to the Lobby screen without interruption.

---


## Test Case 7: Collected Reward Is Persisted After App Close

- **Preconditions**:
  1. User taps to collect reward.
  2. User closes the app immediately after tapping, either by:
     - Closing the app but leaving it in RAM (background),
     - Or force closing the app completely (removed from RAM

- **Steps**: Reopen the app.

- **Expected Result**:
  1. Reward is still marked as collected.
  2. Daily Treat popup is no longer shown.
  3. Diamond counter is updated accordingly.

---

## Test Case 8: Reward Not Collected → Popup "Daily RTreat" Reappears on Next Launch

- **Preconditions**:
  1. User opened the app and saw the Daily Treat popup.
  2. Did **not** tap to collect.
  3. Closed the app:
     - Closing the app but leaving it in RAM (background),
     - Or force closing the app completely (removed from RAM)

- **Steps**:
  1. Reopen the app.

- **Expected Result**:
  1. Daily Treat popup is shown again.
  2. Reward collection remains pending.

---

## Test Case 9: Daily Treat Works Without Internet Connection

- **Preconditions**:
  1. Device is offline.
  2. It's the first launch of the day.

- **Steps**:
  1. Open the app.
  2. Tap to collect reward.

- **Expected Result**:
  1. Daily Treat is displayed.
  2. Reward is collected successfully.
  3. Counter is updated.

---

## Test Case 10: Collect Daily Treat Reward After Losing Internet Connection

- **Preconditions**:
  1. Launch the app with internet connection.
  2. Daily Treat popup is displayed.

- **Steps**:
  1. Disable internet connection (e.g., turn on airplane mode).
  2. Tap anywhere on the Daily Treat popup to collect the reward.

- **Expected Result**:
  1. Reward collection animation plays.
  2. Diamonds are added to the counter.
  3. App handles offline reward collection gracefully.

---

## Test Case 11: Animation of Diamonds Is Triggered on Reward Collect

- **Preconditions**: 
 1. User is launching the app for the first time on day.
 2. Daily Treat popup is active.

- **Steps**:
  1. Tap anywhere on the popup.

- **Expected Result**:
  1. Diamonds fly to the top of the screen toward the diamond counter.

---

## Test Case 12: Correct Diamond Count Is Added After Collection

- **Preconditions**:
  1. User has a known diamond balance (e.g., 120).
  2. Daily reward is known (e.g., +10).

- **Steps**:
  1. Tap to collect reward.

- **Expected Result**:
  1. New balance should be 130.
  2. Animation reflects this change.

---

## Test Case 13: Daily Treat Reward Not Granted Twice on Different Devices Same Day

- **Preconditions**:
  1. User is logged into the same account (e.g., +972 54XXXXXXX) on Device A and Device B.
  2. Daily Treat reward for today has been collected on Device A.

- **Steps**:
  1. On Device B, launch the app.
  2. Observe if the Daily Treat popup appears.

- **Expected Result**:
  1. Daily Treat popup **does NOT** appear on Device B after the reward was collected on Device A.
  2. Reward is not granted twice.
  3. User is taken directly to the Lobby screen on Device B.

---

## Test Case 14: Daily Treat Reward Collection Synchronizes Across Devices

- **Preconditions**:
  1. User is logged into the same account on Device A and Device B.
  2. Both devices have internet connectivity.
  3. Daily Treat reward for today has NOT been collected on either device.

- **Steps**:
  1. On Device A, open the app and collect the Daily Treat reward.
  2. Immediately, open or refresh the app on Device B.

- **Expected Result**:
  1. No Daily Treat popup appears on Device B.
  2. The rewards counter (e.g., diamond count) on Device B matches the updated counter from Device A.

---

## Test Case 15: Streak Progress Consistency Between Devices

- **Preconditions**:
  1. User is logged into the same account on Device A and Device B.
  2. Internet connection is active on both devices.
  3. User has an active streak of N days recorded on Device A.

- **Steps**:
  1. On Device B, open the app.
  2. Verify the displayed streak day on the Daily Treat popup.

- **Expected Result**:
  1. Streak day displayed on Device B matches the streak day on Device A.
  2. Rewards correspond correctly to the current streak day on both devices.

---

## Test Case 16: Simultaneous Daily Treat Reward Collection on Two Devices

- **Preconditions**:
  1. User is logged into the same account on **Device A** and **Device B**.
  2. Both devices have an active internet connection.
  3. Daily Treat popup is visible **simultaneously** on both devices.
  4. Daily Treat reward for today has **not** been collected yet.

- **Steps**:
  1. On **Device A**, tap to collect the Daily Treat reward.
  2. At the **same time**, tap to collect the reward on **Device B**.

- **Expected Result**:
  1. **Only one reward** is granted for the current day.
  2. The second device shows the reward was already collected or skips the reward animation.
  3. No duplicate rewards are added to the player's balance (e.g., coins or diamonds).
  4. The **reward counter** and **streak progress** remain synchronized across both devices.
  5. Optionally, Device B may display a message:  
    `"Reward already collected today."`

---

## Test Case 17: Offline Device Synchronization After Reconnecting

- **Preconditions**:
  1. User is logged into the same account on Device A and Device B.
  2. Device A collects the Daily Treat reward online.
  3. Device B is offline (no internet).

- **Steps**:
  1. On Device B, open the app (offline).
  2. Observe if Daily Treat popup appears.
  3. Reconnect Device B to the internet.
  4. Refresh or reopen the app on Device B.

- **Expected Result**:
  1. Initially, Device B may show the Daily Treat popup.
  2. After reconnecting, Device B syncs and recognizes the reward was collected on Device A.
  3. Daily Treat popup no longer appears.
  4. Streak progress is updated accordingly.

---

### Test Case 18: Timezone Manipulation

- **Preconditions:**
  1. Device is set to real timezone.
  2. User has collected reward today.

- **Steps:**
  1. Change device timezone backward (e.g., +3 → -5).
  2. Relaunch app.

- **Expected Result:**
  1. App uses server time, not device time.
  2. Daily Treat is not shown again based on fake timezone.

---

### Test Case 19: Concurrent Logins From 3+ Devices

- **Preconditions:**
  1. User is logged in on Device A, B, and C (simultaneously).
  2. Open the App in three divices (A & B & C).

- **Steps:**
 1. Collect reward from Device A.
 2. Open app on Device B and C simultaneously.

- **Expected Result:**
  1. No reward duplication.
  2. All 3 devices reflect same streak and diamond count.
  3. No inconsistency or reward desync.

---

### Test Case 20: App Update Between Days

- **Preconditions:**
  1. User has app version X, with streak at Day 4.

- **Steps:**
  1. Update app to version Y.
  2. Open app next day.

- **Expected Result:**
  1. Daily Treat continues at Day 5.
  2. No regression due to app update.
  3. Persistent data remains consistent.

---

### Test Case 21: Accessibility / Screen Reader Test

- **Preconditions:**
  1. Device has TalkBack (or screen reader) enabled.

- **Steps:**
  1. Open app and receive Daily Treat popup.
  2. Try to collect reward via screen reader or keyboard nav (if on emulator).

- **Expected Result:**
  1. UI is accessible (popup focusable, tappable).
  2. Reward can be collected via accessibility tools.

---

### Test Case 22: Cross-Platform Synchronization (Android & iOS) on Daily Treat Collection

- **Preconditions:**
  1. User is logged into the same account on both an Android device and an iOS device.
  2. Both devices are online and the Daily Treat reward has not yet been collected for the day.

- **Steps:**
  1. On the Android/IOS device, open the app and collect the Daily Treat reward.
  2. Immediately after, open or refresh the app on the iOS/Android device.

- **Expected Result:**
  1. The iOS device reflects that the Daily Treat reward has already been collected today.
  2. The Daily Treat popup does **not** appear on the iOS device.
  3. The reward streak counter is consistent across both Android and iOS.
  4. No reward duplication occurs.

---

### Test Case 23: Localization and Text Layout (App Language Remains English)

- **Preconditions:**
  1. App supports multiple device languages (e.g., Hebrew, English, others).
  2. Daily Treat dosent collect today.

- **Steps:**
  1. Change the device language to various supported languages.
  2. Launch the app.
  3. Daily Treat is apear.
  4. Observe the language and layout of the Daily Treat popup.
  5. Check for text clipping, layout issues, and proper rendering.

- **Expected Result:**
  1. Regardless of the device language, the **app interface remains in English**.
  2. Daily Treat popup text is shown in **English only**.
  3. No text clipping, misalignment, or UI layout issues.
  4. All UI elements are fully visible and rendered correctly.

---

### Test Case 24: Responsiveness Across Different Screen Resolutions

- **Preconditions:**
  1. Daily Treat popup is available.
  2. Devices with varying screen sizes and resolutions.

- **Steps:**
  1. Open app on devices ranging from small phones to tablets.
  2. Verify popup scales correctly to screen size.
  3. Check that text and animations are fully visible without scrolling or clipping.

- **Expected Result:**
  1. Popup is responsive and adapts well to all screen sizes.
  2. No UI elements are hidden or clipped.
  3. Consistent user experience across devices.

---

### Test Case 25: OS Version Compatibility (Android & iOS)

- **Preconditions:**
  1. The app supports Android and iOS platforms.
  2. The Daily Treat feature is available.
  3. Test devices are available with a variety of OS versions:
     - Android: Android 8 and above.
     - iOS: iOS 13 and above.

- **Steps:**
  1. Install the app on devices running various versions of Android and iOS.
  2. Launch the app on a day when Daily Treat is expected.
  3. Trigger the Daily Treat popup.
  4. Interact with the popup (e.g., claim reward).
  5. Monitor app behavior and UI responsiveness.

- **Expected Result:**
  1. App runs smoothly and without crashes across all tested OS versions.
  2. Daily Treat popup appears correctly on all devices.
  3. All elements (texts, buttons, animations) function as expected.
  4. No performance issues, layout problems, or missing content.

---

### Test Case 26: Guest User Behavior on Daily Treat

- **Preconditions:**
  1. Open the app for the first time today.
  2. User is in guest mode (not logged in with phone number).
  2. Daily Treat reward is available.

- **Steps:**
  2. The Daily Treat popup appears.
  3. Collect the reward.
  4. Log in to an existing user account.
  5. Close the app and open the app again.

- **Expected Result:**
  1. The Daily Treat screen appears for the account registered based on the design.
  2. After login, reward status is based on the logged-in account.
  3. Verify that reward data from the guest session is not merged with or carried over to the logged-in account.
  4. When a user logs in after using the app as a guest, the rewards shown must reflect only the logged-in account's data, not the guest session's progress.

---




## Notes:
- Observed no critical bugs in the flow; app behavior is consistent.

