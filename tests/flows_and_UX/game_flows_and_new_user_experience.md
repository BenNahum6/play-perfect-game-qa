# Game flows and new user experience

- **Tested on:** 16.07.2025
- **Device:** Android S23 FE
- **OS Version:** Android 15 One UI 7.0
- **App Version:** Not Specified (Tested from APK File)

---

## 1. Installation and permissions

- The app was installed via a pre-received APK file.
- When opening the app for the first time, a request for permission to send notifications (Push Notifications) appears.
- After approving the permission, you are taken to a home screen with a logo and a loading bar.

Loading times:
- Progress Bar loading time: about 2.45 seconds
- Total time from clicking on the app to the end of loading: about 6.5 seconds

---

## 2. Initial Registration Screen ("Choose Your Avatar")

The entire game is accompanied by pleasant, relaxing background music that creates a calm and welcoming atmosphere throughout the experience. 

This is the first **Onboarding** screen, where the user creates their initial identity before entering the core game loop. The experience is interactive, visual, and focuses on personalization.

The screen provides the following customization options:

- **Avatar Selection**  
   - The user can choose a visual avatar from a wide selection of pre-designed characters.  
   - Additionally, there is an option to upload a custom image directly from the device's gallery.  
   - *Note:* The gallery opens using the native Android file picker.

- **Username Selection**  
   - A random (auto-generated) name is pre-filled by default.  
   - The user can either accept it or manually enter a preferred name.

- **Sign in (Optional)**  
   - There is an option to sign in using a mobile number.
   - Upon clicking the **Sign In** button, a new window appears with:
     - A country selector dropdown
     - A field for entering the mobile phone number
   - **Observation:** During testing from Israel, the phone login feature was not available. It’s likely disabled due to regional restrictions or compliance limitations (e.g., regulatory blocks).

After completing the setup, pressing the **Next** button immediately advances the user to the **interactive tutorial stage** of the game.

---

## 3. Initial Training (Tutorial Mode)

After completing the avatar selection and registration screen, the user is transitioned into their **first game session**, which is accompanied by a built-in tutorial.

The game opens with a **short animation of the cards being dealt**, accompanied by a **realistic card dealing sound**, creating a polished and immersive start to the session.

This is a **real Solitaire game** where the tutorial is overlaid on top of live gameplay.  
The tutorial includes:

- A **visual pointer** (animated hand icon) indicating where the player should tap or drag.  
  The pointer demonstrates the required action through animation — for example, it may show the user dragging a King card into an empty slot.  
  These instructions are **not written explicitly** in the floating text box, but are instead **conveyed visually**, guiding the user by motion and highlighting.
- A **floating text box** explaining the required action for each step (e.g., "Use Kings in empty slots")  
- The rest of the screen is **dimmed**, while a **spotlight effect highlights the specific card or area** (e.g., a King card) the user should focus on  
- A **SKIP** button is available within the floating text box, allowing the user to skip the tutorial step and proceed forward  

Each tutorial step is **interactive** — the user must perform the instructed move in order to proceed to the next step.

**Audio Feedback:**  
Every interaction with the cards (e.g., dragging, moving, or stacking) is accompanied by a **light card friction sound**, enhancing realism and providing satisfying auditory feedback to the player.

---

### End Game Prompt

At the end of the tutorial, the system instructs the user to **end the game**.

When tapping the **"End Game"** button, a **confirmation window** appears with the message:  
**"Are you sure you want to end the game?"**

Two buttons are presented:
- **Submit** — confirms ending the game  
- **Play On** — cancels the action and returns to the game

As part of the tutorial flow, the user is **required to tap the Submit button** in order to proceed.  
An **animated hand pointer** appears and repeatedly points to the **Submit** button, guiding the user toward the required action.  
Additionally, the screen is **dimmed**, with a **spotlight effect highlighting only the Submit button**, further focusing the user's attention.  
The game does not continue until this confirmation is completed.

This enforced and guided interaction ensures that new users actively confirm their intent, preventing accidental exits before completing the tutorial.

---

## 4. Game Over Screen (Score Summary)

After completing the tutorial game, the user is presented with a **results screen** summarizing the performance in the session.

