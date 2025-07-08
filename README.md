# Alien Smash

A fast-paced, browser-based reflex game where players click on randomly appearing aliens to score points before they disappear. I created this during a [live presetnation](https://bymarcelolewin.com/presentations/vibe-coding-with-intent-for-better-and-faster-results/) about Vibe Coding.

## 🎮 Game Overview

- **Objective**: Click aliens before they disappear to score points
- **Controls**: Mouse click to hit aliens, Spacebar to start/restart
- **Lives**: 3 lives total - lose one for each missed alien
- **Difficulty**: Progressive challenge increase every 30 seconds

## 🚀 Quick Start

1. Open `index.html` in a modern web browser
2. Press **Spacebar** to start the game
3. Click on aliens as they appear to score points
4. Avoid missing aliens or you'll lose a life!

## 🛠️ Technical Features

- **Pure Web Technologies**: HTML5, CSS3, Vanilla JavaScript
- **Canvas Rendering**: Smooth 60 FPS animations
- **Configurable Rules**: JSON-based scoring and game parameters
- **Responsive Design**: Fixed 800x600 pixel resolution
- **No Dependencies**: Runs in any modern browser

## 📁 File Structure

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

## ⚙️ Game Configuration

The game loads configuration from `rules.json` containing:
- **Scoring Rules**: Points awarded for successful hits per alien type
- **Penalty Rules**: Points deducted for missed aliens
- **Game Parameters**: Spawn rates, visibility duration, etc.

## 🎯 Gameplay Features

- **Random Spawning**: Aliens appear at random positions every 1-2 seconds
- **Timed Visibility**: Each alien stays visible for 2-3 seconds
- **Visual Feedback**: Click animations and explosion effects
- **Space Theme**: Dark background with twinkling stars
- **Multiple Alien Types**: 3-4 different geometric alien shapes

## 🎨 Visual Design

- **Canvas Size**: 800x600 pixels
- **Theme**: Space-themed with dark color scheme
- **UI Elements**: Score display, lives counter, optional timer
- **Animations**: Simple fade in/out effects for aliens

## 🔧 Development

### Prerequisites
- Modern web browser (Chrome recommended)
- No build tools or dependencies required

### Running the Game
Simply open `index.html` in your browser - no server required!

### Customization
Edit `rules.json` to adjust:
- Point values for different alien types
- Spawn rates and timing
- Difficulty progression parameters

## 🎮 Controls

- **Mouse Click**: Hit aliens to score points
- **Spacebar**: Start game or restart after game over

## Updates
Coming soon!