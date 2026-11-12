# Stale ticket sweep

Once a week the support lead gets one sheet of what the queue is hiding: tickets with no real activity past their limit, tickets left waiting on the customer with the three ways out of each, likely duplicates, and each person's load weighed by size and age. A person makes every move.

*Workflow template · Customer support and service · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/stale-ticket-sweep/)*

## The outcome

The week's plan starts from the whole queue, not from whatever arrived last. Every open ticket is accounted for exactly once. The ones past their limit are listed with the longest overdue first, each with the date of its last real activity and one question for the lead. A ticket the support system updated by itself does not pass for one a person worked on.

Each ticket left waiting on the customer too long comes with the three ways to resolve it: another reminder, a named owner in the team who checks for the answer, or closing it. Beside them is the way the team's own rules point to. Tickets whose customer has already answered, while the status still says waiting, get their own list. Likely duplicates are paired, with the reason. Workload is shown as a load, each ticket counted by its size and its age with the arithmetic beside it, so the lead sees who holds the hardest and oldest work as well as who holds the most tickets.

The sweep proposes; the lead decides. The AI assistant closes, merges, reassigns and answers nothing, and changes no ticket.

## Who starts the work, and when

The support lead, or whoever runs the queue day to day, starts it once a week at a fixed time, usually on Monday morning before the team plans its week. It also earns a run before a holiday, when someone goes on leave, or after a busy spell.

The lead exports the open tickets, runs the workflow template and reads the sheet. Each decision on it is the lead's: who chases what, which tickets are closed, linked or merged, and whether any work moves between people. The changes are then made in the support system by the people who own them.

## What they supply

- **The open-ticket export.** One row per open ticket: number, subject, customer, status, assignee, when it was created, when it entered its current status, the team's last note or reply and the customer's last reply. Contact, priority, size, reminders sent and the last update of any kind help when the support system has them.
- **The sweep settings.** How the team's statuses group together, the limit for each group, the reminder and closing rules for tickets waiting on the customer, the duplicate window, the size points and age factors, and the working days and closed days. Sensible defaults are written into the template for anything the team has not set.
- **Who is on the team this week,** and who is away.
- **Last week's sheet,** when there is one, so tickets that were on it are marked.

## What comes out

One sheet in a fixed order:

1. **Stale.** Tickets past the limit for their status, longest overdue first.
2. **Waiting on the customer too long.** Each with the three ways to resolve it and the one the team's rules point to.
3. **Status out of date.** Tickets still marked as waiting although the customer has replied.
4. **Likely duplicates and related tickets,** in pairs, with why.
5. **Workload across the team.** Each person's weighed load with the arithmetic, heavy and light marks, who is away, and one observation.
6. **Could not be placed.** Any ticket whose status the settings do not cover.
7. **From last week's sheet,** the tickets no longer open.

Good looks like this: the lead can check any line against the export in under a minute, the counts at the top add up to the number of open tickets, and nothing has been changed anywhere.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Customer support and service](https://fullypowered.ai/functions/customer-support-and-service/): the weekly look at the whole queue that daily ticket work never gives.
- [Software technology](https://fullypowered.ai/industries/software-technology/): faults wait on developers, set-up questions wait on customers, and both drift out of sight.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/): returns and delivery problems wait on carriers and suppliers, and customers write twice when they hear nothing.
- [Professional services](https://fullypowered.ai/industries/professional-services/): a small service desk where one experienced person ends up holding the hardest work.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/): the queue has grown past the point where the lead can keep every ticket in mind.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/): the queue has habits nobody questions, such as a waiting status where tickets stay for months.

## What has to change for your company

- **Map your statuses.** Write down which of your support system's statuses mean the team is working, waiting on the customer or waiting on someone else, such as a supplier or a carrier.
- **Set your limits.** How many working days without real activity each group may go before it is listed.
- **Write your waiting rules.** How many reminders you send, and when a ticket may be closed without an answer, always once a person agrees.
- **Decide how to weigh work.** Use your support system's size or effort field if it has one, and your own age bands.
- **Check the export.** Its column headings, and which customer details are removed before it leaves the support system.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply; it needs no connection to your support system.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026, and the record of that run is published with it. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three past weeks your support lead remembers well, plus hard cases written in advance, each with the expected result: an export whose headings do not match, a ticket touched only by an automatic update, a customer who replied while the status still says waiting, a status your settings do not cover, a ticket that has used up its reminders. The lead checks every date and figure against the export before anyone relies on the sheet. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the workflow template drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related workflow templates

- [Support ticket triage](../support-ticket-triage/)
- [Customer reply drafting](../customer-reply-drafting/)
- [Support service level definition](../support-service-level-definition/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
