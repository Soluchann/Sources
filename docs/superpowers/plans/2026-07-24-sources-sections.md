# Sources Sections Implementation Plan

> **For agentic workers:** Implement task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add UI tools, AI tools, and Study material sections to the FMHY-style markdown index.

**Architecture:** Insert three new peer sections after Miscellaneous and before Changelog in both `README.md` and `fmhy.md`, keeping files identical.

**Tech Stack:** Markdown only.

## Global Constraints

- Do not modify existing FMHY sections.
- Keep `README.md` and `fmhy.md` identical.
- Follow approved design in `docs/superpowers/specs/2026-07-24-sources-sections-design.md`.

---

## Task 1: Insert sections into README.md and fmhy.md

**Files:** `README.md`, `fmhy.md`

- [x] Insert UI tools, AI tools, and Study material (with nested LLM Cache Management) after Miscellaneous / before Changelog
- [x] Verify both files match
- [x] Commit
