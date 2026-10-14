# Roadmap

V1 is the first working version of the prompt. This is what would make it better, split into what matters next and what can wait.

## Should Do Next

These are the steps I'd consider necessary before calling the project finished.

- **Test Prompt V1 on a learning-heavy chat**
    - Choose a conversation with explanations, misunderstandings, examples, and aha moments.
    - Compare the generated note against the original chat.
    - Check especially whether `Lessons Learned` and `Insights` work as intended.
- **Test Prompt V1 on a personal/productivity chat**
    - Make sure `Important Context` captures useful lifestyle, workflow, preference, and situational information.
    - Check that possibilities aren't incorrectly turned into established facts.
- **Test Prompt V1 on a project/technical chat**
    - Check decisions, reasoning, goals, workflows, code, and technical knowledge.
    - Make sure ChatGPT suggestions you didn't adopt aren't treated as your decisions.
- **Create an extraction quality checklist**
    - Did anything important disappear?
    - Were aha moments preserved?
    - Was personal context preserved?
    - Were any facts invented?
    - Were abandoned ideas presented as current?
    - Was unnecessary conversation removed?
    - Could another AI understand the important context using only the note?
- **Refine Prompt V1 from real failures**
    - Don't add rules just because they sound useful.
    - Add or change instructions when testing reveals an actual problem.
- **Create Prompt V2**
    - Once several different chats work well, consolidate the improvements into a stable version.
- **Test future-AI handoff**
    - Give only an extracted knowledge note to a fresh ChatGPT conversation.
    - Ask questions that require context from the original conversation.
    - See whether the note preserved enough information for useful answers.
    - This is probably the most important final test.

## Could Do Later

These aren't necessary for the core idea to work.

- **Provided-chat version**
    - Make a second prompt for when an old/exported conversation is pasted into a new ChatGPT chat instead of extracting the current conversation.
- **Prompt version history**
    - Keep `v1`, `v2`, etc. so you can compare extraction quality instead of constantly overwriting the prompt.
- **Example outputs**
    - Save a few excellent extracted notes as reference examples.
- **Obsidian organization**
    - Decide where extracted knowledge notes live.
    - Develop naming conventions.
    - Decide whether you eventually want topic folders, Maps of Content, or another organization system.
- **Knowledge updating**
    - Design a way to handle an old knowledge note when a newer conversation changes something it contains.
- **Duplicate knowledge handling**
    - Eventually determine what happens when several conversations contain the same knowledge or personal context.
- **Cross-note connections**
    - Later explore automatically identifying related existing notes instead of merely listing `Related Topics`.
- **Search across the knowledge base**
    - Eventually investigate ways for an AI to search many of your Markdown notes and retrieve only the relevant ones for a conversation.
- **Codex integration**
    - Explore whether Codex can work directly with a folder/repository containing the knowledge notes so you don't have to manually upload individual notes.
- **Automated extraction**
    - If manually running the prompt becomes tedious, revisit the original Python/API idea.
    - A script could process exported chats, generate notes, and save them automatically.
- **Bulk old-chat migration**
    - If you eventually have many conversations to preserve, create a workflow for processing your backlog.
- **Knowledge maintenance**
    - Explore detecting outdated personal context, conflicting information, or knowledge superseded by newer conversations.
- **Privacy rules**
    - If these notes eventually move outside your private vault, create stricter rules for what personal information should be retained.
