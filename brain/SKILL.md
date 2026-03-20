---
name: brain
description: >-
  Manages brain-style repo structure (areas, projects, resources, zettelkasten).
  Respects README for humans and AGENTS.md for agents; applies all AGENTS.md from
  root down to current path as an overlay. Use when working in areas, projects,
  resources, zettelkasten, when creating/updating structure or agent guidance,
  when initializing an uninitialized directory from the template, or when the user
  asks for a review or audit of repo conformance to this contract.
license: GPL-3.0
---

# Operating in a brain-style repository

Guidance for agents working in a brain-style repo: load the overlay, follow the contract (README vs AGENTS.md), and apply procedures from the repo’s own files.

## Contract: README vs AGENTS.md

| File | Audience | Purpose |
|-----------|----------|---------|
| **README.md** | Humans | What people need to know: what this scope is, how to use it, how it connects to the rest of the repo. |
| **AGENTS.md** | Agents | What agents need to know: **scope**, **conventions**, **procedures**, and **how to operate** within this path. |

Do not put agent-only procedures in README; do not put human-only overview in AGENTS.md. When creating or editing either file, keep that split.

### Conventions and procedures (first-class in AGENTS.md)

**Conventions** are the rules: naming, structure, what belongs where, and how things connect. **Procedures** are first-class alongside conventions. Each procedure must have:

1. **Name** — A short, clear title (e.g. "Create a new area", "Process the inbox") so agents and humans can refer to it.
2. **When** — A section header (e.g. `#### When`) followed by the situation or trigger that calls for this procedure.
3. **What to do** — A section header (e.g. `#### What to do`) followed by an **enumerated list** of steps (1. 2. 3. …), not bullets or a single line. So agents can follow them in order.

Document procedures in every AGENTS.md where they apply (root, areas, projects, resources, zettelkasten, etc.). Prefer following documented procedures over inventing new ones.

### Source lines (provenance)

When notes record **where** content was captured (daily entries, meeting notes, person/group back-links, inbox or permanent zettelkasten):

1. Use a single italic line, typically `*Source: …*`.
2. **Always hyperlink the originating file**—do not write only a human date or title. Examples: `*Source: [Mar 19, 2026](../../areas/me/daily-entries/2026-03-19.md).*`, `*Source: [SPM team meeting](../../areas/relationships/groups/security-posture-management/2026-03-20-spm-team-meeting.md) Mar 20, 2026.*`
3. **Multiple origins** → multiple markdown links in the same line, comma-separated.
4. **Avoid:** `*Source: me entries Mar 19, 2026.*` or `*Source: SPM team meeting Mar 20, 2026.*` with no link—readers cannot jump to the capture.

Repo-specific procedures in `areas/me/AGENTS.md`, `areas/relationships/AGENTS.md`, and `zettelkasten/AGENTS.md` should reinforce this for inbox creation and promotion (when those scopes exist in the repo).

## Overlay: parent through root

When working at any path in the repo, **all AGENTS.md files from the repository root down to that path** apply. They **overlay**: root is the base; each level toward the current path adds or refines.

- **Root** `AGENTS.md` — repo-wide scope, conventions, procedures, and how to operate. Always applies.
- **Intermediate** `AGENTS.md` (e.g. `areas/AGENTS.md`, `projects/AGENTS.md`) — scope, conventions, procedures, and how to operate for everything under that directory.
- **Leaf** `AGENTS.md` (e.g. `areas/my-area/AGENTS.md`, `zettelkasten/AGENTS.md`) — scope, conventions, procedures, and how to operate for that folder.

**Behavior:** Before acting in a directory (or a file under it), resolve the chain from root to that directory and **read every AGENTS.md along the path**. Apply them in order (root → … → current). More specific (closer to the current path) overrides or narrows the more general. If a level has no AGENTS.md, skip it and continue.

**Example:** Working in `areas/learning/`:

1. Read and apply root `AGENTS.md`.
2. If `areas/AGENTS.md` exists, read and apply it.
3. Read and apply `areas/learning/AGENTS.md`.

Together they form the full set of rules for that path.

