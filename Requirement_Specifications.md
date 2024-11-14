# **Requirements Specifications for Cosmic Wreckage**

**Game Name:** Cosmic Wreckage

**Team Members:** Polett Arias and Luis Corral

**Client:** Pallas Kennedy

**Date:** November 14, 2024

## **Game Overview**
-  **Brief Description:** Cosmic Wreckage is a remix on the classic arcade game Asteroids with an added shield and double ship shooter mechanic. Players must shoot asteroids with the ship shooter and if they are lucky, can either get a shield or an extra ship shooter for 30 seconds. These power-ups will allow them to continue playing the game for a longer amount of time and get a higher score.

- **Main Goal:** The main goal is to destroy as many asteroids as possible to score points without dying. As the player shoots asteroids, the asteroids split into smaller, harder to shoot asteroids that are worth more points. The player has three lives and the highest score possible is 100,000. If the player loses all three lives, it's game over. If the player reaches 100,000 points, they won.

## **Functional Requirements**
**1. Core Features:**

- Classic Asteroids mechanics with a power-ups

- Double shooter power-up that gives the player another ship to control and shoot double the amount of asteroids

- Shield power-up that gives the player a protective shield from the asteroids in order to live longer and score more points

- Score tracking to keep the player's high score and a save progress feature so the game can be resumed if paused for a long amount of time

- Game Over if the player dies or reaches the score 100,000

**2. User Interations:**

- Controls: Keyboard (right &  left arrow keys for movement and space for rotation)

- Power-Up Usage: Players can activate power-ups for 30 seconds by shooting the power-up symbol when it appears on the screen

- Game Flow: Players can use the mouse to start, pause, or reset the game

## **Non-Functional Requirements**

**1. Usability:** 

- The game should be easy to understand and play since it is meant to be for a large variety of people

- The game controls should feel natural and uncomplicated

- The layout should include indicators of the game state like current score and a menu that includes pause, reset, and quit buttons

**2. Performance:**

- The game should maintain a frame rate of 60 FPS

- The load time should remain under 10 seconds

- The game can only support one player and two power-ups on the screen at the time 

**3. Cross-Platform Compatibility:**

- This game should run on all devices (PC, mobile, tablet, etc.) and the layout and controls should adapt to the different platforms

## **Design Requirements**

**1. Graphics and Visuals:**

- The asteroids and ship shooter will have pixel art style and the background will be retro

- The shoot animation for the asteroids and power-ups will be smooth and clear

**2. Audio:**

- The background music should start off calmer until you reach 50,000 points where the music begins to speed up as you reach the 'end'

- Sound effects for destroying asteroids, shooting power-ups, game-over events, and game-won events.

**3. Data Requirements:**

- What Data Needs to be Saved or Tracked: Highest score, number of power-ups used, and player's saved game state

- How Will the Data be Stored: Game data should be saved online for players with accounts. High scores or achievements should be stored on a online leaderboard

## **Collaboration**

**1. How Will You Gather Feedback from the Client in Each Sprint:**

- Feedback will be collected through testing sessions with Kennedy

- Surveys and team meeting after each sprint to check game progress and change features to client needs

**2. How Will You Ensure the Game is Developing According to the Client's Needs:**

- The development team will conduct check-ins to make sure client's expectations are met

- The team will create demos after major milestones and use feeback to refine gamepla accordingly