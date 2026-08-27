Generate a **Daily Status** summary of completed work for standup or async updates.

## Rules

- **Scope:** Describe work done **today** and **yesterday**. If it's Monday, include **only today**.
- **Tone:** Use **non-technical**, outcome-focused language (what was delivered, not implementation details).
- **Structure:**
  - Group related work under one heading (ticket/issue ID when applicable, e.g. `CRM-38 Client list`; otherwise a short product area).
  - Each heading is a **top-level bullet**. Accomplishments go under it as **indented sub-bullets**.
  - Do not put a standalone accomplishment as both a heading and a sub-bullet. The heading names the area; sub-bullets say what changed.
  - Each sub-bullet **starts with a past-tense verb** (Added, Fixed, Shipped, Enabled) and answers **what was done**. Do not start with nouns, “people can…”, or a status sentence.
- **Deduplicate:**
  - List each outcome **once**. Merge overlapping bullets into a single sub-point.
  - Do not repeat the heading in the first sub-bullet.
  - Do not list the same work under both Today and Yesterday. If it shipped yesterday, it belongs only in Yesterday. Today is only new progress since then.
  - Skip merge-only, rebase-only, or chore work that did not change user-facing outcome.
- **Format:** Plain markdown. Bold the title **Daily Status**, section labels **Today** and **Yesterday**, and each top-level point. Sub-bullets stay unbolded.

## Example

```md
**Daily Status**
**Today**

- **CRM-38 Client list**
  - Moved shared UI, utils, and constants into the monorepo shared package
- **CRM-87 Client details**
  - Added a client details modal with tabs
  - Let admins adjust SMS usage, manage subscriptions, and refresh the Mindbody token
- **CRM-91 Settings**
  - Added access control so admins and support see only the features they should

**Yesterday**

- **CRM-70 Invoices**
  - Added invoice deletion with a warning if payments already exist
```
