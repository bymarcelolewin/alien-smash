# Alien Smash v1.2 - Task List

**Release Version**: v1.2  
**Created**: 2025-07-05  
**Status**: Not Started

## Task Progress Overview
- **Total Tasks**: 10
- **Completed**: 0
- **In Progress**: 0
- **Remaining**: 10

---

## Random Movement Implementation 🎯
**Priority**: HIGH | **Status**: Not Started

### Epic 1: Core Movement System
- [x] **ALIEN-V1.2-001** Implement SeededRandom class for deterministic random number generation - *45 min*
- [x] **ALIEN-V1.2-002** Add movement properties (velocity, direction) to Alien class - *30 min*
- [x] **ALIEN-V1.2-003** Create movement update logic in alien update() method - *45 min*
- [x] **ALIEN-V1.2-004** Implement boundary collision detection and bouncing - *45 min*

### Epic 2: Movement Patterns
- [x] **ALIEN-V1.2-005** Implement Basic Alien wandering movement pattern - *30 min*
- [x] **ALIEN-V1.2-006** Create Fast Alien darting movement with direction changes - *45 min*
- [x] **ALIEN-V1.2-007** Develop Bonus Alien circular/curved movement patterns - *45 min*
- [x] **ALIEN-V1.2-008** Design Special Alien teleportation movement system - *60 min*

### Epic 3: Configuration & Polish
- [x] **ALIEN-V1.2-009** Update rules.json with comprehensive movement configuration - *30 min*
- [x] **ALIEN-V1.2-010** Test and optimize performance with moving aliens - *30 min*

---

## Implementation Details

### SeededRandom Class (ALIEN-V1.2-001)
```javascript
class SeededRandom {
    constructor(seed) {
        this.seed = seed;
    }
    
    next() {
        // Linear congruential generator
        this.seed = (this.seed * 1664525 + 1013904223) % Math.pow(2, 32);
        return this.seed / Math.pow(2, 32);
    }
    
    range(min, max) {
        return min + this.next() * (max - min);
    }
}
```

### Alien Movement Properties (ALIEN-V1.2-002)
- Add `vx`, `vy` (velocity) properties
- Add `direction`, `speed` properties  
- Add `lastDirectionChange` timestamp
- Add `movementPattern` configuration

### Movement Patterns

#### Basic Alien (ALIEN-V1.2-005)
- Slow wandering motion
- Random direction changes every 2-3 seconds
- Gentle speed variations

#### Fast Alien (ALIEN-V1.2-006)
- Quick darting movements
- Frequent direction changes (0.5-1 second)
- Higher base speed

#### Bonus Alien (ALIEN-V1.2-007)
- Circular or figure-8 patterns
- Smooth curved motion
- Predictable but complex paths

#### Special Alien (ALIEN-V1.2-008)
- Teleportation between random positions
- Brief pause at each location
- Unpredictable positioning

### Rules.json Movement Section (ALIEN-V1.2-009)
```json
{
  "movement": {
    "randomSeed": 12345,
    "enabled": true,
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
      "radius": 30,
      "frequency": 0.02
    },
    "special": {
      "teleportInterval": 1500,
      "pauseDuration": 300,
      "maxJumpDistance": 100
    }
  }
}
```

---

## Success Metrics
- **Movement Fluidity**: Smooth, natural-looking alien motion
- **Performance**: Maintain 60fps with all aliens moving
- **Gameplay Balance**: Movement adds challenge without frustration
- **Configurability**: Easy to adjust movement via rules.json
- **Reproducibility**: Same seed produces identical movement patterns

## Testing Checklist
- [ ] All alien types move according to their patterns
- [ ] Movement respects canvas boundaries
- [ ] Click detection works on moving targets
- [ ] Performance remains stable during intense movement
- [ ] Random seed produces consistent results
- [ ] Movement can be disabled via configuration

## Next Steps
1. Implement SeededRandom class (ALIEN-V1.2-001)
2. Add movement properties to Alien class (ALIEN-V1.2-002)
3. Create basic movement update logic (ALIEN-V1.2-003)
4. Test with simple movement before implementing complex patterns
5. Add boundary collision system (ALIEN-V1.2-004)
6. Implement each alien type's movement pattern
7. Update rules.json configuration
8. Performance testing and optimization

---

## Notes
- Mark tasks as complete by changing `[ ]` to `[x]`
- Test movement patterns individually before combining
- Ensure movement enhances rather than hinders gameplay
- Keep movement parameters easily configurable for balancing