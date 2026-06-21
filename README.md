# Teaching Assistant

Teaching Assistant is a simple, local AI setup for teachers.
It is meant to run on a Raspberry Pi or any machine where you can install [Ollama](https://ollama.com) and load a small model like `qwen2.5:1.5b`.

This repo explains:

- why the project exists
- how the image is shared
- how teachers use the `teacher.md` profile
- how the assistant should behave over time

## Start here

1. Read [Download the image](./IMAGE.md)
2. Read [Where the image, updates, and source live](./DOWNLOAD.md)
3. Read [Which model and why](./docs/model.md)
4. Read [Why the teacher profile works this way](./docs/teacher-profile.md)
5. Open [`teacher.md`](./teacher.md) to see the starter profile template

## What this is

Teaching Assistant is a local-first classroom support tool.
It keeps the model on your machine and uses a `teacher.md` file to shape the assistant around a teacher’s voice, classroom context, supports, and boundaries.

The goal is not to replace teacher judgment.
The goal is to help teachers draft, revise, and improve classroom materials while staying aligned with their real philosophy and practice.

## Why we share it this way

Teachers need tools that are:

- private enough to use in real classrooms
- easy to understand without technical training
- flexible enough to reflect a real teacher’s voice and values
- simple enough to set up and maintain

That is why the repo focuses on a starter image, a starter profile, and a clear workflow instead of a big software stack.

## How it works

1. Install Ollama on your machine or Raspberry Pi.
2. Pull a small model such as `qwen2.5:1.5b`.
3. Place the starter `teacher.md` file where your local assistant can read it.
4. Run the teaching assistant launcher or wrapper.
5. Ask the model for lesson plans, handouts, scaffolds, discussion prompts, or profile reviews.

## The `teacher.md` rule

The important part is the `teacher.md` file:

- it is teacher-owned
- it is the source of truth for classroom preferences
- the model can suggest changes, but the teacher decides what gets written

This matters because a model can notice patterns without being trusted to turn those patterns into permanent facts.
For example, if a teacher asks for a concise handout once, that does not automatically mean every future answer should be short.

So the contract is:

- model suggests
- teacher confirms
- file changes only when the teacher agrees

That keeps `teacher.md` trustworthy as a living profile instead of letting it quietly turn into a model-written biography.

## What you get in the repo

- [`teacher.md`](./teacher.md) - starter teacher profile template
- [`IMAGE.md`](./IMAGE.md) - where to download the starter image
- [`DOWNLOAD.md`](./DOWNLOAD.md) - where to get the image, updates, and source
- [`docs/model.md`](./docs/model.md) - the model choice and useful links
- [`docs/teacher-profile.md`](./docs/teacher-profile.md) - the philosophy behind the profile workflow
- this `README.md` - overview, setup, and workflow

## What is not in the repo

- the actual model files
- the Raspberry Pi image itself
- a replacement for Ollama
- student data

## Suggested local model

This setup was tested with:

- `qwen2.5:1.5b`

You can use a different model if you want, but start small if you are using a Raspberry Pi.

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

## Ways to improve later

Good next improvements are:

- a better `teacher.md` starter profile
- a friendlier first-run experience
- more example prompts for teachers
- a clearer path for reviewing and refining the teacher profile over time
- optional notes for people who want to build the image from source instead of downloading it