## What to do in practice

1. **Determine scope** — Identify the path you’re working in (e.g. an area, a project, `resources/`, `zettelkasten/`).
2. **Load the overlay** — For that path, open every `AGENTS.md` from repo root down to that path (each directory segment). Combine them with later (more specific) layers taking precedence where they conflict.
3. **Act** — Follow the combined guidance. Prefer procedures stated in those files over inventing new ones.
4. **When adding or changing structure** — Create or update README.md for humans and AGENTS.md for agents at the right scope. In AGENTS.md, include scope, conventions, procedures (each with a **name**, **When** and **What to do** as section headers, and **What to do** as an enumerated list), and how to operate at that level (repo-wide in root, path-specific in that path’s AGENTS.md).

## Where the contract applies

- **Root** — One README.md (humans), one AGENTS.md (agents).
- **areas/** — Per-area folders: each with its own README.md and AGENTS.md.
- **projects/** — Folder-level or per-project README.md and AGENTS.md as the repo chooses.
- **resources/** — Folder-level (and optionally per-resource) README.md and AGENTS.md.
- **zettelkasten/** — README.md and AGENTS.md at that folder (and any sub-scopes if defined).

The exact layout (e.g. per-project AGENTS.md) is defined by the repo’s root and intermediate AGENTS.md; this skill only requires that README = human, AGENTS = agent, and that the parent-through-root overlay is respected.

## Review or audit

When the user asks for a **review**, **audit**, or **conformance check** of the repository against this contract:

1. **Scan the repo** for all README.md and AGENTS.md files (root and under areas, projects, resources, zettelkasten, and any other scopes the root AGENTS.md defines).
2. **Audit against the contract:**
   - **Presence:** Where does the root (or existing AGENTS.md) say README/AGENTS are expected? Are they present? Missing?
   - **Split:** In each pair, does README hold human-facing content (what this is, how to use it, how it connects) and AGENTS.md hold agent-facing content (scope, conventions, procedures, how to operate)? Flag content that belongs in the other file.
   - **Procedures:** Where AGENTS.md defines procedures, does each have a **name**, **When** and **What to do** as section headers, and **What to do** as an enumerated list (1. 2. 3. …)? Flag procedures that are missing any of these or use bullets/a single line for steps instead of an enumerated list.
   - **Overlay:** Do AGENTS.md files reference or assume the parent-through-root overlay? Are paths/links to parent or root AGENTS.md correct?
   - **Scope:** Is repo-wide guidance only in root? Is scope-specific guidance only in the relevant scope (not duplicated in root)?
   - **Source lines:** In zettelkasten notes, inbox captures, and relationship back-links, do `*Source:*` lines **hyperlink** to the capturing daily entry, meeting note, or other artifact (see **Source lines (provenance)** above)? Flag prose-only provenance with no link.
3. **Report findings** — List what conforms and what does not, with paths and short reasons.
4. **Suggest revisions** — For each issue, propose a concrete change: add a missing file, move or rephrase content to the correct file, fix a link, or split content between README and AGENTS.md. Offer to apply the suggested revisions (edits) when the user approves.

## Initializing from template

When the user wants to **initialize an uninitialized directory or repository** as a brain (or "pull the template"):

1. **Locate the template** — The skill provides a full brain template at **assets/brain-template/** (relative to this skill's root). Path from workspace root is typically `.cursor/skills/brain/assets/brain-template/`.
2. **Target directory** — Copy into the repository root (or the directory the user specifies). If the target already has brain files (e.g. root AGENTS.md, areas/), treat it as already initialized unless the user asks to overwrite or refresh.
3. **Copy template contents** — Copy all files and directories from `assets/brain-template/` into the target, preserving structure. Do not copy the `brain-template` folder itself; copy its contents so that AGENTS.md, README.md, areas/, projects/, resources/, scripts/, zettelkasten/, and .gitignore end up at the target root.
4. **Follow-up** — After copying, point the user to the new root README.md (quick start: customize areas, projects, and zettelkasten).

Template contents are listed in [assets/README.md](assets/README.md).
