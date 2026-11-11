!\[Ink Duel: five opponents drawn in ink](banner.png)

# Ink Duel

A one-screen browser game where the stroke you draw is the attack. Five opponents, one brush, no install.

**Play it:** https://mohib-ur-rehman-automation.github.io/ink-duel/

> They took your name, stroke by stroke. Cut it back.

## How to play

Draw on the page with a mouse or a finger.

|Move|How|What it does|
|-|-|-|
|**Cut**|One fast line through the opponent|Damage. Slow lines do nothing.|
|**Parry**|Cut a red line before it lands|Cancels the attack and staggers the opponent. Cuts on a staggered opponent do double.|
|**Guard**|Draw a circle|Blocks for about a second.|
|**Break**|Hold still until the ink pools, then cut|The only cut that goes through an opponent's ring.|

Every stroke spends ink. Run dry and your strokes do nothing until it refills.

### Reading the attacks

|You see|Answer|
|-|-|
|Thin red line|Cut it, or guard|
|Red line from the edge of the page|Cut it, or guard|
|Thick red line|Cut it. A guard shatters.|
|Red ring growing outward|Guard. It cannot be cut.|
|Red line that fades|A feint. The real one follows.|

Keys: `P` or `Esc` pause, `T` light/dark, `M` sound.

## The five

1. **Hollow Reed** bends and does not hurry.
2. **Nine Crows** attacks from the edges. Count its health in birds.
3. **The Bellwether** tolls rings you cannot cut.
4. **Winter Magistrate** shows one line and means another.
5. **The Unsigned** wants the whole page.

## What is in the file

Everything is in `index.html`: about 600 lines of plain JavaScript on a 2D canvas, no libraries, no build step, no server.

* **Ink:** brush strokes with speed-based width, flying droplets that dry into the page, a paper texture generated at load.
* **Gestures:** each stroke is classified by length, straightness, speed and turning angle.
* **Opponents:** five procedurally drawn bodies, each with its own attack phrases that change below half health.
* **Sound:** a generated score and all effects, synthesised in the browser. No audio files.
* **Fonts:** Anton and Newsreader from Google Fonts. Offline, it falls back to system fonts.

Progress and settings are saved in your own browser and sent nowhere.

## How it was made

Designed and directed by Mohib Ur Rehman. The code was written by Claude (Anthropic) across one evening of play-testing and revision in November 2026: I played each build, said what was wrong, and chose what stayed.

## Known limits

* Tested in Chrome on a laptop and at phone size. Firefox and Safari are untested.
* Balance of duels II to V has had little play-testing.
* The score is generated, not composed, and was mixed by measurement.

## Licence

MIT. See `LICENSE`.

