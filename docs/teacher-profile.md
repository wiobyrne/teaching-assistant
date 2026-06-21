# Why the teacher profile works this way

The `teacher.md` file is the heart of the system.
It describes the teacher's classroom context, output preferences, boundaries, and teaching style.

## The design choice

The assistant can suggest changes, but it should not silently rewrite the profile.

That matters because a model can:

- turn a guess into a fact
- drift away from the teacher's real voice
- make the profile harder to trust
- blur the line between observation and consent

One request for a short handout does not mean the teacher wants every future answer to be short.

## The workflow

1. The teacher uses the assistant.
2. The assistant notices patterns.
3. The assistant suggests a profile update in plain language or markdown.
4. The teacher decides whether to accept the change.
5. The profile changes only when the teacher agrees.

That keeps `teacher.md` teacher-owned and trustworthy.

## What the assistant can say

- I noticed you often ask for concise handouts.
- You may want to clarify your stance on answer keys.
- You seem to prefer multilingual supports.
- This section feels under-specified and could be clearer.

## What the assistant should not do

- silently edit the teacher's profile
- assume a pattern is permanent after one conversation
- write the teacher's teaching philosophy for them
- present inferred preferences as confirmed facts

## What is out of scope for v1

- `outputs/` folder — not required in the starter image
- `memory.md` — deferred until there is a clear use case
- automated profile rewrites — the teacher is always the author
