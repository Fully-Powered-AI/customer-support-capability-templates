# Support service level definition

The support lead gets reply and resolution targets for every priority level, worked out from the team's own ticket history and the hours the team really has. Each target shows how often the team already meets it, and every gap comes back as a question for the lead to settle.

*Workflow template · Customer support and service · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/support-service-level-definition/)*

## The outcome

Your team's targets stop being a number someone liked the sound of. For each priority level there is a time for the first reply from a person and a time for resolution, each counted only in the hours that level is covered, each meant for a stated share of tickets, and each with a warning point at which an open ticket is raised to the lead. Every target sits beside the team's own record, so anyone can see where it came from.

The proposal is honest about what history cannot settle. A level with too few tickets gets no invented target. A target the lead wanted but the team does not yet reach is shown with how often it was met. A week where the work outgrows the hours, because of a busy spell or someone's leave, is named in advance. Each of these arrives as a question with its facts, and the lead decides.

These are internal targets for running the team. They are not a promise to customers, and the workflow template writes no customer-facing terms.

## Who starts the work, and when

The support lead starts it, or the owner where the owner runs support: when the team sets targets for the first time, and again when the team's hours, the product, the volume of tickets or the priority definitions change. A quarterly run on a fresh export keeps the targets current.

The support lead settles every question, approves the targets and names the person who sets them up in the support system. The AI assistant changes nothing in the support system and sends nothing.

## What they supply

- **A ticket export** of at least four full weeks: one row per ticket, with when it was created, its priority, when a person first replied and when it was resolved.
- **The priority definitions:** each level and what earns it.
- **The coverage note:** working hours, closed days, and which levels anyone watches outside working hours.
- **The roster:** each person's weekly hours for the queue once meetings and other duties are taken out, and the hours lost to leave or closed days in the weeks ahead.
- **Minutes per ticket:** the lead's estimate of the work one ticket takes at each level.
- **Any targets already in mind,** so they can be checked against the record.

## What comes out

One proposal in a fixed order: the levels and the hours each is counted in; the tickets left out and why; what the team achieves today at each level; the proposed targets with their basis and warning points; any wanted target the record does not reach; the capacity check for the weeks behind and ahead; the busy-period rule, or the question that sets one; the numbered decisions for the lead; and when to check again.

Good looks like this: the lead can trace any target to the export in a couple of minutes, every ticket is counted or listed, and nothing on the page could be mistaken for a promise to a customer.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Customer support and service](https://fullypowered.ai/functions/customer-support-and-service/): the targets the team works to every day, set from its own record.
- [Software technology](https://fullypowered.ai/industries/software-technology/): faults, set-up questions and billing problems arrive mixed together, and each needs its own clock.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/): order and delivery questions arrive in waves, and a seasonal peak tests targets the quiet months suggested.
- [Professional services](https://fullypowered.ai/industries/professional-services/): clients expect a reply from a person, and a small team's leave changes what it can keep up.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/): volume rises faster than the team, and yesterday's targets need checking against today's hours.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/): targets that live in one long-serving person's head should be written down and measured.

## What has to change for your company

- **Write your priority levels down,** with the names exactly as your support system records them.
- **Say when each level is covered:** working hours, closed days, and any level someone watches in the evening or at the weekend.
- **Check the export,** so that its first-reply column counts only replies written by a person, and decide which customer details are removed before it leaves the support system.
- **Set your own limits:** the share of tickets a target is meant for, the fewest tickets worth measuring, the steps targets are rounded to, the ceiling on load and the warning point.
- **Decide a busy-period rule** once the first proposal shows where you need one.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply; it needs no connection to your support system.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 9 November 2026. It was tried once on its invented example in Claude on 9 November 2026; the record of that run is published with it, and lists the small edits made afterward that have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past month your support lead knows well, plus hard cases written in advance: an export whose first-reply column also holds the messages your support system sends by itself, a ticket created on a Friday evening, a level with only a handful of tickets, a week of leave. The support lead checks every target against the export before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Support ticket triage](../support-ticket-triage/)
- [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
