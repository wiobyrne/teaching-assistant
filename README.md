# Teaching Assistant

Teaching Assistant is a simple, local AI setup for teachers.
It is meant to run on a Raspberry Pi or any machine where you can install [Ollama](https://ollama.com) and load a small model like `qwen2.5:1.5b`.

For the full profile-builder workflow, see the separate [wiobyrne/teacher](https://github.com/wiobyrne/teacher) repo. This repo focuses on the local image, runtime, and starter files.

This repo explains:

- why the project exists
- how the starter image works
- how to get started with the `teacher.md` profile

## Start here

1. Read [the image and build recipe](./IMAGE.md)
2. Open [`teacher.md`](./teacher.md) if you are using the starter image
3. Use the separate [wiobyrne/teacher](https://github.com/wiobyrne/teacher) repo if you want the interview-style profile builder

To learn more about the teacher profile format and how to build one, see the separate [wiobyrne/teacher](https://github.com/wiobyrne/teacher) repo.

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
- [`IMAGE.md`](./IMAGE.md) - what is on the image and how to build it
- this `README.md` - overview and workflow

## What is not in the repo

- the actual model files
- the Raspberry Pi image itself
- a replacement for Ollama
- the interview-style teacher profile builder
- student data

## Suggested local model

This setup was tested with `qwen2.5:1.5b`.
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
