# Call summary check against the transcript

Before anyone acts on the summary of a service call, your quality lead sees every amount, date, outcome and statement in it that the transcript does not back, each with the line and time to check, and what the summary left out. It changes no record; the reviewer decides what is corrected.

*Workflow template · Customer support and service · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/call-summary-transcript-check/)*

## The outcome

The record of a call says what was actually said. A summary is the part of a call everyone else relies on: the next agent, the team approving a credit, the person answering a complaint. When it says a credit was applied and the agent only asked for one, or that the customer agreed to a payment plan when they said they would think about it, the next decision rests on something that never happened.

This workflow template reads the summary one claim at a time. Every amount, every date, every outcome and every statement about who said, asked or promised what gets one verdict from the transcript: supported, not supported, contradicted or cannot tell. Each verdict carries the transcript line, the time on the recording and the speaker, so the reviewer can check it in a minute. Offers recorded as done, conditions dropped, "next Wednesday" turned into the wrong date and amounts with two digits swapped all come to the surface.

Then it reads the transcript the other way, for what a service summary must carry and this one does not: a request for a supervisor, a disputed charge, a complaint, a promise with no date, a mention of an ombudsman. It works the same way on a summary an agent wrote and on one your call platform generated, so it also gives your team a fair way to judge generated summaries before trusting them.

The quality lead or team leader decides what happens next. The summary, the case and the agent's record stay exactly as they were.

## Who starts the work, and when

The contact-center quality lead, a team leader or a quality analyst starts it once a call is over and has both a transcript and a summary: when the call is picked for quality review, when someone is about to act on the summary, or when a customer says the record of a call is wrong. Teams trying out generated summaries run it on a set of calls, one call at a time.

The quality lead or the team leader reads the check and decides, for each finding, whether the summary or the case is corrected and by whom.

## What they supply

- **The transcript,** exported with a line number, the time from the start of the call, the speaker and what was said. The template names the column headers it expects; when yours differ, it stops and asks which is which.
- **The summary,** exactly as it stands on the case.
- **The call details:** call and case references, the date of the call, the queue, the agent, the outcome recorded on the case, and whether the summary was written by the agent or generated.
- **Any later corrections** noted on the case.
- **Your settings:** who reviews, who receives mentions of a regulator or a safety risk, your working days and closed days, and the list of what every summary must carry, if yours differs from the default.

## What comes out

One check for one call, in a fixed order. The header gives the call, the limits of the transcript (hidden and unheard passages) and any line to raise straight away with your escalation role. The result line counts the claims by verdict and shows how many need the reviewer, and the outcome code on the case is compared with how the call actually ended.

Then the claims, contradicted first, then not supported, then cannot tell, each with the summary's words beside the transcript's, and the working for every date. What the summary left out follows, each item with its line and time, then the later corrections and what they touch, and the claims the transcript supports. Card numbers and security answers are never repeated.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Customer support and service](https://fullypowered.ai/functions/customer-support-and-service/), where the contact center's quality lead owns the record of every call.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where a call summary promises refunds, replacements and delivery dates that the next agent will honor.
- [Insurance](https://fullypowered.ai/industries/insurance/), where a claim call's summary carries amounts, dates and what the policyholder said, and the claim moves on that record.
- [Energy](https://fullypowered.ai/industries/energy/), where billing calls turn on estimated readings, credits, payment plans and visit dates, and a customer may take a complaint to the ombudsman.
- [Finance and investment](https://fullypowered.ai/industries/finance-and-investment/), where a service call about a charge or a payment has to be recorded exactly as it happened.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where call summaries have piled up for years and nobody has read them against what was said.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when call volume grows faster than the quality team and generated summaries start to carry the load.

## What has to change for your company

Export transcripts with the column headers and speaker labels the template expects, or tell it yours. Tell it the marks your platform uses for hidden and unheard words. Review the list of what every summary must carry and add what your service must always record, such as a reference number given to the customer. Set your working days and closed days so counted promises such as "within five working days" come out right. Name the reviewer and the escalation role. Decide whether to check every call with a generated summary for a trial period or a chosen sample. It runs in ChatGPT, Claude, Copilot or Gemini from files and text you supply; it needs no connection to your phone or case system.

## What has been checked

Fully Powered AI wrote this workflow template as original work. It was editorially reviewed on 11 November 2026. It was tried once on its invented example on 11 November 2026 in Claude; the record is published with it. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on past calls your quality lead has already reviewed by listening, with hard cases chosen in advance: an amount with two digits swapped, an offer recorded as done, "next Wednesday" with the date unheard, a refusal recorded as agreement, a request for a supervisor the summary leaves out, an export with different column headers. The quality lead checks every quoted line against the transcript and every unclear passage against the recording before anyone relies on a finding. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 11 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 11 November 2026. The record is in [TRIAL.md](TRIAL.md).
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

- [Support escalation brief](../support-escalation-brief/)
- [Complaint and refund request handling](../complaint-and-refund-request-handling/)
- [Account commitments check](https://fullypowered.ai/workflows/account-commitments-check/)
- [Follow-ups promised on service calls](../service-call-promises-list/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
