# pb-monologue

Clean monologue viewer for Listy's personal-brand video scripts. Pulls only the spoken narration from a script's beat table — strips shot lists, captions, and metadata. Built to read scripts on a phone while recording.

**Live:** https://listya6.github.io/pb-monologue/

## How it works

- `index.html` fetches `manifest.json` to populate the script picker.
- On selection, fetches the script's `.md` file from `scripts/` and parses the table.
- Renders only column 2 (narration) with timestamp markers. Quotes, bold markers, and bracketed labels are stripped.

Resize text with S / M / L / XL. Copy whole monologue to clipboard with the Copy button.

## Adding a script

1. Drop the `.md` file into `scripts/` (must use the three-column beat table format: `t (s) | Narration | Shot | Caption`).
2. Add an entry to `manifest.json` with `file`, `title`, `date`, `length`.
3. Commit + push. Pages updates within ~1 minute.

## Source

Scripts are written using the kit at `personal-brand/video-guidelines/` (private). This repo only mirrors the public-facing deliverables.
