Read the **entire conversation so far**, including all relevant user and assistant messages and files, and turn it into a single, organized Markdown knowledge note for long-term storage in Obsidian.

The goal is **knowledge preservation, not aggressive summarization**.

Preserve useful information, context, reasoning, discoveries, and personal understanding that could be valuable in a future conversation. When deciding whether potentially useful information should be kept or removed, favor keeping it.

## Core Rules

- Read the entire conversation before writing the note.
- Extract information rather than simply summarizing the conversation.
- Preserve important information even when it is a small detail.
- Remove conversational filler, greetings, repeated acknowledgments, and meaningless back-and-forth.
- Do not invent facts, motivations, decisions, preferences, conclusions, dates, or intentions.
- Stay faithful to what was actually established in the conversation.
- If something is uncertain, preserve only what is supported and place meaningful unresolved uncertainty under `Open Questions`.
- Distinguish between things I actually decided, things I am considering, and things ChatGPT merely suggested.
- Do not treat ChatGPT suggestions as my beliefs, goals, or decisions unless the conversation shows that I accepted or adopted them.
- Preserve changes in my thinking when they help explain why I reached my final understanding or decision.
- Combine repeated ideas when they are redundant, but preserve multiple explanations when each provides a genuinely useful way of understanding something.
- Preserve useful technical examples, code, commands, formulas, configurations, and workflows when they matter.
- Perform a final completeness review of the entire conversation before producing the note.

## Important Context

Preserve personal information when it is useful for understanding the conversation or helping a future AI respond appropriately.

This may include:

- Personal circumstances.
- Preferences.
- Existing workflows.
- Current systems.
- Constraints.
- Habits.
- Projects.
- Productivity approaches.
- Lifestyle context.
- Relevant background.
- Other information that meaningfully affects the conversation.

If information may become outdated, preserve the timing when known, such as:

- `As of August 2026, ...`

Never guess dates.

Do not preserve:

- Passwords.
- API keys.
- Authentication tokens.
- Financial credentials.
- Security answers.
- Other secrets or credentials.

## Lessons Learned vs. Insights

Treat these as two different things.

### Lessons Learned

Capture **what I actually learned or came to understand better**.

Include:

- New knowledge.
- Concepts I understand better now.
- Things I previously misunderstood and later corrected.
- Skills or principles gained from the conversation.

Write these in first person when appropriate.

### Insights

Capture **how something clicked for me**.

Look especially for:

- "Aha" moments.
- "So basically..." explanations.
- Personal mental models.
- Comparisons.
- Analogies.
- Connections to things I already understand.
- Examples I created that helped something click.
- Distinctions that suddenly made something understandable.
- Changes in my understanding.

Preserve my distinctive wording when it captures an important mental model, while cleaning up unnecessary repetition.

Do not preserve every example I make. Preserve examples when they clearly contributed to an important insight.

## Decisions

Capture important decisions I made.

For each meaningful decision, preserve:

- What I decided.
- Why I decided it, when the reasoning is supported.
- Important alternatives or tradeoffs when they help explain the decision.

Simple decisions can be brief.

Major decisions should preserve more of the reasoning.

Never invent a reason for a decision that was not established.

## Goals

Capture future-oriented intentions and distinguish them clearly.

Use these labels:

- `Goal:` something I intend to accomplish.
- `Action:` a specific thing I intend to do.
- `Idea:` something I may want to pursue but have not committed to.

Do not turn speculation into a commitment.

## Open Questions

Capture:

- Unresolved questions that still matter.
- Uncertainties.
- Concerns.
- Things I am still trying to figure out.
- Important missing information.
- Issues that may need future research or discussion.

If something important appears to be missing, record the uncertainty rather than inventing an answer.

## Related Topics

Capture other meaningful subjects, concepts, projects, tools, or ideas that connect to the conversation.

For each one, briefly explain the connection.

Do not create Obsidian `[[wikilinks]]`.

## Conversation Summary

Provide a detailed summary of how the conversation developed.

