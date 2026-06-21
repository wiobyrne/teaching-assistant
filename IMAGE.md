# Image and build recipe

This page is the single reference for the Raspberry Pi starter image.
It answers three questions:

- what is on the image
- where to get it
- how to build it yourself

## What is on the image

The starter image includes:

- Raspberry Pi OS
- Ollama
- `qwen2.5:1.5b`
- `~/teaching-assistant/`
- starter `teacher.md`
- `ta.py`
- empty `history/`

It does not include old testing history, saved outputs, or build leftovers.
`outputs/` and `memory.md` are not part of the starter image.

The interview-based teacher profile builder lives in the separate [wiobyrne/teacher](https://github.com/wiobyrne/teacher) repo.

## Where to get it

When the image is published, it will be attached to the GitHub Releases page:

- Latest image: <https://github.com/wiobyrne/teaching-assistant/releases/latest>
- Version notes: <https://github.com/wiobyrne/teaching-assistant/releases>
- Source repo: <https://github.com/wiobyrne/teaching-assistant>

## Why `qwen2.5:1.5b`

This project was built and tested around `qwen2.5:1.5b`.

It is small enough to be practical on a Raspberry Pi while still being useful for teacher-facing drafts, handouts, scaffolds, and profile review.

You can use a different model if you want, but start small if you are using a Raspberry Pi.

## Build recipe

If you want to build the image yourself, the path is simple:

1. Install Raspberry Pi OS.
2. Install Ollama.
3. Pull `qwen2.5:1.5b`.
4. Create `~/teaching-assistant/`.
5. Add the starter `teacher.md` file.
6. Copy in `ta.py`.
7. Leave `history/` empty.
8. Keep `outputs/` and `memory.md` out of the starter image for v1.

## Notes

- The image should be simple enough to carry on an SD card.
- The separate `teacher` repo is the profile-building workflow.
- The teaching-assistant repo is the image, runtime, and starter-file side.
