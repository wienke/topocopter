# Topocopter 🚁

**Topocopter** (formerly *Helikopter Topo*) is an interactive, browser-based geography game that combines learning the map of the Netherlands with arcade-style fun. Fly your helicopter to find cities before your fuel runs out, and unlock a secret alien-shooter bonus level!

## 🎮 How to Play

### 1. Geography Mode (Main Game)
*   **Goal**: Fly to the red city markers indicated on the screen.
*   **Provinces**: The map shows all 12 Dutch provinces with distinct colors.
*   **Difficulty Levels**: 
    *   **Saai** (Easy): 30 seconds per city.
    *   **Te Doen** (Medium): 20 seconds per city.
    *   **Moeilijk** (Hard): 10 seconds per city.
*   **Win Condition**: Find all cities to unlock the *Bonus Level*.
*   **Lose Condition**: Run out of time (Game Over).

### 2. Shooter Mode (Bonus Level) 🛸
*   **Goal**: Defeat 25 waves of attacking emojis.
*   **Controls**: Your helicopter is locked to the left side. Move UP/DOWN to dodge and align shots.
*   **Win Condition**: Survive and clear the skies!

## 🕹️ Controls

The game supports both Desktop (Keyboard) and Tablet (Touch).

| Action | Keyboard | Touch / Tablet |
| :--- | :--- | :--- |
| **Move** | Arrow Keys (⬆️⬇️⬅️➡️) | Virtual D-Pad |
| **Shoot Rocket** | Spacebar | 🔥 Button |
| **Heart Shot** | `H` Key | - |
| **Barrel Roll** | `F` Key | - |
| **Toggle Turd** | `T` Key | - |

> **Note**: In Shooter Mode, movement is restricted to UP/DOWN only.

## 🥚 Easter Eggs & Secrets

*   **Heart Shot (**`H`**)**: Spread love instead of destruction. Fires a ❤️ emoji.
*   **Barrel Roll (**`F`**)**: Press 'F' to perform a 360-degree spin maneuver.
*   **Code Brown (**`T`**)**: Press 'T' to transform your helicopter into a... 💩. Press again to revert.
*   **Test Mode**: Append `?testmode=on` to the URL to enable a debug button that skips directly to the shooter level.

## 🛠️ Technology

*   **Core**: HTML5, CSS3, Vanilla JavaScript.
*   **Map Engine**: [Leaflet.js](https://leafletjs.com/).
*   **Tiles**: CartoDB Dark Matter.
*   **Data**: GeoJSON for Dutch provinces.

## 🚀 Installation

No build step required! This is a standalone web application.

1.  Clone the repository:
    ```bash
    git clone https://github.com/wienke/topocopter.git
    ```
2.  Open `index.html` in any modern web browser.
3.  Enjoy flying!

## 📱 Mobile/Tablet Support

The game is fully responsive and includes a dedicated touch interface for tablets (iPad, Android tablets). When a touch device is detected, a virtual joystick and fire button will appear on the screen.


## 🔒 Privacy & Safety

This game is designed to be **safe for kids** and **privacy-friendly**.

*   **No Cookies**: The game does not set any cookies.
*   **No Tracking**: There are no analytics, ads, or tracking scripts.
*   **No Personal Data**: No user data is collected or stored.
*   **External Requests**: The game loads map tiles from *CartoDB* and the map library from *unpkg* (CDNs) to function. These are standard technical dependencies solely for displaying the map.

---

*Fly safe, Pilot!*
