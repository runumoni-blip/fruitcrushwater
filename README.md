# Fruit Flood — Juicy Physics

A match game in a rising glass of water. Fruit drops from the dispenser, splashes in, floats and bobs, and piles up as the water rises. Burst chains of matching fruit to pump the water back down before anything floats over the rim.

Open `index.html` in any modern browser. It's a single file with no downloads or dependencies, and it works on phones (touch) and desktops (mouse).

## How to play

- **Drag** across 3 or more touching fruits of the same kind, then let go to burst them. Slide back to undo the last link.
- **Longer chains** score more (10 × length², plus a combo bonus for quick follow-ups).
- **Chain 6 or more** to earn a **bubble bomb**. Tap it to burst everything nearby. Bombs set each other off.
- Every burst pumps water out, and fewer fruits displace less water, so the level drops.
- **Tap the water** to send a ripple that nudges fruit. **Tap a fruit** to make it hop.
- **DRAIN** (or the space bar) empties a lot of water fast. You get 3 per level, and unused ones pay a bonus.
- If fruit pokes over the rim for 3 seconds, or the water reaches the brim, the glass overflows.
- Pause with the button, `P`, or `Esc`. The game also pauses if you switch away.
- Your progress and best score are saved in the browser. Next time, **Continue** picks up at the level you reached, or start a **New game** from level 1.

When you're stuck, the game helps. After a few idle seconds a hint glows, and on early levels a ghost finger traces a chain. If no chain exists, matching fruit slowly drift toward each other.

## What's inside

**Realistic fruit, painted in code.** Each fruit (apple, orange, lemon, grapes, watermelon, blueberry) is built at load time as albedo, normal and material maps from procedural noise: apple streaks and lenticels, citrus pores, melon stripes, the dusty bloom on grapes and blueberries. It's then lit per pixel in 24 rotation frames, so the highlight stays put while the fruit rolls. The sprite resolution adapts to the screen, and the work is time-sliced so the page never freezes.

**Everything moves by physics.** Fruit are rigid circular bodies in a substepped position-based solver with spin, Coulomb friction (they roll rather than slide) and bounce. In water they get buoyancy from the submerged area, added-mass damping and drag. Apples ride high and grapes sink. The water level comes from the poured volume plus the Archimedes displacement of every fruit. A spring-mass surface carries waves that fruit ride and make.

**Blasts with joy.** Pops cascade along the chain on a rising musical scale. Each pop sprays juice in the fruit's colour (or blooms like ink underwater and throws up a splash plume), scatters flesh, seeds and berries, flashes, and shoves the neighbours. Then come confetti, sparkles, a praise word ("Juicy!", "Fruitastic!", "TUTTI FRUTTI!") and a score that counts up.

**Sound** is a small Web Audio synth with a touch of reverb. No audio files.