Three performance parameters are displayed prominently in the center of the screen:

- **Score** – Points accumulated based on in-game moves and strategy  
- **Time Bonus** – Bonus points awarded for completing the game quickly  
- **Total Score** – A calculated sum: **Score + Time Bonus**

### UI Elements:

- A **Close (X)** button is located at the **top-right corner** of the screen, allowing the user to dismiss the results  
- An **OK** button is located at the **bottom center** of the screen, allowing the user to confirm and proceed to the next screen (Leaderboard)

### Animations and Audio:

- The score numbers feature a **dynamic counting animation**, simulating real-time calculation as the numbers rapidly increase to their final value.  
- Background audio includes a **casino slot machine-like sound effect** playing while the score counts up, enhancing the excitement and engagement of the moment.

This screen provides instant feedback to the user and transitions smoothly into the reward and ranking flow.

---

## 5. Leaderboard Screen (All Player Rankings)

After confirming the score screen, the user is redirected to the **Leaderboard**, which displays a ranking of players based on their performance in the recent match.

### Key Elements:

- A vertical list of the **All players**, sorted by **Total Score** in descending order
- The **first place** is highlighted at the top with a golden crown and laurel icon
- Each entry includes:
  - **Player avatar** and name.
  - **Score** value.
  - **Prize** (for top 3 only): Diamonds.

> The top 3 players (1st–3rd place) receive the **same reward**, indicated by a gold diamonds icon and "Prize: 70"

---

### Call-to-Action:

At the bottom of the screen, a large **green button labeled "CLAIM"** appears.  
- Tapping this button **collects the reward (if applicable)**.  
- A **short animation** is displayed where the diamonds visually "fly" into the **diamonds counter** at the top of the screen.  
- If the user has leveled up, a **Level Up animation** is triggered immediately afterward.  
- Otherwise, the user is **taken directly to the Game Lobby**.

This feedback mechanism reinforces reward collection and enhances player satisfaction.

---

## 6. First Real Game (Post-Tutorial)

Immediately after the leaderboard and reward claim screens, the user is directed to the **main game lobby** for the first time.

Although no longer in tutorial mode, the system still provides **initial guidance** to help the user transition smoothly.

### Visual Prompt:

- A **floating hand pointer** appears again, pointing toward the **Play** button.
- This indicates to the user that they should now initiate their **first real Solitaire game**.

---

### Game Details:

- This match is **not part of the tutorial** — it is a **fully independent game session**.
- The game runs in **standard mode**, meaning:
  - **No visual assistance**
  - **No instructional tooltips or hints**
  - **Full user control over moves and decisions**

- A system message states that entry to the match costs **20 diamonds**.
- Tapping **Play** deducts the required amount and launches the game.

This marks the user's transition into the **core gameplay loop**, where they apply what they learned in the tutorial in a real match setting.

---

## 7. Post-Game: 

After the flow previously described in Sections 4 & 5, the user is presented with the **Daily Login Reward Screen**, which appears once per day upon logging in.

### Daily Login Reward Screen

- Immediately after the Level Up, the user is presented with the **Daily Login Bonus** screen.
- This screen highlights the user's **current login streak day (e.g., Day 1)** and the reward tied to it.
- The player is encouraged to return daily to build their streak and earn better prizes.
- A **Collect** button is shown — pressing it adds the reward to the user's inventory and transitions to the next flow (typically the main lobby).

This flow both **rewards player activity** and reinforces **daily engagement habits**, crucial for retention in casual mobile games.

---

## New User Experience Summary

The game provides a gradual, cohesive, and engaging onboarding experience for new users, including:

- Interactive step-by-step gameplay walkthrough.  
- Confirmations that prevent accidental exits during the tutorial.  
- Instant feedback through score summaries and leaderboards that increase motivation.  
- Engaging animations and daily login rewards to maintain engagement.  
- Smooth transitions between screens to maintain flow and a good user experience.  
- Pleasant background music and integrated sound effects accompany user interactions, such as button confirmations and card movements, enhancing immersion and feedback.

This user experience is designed to allow new users to learn quickly, stay engaged, and build long-term gaming habits.

---
