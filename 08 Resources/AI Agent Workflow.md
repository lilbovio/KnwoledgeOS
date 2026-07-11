# 🤖 AI Agent Workflow Protocol
*Guidance for AI agents reading and modifying this Obsidian vault.*

This document provides a set of operational instructions for LLM agents (Claude Code, Gemini CLI, Cursor, Cline, Roo Code) interacting with this knowledge base.

## 1. Reading the Vault
- **Start at the Hub**: Always read [[10 Agent Memory/Personal Profile|Personal Profile]] and [[00 Dashboard/Main Dashboard|Main Dashboard]] to understand the owner's profile and current focus.
- **Trace Backlinks**: Follow Obsidian wikilinks `[[Note Name]]` to inspect related concepts before making changes.

## 2. Retrieving Context
- Check directory tags and structure.
- Locate target concepts in their respective folders:
  - Career notes in `03 Career/`
  - Algorithms in `02 Knowledge/Algorithms/`
  - Project specifications in `01 Projects/`

## 3. Updating Notes
- Do not destroy existing user notes. Append new details under clear subsections.
- Keep the standard note format: Frontmatter, Summary, Key Concepts, Examples, Related Notes.

## 4. Preventing Duplicate Notes
- Prior to creating a new markdown file, search for existing notes with similar semantic themes.
- If a note exists (e.g. `SOLID.md`), update it instead of creating a new file (e.g. `solid-design.md`).

## 5. Maintaining Links
- Every new note MUST contain at least 2-3 links to existing notes (e.g. linking a LeetCode solution to its primary algorithm note, like [[Sliding Window]]).

## 6. Updating MOCs & Dashboards
- When creating a note, locate its corresponding Map of Content (e.g. [[Algorithms MOC]] or [[AI MOC]]) and add it to the index list.
- If the item is high priority, feature it on the [[00 Dashboard/Main Dashboard|Main Dashboard]].
