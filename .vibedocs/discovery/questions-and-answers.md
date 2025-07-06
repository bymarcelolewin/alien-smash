# Alien Smash - Questions and Answers

Based on the game specification, I have some questions to help clarify the implementation:

## Technical Questions

1. **Screen Size**: What screen dimensions should we target? (e.g., 800x600, 1024x768, or responsive?)
800x600

2. **Mobile Support**: Should the game be fully responsive for mobile devices, or is desktop-first acceptable for the live presentation?
not now

3. **Asset Creation**: Do you want me to create simple geometric shapes for aliens, or would you prefer to use emoji/Unicode characters as placeholders?
Yes - Simple geometric shapes

## Game Design Questions

4. **Game Duration**: Should there be a time limit for each game session, or does it continue until the player runs out of lives?

Yes.  But continue until no mor lives.

5. **High Score**: Should we implement a local high score system using localStorage?

Not yet.

6. **Difficulty Scaling**: Should the difficulty increase be linear or exponential? How fast should it ramp up?

Linear

## Visual Questions

7. **Color Scheme**: Any specific color preferences for the space theme? (dark blues, purples, etc.)

You pick it.

8. **Alien Sizes**: Should aliens be different sizes, or all uniform? Different sizes could affect difficulty.

Yes.

9. **Animation Style**: Simple fade in/out for aliens, or more elaborate spawn/despawn animations?

Simple for now.

## Audio Questions

Skip audio for now.

10. **Audio Priority**: Since this is for a live presentation, should audio be optional/mutable? Some presentation environments don't handle audio well.

11. **Audio Files**: Should I create simple beep sounds using Web Audio API, or do you have specific audio files?

## Implementation Questions

12. **File Structure**: Should this be a single HTML file with embedded CSS/JS for simplicity, or separate files?

I would like to keep the css in it's own file.   And have html file link to it.

13. **Browser Compatibility**: Any specific browser requirements, or modern browsers only?

Modern Chrome.

---

*Please answer the questions above, and I'll implement the game accordingly.*

## Follow-up Questions

**Question 8 Clarification (Alien Sizes)**: You answered "Yes" but the question was asking if aliens should be different sizes OR all uniform. Should I create aliens with different sizes (small, medium, large) or keep them all the same size?

All Uniform.