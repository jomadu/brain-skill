# Zettelkasten Method

This document describes the Zettelkasten method as used in this repository. It is for both humans and agents. It is based on the principles described at [zettelkasten.de](https://zettelkasten.de/overview/), especially the introduction and related posts. Principles are higher than techniques; this guidance emphasizes **why** so you can choose **how** appropriately.

## What a Zettelkasten Is (Working Definition)

- A **personal tool for thinking and writing**, not a shared or project-only box.
- **Hypertextual**: notes refer to each other and form a **web of thoughts**, not a pile of documents.
- **Emphasis on connection, not collection.** The value is in linking and relating ideas, not in hoarding notes.

If in doubt, prefer **fewer, well-connected notes** over many isolated ones.

**Digital-only (no physical notebook).** This guidance assumes you work entirely in a digital archive (plain text, files, optional apps). The zettelkasten.de site sometimes describes a paper-first reading workflow (notes on paper → process into Zettels later). If you don't use a physical notebook: capture directly into the inbox or into draft Zettels, then process and link. The principles are the same; only the capture step differs.

______________________________________________________________________

## Core Principles

### 1. Principle of Connectivity

Every new note should be **placed in some relationship** to at least one existing note. Linking is the main mechanism.

- **Always state explicitly why you linked** (link context). Example: after a link, add a short phrase explaining what the reader will find or why the connection matters. Links without explanation do not create knowledge and make the archive feel unreliable when you surf it later.
- **Principles over techniques**: Luhmann used "Folgezettel" (note sequences) on paper because he had to; in a digital system, **explicit links with context** realize the same principle and are preferable. Do not copy his techniques literally; follow the principle (connect with clear intent).

### 2. Principle of Atomicity

- **One knowledge-building block per note** as a guiding compass, not a rigid rule. A "block" is one thought, argument, or concept you can refer to and link to.
- **Length**: If getting the point out of a note takes too long, simplify or split. Lists of evidence or definitions can stay in one note; prose that mixes several ideas should often become multiple notes. When splitting, consider creating a third note that connects the two new ones and keeps context.
- **Atom size depends on your goal**: a web of thoughts suggests one thought per note; a web of excerpts suggests one excerpt per note. Prefer the former for thinking and writing.

### 3. No Categories; Use Tags (and Prefer Object Tags)

- **Do not pre-build a hierarchy of categories.** Let the archive grow organically; topic clusters and structure notes emerge with use.
- **Use tags**, but prefer **object tags** over **topic tags**:
  - **Object tags**: tag the specific concept or object the note is *about* (e.g. a note about insulin sensitivity is tagged with that concept, not with "diet").
  - **Topic tags**: tagging everything "relevant to diet" with `#diet` makes searches noisy and imprecise. Avoid tagging by broad topic; tag by the concrete object/concept so searches stay precise as the archive grows.
- Optional: use a **double-hash** (e.g. `##topic`) to mark a **top-level structure note** for a concept, so a single search takes you to the main entry point.

### 4. Collector's Fallacy

- **Collecting is not learning.** Bookmarking, copying, or filing without processing does not increase knowledge. Only working with material—reading, interpreting, writing in your own words, and connecting—does.
- **Process early**: short cycles of research → read → assimilate (notes + links) are better than piling up unprocessed material. Prefer finishing a small batch over leaving a large stack for "later."
- **Same for links**: adding links "for later" without stating why is a form of collecting. Add links when you can state the reason; if you cannot yet, it's a signal to think more or defer the link.

______________________________________________________________________

## Anatomy of a Zettel

Each note should have:

1. **Unique identifier** — So it can be referenced. In this repo: filenames use **date+slug** (e.g. `2025-03-13-principle-of-atomicity.md`). Date is `YYYY-MM-DD`; slug is kebab-case. Do not rely on wiki-style `[[links]]`; use standard markdown `[text](path/to/note.md)`.
1. **Body** — The idea in **your own words**. You may keep a short quote on top, but the main content should be your formulation; that improves understanding and recall and makes the Zettelkasten yours.
1. **References** — At the bottom: sources (e.g. citekeys) or links to other Zettels that inspired the note. If it's your own thought, no reference is required.

Use a **creation-date tag** with a hash in the form **#YYYY/MM/DD** (e.g. `#2025/03/13`). Systems that support hierarchical tags can then filter by year, year-month, or full date.

Prefer **knowledge** over raw **information**: add context and relevance. When unsure if something is worth a note, lean toward writing it (within your time constraints); you cannot know in advance which notes will matter later.

______________________________________________________________________

## When to Start a New Note

- **Existing notes on the same topic**: If one note already contains what you have, add the new detail there and link. If several notes roughly match, consider one new note that compiles and comments, plus links both ways. If the new idea doesn't fit existing notes, create a new note and reuse existing keywords/tags.
- **Note too big**: When extracting from a note takes too long or the note clearly contains more than one thought, split. Often the result is three notes: two for the extracted ideas, one that connects them and keeps context. After splitting, leave a trail: e.g. the original note links to the new ones so future browsing still works.
- **Link context**: If you didn't explain why you linked, splits can make old links confusing. Prefer explicit link descriptions so splits don't break meaning.

______________________________________________________________________

## Building Blocks of the System

- **Inbox** (`inbox/`): Quick captures and rough ideas. Process into permanent notes in the main Zettelkasten folder; delete or archive once merged. Do not leave processed material in the inbox indefinitely.
- **Archive**: The single trusted place for permanent notes. Only notes live here; no shoes, no project artifacts—just the hypertext of thoughts.
- **Reference manager**: External (e.g. BibDesk). References and citekeys live there; Zettels point to them. Treat your own finished texts like external sources: if you discover something while writing, capture it as a Zettel and link it; don't rely only on the draft.

Finished texts (articles, books) are **outputs** of the system, not part of it. When writing, use outlines and paste/link from Zettels; new insights during writing should become Zettels and be linked.

______________________________________________________________________

## Knowledge Management (Deeper)

### Layers of evidence

Notes can reflect different **layers of evidence** (from raw to synthesized). Keeping them distinct improves rigor and maintainability:

1. **Phenomenon / data description** — What was actually observed or stated (patterns, conditions, study design). Stick to what you can point to; avoid interpreting here.
1. **Interpretation** — Why you think it is so; theories, causality, meaning. This layer "breaks" more often and needs maintenance; primary sources matter.
1. **Synthesis** — Building blocks combined into a bigger picture; models, conclusions, practical application. This is the bridge toward writing.

Either a note belongs to one layer (and links to notes in other layers), or a single note is explicitly divided into these layers. Don't mix phenomenon and interpretation without labeling. When reading secondary literature, check primary sources when it matters; don't trust "facts" that aren't traced to primary literature.

### Why your own words and interpretation matter

**Information is not "in" the text.** Your brain filters and interprets; what you retain is your construction. Storing original quotes or PDFs does not by itself increase knowledge. Capture **your thoughts and interpretation** in the Zettel so you can rely on the note later without re-reading the source. Notes in your own voice are easier to work with and remember; they become the durable part of the system.

### Extend mind and memory; surprise

The archive extends your mind when it has (1) **permanent storage** (notes you can return to) and (2) **connections** (links so you can surf). The goal is not just retrieval but **surprise**: when you search or follow links, you should sometimes find something you didn't expect. Non-obvious connections are especially valuable for thinking and writing. Design for this: many links, explicit link context, and a habit of connecting so the web can "talk back."

### Learning: coverage, practice, insight

- **Coverage** — Get through material efficiently (skim, mark, then read in depth where it matters). Good reading technique; not part of the Zettelkasten itself but feeds it.
- **Practice** — Write notes in your own words; rephrase and elaborate. If you get stuck, you've found a gap; return to the source. Writing the note is feedback on your understanding.
- **Insight** — Integrate new notes into the existing web. Link to related notes; form concept-based notes rather than slavishly following the source's structure. Connections create lasting knowledge.

### Knowledge cycle (short cycles)

Keep the cycle **short** and iterative: research → read → take notes & link → write (e.g. add to an outline or draft). Repeating short cycles beats one long "research everything then write" phase. You get faster feedback, avoid the collector's fallacy, and keep a clear view of the project. Time-box research (e.g. 1 hour), then process fully before the next research block. Breaks and task switches help the brain consolidate; don't fear stopping and resuming.

### From reading to Zettels (digital workflow)

If you don't use paper reading notes: **collect** (highlights, quick captures, or inline notes in an inbox or temp file), then **process** in batches. When processing: (1) cluster by concept or topic, not necessarily by the source's order; (2) write one Zettel per atomic idea, linking to related Zettels; (3) start with a general note per cluster and branch into details with links. Orthogonal organization (e.g. by concept or index) is often more useful than mirroring the book's structure.

### Identity and stable links

Each Zettel needs a **stable, unique identifier** so other notes and outlines can refer to it. In this repo the filename is that ID: use **date+slug** (e.g. `2025-03-13-principle-of-atomicity.md`). Prefer identifiers that don't depend on a specific app (e.g. plain markdown links by path). Stable IDs make the archive a long-lived hypertext: you can move or rename files with a consistent scheme and still resolve links.

### Kinds of ties between notes

- **Direct links** (strongest) — Explicit references with context. Use these as the main way to connect.
- **Tags/keywords** (weaker) — Indirect grouping; notes share a tag but don't need to "know" each other. Prefer object tags for precise retrieval.
- **Sort order / juxtaposition** — List order can suggest relatedness (e.g. by date or by title). Be aware that UI order influences how you read; use it consciously if at all.

Folgezettel (note sequences by position/ID hierarchy) are one way to create ties on paper; in a digital system, **explicit links with context** are preferred. The important thing is leaving "breadcrumbs" for your future self—links and tags that make sense when you return.

______________________________________________________________________

## Structure Over Time

Structure **emerges**; don't design it all up front.

- **Bottom layer**: Content notes (single thoughts, linked).
- **Middle layer**: **Structure notes** — "notes about notes," e.g. tables of contents or hub notes that group and order other notes. They add overview without forcing one fixed hierarchy.
- **Top layer**: Main structure notes (and optional double-hash tags) that structure whole areas or link structure notes together.

Structure notes give **meaningful** order: the same note can appear in different "tables of contents" for different purposes. Prefer this over a single global hierarchy (e.g. strict Folgezettel-style trees). Folders and project buckets limit cross-linking; the Zettelkasten is one connected web.

______________________________________________________________________

## Buffer Notes (Project Staging)

For ongoing or future projects, use **buffer notes**: notes that list other notes (by ID/title + optional context) that you intend to use for a specific project (e.g. a book or article). They buffer the gap between "note production" and "assignment to a project" and help you avoid losing track of unincorporated material. They are intentionally less structured than structure notes; their role is staging, not hierarchy.

______________________________________________________________________

## Writing (Deeper)

### Separate research and writing

Do **research and writing in separate phases** where possible. Use the Zettelkasten as the place for research (notes, links, structure notes); when you write, pull from the archive instead of switching constantly between reading and drafting. That way you can focus on one mode and still let them reinforce each other: new notes feed the draft, and the draft's outline guides what to research next.

### Ease into writing: outline first, then compile

1. **Get an overview** — Query the archive (search, tags, structure notes) to see what you have on the topic.
1. **Create an outline** — Plan the text as a hierarchy (e.g. full-sentence items). This is the skeleton; you're not writing prose yet.
1. **Attach notes to the outline** — Assign Zettels (by reference/link or ID) to outline items. Gaps show where you need more research.
1. **Paste note contents** into the outline to build a first draft. Then **fill gaps**, **rewrite**, and make the text coherent. Get the first draft done quickly; edit later.

Most of the "writing" is done in advance in the form of notes and links; drafting becomes compiling and rewriting.

### Directional vs indirectional work

- **Indirectional** — Feed the Zettelkasten without a specific project: read, take notes, link. No immediate use required; the archive grows and may later feed many projects.
- **Directional** — Work toward a specific text: attach new Zettels to an outline or buffer note for that project so the draft grows as you research.

Both are valid. You can also do mostly indirectional work and still **attach new Zettels to outlines** when they fit: scan your outlines (or buffer notes) and link the new note to the relevant project. Books and articles can "emerge" when an outline has enough linked notes to become a manuscript.

### Outlines as structure or buffer

Outlines can live **inside** the archive (as structure notes or dedicated outline files). Use them to hold references to Zettels (by path or ID); move and cluster those references until the order makes sense, then paste note contents to build the draft. Referencing by ID first (and pasting later) keeps the outline flexible and avoids tangling the draft with the live note archive. For many parallel projects, keep separate outlines or buffer notes (active, inactive, finished) so every new Zettel can be assigned to one or more projects.

### Where writing ideas go

Don't rely on a traditional task list for "write chapter 1." Instead, put **writing ideas and plans** in the Zettelkasten: e.g. a short note with a rough plan, or an outline file that starts as a few bullets and grows. Vague ideas ("a book about X") and concrete plans ("sections: A, B, C") both fit. Over time, outlines and buffer notes become the project; when an outline has enough linked notes, replace refs with pasted content and you have a first draft. This keeps creative work in the knowledge system and supports many concurrent projects (active, inactive, future).

### Trust the process

The benefit is in the work of connecting, interpreting, and rephrasing—not only in the final text. The process improves thinking and memory; the archive is an extension of mind and memory because it mirrors associative, non-linear thought. Draft early and often; short knowledge cycles and iterative writing reduce anxiety and improve decisions about what to read and note next.
