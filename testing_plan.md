# **Test Plan Frame for Cosmic Wreckage**

**Game Name:** Cosmic Wreckage

**Team Members:** Polett Arias and Luis Corral

**Date:** November 18, 2024

### Unit Testing the Game Mechanics

###### Computer Actions:

- Check that right arrow moves ship shooter right
- Check that left arrow moves ship shooter left
- Check that up arrow moves ship shooter up
- Check that down arrow moves ship shooter down
- Check that clicking space rotate the ship shooter 15 degrees

###### Tablet & Phone Actions:

- Check that moving the toggle up or down moves the ship shooter up or down
- Check that moving the toggle left or right moves the ship shooter left or right
- Check that moving the toggle clockwise allows for rotation of 15 degrees

###### Actions for all platforms:

- Check that collision with asteroids results in -1 life
- Check that shooting a S or DS powerup results in power-up acquirement for 30 seconds
- Check that the menu works properly; pausing the game saves score and progress, quitting the game takes player back to the activity screen, and restarting resets all progress in the current game.
- Check that asteroids do not overlap

### Logic Testing the Game Rules and Calculations

- Check that score is updated accordingly; +400 points per large asteroid, +500 points per medium asteroid, and +800 points per small asteroid

- Check that level is adjusted per 20,000 points. Level 1 includes 0 - 20,000 points, Level 2 includes 20,001 - 40,000 points, Level 3 includes 40,001 - 60,000 points, Level 4 includes 60,001 - 80,000 points, and Level 5 includes 80,001 - 100,000 points

- Check that the speed of asteroids is +5% speed for Level 1, +10% speed for Levels 2 & 3, +15% speed for Level 4, and +20% speed for Level 5

- Check that only 2 power-ups are on screen at a time

### Boundary Testing: Edge Cases and Limits

- Test the lowest and highest speeds to ensure that game is possible to win

- Test achieving the levels to ensure game doesn't break or lag when it transitions

- Test when player loses lives

- Test when player is going to be hit by an asteroid and game over is to occur

- Test when player is going to reach 100,000 points and game won is to occur

- Test that power-ups work properly and disable once time runs out

### Integration Testing: System Interaction

- Ensure that interacting with the menu pauses game temporarily 

- Check that game over screen displays score and level 

- Test that collisions with asteroids are properly detected

- Check if two asteroids are shot at once and that score is properly updated

### Handling Bad Input and Run-Time Errors

##### General
- Test edge cases when for score and level updates, if scores are not updated the activity screen will be useless
- Test speed at which asteroids appear onto the screen, if speed does not increase or increases too much, the game will become boring or incredibily difficult
- Test cases where the wrong keys are pressed and ensure game remains unaffected when it occurs

##### Invalid Key Inputs
- If a player presses a key whether numeric or non-numeric that is not considered valid movement, the game should remain unaffected and not crash
- Check that game does not allow player to travel outside of the play area given
- If game crashes at score or level changes, test to determine whether is issue is frame rate or memoery handling related

### Build a Table to Present All Test Information

| Test Case | Test Data | Expected Outcome |
|:---------:|:---------:|:----------------:|
|Player Count|1 player| Game should only allow one player to participate in the game|
|Score Increase| 0, 400, 1200, 1700, 100,000| The score begins at 0 and can increase by 400, 500 or 800 points until 100,000 points are reached this is when the game ends and game won is displayed on the screen.|
|Invalid Input|"be", "#!", "22", 'enter key'| Game will ignore all key inputs except the arrow keys and the space bar.|
|Menu selected|clicking or pressing the menu button|The game will pause temporarily while menu is open.|