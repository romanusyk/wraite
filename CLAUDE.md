# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**wraite** is a set of instructions for an AI-powered article editor. The author is a non-native English speaker who writes personal essays for Medium and uses an AI assistant to iteratively improve drafts.

The core deliverable is `editor.md` — a detailed, LLM-agnostic, human-readable specification that any AI editor should follow. It defines two editing modes (structure and colour), output format, and the author's quality bar for good writing.

## Key Files

- `editor.md` — The editor instructions. This is the central document of the project. It must remain LLM-agnostic (no references to specific AI systems) and readable by humans.
- `.claude/skills/edit/SKILL.md` — The `/edit` command that loads `editor.md` at runtime and applies it. Usage: `/edit structure <text>` or `/edit colour <text>`.
- `examples/` — Published articles by the author, used as reference for their writing style.

## Author's Writing Style

The author uses British English spelling (colour, savourless, etc.). Their style values:
- Natural pace — one idea at a time, not too dense, not too vague
- Human voice — colourful, personal, not robotic or academic
- Accessibility — Medium-appropriate vocabulary, no jargon

When editing `editor.md`, preserve these values. The pace examples section is particularly important — it demonstrates the difference between "too condensed" and "target pace" with concrete before/after samples.

## Working on editor.md

- Keep instructions precise enough for an AI to follow deterministically, but written in natural prose a human can review.
- Do not reference any specific AI model or product in `editor.md`.
- The two modes (structure and colour) are distinct workflows — do not merge them.
- Structure mode always produces two sequential outputs: correction first, then restructuring. This is intentional (see "Why Both Steps?" section).
