# Support escalation brief

When a support case must move to a specialist or manager, the support lead gets one brief: the customer's impact, a dated timeline from the ticket history, the evidence, the fixes tried, the workaround in place and the decision needed. Nothing goes to the customer.

*Workflow template · Customer support and service · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/support-escalation-brief/)*

## The outcome

The person who receives an escalated case can act on it without reading the whole thread or asking the support team to explain it again. The brief says who is affected and how, in what order things happened, what proof exists and what is missing, what has already been tried, how the customer is coping in the meantime and exactly what the receiving owner is being asked to decide.

Every claim in it is labelled. What the customer says, what the team has confirmed and what nobody has checked are kept apart, and where two accounts disagree the brief shows both and settles neither. Promises already made to the customer are listed so the receiving team does not break them by accident.

The support lead reads the brief before it goes, chooses the destination under the company's escalation policy and confirms who will own the case. The AI assistant sends nothing, changes no ticket and writes nothing for the customer.

## Who starts the work, and when

The support agent holding the case, or the support lead, starts it when a request cannot be resolved at the front line and the policy says it should move on: a fault that keeps recurring, a customer at risk of leaving, a question only a specialist can answer. It is run once per case, at the moment of hand-over, and can be run again if the case is escalated a second time.

The support agent exports the ticket's history, adds the ticket's details and the company's escalation policy, and runs the workflow template. The support lead reads the brief, corrects it, picks the destination and confirms the receiving owner. People then pass it on in the ticket system or the team's usual channel.

## What they supply

- **The ticket history export.** One row per entry on one ticket: date, who, what kind of entry (customer message, team reply, internal note, status change, assignment, automatic) and the text.
- **The ticket's details.** Ticket number, customer, priority, current status, owner and plan if the company uses plans.
- **The escalation policy.** The destinations, the criteria for each, and what a brief must carry.
- **Related reports,** if there are any: other tickets or known issues that look similar, one line each.
- **The support lead's choice,** once made: the destination and the receiving owner.
- **The date of the brief.**

## What comes out

One internal brief in a fixed order: the case, impact, timeline, evidence, fixes already tried, current workaround, promises and open requests, conflicts and gaps, related reports, a check against the policy's criteria as written, the decision needed and the questions the support lead should settle before it goes. Each section says what it prints when it has nothing to report.

Good looks like this: the receiving owner can check any line against the ticket in a minute, nothing is stated more strongly than the history supports, and the decision needed is a question the owner can answer.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Customer support and service](https://fullypowered.ai/functions/customer-support-and-service/): the hand-over that decides whether a specialist starts from the facts or from scratch.
- [Software technology](https://fullypowered.ai/industries/software-technology/): faults reach engineering with a thread, a screenshot and a guess about the cause.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/): order, delivery and payment problems move to operations or a supplier contact.
- [Professional services](https://fullypowered.ai/industries/professional-services/): a client's unresolved request goes to the partner or practice manager who owns the relationship.
- [Hospitality](https://fullypowered.ai/industries/hospitality/): a booking, supply or billing problem reaches the manager with the story of what the guest or customer has already been told.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/): the front line now outnumbers the specialists, and every escalation costs them time unless the brief is complete.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/): hand-overs have been done by habit and by forwarding emails, and what the owner receives varies by who sent it.

## What has to change for your company

- **Write your escalation policy down.** Destinations, the criteria for each, how fast a receiving owner must confirm, and what a brief must carry.
- **Decide who chooses the destination.** The template assumes the support lead and leaves the choice to them.
- **Map your export.** The default column headings, the entry types your ticket system uses, and which customer details are removed before the history leaves the system.
- **Decide what counts as impact** for your customers: lost trade, missed deadlines, a customer saying they may leave.
- **Say where the brief goes** and who may read it. It is internal and is not for the customer.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply; it needs no connection to your ticket system.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026; the record is published with it. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a few past escalations your support lead remembers well, plus hard cases written in advance, each with the expected result: an export whose headings do not match, a customer claim the team never confirmed, two accounts of the same event, a case that meets the criteria for two destinations, a thread that holds a password. The support lead checks every date and statement against the ticket before anyone relies on the brief. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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
- [Stale ticket sweep](../stale-ticket-sweep/)
- [Customer reply drafting](../customer-reply-drafting/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
