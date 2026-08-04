# Welcome to the CSM OS

[Watch the Work OS video tutorial](https://www.youtube.com/watch?v=EcAz6lklq8s&t)

This is a simple Obsidian operating system for Customer Success teams.

Getting started with Obsidian and building an agent-friendly vault can be difficult, so this repository provides a consistent starting point. It follows the [[Principles of an Agent-Friendly Obsidian Vault]] while adapting the original [Work OS](https://github.com/jonathanlewell/work-os) for CSM work.

The idea is to keep useful customer context in linked Markdown files. Those links give people and AI agents such as Claude or ChatGPT enough structured context to understand accounts, stakeholders, meetings, workstreams and tasks.

Use this as a starting Template. Keep what helps, refine it as your team learns, and avoid adding complexity before it is needed.

## The folders

| Place | Use it for |
|---|---|
| `Organisations/` | One working record per customer, including objectives, technology stack, workstreams and battle plans |
| `People/` | Customer stakeholders and the context needed to work with them well |
| `Meetings/` | Customer meeting records with purpose, attendees, notes and follow-up |
| `Notes/` | Research, playbooks, product knowledge, processes and other reusable information |
| `System/` | Small operational files that explain how the vault works or connects to other services |
| `Templates/` | One simple starting format for each record type |
| `Tasks.md` | All CSM tasks, leadership commitments and items waiting on other people |

In most cases, information should live in one of these places:

- Put a customer account in `Organisations/`.
- Put a customer stakeholder in `People/`.
- Put a customer check-in or other meeting in `Meetings/`.
- Put reusable research, guidance or documentation in `Notes/`.
- Put every CSM task in [[Tasks]]. Denote tasks blocked on another person with `waiting`.

There is deliberately no `Projects/` folder. Current customer initiatives are maintained as rows in the **Workstreams and battle plans** table inside the relevant Organisation record.

You may eventually outgrow this structure. That is fine, but add a folder or record type only when a repeated need proves it is necessary, then update the Templates and guidance to match.

## The Templates

The `Templates/` folder contains the approved starting format for each record type:

- [[Templates/Organisation]]
- [[Templates/People]]
- [[Templates/Meeting]]
- [[Templates/Note]]

Each Template uses consistent frontmatter and predictable sections. This makes the vault easier for people to scan and easier for AI agents to interpret reliably.

When creating a record:

1. create a Markdown note in the correct folder;
2. apply the matching Template;
3. fill in what is known;
4. preserve blanks or uncertainty rather than guessing;
5. link the relevant Organisation, People and Meeting records.

## How to use the vault day to day

### Create or update a customer

Create one Organisation record for each customer. Use it as the current working account view for:

- ownership and commercial context;
- customer objectives and current status;
- technology stack;
- stakeholders;
- active workstreams and battle plans.

Do not create a second record for each workstream. Update the table in the Organisation instead.

### Record a meeting

Create a Meeting record using [[Templates/Meeting]]. Link the customer and attendees in the frontmatter, then capture the purpose, agenda, notes, durable account changes and follow-up.

After the meeting:

1. update the Organisation when the account's current state or workstream changed;
2. update a People record when stakeholder context changed;
3. add the resulting tasks to [[Tasks]];
4. mark dependencies on other people with `waiting`.

### Manage tasks

Use [[Tasks]] as the single task list:

- `Now` for the three immediate priorities;
- `This week` for the rest of the active week;
- `Waiting` for tasks blocked on another person or dependency;
- `Later` for work that is not yet active;
- `Completed` for recently finished items.

Link tasks to the relevant Organisation, person or Meeting where that context is useful.

## How to use the vault with Claude or GPT

You can maintain the vault by hand or work with an AI agent. The same rules apply either way: use the correct Template, update the canonical record and preserve uncertainty.

Point Claude Code, Codex or another file-capable agent at the root of the vault. You may also ask it to install [Obsidian skills](https://github.com/kepano/obsidian-skills) so it can work with Obsidian Markdown and links more reliably.

You can then make natural-language requests such as:

> Create a Meeting record for my customer-success check-in with John Dell at Dell Computers. Use the Meeting Template, link the customer and stakeholder, update the Dell Computers workstream if the notes support a change, and add the follow-up tasks to Tasks.md.

The root `AGENTS.md` and `CLAUDE.md` files tell compatible agents how this particular vault should be handled.

## Example data

The repository includes a connected fictional example:

- [[Dell Computers]]
- [[John Dell]]
- [[2026-01-15 Dell Computers Customer Success Check-in Meeting|Dell Computers Customer Success Check-in Meeting]]

Explore the links between them and [[Tasks]] to see how the system fits together.

The Dell Computers scenario and John Dell are fictional training examples. They do not describe a real Dell Technologies relationship or person. Replace or delete them before adding real customer data.

## First use

1. Open this repository as an Obsidian vault.
2. Open **Settings → Core plugins** and enable **Templates**.
3. Open **Settings → Templates** and set **Template folder location** to `Templates`.
4. Review [[Tasks]] and its `Now`, `This week`, `Waiting`, `Later` and `Completed` sections.
5. Create an Organisation using [[Templates/Organisation]].
6. Create stakeholder records using [[Templates/People]] and link their Organisation.
7. Create meeting records using [[Templates/Meeting]] and link the relevant Organisation and People.
8. Use [[Templates/Note]] for research, guidance, processes and reusable context.
9. If external services are connected, update [[System/connections|connections.md]] after a successful live test.

## How records connect

Use double brackets to link one record to another. Frontmatter links make important relationships explicit and easy for an agent to read.

```yaml
organisations:
  - "[[Dell Computers]]"
people:
  - "[[John Dell]]"
```

Links in the body explain why the relationship matters:

```markdown
[[John Dell]] is the day-to-day sponsor for [[Dell Computers]].
```

Link records when the target deserves its own maintained file. Do not create empty records merely to make the graph look busier.

## Working safely

- Treat the vault as confidential because it may contain customer and commercial context.
- Never store passwords, tokens, cookies, API keys or secret-bearing URLs.
- Official company systems remain authoritative for contractual and commercial facts.
- Preserve uncertainty rather than inventing missing information.
- Confirm before sending messages, deleting records, changing permissions or writing to external systems.

## Further guidance

- [[Principles of an Agent-Friendly Obsidian Vault]] explains how to keep records understandable and safe for people and agents.
- [[Recommended Connections]] explains the optional connection routes.
- [[System/connections|Connection Registry]] records which external services the vault can actually reach.

## Origin

The CSM OS is adapted from Jonathan Lewell's open-source [Work OS](https://github.com/jonathanlewell/work-os).
