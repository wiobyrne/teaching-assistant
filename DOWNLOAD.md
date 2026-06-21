# Downloads, source, and updates

Quick links for teachers who want the Raspberry Pi starter image, the source, or update notes.

## Get the image

When published, the latest image is attached to the releases page:

- Latest image: <https://github.com/wiobyrne/teaching-assistant/releases/latest>
- Version notes: <https://github.com/wiobyrne/teaching-assistant/releases>

## Get the source

- Source repo: <https://github.com/wiobyrne/teaching-assistant>
- Model info: <https://github.com/wiobyrne/teaching-assistant/blob/main/docs/model.md>

## What the image contains

- Raspberry Pi OS
- Ollama
- `qwen2.5:1.5b`
- `~/teaching-assistant/`
- starter `teacher.md`
- `ta.py`
- empty `history/`

`outputs/` and `memory.md` are not included. They are out of scope for v1.

## Why image and source are separate

Some people want a working download.
Others want to inspect the files, adjust the profile, or rebuild for their own setup.

The repo covers both:

- downloadable image for convenience
- source repo for transparency and customization

## If GitHub is unavailable

The image is easy to carry on an SD card as a backup.
