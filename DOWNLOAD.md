# Download the image

This page is the quick handoff for teachers who want the Raspberry Pi starter image, plus the source and update links.

## What to download

When the image is published, the latest version should be attached to the repo releases page:

- Latest image: <https://github.com/wiobyrne/teaching-assistant/releases/latest>

If you want the source instead of the prebuilt image:

- Source repo: <https://github.com/wiobyrne/teaching-assistant>

If you want to know which model the image is built around:

- Model page: <https://github.com/wiobyrne/teaching-assistant/blob/main/docs/model.md>

## What the image is for

The image is a clean, ready-to-flash Raspberry Pi starter:

- Raspberry Pi OS
- Ollama
- a small local model
- `teaching-assistant/`
- starter `teacher.md`
- empty `history/`

It should not include old testing history, saved outputs, or hidden build leftovers.

## How to get updates

Use the repo releases page for the newest published image:

- Updates and version notes: <https://github.com/wiobyrne/teaching-assistant/releases>

If you want to rebuild from source, clone the repository and follow the setup notes in the README.

## Why we separate image and source

Some people just want a working download.
Other people want to inspect the files, tweak the profile, or rebuild the image for their own use.

That is why the repo points to both:

- the downloadable image for convenience
- the source repo for transparency and customization

## If GitHub is unavailable

The image is intended to be easy to carry on an SD card too.
That gives you a backup path when network access or GitHub is unreliable.
