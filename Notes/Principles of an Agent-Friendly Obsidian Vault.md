---
type: note
topics:
  - agent-friendly
  - obsidian
  - markdown
organisations: []
people: []
created: "2026-08-02"
updated: "2026-08-03"
---

# Principles of an Agent-Friendly Obsidian Vault

An agent-friendly vault is first a human-readable vault. Files should be easy to identify, interpret, link and update without hidden conventions.

## 1. One file, one primary subject

A file should represent one identifiable Organisation, person, Meeting or Note subject. Meeting records may contain several topics because they are evidence of one event.

This CSM OS deliberately does not use separate Project records. Current workstreams and battle plans remain inside the Organisation that owns the customer strategy.

## 2. Predictable identity

Use the matching Template and a unique, descriptive filename. The controlled record types are:

```yaml
type: organisation | people | meeting | note
```

Use `YYYY-MM-DD` for dates and the same property name for the same meaning.

## 3. Put the answer near the top

The first screen should explain what the record is, why it matters and its current state. Put history and deep evidence below the current position.

## 4. One canonical owner

| Fact | Canonical owner |
|---|---|
| Customer identity, health context and strategy | Organisation record |
| Customer workstreams and battle plans | Workstream table inside the Organisation record |
| Stakeholder identity, role and working context | People record |
| Meeting event, attendees, notes and decisions | Meeting record |
| Reusable research or decision evidence | Note file |
| Structured OKRs, KPIs and advocacy targets | Linked Google Sheet described in `CSM Scorecard.md` |
| Shared or leadership work not owned elsewhere | `Tasks.md` |

Other files should link to the owner rather than copying its current value.

## 5. Workstreams stay with the customer

Use one compact table in each Organisation:

```markdown
| Workstream or battle plan | Outcome | Status | Owner | Next milestone and date | Blocker |
|---|---|---|---|---|---|
```

Create one row per active initiative. Update that row when the current position changes. Put meeting evidence and deeper research in linked Meetings or Notes.

## 6. Separate current truth from history

Keep the current snapshot, health and workstream table near the top. Record dated material changes below them. Do not bury current state inside a chronological journal.

## 7. Make relationships meaningful

Use named properties such as `organisations` and `people`. Add links only when the target deserves its own maintained record. Do not create empty nodes merely to make the graph denser.

## 8. Preserve evidence and uncertainty

Distinguish source evidence, interpretation, current accepted state and human-approved decisions. Do not silently merge conflicting claims. Missing evidence means `Not assessable`, not automatically Red.

## 9. Controlled vocabulary and plain language

Use the status values defined by the matching Template or approved operating source. Avoid near-duplicate labels and unexplained shorthand.

## 10. Narrow and verifiable agent writes

Before changing the vault, an agent should:

1. identify the exact canonical owner;
2. read the matching Template and evidence;
3. check for an existing record;
4. preserve unrelated content and uncertainty;
5. apply the smallest sufficient change;
6. read the changed file back and verify frontmatter and links;
7. confirm before external sends or system writes.

Never store passwords, tokens, API keys or secret-bearing links in vault notes.

## Minimum checks

A growing vault should eventually detect malformed frontmatter, invalid record types or statuses, broken links, duplicated canonical records and missing current-state sections. Add stronger machinery only after a repeated failure proves it necessary.
