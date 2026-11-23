# Forbidden Island mobile app assignment: starter guide

## What the game is

Forbidden Island is a cooperative game: players work together against the island flooding. A typical turn involves taking up to three actions (for example, moving to an adjacent tile, shoring up a flooded tile, collecting a treasure, or using a role ability), then drawing cards that may flood tiles. The team wins by collecting all four treasures and escaping from the helipad; the team loses if key locations sink or the water level gets too high. Check the official rules or the version your tutor expects before treating these details as final.

Your assignment is to design the **mobile interface** that helps people play this kind of game. The wireframes show what appears on the phone and how a player moves between screens. They do not need to implement the game or look like a finished, colourful product.

## Work plan

1. Ask 4–5 real potential users about cooperative games, playing on phones, and access needs. Get their agreement before taking notes; do not record names unless needed.
2. Summarise what you heard, including differing views. Use those findings to create three evidence-based personas, one a computing student and one with accessibility needs.
3. Convert findings into user and experience requirements. Sort each into Must, Should, Could, or Won't for this version (MoSCoW).
4. Sketch mobile-sized wireframe storyboards for the key flows: open/create or join a game; view the board and status; take a turn; resolve flooding; handle an important warning or end state. Show arrows and decisions between screens.
5. Run cognitive walkthroughs for (a) opening the app and creating a game and (b) a turn with several actions. Note where a first-time user might not know what to do or understand the feedback.
6. In your class group, complete the individual heuristic reviews and group discussion required by the brief. Keep the three reviews you make and the three you receive, using the provided template.
7. Write the report, discuss the important screens and feedback, and include the required material in appendices. Use research literature to justify design decisions; at least two-thirds of references should be books or journal papers.

## Starter interview script (about 10 minutes)

Start by saying: “I’m designing a phone interface for a cooperative island-rescue game for a university assignment. I’m interested in your preferences and needs; there are no right answers. You can skip any question. May I take notes?”

Ask 4–5 people, ideally with varied gaming experience and devices. Ask the same core questions, then use follow-ups where useful.

1. What kinds of games do you play, if any? What do you enjoy or find frustrating about playing with other people?
2. Have you played a cooperative board or mobile game? Tell me about a recent example.
3. If you and friends were trying to rescue a team from a flooding island, what information would you need to see at a glance?
4. What would you expect to be able to do on your turn? What might be confusing if the app did not explain the rules?
5. Would you prefer to play together around one phone, each on your own phone, or either? Why?
6. What phone or input methods do you normally use (touch, keyboard, switch, voice control, screen reader, stylus, other)?
7. Are there any visual, hearing, motor, cognitive, or other access needs or settings that affect how you use games? Only share what you are comfortable sharing.
8. What would make the game easier or more enjoyable to use? What would put you off?
9. Is there anything else you would want the designer to know?

Avoid leading questions such as “Would you like a big button?” Ask what the person needs first, and record their words or a faithful summary. Do not claim these few participants represent all UWTSD students.

## Notes table for your real interviews

| Participant code | Broad context they chose to share | Games/device context | Needs or preferences (short quotes or faithful notes) | Design implications to investigate |
|---|---|---|---|---|
| P1 |  |  |  |  |
| P2 |  |  |  |  |
| P3 |  |  |  |  |
| P4 |  |  |  |  |
| P5 (optional) |  |  |  |  |

Keep consent and notes private and follow your course’s research ethics guidance. Do not invent responses or attribute a need to someone who did not report it.

## Suggested report structure

1. **Introduction and scope** – the problem, intended players, and what this prototype covers.
2. **User research** – participants (anonymous codes), method, questions, findings, limitations, and how findings informed design.
3. **Personas and scenarios** – three evidence-linked personas, including the required computing student and accessibility persona; each has goals, context, needs, and a game-use scenario.
4. **Requirements** – summarise the key needs in the main report; include the full MoSCoW list in an appendix.
5. **Devices and accessibility** – discuss touch-screen constraints and relevant assistive technology based on research and participant findings (for example screen readers, text scaling, switch access, voice control, captions/haptics where relevant). Explain concrete interface responses.
6. **Wireframe storyboards** – explain key screens, navigation, status information, action choices, feedback, and error prevention. Put the complete storyboard set in an appendix.
7. **Evaluation** – report the two cognitive walkthroughs and the student heuristic/group evaluation. Summarise agreement, disagreement, and the changes to prioritise next.
8. **Conclusion** – what the next design iteration should address.
9. **References** – consistent academic style; ensure at least two-thirds are books or journal papers.
10. **Appendices** – interview/questionnaire questions; MoSCoW requirements; full storyboards; both walkthrough reports; the three peer reviews you completed; the three reviews received.

## Wireframe screen checklist

- Welcome/home: start, join, rules/help, accessibility/settings.
- Create/join: player count or invite/join method, role selection if applicable, ready state.
- Game board: island tiles, player positions, flooded/sunken states, treasures, helipad, water level, whose turn, action count, and a clear way to inspect a tile.
- Turn actions: move, shore up, collect treasure, share card/use role ability where the rules permit; show available actions and remaining actions.
- Feedback: explain what happened after each action and after flood-card draws; make urgent warnings understandable without relying on colour alone.
- End states: team win, loss, and what happened.

Use labels, arrows, and numbered steps to show transitions. Keep each drawing at a plausible phone-screen size and use monochrome shapes and text at this stage.

## MoSCoW worksheet

For each requirement, write a short testable statement and cite the interview evidence or design rationale behind it. Avoid filling this with assumptions before the interviews.

| Priority | Requirement (The player can / needs to…) | Evidence or rationale | How the wireframe addresses it |
|---|---|---|---|
| Must |  |  |  |
| Should |  |  |  |
| Could |  |  |  |
| Won't (this version) |  |  |  |

## Cognitive walkthrough note template

For each step in the task, record: **user goal**, **visible action**, **will a first-time user know this is the right action?**, **will they notice the control?**, **will they understand the feedback?**, and **issue/recommendation**.

- Task A: open app and create a game.
- Task B: complete a moderately complex turn with two or three common actions, then resolve the resulting game feedback.

## Important class materials to collect

- The tutor-provided heuristic evaluation template.
- Three completed individual reviews you make of other students' storyboards.
- Three individual reviews other students make of your storyboard.
- Notes from the group's discussion of your design, including points of agreement and disagreement.

These are real course activities and cannot be filled in accurately in advance. Add them after the class session.
