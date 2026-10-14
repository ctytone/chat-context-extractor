# Specification

The full design behind the extraction prompt. The prompt in `prompts/` is the condensed, ready-to-paste version of this document.

## Purpose

- The ChatGPT Knowledge Extractor turns one complete ChatGPT conversation into a structured Markdown knowledge note for long-term storage in Obsidian.
- Its purpose is knowledge preservation, not aggressive summarization.
- The finished note should preserve:
    - Important information and concepts.
    - Personal context.
    - Things I learned.
    - The specific ways concepts clicked for me.
    - Decisions and their reasoning.
    - Goals, ideas, and actions.
    - Unresolved questions and uncertainties.
    - Useful workflows and best practices.
    - Resources worth returning to.
    - Small details that may have reasonable future value.
    - The overall development of the conversation.
- The note should contain enough context that I can give it to a future ChatGPT conversation and recover much of the useful context from the original conversation without rereading the entire chat.

## Standard Structure

- Use this section order:

```md
# Conversation Title

## Metadata
- Source: ChatGPT — "Original Conversation Title"
- Conversation Date: YYYY-MM-DD
- Extracted: YYYY-MM-DD

## Overview
- ...

## Important Context
- ...

## Key Knowledge
- ...

## Lessons Learned
- ...

## Insights
- ...

## Decisions
- ...

## Goals
- Goal: ...
- Action: ...
- Idea: ...

## Open Questions
- ...

## Related Topics
- ...

## Conversation Summary
- ...
```

- Standard section names should remain exactly the same across notes.
- Optional sections may be added when relevant.
- New descriptive sections may be created when important information genuinely does not fit the standard structure.

## Metadata

- Records where the knowledge came from.
- Appears immediately below the title.
- Include the original ChatGPT conversation title when known.
- Include individual conversation dates when available.
- Include the extraction date.
- Never guess dates.
- Only include dates actually known from the conversation or context.
- Process one ChatGPT conversation per knowledge note.
- Do not automatically generate Obsidian tags.
- Do not automatically generate `[[wikilinks]]`.

### Example

```md
## Metadata
- Source: ChatGPT — "Project Workflow Discussion"
- Conversation Date: 2026-08-08
- Conversation Date: 2026-08-09
- Conversation Date: 2026-08-10
- Extracted: 2026-08-10
```

## Overview

- Answers: **What was this conversation about overall?**
- Acts as an executive summary of the conversation.
- Quickly communicate:
    - The main subject.
    - Why the conversation happened.
    - Major things discussed.
    - Most important conclusions.
    - Overall outcome.
- Should make sense without reading the rest of the note.
- Use a neutral summary voice rather than first person.

## Important Context

- Answers: **What should a future AI know about me or my situation to understand this correctly?**
- Can include:
    - Personal circumstances.
    - Preferences.
    - Existing workflows.
    - Current systems.
    - Constraints.
    - Background.
    - Relevant habits.
    - Current projects.
    - Productivity approaches.
    - Lifestyle context.
    - Previous experiences.
    - Information affecting how future advice should be given.
- This section is especially important for lifestyle, productivity, personal organization, project, planning, and learning conversations.
- Preserve personal information from the conversation when useful for reconstructing its context.
- Never preserve passwords, API keys, authentication tokens, financial credentials, security answers, or other authentication secrets.
- If information could become outdated, preserve its timing when known.
- Never guess when something was true.
- Only state something about me as fact when the conversation supports it.
- Preserve uncertain possibilities as possibilities rather than turning them into preferences or decisions.

## Key Knowledge

- Answers: **What important information or concepts appeared in this conversation?**
- Preserve important facts and concepts whether or not they were new to me.
- Can include:
    - Facts.
    - Definitions.
    - Concepts.
    - Explanations.
    - Distinctions.
    - Technical information.
    - Useful principles.
    - Important background information.
- Favor completeness.
- Preserve small details when they have reasonable future value.
- `Key Knowledge` contains all important knowledge.
- Information may also appear in `Lessons Learned` when it represents something I personally learned.

## Lessons Learned

- Answers: **What did I actually learn or come to understand better?**
- Use first person.
- Include:
    - New things I learned.
    - Concepts I came to understand better.
    - Previous misunderstandings that were corrected.
    - Skills or principles I gained from the conversation.
- If I misunderstood something and later corrected it:
    - Preserve the corrected understanding.
    - Briefly preserve the original misunderstanding when doing so helps explain the lesson.
- `Lessons Learned` focuses on **what I learned**.

## Insights

- Answers: **How did I understand it? What made it click?**
- Use first person.
- `Lessons Learned` captures what I learned.
- `Insights` captures how I came to understand it.
- Actively look for:
    - "Aha" moments.
    - Personal mental models.
    - Comparisons.
    - Analogies.
    - Connections to things I already understand.
    - "So basically..." explanations.
    - Moments where my understanding changed.
    - Distinctions that suddenly made something clearer.
    - Examples I created that helped something click.
