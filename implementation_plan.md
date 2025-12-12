# Refactoring Shooter Mode: Progressive Survival

## Goal
Transform the Shooter Mode from a fixed-wave level into a progressive survival challenge.
- **Fail Condition**: Missing more than 3 enemies (enemies flying past you).
- **Difficulty**: Progressively increases enemy speed and spawn rate.
- **Goal**: Survive as long as possible (High Score).

## User Review Required
> [!IMPORTANT]
> The "Win" condition of reaching 25 kills is being removed. The game is now endless until you lose.

## Proposed Changes

### UI
- Change `shooter-score-display` to show:
    - **Score** (Kills)
    - **Missed** (Lives/Health: X/3)

### Game Logic (`index.html`)

#### State Variables
- `missedEnemies`: Tracks enemies that go off-screen.
- `difficultyMultiplier`: Increases over time or score.
- `nextSpawnTime`: Timestamp for dynamic spawning.

#### Function: `startShooterGame()`
- Reset `missedEnemies = 0`.
- Reset `difficulty` metrics.
- Remove fixed `setInterval` for spawning.

#### Function: `gameLoop` (Shooter Section)
- Implement dynamic spawning check:
  `if (Date.now() > nextSpawnTime) { spawnEnemy(); calculateNextSpawn(); }`

#### Function: `spawnEnemy()`
- Assign speed based on current difficulty.
- `currentSpeed = baseSpeed + (score * 0.1)` (Example)

#### Function: `updateShooterEntities()`
- **Miss Detection**: If enemy `x < 0`, increment `missedEnemies`.
- If `missedEnemies > 3`, trigger `gameOverShooter()`.
- **Difficulty Ramp**: Update spawn rates/speeds based on `enemiesDefeatedCount`.

#### Function: `endShooterGame()`
- Update to reflect High Score nature (no "Mission Complete", just "Game Over" with stats).
- **Note**: The user didn't explicitly say "Endless", but "progressively increases" implies it. I will keep the game ending only on "Game Over" (collision or misses).

## Verification
- **Test**: Start Shooter mode.
- **Test**: Let 3 enemies pass -> Verify Game Over.
- **Test**: Kill enemies -> Verify spawn rate feels like it's increasing.
