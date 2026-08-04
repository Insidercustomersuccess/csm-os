# Insider CSM Work OS

This is a lean, private Obsidian workspace for Customer Success account context, meeting evidence, customer initiatives and leadership preparation.

The system deliberately separates three jobs:

1. **Obsidian** holds customer strategy, battle plans, stakeholder context, meeting evidence and finite initiatives.
2. **Google Sheets** holds the structured CSM scorecard, calculations, filters, targets and team updates.
3. **Official company systems** retain their authoritative commercial, contractual and operational data.

Do not copy a value into several places. Link to the canonical source instead.

## Where information belongs

| Place | Use it for |
|---|---|
| `Organisations/` | One canonical working record per customer account, including its battle plan |
| `People/` | Customer stakeholders and relevant working relationships |
| `Projects/` | Customer initiatives with a clear finish line |
| `Meetings/` | Meeting evidence, decisions and commitments |
| `Notes/` | Playbooks, product knowledge, research, decisions and processes |
| `Tasks.md` | Shared or leadership commitments not already owned by another system |
| `CSM Scorecard.md` | Landing page and operating contract for the canonical Google Sheet scorecard |
| `System/connections.md` | Live connection and source registry, without secrets |
| `Templates/` | The approved starting shape for each record type |

## Canonical ownership

| Information | Canonical owner |
|---|---|
| Customer strategy, health context and battle plan | Customer Organisation record |
| Stakeholder role and relationship context | People record |
| Finite customer outcome | Project record |
| What happened in a meeting | Meeting record |
| Structured OKRs, KPIs and customer-marketing targets | Google Sheet linked from `CSM Scorecard.md` |
| Commercial or contractual facts | The approved official company system |
| Shared leadership commitment not owned elsewhere | `Tasks.md` |
| Connection route and permission boundary | `System/connections.md` |

## Core workflow

### After a customer meeting

1. Create a Meeting from `Templates/Meeting.md`.
2. Preserve decisions, commitments and uncertainty as evidence.
3. Update the Organisation only with durable, supported current-state changes.
4. Update relevant People or Projects when their owned state changed.
5. Add a task only when it is material and not already owned elsewhere.

### Weekly CSM review

Review accounts tier-first. For each selected account confirm:

1. health and renewal position;
2. current priority;
3. material change since the previous review;
4. blocker or leadership support needed;
5. next meaningful step and date.

Deep-dive exceptions rather than walking every green account.

### Weekly scorecard update

Use the Google Sheet for structured values and calculations. Check source freshness before judging performance. Missing evidence means `Not assessable`, not automatically Red.

## Google Sheet boundary

The Google Sheet should contain these tabs:

- `Dashboard`
- `Accounts`
- `OKRs`
- `KPIs`
- `Advocacy & Marketing`
- `Definitions & Sources`

Do not duplicate the Sheet's metric values in Markdown. Organisation notes may link to the relevant account row or source, while retaining the narrative battle plan.

## First use

1. Open this folder as an Obsidian vault.
2. Enable the **Templates** core plugin.
3. Set **Template folder location** to `Templates`.
4. Create the Google Sheet and record its link in `CSM Scorecard.md` and `System/connections.md`.
5. Create customer records from `Templates/Organisation.md`.
6. Add People, Projects and Meetings only when they provide useful maintained context.
7. Keep external sends and changes to official systems behind explicit approval.

## Privacy and safety

- This vault is backed by the private `Insidercustomersuccess/csm-os` GitHub repository.
- Never store passwords, tokens, cookies, API keys or secret-bearing URLs here.
- Preserve evidence and uncertainty rather than guessing.
- Confirm before sending messages, changing permissions, deleting records or writing to external systems.
- Do not add folders, record types or automation until a repeated need proves necessary.