- When my wording captures an important mental model:
    - Preserve the distinctive comparison or idea.
    - Clean up unnecessary repetition when needed.
    - Add a clearer explanation when useful.
- Preserve my own examples when they clearly contributed to an important insight.
- Do not preserve every example merely because I created one.

## Decisions

- Answers: **What did I decide, and why?**
- Capture important choices made during the conversation.
- Include:
    - The decision.
    - Reasoning when available.
    - Important alternatives when relevant.
    - Tradeoffs for major decisions.
    - Previous approaches when understanding the change matters.
- Simple decisions can remain short.
- Major decisions should preserve more reasoning.
- Never invent reasoning.
- If the conversation establishes a decision but not its reason, preserve only what is actually supported.

## Goals

- Answers: **What do I want to do?**
- Use first person where appropriate.
- Distinguish three types of future-oriented information:
    - `Goal:` Something I intend to accomplish.
    - `Action:` A specific thing I intend to do that contributes to a goal.
    - `Idea:` Something I might want to pursue but have not committed to.
- Do not turn speculative ideas into goals.

### Example

```md
## Goals
- Goal: Create a reusable ChatGPT knowledge-extraction prompt.
- Action: Test the finished prompt on an old conversation.
- Idea: Eventually make stored knowledge accessible to AI across conversations.
```

## Open Questions

- Answers: **What remains unresolved?**
- Include:
    - Unanswered questions that still matter.
    - Uncertainties.
    - Concerns.
    - Things I am still figuring out.
    - Important missing context.
    - Issues that may need future investigation.
- If important information appears to be missing, preserve the uncertainty here when useful.
- Do not invent answers merely to make the note appear complete.

## Related Topics

- Answers: **What other meaningful subjects connect to this conversation?**
- Include:
    - Related concepts.
    - Projects.
    - Subjects.
    - Tools.
    - Ideas.
- Briefly explain why each one is related.
- Do not create `[[wikilinks]]` because the extractor cannot assume corresponding notes exist.

### Example

```md
## Related Topics
- Obsidian — intended as the long-term storage location for extracted knowledge notes.
- Codex — may eventually provide a way for AI to work with larger collections of stored Markdown context.
```

## Conversation Summary

- Answers: **How did the conversation develop, and where did it end up?**
- Should be more detailed than `Overview`.
- Organize it mostly chronologically.
- Group repeated discussions about the same topic together when doing so improves clarity.
- Preserve:
    - Where the conversation started.
    - Major topics explored.
    - Important changes in thinking.
    - Discoveries.
    - Corrections.
    - Decisions.
    - Where the conversation ended.
- The summary should stand on its own.
- Some repetition with other sections is intentionally allowed.
- The goal is to preserve the story and development of the conversation.

## Optional Sections

- Optional sections should appear only when relevant.
- Omit them entirely when they contain no meaningful information.

### Procedures & Workflows

- Use when the conversation contains a useful repeatable process.
- Preserve steps in their correct order.
- Numbered lists may be used when sequence matters.

### Best Practices

- Use when the conversation produces multiple useful rules, recommendations, or principles worth remembering.

### Resources

- Use when meaningful resources were discussed or recommended.
- Resources may include:
    - Websites.
    - Books.
    - Videos.
    - Applications.
    - Tools.
    - Documentation.
    - Files.
    - Articles.
- Preserve enough context to remember why the resource mattered.

## Custom Sections

- Standard section names must remain fixed.
- If important knowledge genuinely does not fit anywhere, create a new descriptive `##` section.
- Custom sections should be the exception rather than the default.
- Descriptive `###` subsections may be used inside large sections to organize major subtopics.

## Empty Sections

- Keep the standard structure consistent.
- If a standard section contains no meaningful information, retain it with a short explanation.

### Example

```md
## Decisions
- No meaningful decisions were made.
```

- Never invent content merely to fill a section.
- Optional sections should simply be omitted when irrelevant.

## Formatting Rules

- Use simple Markdown.
- Prefer bullet points for normal information.
- Use nested bullets freely when they improve organization.
- There is no strict nesting-depth limit, but every level must improve clarity.
- Group related information together.
- Put more important information before minor supporting details.
- Use `###` subsections for very large sections or clearly distinct subtopics.
- Use numbered steps when a procedure genuinely requires sequence.
- Preserve code blocks, commands, formulas, configuration, and technical examples when useful.
- Avoid unnecessary decorative formatting.

## Detail Level

- Favor knowledge preservation over brevity.
- Guiding principle: **If information has reasonable future value, preserve it.**
- Notes are allowed to become long.

### Remove

- Greetings.
- Conversational filler.
- Repeated acknowledgments.
- Meaningless back-and-forth.
- Repetition that adds nothing.
- AI suggestions that never affected the conversation.

