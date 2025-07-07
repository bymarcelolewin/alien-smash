# Alien Smash v1.2 - Random Alien Movement

**Release Version**: v1.2  
**Release Date**: TBD  
**Plan ID**: ALIEN-SMASH-V1.2-2025-001  
**Based on**: v1.1 Enhanced Alien Visuals

## Release Overview
This release adds dynamic random movement to aliens, making them more challenging and engaging to click. The movement patterns are configurable through the rules.json file, allowing for fine-tuning of gameplay difficulty and alien behavior.

## Release Goals
- Add random movement patterns to all alien types
- Make movement configurable via rules.json
- Maintain click detection accuracy with moving targets
- Enhance gameplay challenge and visual appeal
- Preserve all v1.1 visual enhancements

## New Features in v1.2

### Random Movement System
- **Configurable Movement**: All movement parameters stored in rules.json
- **Type-Specific Patterns**: Different movement styles per alien type
- **Boundary Collision**: Aliens bounce off screen edges
- **Smooth Motion**: Fluid movement using velocity vectors
- **Performance Optimized**: Movement calculations don't impact 60fps

### Movement Patterns by Alien Type

#### Basic Alien Movement
- **Slow, wandering motion** in random directions
- **Gentle direction changes** every few seconds
- **Low speed** for easier targeting

#### Fast Alien Movement
- **Quick, darting motions** with sudden direction changes
- **Higher velocity** reflecting their "fast" nature
- **More erratic patterns** for increased difficulty

#### Bonus Alien Movement
- **Circular or figure-8 patterns** 
- **Predictable but complex** movement paths
- **Medium speed** with smooth curves

#### Special Alien Movement
- **Teleportation-style jumps** between positions
- **Brief pauses** at each location
- **Unpredictable positioning** for maximum challenge

## Technical Implementation

### Rules.json Configuration Structure
```json
{
  "movement": {
    "randomSeed": 12345,
    "basic": {
      "speed": 0.5,
      "directionChangeInterval": 2000,
      "chaosLevel": 0.3
    },
    "fast": {
      "speed": 1.2,
      "directionChangeInterval": 800,
      "chaosLevel": 0.8
    },
    "bonus": {
      "speed": 0.8,
      "pattern": "circular",
      "radius": 30
    },
    "special": {
      "teleportInterval": 1500,
      "pauseDuration": 300
    }
  }
}
```

### Movement System Components
1. **SeededRandom Class**: Deterministic random number generation
2. **MovementController**: Handles velocity and position updates
3. **BoundaryManager**: Handles edge collisions and bouncing
4. **PatternGenerator**: Creates specific movement patterns per type

## Success Criteria
- [ ] Aliens move smoothly and randomly during gameplay
- [ ] Movement patterns are configurable via rules.json
- [ ] Click detection works accurately on moving targets
- [ ] Performance remains at 60fps with movement enabled
- [ ] Each alien type has distinct movement characteristics
- [ ] Random seed produces reproducible movement patterns

## Implementation Tasks

### Core Movement System
1. **Seeded Random Number Generator**
   - Implement deterministic random number generation
   - Use seed from rules.json for reproducible results

2. **Alien Movement Properties**
   - Add velocity, direction, and movement state to Alien class
   - Implement position update logic

3. **Movement Pattern Controllers**
   - Basic alien wandering behavior
   - Fast alien darting patterns
   - Bonus alien circular/curve patterns
   - Special alien teleportation system

### Configuration & Integration
4. **Rules.json Movement Section**
   - Add comprehensive movement configuration
   - Include speed, timing, and pattern parameters

5. **Boundary Management**
   - Implement edge detection and bouncing
   - Ensure aliens stay within canvas bounds

6. **Click Detection Updates**
   - Maintain accurate collision detection for moving targets
   - Account for alien velocity in hit registration

## Risk Assessment
- **Performance Risk**: Additional movement calculations might impact frame rate
  - *Mitigation*: Optimize movement updates, use efficient collision detection
- **Gameplay Balance**: Movement might make aliens too difficult to hit
  - *Mitigation*: Configurable movement parameters for fine-tuning
- **Visual Confusion**: Rapid movement might be hard to track
  - *Mitigation*: Test movement speeds, add motion blur if needed

## Backwards Compatibility
- All v1.1 alien visual enhancements preserved
- Same scoring system and game mechanics
- Existing rules.json structure extended (not replaced)
- Option to disable movement (speed = 0) for v1.1 behavior

## Definition of Done
- [ ] All alien types have configurable movement patterns
- [ ] Movement parameters controlled via rules.json
- [ ] Seeded random system produces consistent results
- [ ] Click detection works accurately on moving aliens
- [ ] Performance testing confirms 60fps maintained
- [ ] Movement enhances gameplay without making it frustrating
- [ ] Code remains clean and maintainable