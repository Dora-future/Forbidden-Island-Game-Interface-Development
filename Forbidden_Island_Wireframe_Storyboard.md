# Forbidden Island: mobile interface wireframe storyboard

**Status:** Initial low-fidelity concept for discussion and user research. These screens are not validated findings. Revise them after interviews and peer evaluation.

**Format:** Portrait phone wireframes. Boxes represent controls; labels and text are intentionally plain. This is a storyboard, so each numbered screen shows a moment in a user journey.

## Flow overview

```text
[1 Home] -> [2 Create game] -> [3 Lobby] -> [4 Board / turn]
                                               |
                            choose action <-----+
                               |       |       |
                         [5 Move] [6 Shore] [7 Treasure]
                               \       |       /
                                [8 Action result]
                                         |
                              actions remain? -- yes --> [4 Board]
                                         |
                                         no
                                         v
                                [9 Flood phase]
                                  |         |
                            safe update   critical event
                                  |         v
                                  +----> [10 Board update]
                                             |
                                   win/loss condition met?
                                       |             |
                                      no            yes
                                       |             v
                                  [4 Board]    [11 End screen]
```

## Storyboard panels

### 1. Home — start or join a cooperative game

```text
+----------------------------------+
|  UWTSD: FORBIDDEN ISLAND         |
|                                  |
|  Work together. Escape together. |
|                                  |
|       [ CREATE GAME ]            |
|       [ JOIN GAME ]              |
|                                  |
|  [How to play]     [Settings]    |
|  Accessibility options           |
+----------------------------------+
```

**Interaction:** Create Game opens panel 2. Join Game opens a join-code screen (not expanded in this first storyboard). How to play opens concise rules and a tutorial. Settings opens text, audio, contrast, and input preferences.

**Design question to test:** Do players understand whether this is pass-and-play on one device or networked play? Add a mode choice if users expect both.

### 2. Create game — choose table setup

```text
+----------------------------------+
|  < Back       CREATE GAME        |
|                                  |
|  Players                        |
|  [ - ]       2       [ + ]       |
|                                  |
|  Game difficulty                 |
|  ( ) Beginner  ( ) Standard      |
|                                  |
|  Play mode                       |
|  (•) Pass this phone             |
|  ( ) Each player has a device    |
|                                  |
|  [ CONTINUE ]                    |
+----------------------------------+
```

**Interaction:** Continue opens panel 3. For a networked mode, this screen would also offer invite/link and access code. Difficulty labels need to match the ruleset used in the course project.

### 3. Lobby — confirm players and roles

```text
+----------------------------------+
|  < Back          GAME LOBBY      |
|                                  |
|  Player 1    [Choose role v]     |
|  Player 2    [Choose role v]     |
|  Player 3    [Open slot]         |
|                                  |
|  Roles have different abilities. |
|  [What does each role do?]       |
|                                  |
|  Mode: Pass this phone           |
|                                  |
|       [ START GAME ]             |
+----------------------------------+
```

**Interaction:** Role selector opens a short, readable role description; role is confirmed before returning to lobby. Start Game opens the board. Use text and icon labels so role meaning is not colour-only.

### 4. Game board — shared situation and turn controls

```text
+----------------------------------+
|  TURN: MAYA       Actions: 3     |
|  Water level:  [|||----]         |
|                                  |
|       ISLAND MAP (6 x 6)         |
|   [ ] [~] [ ] [ ] [X] [ ]        |
|   [ ] [M] [ ] [T] [ ] [ ]        |
|   [ ] [ ] [~] [ ] [ ] [ ]        |
|   [ ] [ ] [ ] [J] [ ] [ ]        |
|   [ ] [T] [ ] [ ] [H] [ ]        |
|   [ ] [ ] [ ] [ ] [ ] [ ]        |
|                                  |
|  [Move] [Shore up] [More...]     |
|  Hand: [Card] [Card] [Card]      |
|  [End actions / Draw floods]     |
+----------------------------------+
```

**Legend in prototype:** `[ ]` safe tile, `[~]` flooded tile, `[X]` sunken tile, `M/J` player markers, `T` treasure site, `H` helipad. In the real wireframe, do not rely on these letters or colour alone: pair clear symbols with labels, and provide a tile detail view. Keep map tiles large enough to tap; allow pan/zoom or an alternate list if the board cannot fit legibly.

**Interaction:** Tapping a tile shows its name, state, occupants, and available actions. Move/Shore up open the relevant selection state. More opens Collect treasure, Give card, Role ability, and help when legal under the chosen rules. End actions starts the flood phase after confirmation.

### 5. Move — select a legal neighboring tile

```text
+----------------------------------+
|  < Board        MOVE             |
|                                  |
|  Choose a neighboring tile.      |
|  Current tile: Fools' Landing    |
|                                  |
|    [North tile]                  |
|  [West tile] [You] [East tile]   |
|    [South tile]                  |
|                                  |
|  Selected: East tile             |
|  [Tile details]                  |
|  [ MOVE HERE ]    [Cancel]       |
+----------------------------------+
```

**Interaction:** Only legal destinations are enabled and identified in more than one way (shape/label and state, not colour alone). Confirming moves the player and returns to panel 8. Disabled destinations explain why they cannot be selected.

### 6. Shore up — choose a flooded tile

```text
+----------------------------------+
|  < Board       SHORE UP          |
|                                  |
|  Choose a flooded tile nearby.   |
|                                  |
|      [Safe]                      |
|  [Safe] [You] [Flooded]          |
|      [Flooded]                   |
|                                  |
|  Selected: Moon Palace           |
|  This tile will become safe.     |
|  [ SHORE UP ]      [Cancel]      |
+----------------------------------+
```

