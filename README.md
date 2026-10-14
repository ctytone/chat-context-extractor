# Chat Context Extractor

A copy-paste prompt that turns a long ChatGPT conversation into one clean, structured Markdown note you can keep in Obsidian (or any notes app) and hand back to an AI later.

> **Status: V1.** The prompt works and is usable as-is. It has not been systematically tested across many kinds of conversations yet. See [Limitations](#limitations) and the [roadmap](docs/roadmap.md).

## Why

Useful conversations with an AI get buried. Weeks later you remember *that* you figured something out, but not the details, the reasoning, or the moment it clicked. Rereading a 200-message chat is painful, and most "summarize this chat" prompts compress too hard and lose exactly the parts that mattered.

This prompt is built around one idea: **knowledge preservation, not aggressive summarization.** It keeps the small details, your personal context, the decisions you made and why, and the way a concept finally made sense to you, while stripping out greetings and back-and-forth.

The resulting note is meant to do two jobs:

1. Be a readable long-term record in your notes vault.
2. Be pasted into a **fresh** AI chat so it can pick up where the old conversation left off, without the original transcript.

## What it produces

One Markdown note per conversation, always with the same sections:

| Section | Answers |
| --- | --- |
| Metadata | Where did this come from, and when? |
| Overview | What was this conversation about overall? |
| Important Context | What should a future AI know about me or my situation? |
| Key Knowledge | What important facts and concepts came up? |
| Lessons Learned | What did I actually learn or come to understand better? |
| Insights | How did it click? Analogies, mental models, "aha" moments. |
| Decisions | What did I decide, and why? |
| Goals | What do I intend to do? Split into `Goal:`, `Action:`, `Idea:`. |
| Open Questions | What is still unresolved? |
| Related Topics | What else connects to this, and how? |
| Conversation Summary | How did the conversation develop, and where did it end? |

Optional sections (**Procedures & Workflows**, **Best Practices**, **Resources**) appear only when the conversation has real material for them.

A few rules the prompt enforces that make the output trustworthy:

- **No invention.** It must not make up facts, motivations, decisions, or dates. Unknown dates stay unknown.
- **Your decisions vs. the AI's suggestions.** A suggestion only becomes "your" decision if the conversation shows you adopted it.
- **Possibilities stay possibilities.** "I might switch to X" is recorded as an idea, not a commitment.
- **Changes of mind.** Your final position wins; earlier positions are kept only when they explain the change.
- **No secrets.** Passwords, API keys, tokens, and similar credentials are never copied into the note.
- **Clean output.** Only the note is returned, with no preamble, so it is ready to paste.

## Usage

1. Open the ChatGPT conversation you want to preserve.
2. Copy the full contents of [`prompts/extract-current-chat.md`](prompts/extract-current-chat.md).
3. Paste it as a new message at the end of that same conversation and send it.
4. Copy the response into a new note in Obsidian (or wherever you keep notes).
5. Skim it once against the original chat, especially **Decisions** and **Important Context**, before relying on it.

To reuse the context later, start a new chat and paste the note in with something like *"Here is a knowledge note from an earlier conversation. Use it as context."*

### Tips

- Run it in the conversation itself, not in a new chat. The prompt asks the model to read "the entire conversation so far."
- Very long chats can exceed what the model reliably attends to. If the note feels thin on the early parts of a conversation, ask a follow-up like *"Re-check the first half of the conversation for anything missing from the note."*
- The extraction date is filled in by the model. If it gets the date wrong, correct it by hand.

## Example output shape

```md
# Choosing a Note-Taking Workflow for Class and Projects

## Metadata
- Source: ChatGPT — "Note-taking setup"
- Conversation Date: 2026-08-10
- Extracted: 2026-08-10

## Overview
- ...

## Important Context
- ...

## Decisions
- Decided to ...
  - Reason: ...

## Goals
- Goal: ...
- Action: ...
- Idea: ...
```

This only shows the structure. Real before/after examples are on the [roadmap](docs/roadmap.md).

## Repository layout

```
.
├── prompts/
│   └── extract-current-chat.md   # The prompt you paste into a chat
├── docs/
│   ├── specification.md          # Full design: what each section is for and why
│   └── roadmap.md                # Testing plan and future ideas
├── CHANGELOG.md
├── LICENSE
└── README.md
```

## Limitations

- **Written for ChatGPT.** The wording refers to ChatGPT. It should work in other assistants that can see the whole conversation (Claude, Gemini, etc.), but that has not been tested.
- **Current conversation only.** V1 extracts the chat you are in. A version for pasted or exported chats is planned but not built.
- **Limited testing.** V1 has been used, but not yet run through a structured test across learning, personal, and technical conversations.
- **Model quality varies.** The prompt reduces, but cannot eliminate, the chance that a model misses details or overstates something. Review important notes.
- **Long notes by design.** It favors keeping information over brevity, so notes can be long.
- **Personal by default.** It deliberately keeps personal context. If you plan to share notes outside a private vault, review them first.
- **Manual workflow.** There is no script or automation; you copy and paste.

## Roadmap

The short version (full list in [docs/roadmap.md](docs/roadmap.md)):

- Test V1 on learning-heavy, personal/productivity, and technical chats.
- Build a quality checklist and refine the prompt from real failures, then release V2.
- Test the "future-AI handoff": give only the note to a fresh chat and see what it can answer.
- Later: a prompt for pasted/exported chats, before/after examples, a prompt to update an existing note instead of creating a new one, and possibly a script for bulk processing.

## License

[MIT](LICENSE)
