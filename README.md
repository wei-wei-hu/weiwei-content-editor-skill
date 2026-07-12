# Weiwei's Content Editor

This is the AI editing skill behind everything I publish. It knows my voice, checks my grammar, verifies my sources, and tells me honestly when a draft is not ready.

> **Note:** This is a public showcase of the skill's design. The skill runs on both Claude Code and OpenAI Codex. The skill itself (the prompt library, voice rules, workflows, and templates) is proprietary and lives in a private repository. All rights reserved.

## The two jobs it never skips

**Grammar and language checks.** Every draft gets a full pass for grammar, punctuation, capitalization, and garbled sentences, including the damage that happens when text travels between editors. It also catches the quieter problems: the same word landing twice in two sentences, doubled emphasis, broken lists, and phrasing that sounds like a machine wrote it.

**Source and reference verification.** Every fact has to earn its place. The skill finds the primary source behind a citation, checks that product and company names are current and correct, flags statistics that have gone stale, and strips tracking parameters from links before anything goes public. When a claim cannot be verified, it gets marked as unverified instead of published as fact.

## What else it does

| I ask | It delivers |
|---|---|
| "Which direction is strongest?" | Scores the candidate angles and says which ones readers have already seen a hundred times |
| "Show me the outline first" | An outline for approval before any full draft gets written |
| "Make this more practical" | An edit that keeps every idea and adds what a reader can actually do |
| "Turn this transcript into an episode" | A podcast or YouTube outline in a warm host voice |
| "Repurpose this article" | A feed post, carousel notes, and a promotion plan from one source |
| "One image per slide, 16:9, no collage" | Visual prompts in a consistent hand-drawn style |

## Where it helps most

**Before I write.** I paste raw notes and ask for the strongest angle. It also asks me for the real story behind the idea instead of making one up, because a true moment beats three plausible inventions.

**While I write.** Structure, titles, hooks, and honest line-by-line feedback. When my own edit makes a sentence weaker, it says so and explains why.

**After I publish.** One article becomes a feed post, carousel notes, and a promotion plan, and the next piece in the series stays consistent with the last one.

## The rules it enforces

- **No invented facts.** No made-up examples, data, quotes, or stories, ever. Missing information gets marked "Not provided."
- **Outline before draft.** Long pieces start with an outline I approve, so revisions happen while they are still cheap.
- **My latest edit wins.** It never quietly reverts something I changed.
- **My voice is protected.** A reference file lists the words, patterns, and punctuation habits that make writing sound AI-generated, and every draft gets swept for them.
- **The formula is written down.** My best-performing pieces share a structure (a personal story that creates recognition, one surprising reframe early, a numbered framework with copy-paste value, and a warm close), and the skill applies it to new drafts.
- **Every point faces one question:** what can my target audience do after reading this content?

## How it is organized

A small entry file holds the rules and decides which deeper instructions to load for each task, so the skill stays fast and focused.

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

## How it was tested

The skill was tested with parallel runs against a baseline version, graded on things that can be checked (did it stop at the outline, did it preserve every fact, did any banned word slip through), and improved through live editing sessions on real articles.

## Author

Built by **Weiwei Hu**. 

Read the work this skill produces:

- Newsletter: [Second Draft Studio](https://seconddraftstudio.substack.com/)
- Medium: [Medium](https://medium.com/@weiwei.hu)

---

Copyright (c) 2026 Weiwei Hu. This showcase is licensed under [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/): you may share it with credit, but not modify or use it commercially. The skill itself (prompts, voice rules, workflows, templates) is proprietary and all rights to it are reserved.
