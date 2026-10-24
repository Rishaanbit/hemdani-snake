# HEMDANI — Snake

Open `index.html` in a modern browser. The entire game, fonts, logo, music, and sounds are contained in this one file. No installation, server, or internet connection is required.

## Play

- Arrows or WASD steer; two valid turns can be buffered.
- Space pauses/resumes and starts/replays. R starts a fresh run. M toggles sound.
- On touch devices, swipe the field or use the large directional pad. Tap the pause button to pause or change speed.
- Eat amber pixels for 10 points, grow, and avoid walls and your own body.
- Cruise, Classic, and Overdrive use constant speeds. You can change speed while paused.
- Desktop keeps the fixed 800 × 400 pixel, 40 × 20 grid. Phones use a responsive layout, with a 24 × 24 square grid for new portrait runs and a 40 × 20 grid for landscape runs. Rotating during a run pauses it and preserves its grid, score, and snake.

## Feedback and replay

Pickups combine a small pixel burst, an expanding ring, a short score pop, and a five-note musical pattern. The first food appears a short distance ahead to make the initial interaction clear. A thin HUD line shows progress to the run's personal-best target; a first run uses a 50-point opening target. Passing the target produces a brief record celebration. Effects respect reduced-motion preferences.

The final board remains visible after a crash. The result shows the score and its actual distance from the previous best, followed by an immediate replay action. An original, moody eight-bar chiptune in A minor at 112 BPM plays during a run, quietly underneath pickup sounds. It pauses with the game, stops at game over, and restarts cleanly on replay. SOUND and the M shortcut control both music and effects. Selected speed and sound preferences are remembered in the browser.

Scores are stored locally by speed. When speed is changed during a run, the final record belongs to the slowest mode used; a score earned before slowing remains a valid record for the earlier mode. Storage failures do not prevent play. The game automatically pauses when its window loses focus.

## Design sources

The changes apply ideas from original developer work and motivation research:

- [Martin Jonasson and Petri Purho, *Juice It or Lose It*](https://www.youtube.com/watch?v=Fy0aCDmgnxg): layered audiovisual feedback can make simple interactions feel more alive.
- [Ryan, Rigby, and Przybylski, *The Motivational Pull of Video Games* (2006)](https://selfdeterminationtheory.org/SDT/documents/2006_RyanRigbyPrzybylski_MandE.pdf): perceived competence, autonomy, and intuitive controls are associated with enjoyment and willingness to play again.
- [Maddy Thorson, *Celeste & Forgiveness*](https://www.mattmakesgames.com/articles/celeste_and_forgiveness/index.html): forgiving input handling helps players act on their intentions.

The specific Snake implementation is a design application of those ideas. Its effect on replay rates has not been measured with players.

## Project files

- `index.html` — the complete HEMDANI Snake game, with embedded styles, JavaScript, fonts, logo, and audio.
- `preview.png` — a screenshot of the game.
- `.nojekyll` — tells GitHub Pages to serve the website directly, without a build step.
- `.gitignore` — keeps local development files out of the public repository.

## Hosting

GitHub Pages publishes the root of the `main` branch. No packages, build command, or custom workflow are needed. Changes pushed to `main` are published automatically.

Local drafts, backups, and verification scripts remain in the ignored `work/` folder. They are not needed to run the website.
