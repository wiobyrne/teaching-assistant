# Teaching Assistant

Teaching Assistant is a simple, local AI setup for teachers.
It is meant to run on a Raspberry Pi or any machine where you can install [Ollama](https://ollama.com) and load a small model like `qwen2.5:1.5b`.

The idea is straightforward:

- keep the model local
- keep the teacher in control
- use a `teacher.md` file as the profile for tone, classroom context, supports, and boundaries
- let the assistant suggest improvements to that profile over time without rewriting it behind the teacher’s back

## Why this exists

Teachers need tools that are:

- private enough to use in real classrooms
- easy to understand without technical training
- flexible enough to reflect a real teacher’s voice and values
- simple enough to set up and maintain

This project is not trying to replace teacher judgment.
It is trying to make it easier to draft, revise, and improve classroom materials in a way that stays aligned with how the teacher actually works.

## What you get

- a starter `teacher.md` profile template
- a clear explanation of the workflow
- a local-first model setup that works with Ollama
- a path for teachers to personalize the assistant over time

## How it works

1. Install Ollama on your machine or Raspberry Pi.
2. Pull a model such as `qwen2.5:1.5b`.
3. Place the starter `teacher.md` file where your local assistant can read it.
4. Run the teaching assistant launcher or wrapper.
5. Ask the model for lesson plans, handouts, scaffolds, discussion prompts, or profile reviews.

The important part is the `teacher.md` file:

- it is teacher-owned
- it is the source of truth for classroom preferences
- the model can suggest changes, but the teacher decides what gets written

## What is in the repo

- [`teacher.md`](./teacher.md) - starter teacher profile template
- this `README.md` - overview, setup, and workflow

## What is not in the repo

- the actual model files
- the Raspberry Pi image
- a replacement for Ollama
- student data

## Suggested local model

This setup was tested with:

- `qwen2.5:1.5b`

You can use a different model if you want, but start small if you are using a Raspberry Pi.

## Teacher profile workflow

The `teacher.md` file should grow with use.

- day one: fill in the basics
- during use: the assistant can point out gaps, contradictions, or places where the profile could be clearer
- over time: the teacher can revise the profile to better reflect their actual philosophy and classroom needs

The assistant should suggest edits rather than silently rewriting the profile.

## Privacy and safety

- do not put real student names, ID numbers, or other identifying details in `teacher.md`
- do not use the assistant as a grading system or student record system
- keep the focus on teaching and learning materials

## If you are using the Raspberry Pi image

The Pi image is intended to be a clean starter image:

- Raspberry Pi OS
- Ollama
- a small local model
- `teaching-assistant/`
- starter `teacher.md`
- empty `history/`

It should not ship with old chat history, saved outputs, or test crud.

## Quick start

If you already have Ollama installed:

```bash
ollama pull qwen2.5:1.5b
```

If you are using the Raspberry Pi launcher, start it from the `teaching-assistant` folder on the device and point it at your `teacher.md`.

## Want to improve it?

Good next improvements are:

- a better `teacher.md` starter profile
- a friendlier first-run experience
- more example prompts for teachers
- a clearer path for reviewing and refining the teacher profile over time

