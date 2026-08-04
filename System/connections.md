# Connections

This is the live source and connection registry for the Insider CSM Work OS. Record exact account or workspace scope, approved route, permission boundary and a successful live test. Never store secrets.

## Status meanings

- **Ready:** authenticated and successfully tested for the stated scope.
- **Setup required:** intended but not yet authenticated or tested.
- **Optional:** add only when the capability is needed.
- **Unavailable:** blocked, disabled or unsupported.

## Registry

| Connection or source | Purpose | Account or workspace | Status | Approved route | Allowed without confirmation | Confirm before | Last verified | Notes |
|---|---|---|---|---|---|---|---|---|
| CSM Scorecard Google Sheet | Canonical structured OKRs, KPIs, account roll-up and advocacy targets | Verify exact Insider Workspace account | Setup required | Account-scoped Google Workspace route | Read after a successful live test | Writing values or formulas; sharing; permission changes; deleting tabs or files |  | Add the exact Sheet ID and link after creation; see [[CSM Scorecard]] |
| Official commercial system | Contractual, commercial and renewal authority | Verify exact workspace | Setup required | Approved company route | Read after approval and a live test | Any write or lifecycle change |  | The Sheet may summarise but must not silently replace this authority |
| Slack | Decisions, commitments and discussion evidence | Verify exact Insider workspace | Setup required | Approved Slack route | Search and read after a successful live test | Sending, editing, scheduling or configuration changes |  | Preserve stable message references |
| Google Calendar | Meeting evidence and preparation | Verify exact Insider account | Setup required | Approved account-scoped route | Search and read after a successful live test | Creating, moving, responding to or cancelling events |  | Preserve timezone and response state |
| Gmail | Email evidence and drafting | Verify exact Insider account | Setup required | Approved account-scoped route | Search, read and draft after a successful live test | Sending, deleting, moving or changing labels unless separately approved |  | Keep source messages as evidence |
| Granola | Meeting notes and summaries | Verify exact account | Setup required | Approved Granola route | Search and retrieve after a successful live test | Recording, sharing, deleting or automatic canonical writes |  | Meeting summaries are evidence, not automatically current truth |

## Rules

1. A documented route is not Ready until a real read succeeds.
2. Keep each account and workspace scope explicit.
3. Separate read permission from write permission.
4. Confirm external sends, deletes, shares, permission changes and writes.
5. Never store passwords, API keys, tokens, cookies, OAuth codes or secret-bearing URLs.
6. Update `Last verified` only after a real live test.
7. Keep metric definitions and source ownership in the Google Sheet's `Definitions & Sources` tab.
