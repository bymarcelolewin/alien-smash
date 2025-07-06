# Alien Smash - Product Requirements Document

## Overview
Alien Smash is a fast-paced, browser-based reflex game where players click on randomly appearing aliens to score points before they disappear. Designed for live presentation demonstrations with simple, engaging gameplay.

## Technical Specifications

### Platform & Compatibility
- **Target Platform**: Web Browser (Modern Chrome)
- **Screen Resolution**: 800x600 pixels (fixed)
- **Mobile Support**: Not required for initial version
- **File Structure**: Separate HTML and CSS files, embedded JavaScript

### Technology Stack
- **Frontend**: HTML5, CSS3, JavaScript (vanilla - no frameworks)
- **Rendering**: HTML5 Canvas for animations and alien rendering
- **Audio**: None (skipped for initial version)
- **Storage**: None (no high score system initially)
- **Configuration**: JSON file for game rules and scoring

## Game Mechanics

### Core Gameplay
- **Objective**: Click aliens before they disappear to score points
- **Spawn System**: Aliens appear at random positions every 1-2 seconds
- **Alien Visibility**: Each alien stays visible for 2-3 seconds before disappearing
- **Game Duration**: Continues until player runs out of lives (no time limit)

### Scoring System
- **Successful Hit**: Points per alien (configurable via rules.json)
- **Missed Alien**: Point penalty (configurable via rules.json)
- **Lives**: 3 lives total, lose one for each missed alien

### Difficulty Progression
- **Scaling**: Linear difficulty increase
- **Timing**: Difficulty increases every 30 seconds
- **Changes**: Faster spawn rates, shorter alien visibility duration

## Visual Design

### Layout & Dimensions
- **Canvas Size**: 800x600 pixels
- **Background**: Space-themed with twinkling stars
- **Color Scheme**: Dark space theme (designer's choice)

### Alien Design
- **Type**: Simple geometric shapes
- **Variety**: 3-4 different alien types
- **Size**: Uniform size for all aliens
- **Animation**: Simple fade in/out effects

### User Interface
- **Score Display**: Current score prominently displayed
- **Lives Counter**: Visual representation of remaining lives
- **Game Timer**: Optional timer display
- **Effects**: Simple click animations and explosion effects on hit

## Controls & Interaction
- **Primary Control**: Mouse click only
- **Game Control**: Spacebar to start/restart game
- **Touch Support**: Not required for initial version

## Technical Requirements

### Performance
- **Target FPS**: 60 FPS smooth animation
- **Response Time**: Immediate click detection
- **Memory Usage**: Minimal footprint for presentation environment

### Browser Features
- **Canvas API**: For rendering and animations
- **RequestAnimationFrame**: For smooth animations
- **Event Listeners**: Mouse and keyboard input handling
- **Fetch API**: For loading game configuration from rules.json

## Success Metrics
- **Gameplay**: Engaging and intuitive within 30 seconds of play
- **Performance**: Smooth operation during live presentation
- **Visual Appeal**: Clear, colorful graphics visible to audience

## Future Enhancements (Post-MVP)
- Audio system with sound effects
- High score tracking with localStorage
- Mobile responsive design
- Additional alien types and behaviors
- Power-ups and special effects
- Multiplayer functionality

## Development Priorities
1. **Core Gameplay Loop**: Alien spawning, clicking, scoring
2. **Visual Polish**: Smooth animations and appealing graphics
3. **User Interface**: Clear score and lives display
4. **Game States**: Start screen, gameplay, and game over
5. **Difficulty Scaling**: Progressive challenge increase

## File Structure
```
/
├── index.html          # Main game file
├── styles.css          # Game styling
├── rules.json          # Game configuration and scoring rules
└── .vibedocs/
    └── discovery/
        ├── starting-prompt.md
        ├── questions-and-answers.md
        └── prd.md
```

## Configuration Management

### Rules.json Structure
The game will load configuration from a `rules.json` file containing:
- **Scoring Rules**: Points awarded for successful hits per alien type
- **Penalty Rules**: Points deducted for missed aliens
- **Game Parameters**: Configurable values for spawn rates, visibility duration, etc.

### Benefits
- **Easy Balancing**: Adjust scoring without code changes
- **Flexible Rules**: Support for different alien types with different point values
- **Rapid Iteration**: Test different configurations quickly during development

## Acceptance Criteria
- [ ] Game loads and displays correctly at 800x600 resolution
- [ ] Game successfully loads and parses rules.json configuration
- [ ] Aliens spawn randomly and disappear after timeout
- [ ] Click detection works accurately on aliens
- [ ] Score increases/decreases correctly based on rules.json values
- [ ] Lives decrease when aliens are missed
- [ ] Game ends when all lives are lost
- [ ] Difficulty increases linearly over time
- [ ] Smooth animations and visual feedback
- [ ] Game can be restarted with spacebar