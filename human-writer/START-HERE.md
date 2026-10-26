# Human Writer
## A free writing resource from PrismAgent Solutions

**Keep your meaning. Keep your voice. Lose the unnecessary filler.**

Use Human Writer to edit emails, LinkedIn posts, articles, video scripts, and fiction. It looks beyond a list of banned words: the emphasis is on what the text says, how it is organized, and what the reader needs.

Version 2.0.1 · October 25, 2026

## Try it first

Provide a draft and say:

> Use Human Writer to edit this for a business owner. Keep my facts, uncertainty, and call to action. Make it direct and conversational without adding claims. Return only the revised text.

For closer voice matching, add two or three short samples of your own writing. You can specify a channel, word limit, or level of editing. The skill also works when a draft needs only small changes.

## Set up your preferred tool

### Claude chat or Cowork

Upload the supplied skill ZIP through **Customize → Skills → + Create skill → Upload a skill**, then enable it. Available controls depend on account and organization settings. Ask Claude to use Human Writer and supply your draft.

The ZIP contains one top-level `human-writer` folder with `SKILL.md` inside it. Preserve that structure.

### Claude Code

Extract the `human-writer` folder into your personal `~/.claude/skills/` directory, or the project's `.claude/skills/` directory. The resulting file should be `human-writer/SKILL.md` beneath that skills directory. Invoke it with `/human-writer` and your editing request. Local Claude Code paths do not by themselves install a skill into Cowork.

### Codex

Extract `human-writer` into your personal `~/.agents/skills/` directory or the project's `.agents/skills/` directory. Select it from the skill picker, or explicitly ask Codex to use `human-writer`. If it is not listed, start a new chat and check the folder location. Merely saving the ZIP in Google Drive does not install it.

### A chat without skill installation

Attach `SKILL.md` to your chat and ask the assistant to follow its editing instructions for the supplied draft. For fiction, also attach `references/research-findings.md`. This is a session-level instruction workflow, not a claim that a slash command has been installed.

## New in version 2

- **Edit:** improve the draft while keeping its meaning and voice.
- **Audit:** quote weak passages and explain what to change without rewriting the whole draft.
- **Voice matching:** use your samples and optional preferences, rather than a fixed creator persona.
- **Contextual checks:** preserve technical terms, exact quotes, meaningful Unicode, and useful sentence patterns.

Try: “Audit this LinkedIn post for generic wording. Quote only the passages worth changing. Keep my facts and intended call to action.”

For closer matching, use the optional [voice profile](references/voice-profile.md). See [editing boundaries](references/edge-cases.md) for examples of what should stay unchanged.

## Three useful requests

- **Email:** “Keep the deadline, price, and request exactly as intended. Cut the corporate padding.”
- **LinkedIn:** “Preserve my point of view. Remove generic framing and repeated conclusions. Do not invent a client story.”
- **Fiction:** “Tighten explanations and repetitive sensory detail. Preserve the plot, viewpoint, and ending; list any larger structural suggestions separately.”

## What the research does and does not say

StoryScope examines long fiction. Its narrative classifier achieved **93.2% macro-F1** on its benchmark; this is not a universal accuracy claim for emails, posts, or websites. Editing prose does not certify human authorship or make text undetectable. Our business-writing guidance is an editorial adaptation, not a tested result from that paper.

Read [the findings and examples](references/research-findings.md) or [before-and-after demonstrations](references/examples.md).

## About this resource

Combined editing instructions and original examples prepared for PrismAgent Solutions, with guidance adapted from credited open-source writing skills. See [credits and notices](CREDITS.md). Research credit: Jenna Russell, Rishanth Rajendhran, Chau Minh Pham, Mohit Iyyer, and John Wieting, *StoryScope: Investigating idiosyncrasies in AI fiction*, arXiv:2604.03136v6 (August 10, 2026). The authors and their institutions do not endorse this skill. No research code or source stories are required to use it. The skill contains no executable scripts, account connections, or tracking code.

Want help making your team's recurring writing work more consistent? Contact **PrismAgent Solutions** at [prismagentsolutions.com](https://prismagentsolutions.com).

## Setup references

Instructions checked October 25, 2026. Product menus may change.
- [OpenAI: Build skills](https://learn.chatgpt.com/docs/build-skills)
- [Anthropic: Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude)
- [Anthropic: Create custom skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills)
- [Anthropic: Claude Code skills](https://code.claude.com/docs/en/skills)
