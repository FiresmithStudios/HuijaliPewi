# Huijari Peli (Impostor Game) - Project Analysis

## Project Overview

**Huijari Peli** is a Finnish social deduction game similar to "Spyfall" or "The Resistance." It's a multiplayer game where players try to identify an impostor among them while the impostor tries to blend in and guess the location.

## Game Mechanics

### Core Concept
- **Players**: 3-8 players
- **Duration**: 10 minutes
- **Objective**: Regular players must identify the impostor; the impostor must either avoid detection or correctly guess the location

### How It Works
1. **Setup**: Each player gets a role and location, except one player who becomes the "huijari" (impostor) with "???" for both role and location
2. **Gameplay**: Players take turns asking questions about the location and roles
3. **Strategy**: Regular players must reveal enough information to identify the impostor without giving away too much; the impostor tries to blend in and gather clues
4. **End Game**: After 10 minutes, players vote on who they think is the impostor
5. **Victory Conditions**:
   - Regular players win if they correctly identify the impostor
   - Impostor wins if they avoid detection OR correctly guess the location

## Technical Implementation

### Current Version (Huijalipewi/index.html)
- **Technology**: Pure HTML/CSS/JavaScript (client-side only)
- **Data Storage**: Game data is hardcoded in JavaScript as a `gameData` object
- **Features**:
  - Player count selection (3-8)
  - Sequential card revelation system
  - 10-minute countdown timer
  - Example questions display
  - Game rules display

### Original Version (original/ folder)
- **Technology**: Flask (Python web framework)
- **Architecture**: Server-side with session management
- **Features**: Similar functionality but with server-side game state management

## Data Structure

### Game Data Format
The game uses a JSON structure with locations and associated roles:

```json
{
  "paikat": [
    {
      "place": "Kirjasto",
      "roles": ["Siivooja", "Kirjaston hoitaja", "Asiakas", "Pikkulapsi", "Opiskelija", "Piileskelevä valtionrikollinen", "ES-jonne"]
    }
  ]
}
```

### Content
- **34 different locations** ranging from realistic (Library, Hospital) to fantastical (Space Station, Castle)
- **7 roles per location** with humorous and creative character types
- **Finnish language** throughout the interface and content

## Development Tools

### Data Processing
- **JsonMaker.py**: Python script that converts `input.txt` (plain text format) to `output.json` (JSON format)
- **input.txt**: Human-readable format with locations and roles separated by colons and commas
- **output.json**: Machine-readable JSON format used by the game

### Deployment
- **git push.bat**: Simple batch script for Git deployment
- **Static hosting**: Current version can be deployed as static files

## User Experience Flow

1. **Start Screen**: Player selects number of players (3-8)
2. **Card Distribution**: Players take turns revealing their cards on the same device
3. **Game Phase**: 10-minute timer starts, example questions are shown
4. **Voting**: After time expires, players vote on the impostor

## Key Features

### Game Management
- Random location and role assignment
- Impostor selection (one player gets "???" for both role and location)
- Sequential card revelation system
- Countdown timer with visual display

### User Interface
- Dark theme with modern styling
- Mobile-responsive design
- Clear game rules and example questions
- Intuitive button-based navigation

### Content Quality
- Rich, diverse locations (34 total)
- Creative and humorous role descriptions
- Finnish cultural references and humor
- Balanced mix of realistic and fantastical settings

## Technical Notes

### Current Implementation
- **Pros**: Simple deployment, no server required, works offline
- **Cons**: All players must share one device, no persistent game state

### Original Implementation
- **Pros**: Server-side state management, could support multiple devices
- **Cons**: Requires server setup, more complex deployment

## Development History

The project appears to have evolved from a Flask-based implementation to a simpler client-side version, possibly for easier deployment and distribution. The data processing tools suggest the content was originally created in a simple text format and converted to JSON for programmatic use.

## Potential Improvements

1. **Multi-device support**: WebSocket or WebRTC for real-time multiplayer
2. **Game state persistence**: Save/load game sessions
3. **Additional content**: More locations and roles
4. **Customization**: Allow players to create custom locations/roles
5. **Statistics**: Track win rates and game history
6. **Accessibility**: Better screen reader support and keyboard navigation

## File Structure Summary

```
HuijaliPewi/
├── Huijalipewi/index.html          # Main game (current version)
├── original/                        # Flask-based version
│   ├── index.py                    # Flask server
│   ├── data.json                   # Game data
│   └── templates/index.html        # Flask template
├── JsonMaker.py                    # Data conversion tool
├── input.txt                       # Human-readable game data
├── output.json                     # Machine-readable game data
├── git push.bat                    # Deployment script
└── README.md                       # Project documentation
```

This is a well-structured social deduction game with good content and a clean implementation. The transition from server-side to client-side suggests a focus on simplicity and ease of use.
