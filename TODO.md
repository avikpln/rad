# TODO

## General

- [ ] Add unit testing, test automation, and logging throughout
- [ ] Add documentation throughout the entire codebase
- [ ] Add gameplay stats (e.g., step counter)
- [ ] Migrate remaining tasks from legacy `TODO.txt`

---

## Web & Compatibility

- [ ] Smooth page loading
- [ ] Touch support
- [ ] Responsive web design
  - Responsive text (e.g., `font-size: 10vw`)
  - Responsive images (e.g., `max-width: 100%; height: auto`)
- [ ] Cross-browser testing via [BrowserStack](https://www.browserstack.com/)
- [ ] W3C validation via [validator.w3.org](https://validator.w3.org/)
- [ ] Fix Safari/Mac compatibility — anchor `#` fragments may need to be replaced with `_`
- [ ] Fix loading issue on iPhone
- [ ] Test on tablet

---

## Script / Architecture

- [ ] Use radial gradient to color player and Randy
- [ ] Apply lessons learned from studying HTML canvas (context handling)
- [ ] Add fallback text in HTML for unsupported elements (e.g., `<canvas>`)
- [ ] Validate `canvas` and `getContext` after `querySelector`
- [ ] `GAME`: Remove player as argument to state extraction
- [ ] `GAME`: Add `numLevels` and `roomsPerLevel` arguments to game tester
- [ ] `GAME`: Fix `stoneRequirement` and player 0 issue in game tester
- [ ] `GAME`: Split oversized `#createNetwork` method
- [ ] `GAME`: Cache game state info that doesn't change between calls
- [ ] `GAME`: Consider a `DoorManager` class
- [ ] `GAME`: Consider a `Network` / `NetworkBuilder` class
- [ ] `ROOM`: Merge `createGrid` and `createCells`
- [ ] `ROOM`: Reconsider `availableLocs` / `occupiedLocs` data structures
- [ ] `GUI`: Color welcome door according to level
- [ ] `GUI`: Handle `randyIsDone` index more cleanly
- [ ] `GUI`: Add `launch()` method
- [ ] `GUI`: Split `GUI` class into smaller classes (consider `HTMLManager`, `EventManager`)
- [ ] `GUI`: Display something when quitting
- [ ] `GUI`: Separate page title from game title
- [ ] `DISPLAYER`: Reconsider `TERMINAL` prefix
- [ ] `DISPLAYER`: Use proper `<blockquote>` for quotes
- [ ] `DISPLAYER`: Remove `Displayer`'s dependence on `Game`
- [ ] `DRAWER`: Revisit `clearDisplay` — consider using `clearRect`
- [ ] `DRAWER`: Improve validation process
- [ ] `DRAWER`: Make CSS properties (e.g., `font-family`) configurable
- [ ] `DOORS`: Decide whether terminal door should be a plain door
- [ ] `RANDY-MANAGER`: Revisit delay formula
- [ ] `GRAPH`: Use private members
- [ ] `GRAPH`: Consider `Vertex` and `Edge` classes
- [ ] `GRAPHUTILS`: Early exit in MST search once tree is found

---

## Easy Wins

- [ ] Group `Validator` tests in a `#validator` method
- [ ] Fix circular inclusion of `Room` and `Door` (options: `Enterable` superclass, or `addElement` in `Room`)
- [ ] Organize folders into subfolders of related modules
- [ ] Replace `Location` class with plain `x, y` coordinates (consider a `Point` class)
- [ ] Write a TODO comment block at the top of each module
- [ ] Have door measures be multiples of 1/16 (or 1/32) for drawing resolution consistency
- [ ] Decide: 30 or 47 rooms per level?
- [ ] Decide: should room count increase with level?
- [ ] Decide: should Randy's delay be reduced from 400ms to 300ms?
- [ ] Decide: scatter stones randomly across levels, or strictly one per level?
- [ ] Decide: which door shapes belong in which levels?
- [ ] Add a "sound off" button
- [ ] Control randomness with a seed to help reproduce bugs
- [ ] Cap max graph degree — re-roll if too high (`Graph.getMaxDegree`)
- [ ] Add game mode selector — Memory mode vs. Fantasy mode:
  - **Memory**: no stones, uniform door colors, single level
  - **Fantasy**: stones, varied door colors, multiple levels
- [ ] Use `CamelCase` for color names
- [ ] Rename private fields from `#name` to `_name` for Mac Safari compatibility
- [ ] Highlight missing stones for the current level in the plate display

---

## Hard / Long-Term

- [ ] Host Git repository on a cPanel account
- [ ] Investigate why JavaScript updates are sometimes not seen by users (caching)
- [ ] Benchmark Randy to calibrate delay vs. auto-pilot speed
- [ ] Fix inconsistency in game element display (relative vs. absolute pixel sizing)
- [ ] Mark visited doors visually (show them as open)
- [ ] Make Randy prioritize rooms by rank/shape
- [ ] Display distance from target
- [ ] Add auto-play via click, touch, or voice
- [ ] Resume from pause when arrow key is pressed
- [ ] Fix overlapping sounds being silently ignored
- [ ] Implement Python tests (Randy expectation, diameter consistency, etc.)
- [ ] Add richer response when player tries to open final door without all stones
