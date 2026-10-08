# Stella Rain stage repo

Template for publishing your own **Stella Rain** stages. You normally never need to touch git:
the game guides you through setup and publishes for you.

## First publish

The first time you publish, the game opens two pages in your browser:

1. **Use this template** to create your stage repository (or pick a stage repository you
   already have).
2. **Install the Stella Rain GitHub App** on that one repository. It only needs access to
   that repository.

After that, sign in from the game with the short code it shows you. Each publish is then one
commit and one tag, made by the game.

## How it works

- Stages live in `stages/` as `<stage-id>.json` with a matching `<stage-id>.replay`, the
  recorded clear that proves the stage can be beaten.
- `stages/index.json` lists your published stages and their versions. The game writes it on
  each publish; it only points to stages, which are always downloaded by tag.
- Each published version is a tag named `<stage-id>@v<N>`, for example `frost-cavern@v1`.
  Tags never move: to change a stage, publish `v<N+1>`. If a published version's files change,
  the game refuses that stage.
- The game finds your stages because its GitHub App is installed on this repository.
  If you publish with plain git instead of the game, add the repository topic
  `stella-rain-stage` so your stages can be found.
- This template has no workflows: Stella Rain checks published stages on its side.

## License

Stages in this repository are licensed under
[Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE) unless stated otherwise.
Anyone may download, play, share and remix them, as long as they credit the creator.
