# Human Writer by PrismAgent Solutions

A free editing skill for Claude, Claude Code, Cowork, and Codex. Give it a draft, such as an email, a LinkedIn post, an article, or a video script, and it cuts the generic filler while keeping your facts, your meaning, and your voice.

## Download

**[Download Human Writer v2.0.1 (ZIP)](https://github.com/ckruegs71-ctrl/prismagent-human-writer/raw/main/download/PrismAgent-Human-Writer-v2.0.1.zip)**

The ZIP holds one `human-writer` folder with `SKILL.md` inside. Keep that structure when you install it.

## Install

- **Claude chat or Cowork:** go to Customize → Skills → + Create skill → Upload a skill, choose the ZIP, then turn the skill on.
- **Claude Code:** unzip it into `~/.claude/skills/` so the file sits at `~/.claude/skills/human-writer/SKILL.md`. Then type `/human-writer` with your request.
- **Codex:** unzip it into `~/.agents/skills/` and pick it from the skill list.
- **Any other chat:** attach `SKILL.md` and ask the assistant to follow it for your draft.

[START-HERE.md](human-writer/START-HERE.md) has the full setup notes and more sample requests.

## Try it

Paste a draft and say:

> Use Human Writer to edit this for a business owner. Keep my facts, uncertainty, and call to action. Return only the revised text.

Add two or three short samples of your own writing if you want a closer match to your voice.

## What it does

- **Edit:** tightens the draft and keeps every fact, number, date, link, and call to action.
- **Audit:** quotes the weak passages and says what to change, without rewriting the whole piece.
- **Match your voice:** works from your samples, not a fixed persona.

It will not invent customers, results, statistics, or stories to make a draft sound vivid. It does not score text as human or AI, and it does not promise to get past AI detectors.

## More from PrismAgent

PrismAgent Solutions builds AI automation for small businesses. See what else we do at [prismagentsolutions.com](https://prismagentsolutions.com).

## Credits and license

Human Writer draws on MIT-licensed work by Peter Yang (no-ai-slop), Siqi Chen (humanizer), and Jake Schincariol (li-human), and on the StoryScope research paper by Russell, Rajendhran, Pham, Iyyer, and Wieting. None of them endorse this resource. Details are in [CREDITS.md](human-writer/CREDITS.md). Released under the [MIT license](LICENSE).
