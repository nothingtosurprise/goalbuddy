---
description: Run the GoalBuddy execution loop against a prepared goal board
---

Run the GoalBuddy `/goal` execution loop.

Goal: $ARGUMENTS

If the argument names a `docs/goals/<slug>/goal.md` charter, load it and its sibling `state.yaml` board. If it is raw intent, run the GoalBuddy intake first (see the goal-prep skill).

Follow the GoalBuddy execution contract from the goal-prep skill: `state.yaml` is board truth; exactly one active task unless disjoint write scopes are proven; Scout and Judge tasks are read-only; Worker tasks write only inside `allowed_files` and run their `verify` commands; every completed, blocked, or escalated task gets a receipt; after each receipt select the next safe task and keep executing; mark the goal done only through a final Judge or PM audit that maps receipts and verification back to the original outcome with `full_outcome_complete: true`.
