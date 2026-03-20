# Zettelkasten: Agent guidance

Guidance for AI agents (and humans) working in **zettelkasten/**. Repo-wide rules apply: see [AGENTS.md](../AGENTS.md) (repo root) for conventions and layout.

**Full method (humans and agents):** The Zettelkasten method—principles, anatomy, linking, structure, writing—is in **[zettelkasten.md](zettelkasten.md)**. Read that for the complete guidance. This file adds repo-specific conventions and a quick reference for agents.

______________________________________________________________________

## Zettelkasten Conventions (Quick Reference)

- **File names**: date+slug in kebab-case (e.g. `2025-03-13-principle-of-atomicity.md`). Use `YYYY-MM-DD` then a slug. See [AGENTS.md](../AGENTS.md) (repo root) for repo-wide conventions.
- **Links**: Standard markdown `[text](path/to/note.md)`. Do not use wiki-style `[[links]]`.
- **Permanent notes**: In `zettelkasten/`. When creating a new note, **name the file** date+slug (e.g. `2025-03-13-title-slug.md`); use [template-zettel.md](template-zettel.md) for the **content** (title, tags, Summary, Notes, Links). Include a creation-date tag with a hash: **#YYYY/MM/DD** (e.g. `#2025/03/13`) so systems with hierarchical tags can filter by year, year-month, or full date.
- **Inbox**: Use `inbox/` for fleeting captures; process into `zettelkasten/` and clear the inbox regularly.
- **Source lines (provenance)**: When a note records where content came from, put it in italics as `*Source: …*` and **always include a markdown link** to the capturing artifact (daily entry, meeting note, etc.). Multiple sources → multiple links in one line. Avoid prose-only dates with no link.

______________________________________________________________________

## Procedures

Each procedure has a **name**, then **When** and **What to do** as section headers. **What to do** is an enumerated list (1. 2. 3. …). Full method in [zettelkasten.md](zettelkasten.md).

### Create a permanent note

#### When

Creating a new permanent note (atomic thought, concept, or reference you want in the slip-box).

#### What to do

1. Name the file `YYYY-MM-DD-slug.md` (date + kebab-case slug).
2. Use [template-zettel.md](template-zettel.md) for content: title, tags (include **#YYYY/MM/DD**), Summary, Notes, Links.
3. Write in your own words; add link context for any links (why the link matters).
4. Place the file in `zettelkasten/` (not in inbox).
5. Link to at least one existing note and state why; avoid isolated notes.

### Process the inbox

#### When

Processing the inbox (turning fleeting captures into permanent notes or discarding).

#### What to do

1. Open items in `inbox/`.
2. For each item: either create a new permanent note following **Create a permanent note** above (and add links with context), merge into an existing note, or discard. When promoting to permanent, **preserve or add hyperlinked** `*Source:*` lines (link to daily entry, meeting note, or other origin).
3. Remove or clear processed items from inbox so the inbox stays for quick captures only.

______________________________________________________________________

## Summary for Agents

| Decision | Prefer |
|----------|--------|
| Linking | Always add link context (why this link). |
| Note size | One thought per note; split when a note is hard to use or mixes ideas. |
| Organization | Tags (object, not topic); structure notes that emerge; no upfront categories. |
| New material | Process into notes and links soon; avoid collecting without processing. |
| Note content | Your own words; add context and relevance. |
| Structure | Let layers emerge (content → structure notes → main structure); use buffer notes for project staging. |
| Evidence layers | Keep phenomenon, interpretation, and synthesis distinct in or between notes; check primary sources. |
| Writing | Outline first (attach note refs), then paste and rewrite; separate research and drafting; use outlines/buffers for many projects. |

When in doubt, favor **connection with explicit meaning** over more notes or more links without context. Principles over techniques; less clutter, more clarity.