- Start with where the conversation began.
- Preserve major topics discussed.
- Preserve important changes in thinking.
- Preserve discoveries and corrections.
- Preserve important conclusions and decisions.
- End with where the conversation currently stands.
- Keep the summary mostly chronological.
- When the same topic appears repeatedly, group those discussions together when that improves clarity.

The summary may repeat important information found elsewhere. That is intentional.

## Optional Sections

Add these only when the conversation contains meaningful material for them.

### Procedures & Workflows

Use for useful repeatable processes.

Preserve steps in the correct order.

### Best Practices

Use for useful rules, principles, recommendations, or rules of thumb worth remembering.

### Resources

Use for meaningful:

- Websites.
- Books.
- Videos.
- Tools.
- Applications.
- Documentation.
- Files.
- Articles.
- Other resources.

Preserve why the resource mattered when that context is useful.

### Custom Sections

If important information genuinely does not fit any existing section, create a new descriptive `##` section.

Do this only when necessary.

## Information That Is Uncertain or Temporary

Do not turn possibilities into facts.

For example:

- "I might switch to X" is not a decision.
- "Maybe I'll build Y later" is not a committed goal.
- A ChatGPT recommendation is not something I believe unless I accepted it.
- An old preference should not be presented as current without evidence.

When timing matters and the date is known, preserve it.

Never guess a date.

## Changes of Mind

If I changed my mind during the conversation:

- Treat my final/current position as authoritative.
- Preserve the earlier position only when understanding the change is useful.
- Do not present abandoned ideas as current decisions or goals.

## Formatting Rules

Use simple Markdown.

The standard structure is:

```
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

Optional sections may follow when relevant:

```
## Procedures & Workflows
- ...

## Best Practices
- ...

## Resources
- ...
```

### Formatting requirements

- Keep the standard section names exactly as written.
- Use bullet points for normal information.
- Use nested bullets freely when supporting details improve clarity.
- There is no fixed nesting-depth limit, but nesting must improve organization.
- Group related information together.
- Put more important information before minor supporting details.
- Use `###` subsections when a section becomes large or contains clearly different subtopics.
- Use numbered steps when sequence matters.
- Preserve useful code blocks and technical examples.
- Do not add unnecessary decorative formatting.

## Empty Sections

Keep the standard sections consistent.

When a standard section has no meaningful content, keep it and briefly explain that nothing significant was found.

For example:

```
## Decisions
- No meaningful decisions were made.
```

Optional sections should be omitted when they are not relevant.

## Metadata

Place `Metadata` immediately below the title.

Use:

```
## Metadata
- Source: ChatGPT — "Original Conversation Title"
- Conversation Date: YYYY-MM-DD
- Extracted: YYYY-MM-DD
```

Include individual conversation dates when they are actually known.

Never guess missing dates.

Do not generate tags automatically.

Do not generate Obsidian wikilinks.

## Title

Create a title that represents the **overall knowledge contained in the conversation**, not simply the first topic discussed.

For a focused conversation, use a focused title.

For a broad conversation, include the major themes when necessary.

The title should make the note recognizable later in Obsidian.

## Completeness Review

Before producing the final answer, review the entire conversation one more time and check specifically for:

- Important facts.
- Small but useful details.
- Personal context.
- Lessons learned.
- Aha moments.
- Mental models.
- User-created comparisons or examples that produced insights.
- Decisions.
- Decision reasoning.
- Goals.
- Actions.
- Ideas.
- Open questions.
- Changes in thinking.
- Corrections.
- Procedures.
- Best practices.
- Resources.
- Technical examples.
- Related topics.
- Important dates or timing.

If an important piece of information was missed during the first extraction pass, add it before finishing.

## Final Output

Output **only the finished Markdown knowledge note**.

Do not include:

- An introduction.
- An explanation of what you extracted.
- A summary outside the note.
- Warnings outside the note.
- Follow-up questions.
- Suggestions.
- "Here is your note" or similar text.

The final response must be immediately ready to copy into Obsidian.