### Preserve

- Important facts.
- Useful small details.
- Personal context.
- Reasoning.
- Learning.
- Mental models.
- Decisions.
- Goals.
- Meaningful examples.
- Technical material.
- Changes in understanding.

## Repetition Rules

- Avoid unnecessary duplication without sacrificing meaning.
- When an idea belongs in multiple sections:
    - Put its complete treatment in the best section.
    - Briefly reference it elsewhere when necessary.
- `Key Knowledge` and `Lessons Learned` may intentionally overlap:
    - `Key Knowledge` records important knowledge.
    - `Lessons Learned` records what I personally learned.
- Consolidate repeated ideas from the conversation.
- Preserve multiple explanations when each provides a genuinely different and useful way of understanding the idea.

## Changes of Mind

- Treat my final or current position as authoritative.
- Preserve earlier thinking when it helps explain why my position changed.
- Do not present an abandoned idea as a current preference, goal, or decision.

## AI Suggestions

- Do not preserve ChatGPT suggestions simply because ChatGPT made them.
- Preserve an AI suggestion when it contributed meaningfully to:
    - Something I learned.
    - An insight.
    - A decision.
    - A goal.
    - A workflow I adopted.
    - Another meaningful outcome.
- The note represents knowledge gained from the conversation, not a transcript of everything the AI proposed.

## Fidelity and Inference

- Stay highly faithful to the source conversation.
- The extractor may:
    - Organize.
    - Condense.
    - Clarify.
    - Combine repeated information.
    - Categorize information.
    - Improve readability.
- The extractor must not:
    - Invent facts.
    - Invent motivations.
    - Invent decisions.
    - Invent preferences.
    - Invent conclusions.
    - Invent dates.
    - Turn speculation into certainty.
    - Present AI advice as something I adopted when I did not.
- When something is uncertain:
    - Preserve only what is supported.
    - Express uncertainty accurately.
    - Add important unresolved uncertainty to `Open Questions` when appropriate.

## Long Conversations

- Even very long conversations should normally produce one knowledge note.
- When multiple major topics exist:
    - Keep one note.
    - Organize major topics using `###` subsections.
    - Group related discussions together even when they occurred at different points in the original conversation.
- The title may represent multiple major topics when necessary.

## Title Rules

- The title should represent the overall contents of the conversation rather than merely the first topic discussed.
- For focused conversations, use a focused title.
- For broad conversations, include multiple important themes when necessary.
- The title should make the stored knowledge recognizable later in Obsidian.

## Dates and Time Context

- Preserve meaningful dates.
- Add timing such as `As of August 2026` when information may become outdated and that timing is known.
- Never invent or estimate missing dates.
- Preserve individual conversation dates in Metadata when they are actually available.

## Code and Technical Content

- Preserve all useful technical examples.
- This may include:
    - Code.
    - Commands.
    - Formulas.
    - Configuration.
    - Technical examples.
- Do not remove useful technical material merely to shorten the note.

## Completeness Review

- Before producing the final note, review the entire conversation again.
- Specifically check for overlooked:
    - Important facts.
    - Small but useful details.
    - Personal context.
    - Lessons.
    - "Aha" moments.
    - Mental models.
    - User-created examples.
    - Decisions.
    - Decision reasoning.
    - Goals.
    - Actions.
    - Ideas.
    - Open questions.
    - Changes of mind.
    - Corrections.
    - Procedures.
    - Best practices.
    - Resources.
    - Technical examples.
    - Related topics.
    - Time-sensitive context.
- This final pass exists specifically to reduce the chance that important information is lost during compression.

## Output Rules

- Output only the finished Markdown knowledge note.
- Do not include:
    - An introduction.
    - "Here's your note."
    - An extraction report.
    - Follow-up suggestions.
    - Commentary before the note.
    - Commentary after the note.
- The output should be immediately ready to copy into Obsidian.

## Final Knowledge Note Template

```md
# Conversation Title

## Metadata
- Source: ChatGPT — "Original Conversation Title"
- Conversation Date: YYYY-MM-DD
- Extracted: YYYY-MM-DD

## Overview
- ...

## Important Context
- ...

## Key Knowledge
- ...

## Lessons Learned
- ...

## Insights
- ...

## Decisions
- ...

## Goals
- Goal: ...
- Action: ...
- Idea: ...

## Open Questions
- ...

## Related Topics
- Topic — explanation of its connection.

## Conversation Summary
- ...

## Procedures & Workflows
- ...

## Best Practices
- ...

## Resources
- ...
```

## Core Principle

- The extractor's job is not to make a long conversation short at all costs.
- Its job is to turn a messy conversation into a clean, faithful, information-dense piece of long-term memory.
- Preserve both **what I know** and **how I came to understand it**.
- When deciding whether potentially useful information should be removed or preserved, favor preservation.