**Interaction:** Confirmation changes the tile state and returns to panel 8. Make the result explicit in text and screen-reader announcement. If no legal tile is in range, explain this and offer a route back.

### 7. Collect treasure — check and confirm requirement

```text
+----------------------------------+
|  < Board     COLLECT TREASURE    |
|                                  |
|  You are at: Temple of the Sun   |
|  Treasure: Sun                   |
|                                  |
|  Cards needed: 4 Sun cards       |
|  Your hand:  [Sun] [Moon] [Sun]  |
|  Team has:   2 / 4 Sun cards     |
|                                  |
|  [ COLLECT SUN ]   [Cancel]      |
|                                  |
|  Not ready? [View team cards]    |
+----------------------------------+
```

**Interaction:** Enabled only if the rules' conditions are met. If not, explain exactly what is missing and return without consuming an action. Confirming updates the shared treasure status and returns to panel 8.

### 8. Action result — confirm what changed

```text
+----------------------------------+
|  ACTION COMPLETE                 |
|                                  |
|  Maya moved to Moon Palace.      |
|  Actions remaining: 2            |
|                                  |
|  Island status: 3 flooded tiles  |
|  Team treasures: Sun 1/4         |
|                                  |
|  [NEXT ACTION]  [View board]     |
+----------------------------------+
```

**Interaction:** Next Action returns to the board with legal options updated. If zero actions remain, guide the player to the flood phase. Results should be announced accessibly and remain visible until acknowledged.

### 9. Flood phase — draw and resolve island changes

```text
+----------------------------------+
|  FLOOD PHASE                     |
|                                  |
|  Flood cards to resolve: 2       |
|  1. Moon Palace — now flooded    |
|  2. Coral Gate — already flooded |
|     -> Coral Gate has sunk       |
|                                  |
|  Sunken tiles cannot be used.    |
|  [Show changes on map]           |
|  [ CONTINUE ]                    |
+----------------------------------+
```

**Interaction:** Explain whether a tile flooded, sank, or was discarded according to the actual rules. Continue returns to panel 10. Critical loss conditions should be plainly stated and not conveyed by animation alone.

### 10. Updated board — next player handoff

```text
+----------------------------------+
|  BOARD UPDATED                   |
|  Coral Gate has sunk.            |
|  Water level: [||||---]          |
|                                  |
|       ISLAND MAP                 |
|   [ ] [~] [ ] [ ] [X] [ ]        |
|   [ ] [M] [ ] [T] [ ] [ ]        |
|   [ ] [ ] [X] [ ] [ ] [ ]        |
|   [ ] [ ] [ ] [J] [ ] [ ]        |
|   [ ] [T] [ ] [ ] [H] [ ]        |
|                                  |
|  Next player: JAMIE              |
|       [ PASS PHONE ]             |
+----------------------------------+
```

**Interaction:** In pass-and-play mode, Pass Phone hides private hand information before handing over. In network mode, next-player handoff is automatic. If a loss or win condition has been met, show panel 11 instead.

### 11. End state — communicate outcome and next step

```text
+----------------------------------+
|  THE ISLAND IS LOST              |
|                                  |
|  Coral Gate sank before everyone |
|  escaped. Your team collected    |
|  2 of 4 treasures.               |
|                                  |
|  [See final island]              |
|  [Play again]  [Return home]     |
+----------------------------------+
```

**Alternative win state:** “You escaped together!” State which objective was completed, then offer the same clear next steps. Avoid a result that depends on colour, sound, or animation alone.

## Storyboard assumptions to validate

- This concept uses turn-based play and a shared island map, based on the familiar Forbidden Island rules. Confirm the exact rules with the tutor/course specification.
- Pass-and-play and network play are shown as possible modes, but the assignment may only require one. Ask users which mode fits their expected play context.
- The map uses a 6 x 6 arrangement as a placeholder. Use the correct board setup for the selected rules and test whether it is usable on a phone.
- Action labels, hand visibility, team card information, and end conditions should be checked against the official/course rules.
- Accessibility needs are not represented by a single persona or setting. Interview users and document relevant preferences; design clear text labels, scalable text, adequate touch targets, non-colour state cues, screen-reader names and announcements, and alternatives to time-dependent or gesture-only interactions.

## Cognitive walkthrough task outlines

### Task A: Open app and create a game

1. From panel 1, find and activate Create Game.
2. Choose player count, difficulty, and play mode on panel 2.
3. Continue to panel 3; choose roles and start.
4. Confirm the board clearly communicates whose turn it is and what to do first.

At each step ask: Will a first-time player know what goal they are trying to achieve? Will they notice the control? Will its label make the correct action clear? After acting, will they understand the feedback and know what to do next?

### Task B: Moderately complex turn

Example route: on panel 4, move to a neighboring tile using panel 5; shore up a flooded nearby tile using panel 6; collect a treasure if the rules and cards permit using panel 7; review action feedback at panel 8; finish actions and resolve flood cards in panel 9; review the updated board and hand off at panel 10.

Walk through only actions legal under the exact game rules. Record any point where the player cannot see available actions, understand a restriction, recover from an error, or understand how the island changed.

## Next iteration checklist

- Replace assumptions with themes from 4–5 user interviews; keep raw notes anonymous.
- Confirm all game rules, action counts, card requirements, and failure conditions against the course-approved rules.
- Draw the final storyboard at a consistent phone viewport size; show arrows, branches, and back/cancel routes.
- Run and document both walkthroughs using the supplied course format if one exists.
- Update the wireframes after peer reviews; preserve the three reviews you make and the three you receive for the report appendices.
