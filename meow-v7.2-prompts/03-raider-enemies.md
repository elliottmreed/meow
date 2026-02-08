# Raider Enemies System Implementation

## Overview
This document outlines the implementation details for spawning raiders starting from wave 9 in the game. The raiders will introduce new challenges and dynamics as players progress through the waves.

## Raider Spawning Mechanics
- Raiders will spawn at the start of wave 9 and continue to spawn in subsequent waves.
- The number of raiders spawned will increase with each wave to escalate the difficulty.

## Functions

### 1. createRaider
This function is responsible for creating a new raider enemy.

#### Definition:
```javascript
function createRaider() {
    // Code to instantiate a raider object
    // Set raider attributes (health, speed, damage, etc.)
    const raider = {
        health: 100,
        speed: 2,
        damage: 10,
        alive: true,
    }; 
    return raider;
}
```

### 2. updateRaiders
This function updates the state of all active raiders each game tick.

#### Definition:
```javascript
function updateRaiders(raiders) {
    raiders.forEach((raider) => {
        if (raider.alive) {
            // Update raider position or state
            // Logic for raider attacks, movement, etc.
        }
    });
}
```

### 3. Integration with Evil Miracles
- Raiders will leverage a new damage mechanic through the evil miracles system.
- When a raider attacks, it may activate an evil miracle that modifies the damage output or inflicts additional effects.

#### Damage Calculation example:
```javascript
function calculateDamage(raider) {
    let baseDamage = raider.damage;
    if (activateEvilMiracle()) {
        baseDamage *= 2; // Example of doubling damage if miracle activated
    }
    return baseDamage;
}
```

## Conclusion
The raider spawning system enhances difficulty and player engagement in waves 9 and beyond, with strategic integration with existing mechanics to enrich gameplay.