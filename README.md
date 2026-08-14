
# ⚽ Offside Detector — Position ≠ Offense

An interactive football offside simulation designed to demonstrate the distinction between **offside position** and an actual **offside offense** under Law 11 of the IFAB Laws of the Game.

The project uses animation, synchronized playback, a simplified rule engine, and step-by-step event analysis to make an offside scenario easier to understand and test.

---

## 📌 Problem Statement

The project demonstrates a position-based offside detection scenario where an attacking player can be identified as being in an **offside position** when a teammate plays the ball toward them.

The important distinction is:

> **Being in an offside position is not, by itself, an offside offense.**

The player's subsequent involvement in play must be considered according to the relevant conditions of Law 11.

The project focuses on a specific scenario:

```text
Player A passes the ball
        ↓
Player B is in an offside position
        ↓
Player B moves toward the ball
        ↓
Player B has not touched the ball
        ↓
Player D, a defender, reaches the ball first
        ↓
Player D intercepts the ball
````

The purpose of the simulation is to make the difference between **offside position** and **offside offense** visible.

---

# 🎯 Project Objective

The main objectives are to:

1. Detect when Player B is in an offside position.
2. Record the moment Player A plays the ball.
3. Track Player B's movement after the pass.
4. Determine whether Player B touches or plays the ball.
5. Track Player D's movement toward the ball.
6. Detect when Player D intercepts the ball.
7. Compare a simplified position-based detector with a Law 11-inspired analysis.
8. Show the complete sequence through an interactive replay.
9. Keep animation, voice, captions, and rule analysis synchronized.
10. Allow the user to inspect the critical moments using slow motion and step controls.

---

# ⚽ Main Simulation Scenario

The simulation uses three relevant players:

* **Player A** — Attacking player who plays the pass
* **Player B** — Attacking player who is in an offside position
* **Player D** — Defender who reaches and intercepts the ball

There is **no Player C in the main scenario**.

The sequence is:

```text
              SECOND-LAST DEFENDER
                      │
                      │
----------------------│---------------- OFFSIDE LINE


Player A                         Player B
   🔴                               🔴
   ⚽  ─────────────────────────────→
                                     ↑
                              Offside Position

                              Player D
                                 🔵
                              Defender
```

---

# 1. Initial Position

Player B is positioned beyond the second-last defender.

The system identifies:

```text
Player B
   ↓
OFFSIDE POSITION
```

This represents a **positional state**.

The simulation does not treat this positional state alone as the complete analysis.

---

# 2. Player A Plays the Ball

Player A plays the ball toward Player B.

```text
Player A

   🔴
   ⚽
    \
     \
      \────────────────────→ ⚽
                              \
                               \
                              Player B
                                🔴
```

The simulation records the exact moment the ball is played.

This moment becomes an important reference point for the offside analysis.

---

# 3. Player B Moves Toward the Ball

After Player A plays the ball, Player B begins moving toward it.

```text
Player B
   🔴
    \
     \
      → ⚽
```

The simulation visibly shows Player B advancing toward the ball.

---

# 4. Player B Has Not Touched the Ball

Player B approaches the ball but has not touched or played it.

```text
Player B
   🔴
    \
     \

       ⚽
```

This is one of the key moments of the demonstration.

The simulation records:

```text
PLAYER B
↓
NO TOUCH
```

---

# 5. Player D Intercepts

Before Player B can play the ball, Player D, the defender, reaches it first.

```text
Player B                         Player D
   🔴                              🔵
    \                              /
     \                            /
      \          ⚽              /
       \________________________/
                  ↑
             INTERCEPTION
```

The simulation records:

```text
PLAYER D
↓
DEFENDER INTERCEPTION
```

The complete sequence is therefore:

```text
Player A passes
      ↓
Player B is in offside position
      ↓
Player B moves toward ball
      ↓
Player B does not touch ball
      ↓
Player D reaches ball first
      ↓
Player D intercepts
      ↓
Law 11-inspired analysis
```

---

# 🧠 Core Concept

The central principle demonstrated by this project is:

```text
╔══════════════════════════════════╗
║                                  ║
║       OFFSIDE POSITION           ║
║                ≠                 ║
║       OFFSIDE OFFENSE            ║
║                                  ║
╚══════════════════════════════════╝
```

Player B being in an offside position is a different concept from determining whether an offside offense has occurred.

The simulation therefore separates:

```text
PLAYER B'S POSITION
        ↓
PLAYER A PLAYS THE BALL
        ↓
PLAYER B'S SUBSEQUENT ACTION
        ↓
PLAYER B'S INVOLVEMENT
        ↓
PLAYER D'S INTERCEPTION
        ↓
RULE ANALYSIS
        ↓
FINAL DECISION
```

---

# 🔴 Position-Based Detection

The project includes a simplified position-based detector for comparison.

Its simplified sequence is:

```text
Player B is in an offside position
              ↓
Player A plays the ball
              ↓
Position detected
              ↓
