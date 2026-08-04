---
type: note
topics:
  - agent-friendly
  - obsidian
  - markdown
organisations: []
people: []
projects: []
created: 2026-08-02
updated: 2026-08-02
---

# Principles of an Agent-Friendly Obsidian Vault

An agent-friendly vault is first a human-readable vault. Files should be easy to identify, interpret, link and update without hidden conventions.

The contract rests on three principles:

1. **Every file has an obvious purpose.**
2. **Every relationship has explicit meaning.**
3. **Every important claim has an identifiable owner and source.**

## 1. One file, one primary subject

A file should represent one identifiable Organisation, People, Project, Meeting or Note subject. Do not combine several unrelated subjects into one long document merely because they arrived together.

Meeting records may contain several topics because they are evidence of one event. Store them in `Meetings/` and move durable current state into the record that owns it.

## 2. Give every file a predictable identity

Use the matching Template and a unique, descriptive filename. People records use `Templates/People.md`, and Meeting records use `Templates/Meeting.md`. The `type` property should come from the controlled starter set:

```yaml
type: organisation | people | project | meeting | note
```

Use `YYYY-MM-DD` for dates. Use the same property name for the same meaning across every file.

For this small starter, a unique filename and controlled `type` are sufficient. Add immutable IDs only when external synchronisation, duplicate names or larger-scale automation creates a proven need.

## 3. Put the answer near the top

A reader or agent should understand a file without reading the full history. The first screen should answer:

- What is this?
- Why does it matter?
- What is its current state?

Keep the summary or current context near the top. Put deep detail, evidence and history below it.

## 4. Use consistent headings for each record type

Files created from the same Template should use the same broad structure. Consistency helps people scan and helps agents update the correct section without rewriting unrelated content.

Do not force every Note into an identical shape. Notes are the flexible evidence layer, while Organisations, People, Projects and Meetings need more predictable sections.

## 5. Separate current truth from history

Do not bury the current position inside a chronological journal.

```markdown
## Current position

The launch remains planned for October and is waiting for security approval.

## Updates

- 2026-08-02: Security review moved to final approval.
- 2026-07-14: Launch moved from September to October.
```

Current state belongs near the top. Dated changes and source evidence belong below it.

## 6. Give each fact one canonical owner

| Fact | Canonical owner |
|---|---|
| Organisation identity and context | Organisation file |
| People identity, role and working context | People record in `People/` |
| Project outcome, status and current position | Project file |
| Meeting event, attendees, notes and decisions | Meeting record in `Meetings/` |
| Research or decision evidence not tied to a Meeting | Note file |
| Structured CSM OKRs, KPIs and advocacy targets | Linked Google Sheet described in `CSM Scorecard.md` |
| Shared or leadership work not owned elsewhere | `Tasks.md` |

Other files should link to the owner rather than copying its current value. A completed task does not automatically prove that a Project outcome was achieved.

## 7. Make relationships meaningful

Prefer named properties such as `organisations`, `people` and `projects` over an unexplained collection of links. Explain important links in a sentence when the reason is not obvious.

Weak:

```markdown
Related: Client and Launch Project
```

Stronger:

```markdown
The launch decision was agreed with the client and applies to the Launch Project.
```

Do not impose a minimum number of links. Meaningful links are better than a dense but ambiguous graph.

## 8. Use exact links and avoid imaginary nodes

Every internal link should resolve to one intended file. Use a link only when the target deserves its own maintained record.

If `industry: retail` is merely a classification, keep it as a controlled value. Do not create a nearly empty “Retail” note just to make the property look like a graph.

## 9. Preserve evidence and uncertainty

Distinguish between:

- source evidence;
- interpretation;
- current accepted state;
- a human-approved decision.

Do not silently merge conflicting claims. State what is uncertain, preserve the competing evidence and ask for clarification when the current owner cannot be updated safely.

## 10. Use controlled vocabulary and plain language

Use the status values defined by the matching Template. Do not create near-duplicates such as `in progress`, `in-progress`, `ongoing` and `underway` unless they deliberately mean different things.

Prefer complete, plain-language statements over shorthand, unexplained acronyms, emoji-only statuses or meaning encoded solely through colour.

## 11. Keep files bounded and scannable

Use:

- one-sentence summaries;
- short sections;
- bullets for discrete facts;
- tables only for genuinely tabular information;
- links to deep detail rather than copying it everywhere.

Length alone is not the problem. Mixed purpose and unclear ownership are.

## 12. Make agent writes narrow and verifiable

Before an agent changes the vault, it should:

1. Identify the exact target file and its canonical responsibility.
2. Read the matching Template and relevant evidence.
3. Check for an existing matching record.
4. Preserve unrelated content and uncertainty.
5. Apply the smallest sufficient change.
6. Read the changed file back and verify frontmatter and links.
7. Keep external sends and system writes behind separate explicit approval.

Never store passwords, tokens, API keys or secret-bearing links in vault notes.

## Minimum mechanical checks

A growing vault should eventually be able to detect:

- malformed frontmatter or dates;
- invalid record types or statuses;
- broken or ambiguous links;
- relationship fields pointing to the wrong kind of record;
- duplicated canonical records;
- current-state sections missing from operational records.

Do not add a validator before the starter needs one. The immediate goal is a small, predictable structure that remains easy to maintain manually.
