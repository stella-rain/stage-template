# Stella Rain stage repository

This repository holds Stella Rain stages: levels for the mobile vertical shooter, built in the
game's stage editor and published here. It was created from `stella-rain/stage-template`;
usually the game does all the git work, so edits by hand should be rare and careful.

## Layout

| Path | What |
|---|---|
| `stages/<stage-id>.json` | A stage: data only (no images, sound or code) |
| `stages/<stage-id>.replay` | The recorded clear that proves the stage can be beaten |
| `LICENSE` | CC BY 4.0 by default: anyone may play, share and remix with credit |

## Rules

- **Published versions never change.** A version is the tag `<stage-id>@v<N>`
  (for example `frost-cavern@v2`). Never move, delete or re-create a tag; publish `v<N+1>` instead.
- **A stage and its replay belong together.** Changing a stage's JSON invalidates its replay;
  the stage must be cleared again in the game before the next version is tagged.
- **Edit stages in the game's editor** where possible. Hand edits must keep the file valid
  against the stage JSON Schema published with each `stella-rain/core` release; unknown fields
  are rejected and the game will refuse the stage.
- Keep `schema_version`, `sim_version` and `seed` as the game wrote them: changing them breaks
  the replay.
- Keep the `stella-rain-stage` repository topic so the game can find these stages.
- Stage titles and descriptions are public and covered by the game's terms of use.

## Maintainers of `stella-rain/stage-template`

Everything in the template is copied into every creator's repository. Keep it generic:
no organization workflows, no secrets, nothing about Stella Rain's development, and no
references to private repositories.
