I'm want to create a cool video game, that I'm calling Alien Smash.

It's a quick reflex game where aliens appear and you try to click them as fast as possible to score points.

I'm not sure of the tech stack, but i'm doing a live presentation, so keep it simple.

## Alien Smash - Enhanced Game Specification

### Core Concept
A fast-paced, browser-based reflex game where players click on randomly appearing aliens to score points before they disappear.

### Technical Stack (Live Presentation Friendly)
- **Frontend**: HTML5, CSS3, JavaScript (vanilla - no frameworks for simplicity)
- **Canvas**: HTML5 Canvas for smooth animations and alien rendering
- **Audio**: Web Audio API for sound effects
- **No backend required** - client-side only for demo purposes

### Game Mechanics
- **Spawn System**: Aliens appear at random positions every 1-2 seconds
- **Timing**: Each alien stays visible for 2-3 seconds before disappearing
- **Scoring**: +10 points per successful click, -5 points for missed aliens
- **Difficulty**: Speed increases every 30 seconds (faster spawns, shorter visibility)
- **Lives**: 3 lives, lose one for each missed alien

### Visual Design
- **Aliens**: Colorful, simple sprite-based creatures (3-4 different types)
- **Background**: Space-themed with twinkling stars
- **UI**: Clean score display, lives counter, and game timer
- **Effects**: Click animations, explosion effects when aliens are hit

### Audio
- Alien spawn sound
- Success hit sound
- Miss/failure sound
- Background ambient space music

### Controls
- Mouse click only (touch-friendly for mobile)
- Spacebar to start/restart game