# Support ticket triage

Your queue manager opens the morning’s tickets already sorted: each one with a category, a priority and a route, and the reason for all three in a line. The tickets that cannot wait sit at the top, stopped for a person to decide.

*Workflow template · Customer support and service · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/support-ticket-triage/)*

## The outcome

The queue is read before anyone picks from it. Every new ticket has a category, a priority, a route and one line saying why, all taken from your own written rules. Duplicates are tied to the ticket they repeat. Known issues are matched to the answer you have already posted. Three customers describing the same fault in three different ways show up as one pattern, not three tickets.

Triage stops where judgment starts. A security report, an outage, a customer who says they are leaving: each goes to the top of the sheet with the facts and the rule it met, and the assistant goes no further with it. The queue manager decides who is called. Your agents start the day on the right ticket, and the urgent one is seen in minutes instead of being found at lunch.

## Who starts the work, and when

The queue manager or the agent on triage duty starts it: at the start of a shift, after a weekend, or whenever the unassigned queue has grown past what one person can read carefully. They export the new tickets, run the workflow template, and check the sheet before anyone acts on it.

The queue manager accepts or changes each line, assigns the tickets in the support system, and decides every escalation. The assistant assigns nothing, answers no customer and changes no ticket.

## What they supply

- **The queue export.** The new or unassigned tickets as rows: ticket number, when it arrived, customer, subject, the full message and how many replies have gone out.
- **Your triage rules.** Your categories, what each priority means and its first-reply target, which team takes what, and the conditions that make a ticket an escalation.
- **Your known issues.** The current list, each with its number and the workaround you have posted.
- **The time of the export and your working hours,** so reply targets can be counted.

## What comes out

One triage sheet in a fixed order:

1.  **Stopped for a decision.** Each ticket or group that met an escalation condition: the condition, who is affected, since when, what is known, what is not, and who your rules say decides.
2.  **Ready to route.** One line per ticket: category, priority, route, when the first reply is due, and the reason.
3.  **Duplicates and known issues.** Which ticket repeats which, and which known issue each match rests on.
4.  **Could not be triaged.** Any ticket the rules do not cover or the export does not show in full, with the question that would settle it.

Good looks like this: the queue manager can check any line against the ticket and the rule in under a minute, and every ticket in the export appears on the sheet exactly once.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Customer support and service](https://fullypowered.ai/functions/customer-support-and-service/): the first read of the queue, done the same way on every shift.
- [Software technology](https://fullypowered.ai/industries/software-technology/): faults, integrations and account questions arrive mixed together, and one release can fill the queue with the same problem.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/): order, delivery, refund and payment tickets arrive in volume, and a checkout fault hides among them.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/): the queue has outgrown the one person who used to read every ticket.

## What has to change for your company

- **Write the rules down.** Your categories, your priority definitions with their reply targets, and your routes. The workflow template applies your rules; it does not bring its own.
- **Name the escalation conditions and who decides each.** Which conditions stop a ticket, and the role that takes it from there.
- **Keep the known-issue list current,** with the posted workaround beside each issue.
- **Decide what the export may contain.** Which columns leave the support system, and which customer details are removed first.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini. Decide which exports the assistant may read.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 9 November 2026. It was tried on its invented example on 9 November 2026 in four runs; the record of the last is published with it, and lists the small edits made afterward that have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past day’s queue your queue manager already knows, plus hard cases written in advance: a security report worded as a how-to question, the same fault in three tickets, a customer writing twice, a ticket your rules do not cover. The queue manager checks every line against the ticket. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 9 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 9 November 2026. The record is in [TRIAL.md](TRIAL.md).
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

- [SOP exception capture](https://fullypowered.ai/workflow templates/sop-exception-capture/)
- [Pilot acceptance-test preparation](https://fullypowered.ai/workflow templates/pilot-acceptance-test-preparation/)
- [Customer reply drafting](../customer-reply-drafting/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
