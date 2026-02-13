# SPCO — Single Player Co-Op

Draft and materials for the memoir.

## Cursor rule (mental health memoir editor)

This repo includes a Cursor rule that only applies in this project:

- **Location:** `.cursor/rules/mental-health-memoir-editor.mdc`
- **Role:** Editor in the mental health memoir space. It does not change your voice; it works to amplify it (clarify, tighten, flag disclosure choices, preserve raw phrasing, respect the line between memoir and diagnosis).
- **Scope:** Only when this folder is open in Cursor. Not used in other workspaces.

If you clone the repo elsewhere, the rule comes with it—no need to recreate it.

## Latest draft (compiled)

A single-file draft is built from the scene order in `noveltools.yaml` (chapters → scenes).

- **Automated:** The **Compile draft** GitHub Action runs on push to `main` and on manual trigger. It concatenates the scene files in order and uploads the result as an artifact.
- **Download:** Open the repo on GitHub → **Actions** → select the latest **Compile draft** run → under **Artifacts**, download `draft` (contains `draft.md`).
- **Manual:** You can also compile locally by running the script used in the action: see `.github/workflows/compile-draft.yml` (or run the same `python3` one-liner / script that reads `noveltools.yaml` and cats the files).

## Repo layout

- **Scene/chapter files** — Markdown files listed in `noveltools.yaml` (e.g. `Content Warning.md`, `Not the Same.md`).
- **noveltools.yaml** — Defines title, chapter/scene order, and writing prompts. The compile action uses this for draft order.
- **Writing Prompts.md / EXPANSION_NOTES.md** — Prompts and notes for expanding the draft.
