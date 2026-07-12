# Weiwei's Content Editor

A custom skills package that runs a personal executive-content editor: it evaluates source material, builds outlines, edits drafts, converts articles into podcast scripts, and repurposes one piece of content into a full multi-platform package, all in a consistent personal voice, with strict source-integrity rules.

> **Note:** This is a public showcase of the skill's design. The skill runs on both Claude Code and OpenAI Codex. The skill itself (the prompt library, voice rules, workflows, and templates) is proprietary and lives in a private repository. All rights reserved.

## What it does

| Capability | Example request |
|---|---|
| Deep content evaluation | "Rerun the analysis. Which direction is strongest?" |
| Newsletter outlining | "Show me the best outline first, wait for my approval" |
| Draft editing & polish | "Make this more practical. Do not compress or drop content." |
| Podcast / YouTube conversion | "Turn this transcript into a 20-minute episode outline" |
| Content repurposing | "Turn this article into a post, carousel notes, and a promo note" |
| Visual prompt engineering | "One image per slide, 16:9, no collage" |
| Source integrity auditing | "Did you leverage all uploaded content? Show me where." |

## Where it creates the most value

The skill works at three moments in the life of a piece, and the earliest moments pay the most.

**Before a draft exists.** Paste raw notes, a transcript, or a half-formed idea and ask for the strongest angle. The skill scores candidate directions for timeliness, narrative pull, and evidence, and tells you honestly which parts your audience has already read a hundred times. It also asks for the real story behind the idea instead of inventing one, because a true moment of struggle beats three plausible hypotheticals.

**While writing.** Structural editing (front-load the value, face the strongest objections, plant one memorable line), line-level iteration on titles and hooks with verdict-first feedback, and citation work that goes beyond formatting: finding primary sources, verifying product names, flagging stale statistics, and stripping tracking parameters before they reach the public.

**After publishing.** Repurposing one piece into a companion feed post, carousel notes, and a lightweight promotion plan, plus series consistency: sequels link back, frameworks never repeat across pieces, and the voice stays recognizable from one article to the next.

It also checks grammar. That is simply the least interesting thing it does.

## Design principles

- **Source facts are sacred.** The skill never invents examples, data, quotes, or names. Missing information is flagged as `Not provided` or `Proof needed` instead of papered over.
- **Outline before draft.** Long-form work is gated on an approved outline, so revisions happen at the cheap stage.
- **The latest human version wins.** The skill treats the author's most recent edit as the source of truth and never silently reverts it.
- **Voice is enforced, not hoped for.** A reference file defines tone, banned filler words, and banned sentence patterns: the tells that make writing sound AI-generated.
- **The formula is codified.** A "viral DNA" reference captures the reusable structure of the best-performing pieces: a personal confession that creates recognition, one contrarian reframe in the first 100 words, a numbered framework with copy-paste elements, and a close that gives permission instead of pressure.
- **Every point must survive one test:** *what can an executive do after reading this?*

## Architecture

The skill uses progressive disclosure: a compact `SKILL.md` entry point that loads deeper instruction files only when the task needs them.

```
weiwei-content-editor/
├── SKILL.md                  # entry point: rules, routing, response pattern
├── workflows/                # 9 task-specific procedures
│   ├── content-intake.md
│   ├── deep-evaluation.md
│   ├── linkedin-newsletter-outline.md
│   ├── podcast-conversion.md
│   ├── editing-and-polish.md
│   ├── argument-piece.md
│   ├── source-integrity.md
│   ├── repurpose-package.md
│   └── visual-content-prompting.md
├── references/               # voice & style, viral DNA formula, prompt library, content pillars
├── templates/                # canonical output formats
├── checklists/               # final-review gate before delivery
└── examples/                 # sample trigger requests
```

## Quality process

The skill was iteratively improved and benchmarked with Anthropic's skill-creator tooling: parallel test runs against a baseline snapshot, assertion-based grading (outline discipline, template fidelity, banned-word scans, fact-preservation checks), and a human review loop.

## Author

Built by **Weiwei Hu**. 

Read the work this skill produces:

- Newsletter: [Second Draft Studio](https://seconddraftstudio.substack.com/)
- Medium: [Medium](https://medium.com/@weiwei.hu)

---

Copyright (c) 2026 Weiwei Hu. This showcase is licensed under [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/): you may share it with credit, but not modify or use it commercially. The skill itself (prompts, voice rules, workflows, templates) is proprietary and all rights to it are reserved.
