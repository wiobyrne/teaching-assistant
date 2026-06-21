# Why the teacher profile works this way

The `teacher.md` file is the heart of the system.
It describes the teacher’s classroom context, output preferences, boundaries, and teaching style.

## The design choice

The assistant can suggest changes, but it should not silently rewrite the profile.

That is important because a model can:

- turn a guess into a “fact”
- drift away from the teacher’s real voice
- make the profile harder to trust
- blur the line between observation and consent

For example, one request for a short handout does not necessarily mean the teacher wants every future answer to be short.

## The workflow we want

1. The teacher uses the assistant.
2. The assistant notices patterns.
3. The assistant suggests a profile update in plain language or markdown.
4. The teacher decides whether to accept the change.
5. The profile changes only when the teacher agrees.

That keeps `teacher.md` teacher-owned and trustworthy.

## What the assistant can say

The assistant can say things like:

- I noticed you often ask for concise handouts.
- You may want to clarify your stance on answer keys.
- You seem to prefer multilingual supports.
- This section feels under-specified and could be clearer.

## What the assistant should not do

- silently edit the teacher’s profile
- assume a pattern is permanent after one conversation
- write the teacher’s teaching philosophy for them
- present inferred preferences as confirmed facts

## The middle ground

A good compromise is:

- `teacher.md` stays teacher-owned
- the assistant writes suggested updates into the transcript or a review note
- the teacher copies approved changes back into `teacher.md`

That gives you growth over time without losing authorship or trust.

