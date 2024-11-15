
# Cosmic Wreakage  

# astroids Pseudocode with Power-ups

## Game Initialization

- Set `playerHealth` to 3
- Set `playerShield` to 0 (No shield active)
- Set `playerBlaster` to "normal" (No special blaster)
- Set `shieldTimeRemaining` to 0
- Set `blasterTimeRemaining` to 0

## Main Game Loop

WHILE `playerHealth` is greater than 0

    - **Check for power-up collection**
        - IF player collects a power-up
            - Set `powerUpType` to the type of power-up collected (e.g., shield, minigun, shotgun)
            - APPLY the collected power-up

    - **Check if the shield is active and handle its timer**
        - IF `playerShield` is active
            - IF `shieldTimeRemaining` is greater than 0
                - Decrease `shieldTimeRemaining` by 1 (each frame)
            - ELSE
                - Deactivate the shield
                - Display "Shield expired"

    - **Check if player is hit by an asteroid**
        - IF player is hit by an asteroid
            - IF `playerShield` is active
                - Deactivate the shield (shield absorbs the hit)
                - Display "Shield absorbed a hit"
            - ELSE
                - Reduce `playerHealth` by 1 (player loses health)
                - Display "Player hit, health reduced"

    - **Check if blaster power-up is active and manage its timer**
        - IF player has an active blaster power-up
            - IF `blasterTimeRemaining` is greater than 0
                - Decrease `blasterTimeRemaining` by 1 (each frame)
            - ELSE
                - Reset `playerBlaster` to "normal" (blaster power-up expires)
                - Display "Blaster power-up expired"

    - **Handle player input for movement and shooting**
        - IF player presses "left" key
            - Move player left
        - IF player presses "r
