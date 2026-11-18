# Working on ahom-kings-lessons

Standalone Ahom Kings course (static PWA, no framework). Part of AxomRank: see README.md for the overview and roadmap.

## Layout

- `content/lessons/<id>.json`: one lesson. Every text is `{en, as}`. Every step has a permanent `id`
- `content/courses/ahom-kings.json`: the course outline (eras, kings, tiers)
- `content/entities.json`: shared names that learners can tap
- `app/`: player, home and sync code. `app/config.js` is the only file for service settings

## Commands

- `python3 scripts/build.py` (validates content, writes `content/manifest.json`, stamps `sw.js`)

## Rules

- Never change or reuse a published step `id`, because saved progress and review refer to it
- Follow the word limits and the exercise mix in the README. The build fails when they are broken
- Every lesson lists its `sources`. Do not invent dialogue, dates or outcomes
- Write English and Assamese in the same change, and never claim an Assamese review that has not happened
- Do not hand-edit `content/manifest.json`, because it is generated
- Commit as the `axomrank` account, in small reviewable commits.