OFFSIDE
```

This represents the behavior being investigated by the simulation.

The purpose is not to claim that any particular commercial system actually uses this exact algorithm.

It is a simplified model used to demonstrate the difference between **position detection** and **offense determination**.

---

# 🟢 Law 11-Inspired Analysis

The second approach evaluates what happens after Player A plays the ball.

```text
Player B in offside position
            ↓
Player A plays ball
            ↓
Player B moves toward ball
            ↓
Player B has not touched ball
            ↓
Player D intercepts
            ↓
Evaluate subsequent involvement
            ↓
Law 11-inspired analysis
            ↓
Final decision
```

This approach makes the sequence of events visible instead of relying only on Player B's initial position.

---

# 🔬 Comparison

The same football scenario is evaluated using two approaches.

## Position-Based Approach

```text
Player B's position
        ↓
Offside position
        ↓
Player A plays ball
        ↓
OFFSIDE
```

## Law 11-Inspired Approach

```text
Player B's position
        ↓
Player A plays ball
        ↓
Player B moves
        ↓
Player B does not touch ball
        ↓
Player D intercepts
        ↓
Evaluate relevant criteria
        ↓
Final decision
```

The comparison is the main purpose of the project.

---

# 🎥 Interactive Replay

The project provides an animated replay of the complete scenario.

The controls are:

| Button | Function             |
| ------ | -------------------- |
| ⏮      | Step Back / Previous |
| ▶      | Play / Resume        |
| ⏭      | Step Forward         |
| ↻      | Reset                |

The simulation also supports:

```text
0.5×
```

slow-motion playback.

This allows the user to inspect the important moments carefully.

---

# ⏯ Master Simulation Timeline

The simulation uses one master timeline.

```text
                    MASTER TIMELINE
                           │
          ┌────────────────┼────────────────┐
          ↓                ↓                ↓
       Player A         Player B         Player D
          ↓                ↓                ↓
        Pass            Movement        Interception
          │                │                │
          └────────────────┼────────────────┘
                           ↓
                       Ball State
                           ↓
                       Rule Engine
                           ↓
                        Decision
```

All major simulation components are synchronized with the same timeline.

---

# ⏸ Pause Behavior

When the simulation is paused:

```text
⏸ PAUSE
```

everything must stop.

This includes:

* Player A movement
* Player B movement
* Player D movement
* Ball movement
* Timeline
* Voice narration
* Captions
* Event progression
* Rule-analysis progression

The voice must also stop when the simulation stops.

Nothing should continue independently in the background.

---

# ▶ Resume Behavior

When the user presses:

```text
▶
```

the simulation continues from the exact point where it was paused.

For example:

```text
Simulation time: 05.42 seconds

        ↓
      PAUSE

Everything stops

        ↓
      RESUME

Simulation continues from:

05.42 seconds
```

The simulation should not restart from the beginning.

The narration should also continue from the corresponding point.

---

# 🐌 Slow Motion

The simulation supports:

```text
0.5× Slow Motion
```

Slow motion applies to the master simulation timeline.

The following should remain synchronized:

* Player A
* Player B
* Player D
* Ball
* Timeline
* Captions
* Events
* Voice narration

This allows the user to inspect the exact moment when Player D reaches the ball.

---

# 🎙 Voice Narration

The simulation includes synchronized narration.

Example narration:

> "Player B is currently in an offside position."

Then:

> "Player A plays the ball forward."

Then:

> "Player B moves toward the ball."

Then:

> "Player B has not touched the ball."

Then:

> "Player D reaches the ball first and intercepts."

Then:

> "The sequence is now evaluated according to the relevant Law 11 criteria."

The narration follows the master simulation timeline.

When the simulation pauses:

```text
VOICE → PAUSED
```

When the simulation resumes:

```text
VOICE → RESUMED
```

---

# 📝 Captions

The simulation displays captions synchronized with the current event.

Example:

```text
┌──────────────────────────────────────────┐
│ Player B is moving toward the ball.      │
└──────────────────────────────────────────┘
```

The caption changes as the simulation progresses.

---

# 👟 Player Movement

The movement of the three players follows the event sequence.

### Player A

Player A remains the passer and initiates the play.

```text
Player A
   ↓
Plays the ball
```

### Player B

Player B is the attacking player in an offside position.

```text
Player B
   ↓
Offside position
   ↓
Moves toward ball
   ↓
Does not touch ball
```

### Player D

Player D is the defender.

```text
Player D
   ↓
Moves toward ball
   ↓
Reaches ball first
   ↓
Intercepts
```

---

# ⚽ Ball Movement

The ball starts with Player A.

```text
Player A
   ⚽
    \
     \
      \────────────────→
                         ⚽
                      Player B
```

The ball travels toward the area where Player B is moving.

Player D then reaches the ball before Player B can touch it.

The ball therefore becomes part of the interception event.

---

# 🛡 Player D — Defender Interception

Player D is the only defender involved in the main scenario.

```text
Player B                         Player D
   🔴                              🔵
    \                              /
     \                            /
      \          ⚽              /
       \________________________/
                  ↑
             INTERCEPTION
```

This event is important because Player B has not touched the ball before Player D reaches it.

---

# 📊 Event Timeline

A typical simulation sequence can be represented as:

```text
00:00  Initial player positions

