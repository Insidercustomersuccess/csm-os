# Insider CSM Work OS

This is a lean, private Obsidian workspace for Customer Success account context, battle plans, stakeholder relationships, meeting evidence and leadership preparation.

The system deliberately separates two jobs:

1. **Obsidian** holds customer strategy, workstreams, battle plans, stakeholder context and meeting evidence.
2. **Official company systems** retain their authoritative commercial, contractual and operational data.

Do not copy a value into several places. Link to the canonical source instead.

## Where information belongs

| Place | Use it for |
|---|---|
| `Organisations/` | One canonical working record per customer, including its current workstreams and battle plans |
| `People/` | Customer stakeholders and relevant working relationships |
| `Meetings/` | Meeting context, notes and follow-up |
| `Notes/` | Playbooks, product knowledge, research, decisions and reusable context |
| `Tasks.md` | All CSM tasks, shared or leadership commitments, and items waiting on other people |
| `System/connections.md` | Live connection and source registry, without secrets |
| `Templates/` | The approved starting shape for each record type |

There is deliberately no `Projects/` folder. Current customer workstreams and battle plans are maintained as rows inside the relevant Organisation record.

## Canonical ownership

| Information | Canonical owner |
|---|---|
| Customer strategy, health context, workstreams and battle plans | Customer Organisation record |
| Stakeholder role and relationship context | People record |
| What happened in a meeting | Meeting record |
| Reusable knowledge or evidence | Note file |
| Commercial or contractual facts | The approved official company system |
| CSM task, shared or leadership commitment, or waiting item | `Tasks.md` |
| Connection route and permission boundary | `System/connections.md` |

## Core workflow

### After a customer meeting

1. Create a Meeting from `Templates/Meeting.md`.
2. Preserve useful context, open questions and uncertainty in the notes.
3. Update the Organisation only with durable, supported changes to current state, workstreams or battle plans.
4. Update relevant People records when stakeholder context changed.
5. Add resulting CSM tasks to `Tasks.md`; denote dependencies on other people with `waiting`.

### Weekly CSM review

Review accounts tier-first. For each selected account confirm:

1. health and renewal position;
2. current priority;
3. movement across active workstreams;
4. material change since the previous review;
5. blocker or leadership support needed;
6. next meaningful step and date.

Deep-dive exceptions rather than walking every green account.

## Example data

A clearly fictional connected example is included:

- [[Dell Computers]]
- [[John Dell]]
- [[2026-01-15 Dell Computers Customer Success Check-in Meeting|Dell Computers Customer Success Check-in Meeting]]

The Dell Computers scenario and John Dell are fictional training examples. They do not describe a real Dell Technologies relationship or person. Replace or delete the records before adding real customer data.

## First use

1. Open this folder as an Obsidian vault.
2. Enable the **Templates** core plugin.
3. Set **Template folder location** to `Templates`.
4. Create customer records from `Templates/Organisation.md`.
5. Add People and Meetings only when they provide useful maintained context.
6. Keep external sends and changes to official systems behind explicit approval.

## Privacy and safety

- This vault is backed by the private `Insidercustomersuccess/csm-os` GitHub repository.
- Never store passwords, tokens, cookies, API keys or secret-bearing URLs here.
- Preserve evidence and uncertainty rather than guessing.
- Confirm before sending messages, changing permissions, deleting records or writing to external systems.
- Do not add folders, record types or automation until a repeated need proves necessary.