00:01  Player B identified in an offside position

00:02  Player A plays the ball

00:03  Player B begins moving toward the ball

00:04  Position-based detection is triggered

00:05  Player B approaches the ball

00:06  Player B has not touched the ball

00:07  Player D reaches the ball

00:08  Player D intercepts

00:09  Law 11-inspired analysis begins

00:10  Final analysis
```

The exact timing is controlled by the simulation.

---

# 🧪 Test Scenario

## Scenario — Player D Intercepts Before Player B Touches

```text
START
  ↓
Player B is in an offside position
  ↓
Player A passes
  ↓
Player B moves toward ball
  ↓
Player B does not touch ball
  ↓
Player D reaches ball
  ↓
Player D intercepts
  ↓
Analyze sequence
```

This is the primary scenario demonstrated by the project.

---

# 🧩 Rule Engine Concept

The simplified rule engine follows this structure:

```text
START
  │
  ↓
Determine Player B's position
  │
  ↓
Is Player B in an offside position?
  │
  ├── NO ─────────→ Continue Play
  │
  └── YES
        │
        ↓
Player A plays the ball
        │
        ↓
Evaluate subsequent events
        │
        ↓
Player B involved?
        │
        ├── NO
        │    ↓
        │  Continue analysis
        │
        └── YES
             ↓
       Apply relevant
       Law 11 criteria
             ↓
        Final Decision
```

The rule engine is intentionally simplified for educational purposes.

---

# 🏗️ Technical Architecture

The current prototype is designed as a lightweight standalone web application.

```text
HTML
 │
 ├── User Interface
 │
 ├── Football Pitch
 │
 ├── Player A
 │
 ├── Player B
 │
 ├── Player D
 │
 ├── Ball
 │
 ├── Animation System
 │
 ├── Timeline
 │
 ├── Voice / Audio
 │
 ├── Captions
 │
 └── Rule Engine
```

A central simulation state can contain values such as:

```javascript
simulationTime
isPlaying
playbackSpeed
currentEvent
playerStates
ballState
```

Animation, voice, captions, and rule events should use the same simulation state.

---

# 🔄 Simulation Flow

The complete flow is:

```text
INITIAL POSITIONS
       ↓
PLAYER B OFFSIDE POSITION
       ↓
PLAYER A PASSES
       ↓
PLAYER B MOVES
       ↓
PLAYER B DOES NOT TOUCH BALL
       ↓
PLAYER D INTERCEPTS
       ↓
RULE ANALYSIS
       ↓
FINAL DECISION
```

---

# ⚠️ Important Scope

This project is an **educational simulation**.

It is not:

* An official VAR system
* A professional referee assistant
* A replacement for human refereeing
* A complete implementation of every Law 11 situation
* A commercial football game's internal detection system

Real-world offside decisions can involve additional situations and detailed conditions, including:

* Deliberate play by an opponent
* Deflections
* Saves
* Rebounds
* Interference with an opponent
* Challenging for the ball
* Blocking an opponent's line of vision
* Gaining an advantage
* Other situations specified by Law 11

The current prototype focuses on a specific controlled scenario involving **Player A, Player B, and Player D**.

---

# 🔐 Independent Project

This project is an independent educational and technical demonstration.

It does not inspect, reproduce, or claim knowledge of proprietary source code or internal algorithms belonging to any commercial football game or company.

The position-based detector is a **simplified model created specifically for comparison and experimentation**.

---

# 🚀 Future Improvements

Possible future improvements include:

* More realistic player movement
* Improved ball physics
* Multiple attackers
* Multiple defenders
* Additional Law 11 scenarios
* Deliberate-play scenarios
* Deflection scenarios
* Save and rebound scenarios
* Interactive player positioning
* Drag-and-drop player placement
* Custom scenario creation
* Automated test cases
* Rule-engine unit tests
* Detailed event logs
* Replay export
* JSON-based scenario definitions
* Scenario comparison mode
* Improved voice synchronization
* Improved slow-motion playback
* Frame-by-frame analysis
* Detailed decision explanations
* Additional referee-style visual indicators

---

# 📈 Project Goal

The goal is to make offside analysis:

**Visual.**

**Interactive.**

**Testable.**

**Understandable.**

Instead of simply displaying:

```text
OFFSIDE
```

the simulation shows the sequence of events that occurred before the final analysis.

---

# ⚽ Core Principle

```text
╔════════════════════════════════════╗
║                                    ║
║       OFFSIDE POSITION             ║
║                ≠                   ║
║       OFFSIDE OFFENSE              ║
║                                    ║
╚════════════════════════════════════╝
```

The project demonstrates why offside analysis should distinguish between **where Player B is** and **what subsequently happens in play**.

---

## Status

**Current Version:** Interactive Prototype

**Format:** Standalone Web Application

**Primary Technology:** HTML / CSS / JavaScript

**Focus:** Football Offside Detection and Law 11 Analysis

---

## License

This project is intended for educational and experimental purposes.

An appropriate open-source license can be added if the project is later released for public reuse.

```
```
