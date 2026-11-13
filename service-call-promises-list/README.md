# Follow-ups promised on service calls

After service calls, the contact-center team leader gets every follow-up the agent promised, each quoted from its transcript line, with the deadline as said, any condition, who owns it and the record that matches it. Nothing is booked, assigned or sent, and no customer is contacted.

*Workflow template · Customer support and service · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/service-call-promises-list/)*

## The outcome

The team leader sees what customers were told they would get, in the agent's own words, before a customer has to ring back and ask. Every promise points to the line of the transcript where it was said, so anyone can check it against the call. A callback "by Thursday" shows the Thursday it means. A refund that "should" arrive is marked as hedged. "We'll sort that out" shows that nobody was named to sort it out.

Each promise is set beside the follow-up records your systems hold: a callback booked, a refund raised, a replacement sent. Where the record is due later than the customer was told, or there is no record at all, the list says so. Where the deadline as read has passed and no record shows the work done, the list says that too, and says plainly that this is not proof the promise was broken.

Lines that only describe how things usually go ("replacements normally go out within five working days") are kept apart from promises, because customers often hear them as one. Actions the agent finished while still on the call are kept apart as well.

The list ends with one question for each promise that has a gap. The team leader decides who owns each follow-up, by when, and whether a promise beyond the agent's limits stands. The AI assistant contacts no customer, books and assigns nothing, and changes no record. It describes calls, never people, and nothing on it is for an agent's file.

## Who starts the work, and when

The contact-center team leader, or a quality analyst working for the team leader, starts it on request: on a day's calls for one agent, on calls picked for review, on calls about a known problem, or before answering a customer who says they were promised something. The calls must have ended and have a transcript with numbered lines.

The team leader reads the list, confirms or corrects each promise, deadline and owner, and settles each question. The people who own each follow-up then book or correct it in your own systems, and contact the customer where the team leader decides they should.

## What they supply

- **The call list.** One row per call: the call's reference, date, start time, agent, your customer reference, the case number and the agent's wrap-up note.
- **The transcripts.** One row per spoken line, numbered, with the time into the call and who was speaking.
- **The follow-up records,** where you can export them: callbacks, refunds, deliveries, visits and tasks, each with the call or case it belongs to, its type, owner, due date, when it was created and its status.
- **The run settings.** Your working days and hours, the labels your transcription uses for agent and customer, who owns each kind of follow-up when the call names nobody, the names of your record types and statuses, and any limits on what an agent may promise without approval. The template carries sensible defaults for anything you have not set.

## What comes out

One list in plain text, call by call, in a fixed order:

1. **A header** with the counts: calls read, promises found, how many are hedged and flagged, and which settings were taken as defaults.
2. **Each promise,** numbered, with its transcript line and time, its kind (callback, send, refund or credit, replacement or delivery, visit, escalation or task), the words, the deadline as said and the date and time it reads as with the rule used, any condition, the owner as said, the matching record, and whether the wrap-up note mentions it.
3. **Fixed flags** where something is missing or out of line: owner missing, deadline not stated, hedged, conditional, needs approval under your limits, no record found, more than one record, record later than promised, deadline passed, outside working hours, speaker unclear.
4. **Expectations set, not promises,** and **completed during the call,** for each call.
5. **Questions for the team leader,** one for each flagged promise, the facts first.
6. **Could not be read,** for any call or line that could not be used.

Good looks like this: the team leader can check every line against the transcript line it cites, no date appears that the call did not support, and nothing has been changed anywhere.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Customer support and service](https://fullypowered.ai/functions/customer-support-and-service/): the contact center's check on what its agents have promised, before the promises turn into repeat calls.
- [Insurance](https://fullypowered.ai/industries/insurance/): claims and policy lines where an agent promises a callback, a document or a decision by a date the customer remembers.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/): replacements, refunds and redeliveries promised on the phone and carried out by other teams.
- [Energy](https://fullypowered.ai/industries/energy/): engineer visits, meter readings and bill corrections promised on a call and owned by field and billing teams.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/): the phone queue has grown past the point where the team leader hears enough calls to know what is being promised.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/): long-standing habits of saying "we'll sort it" that nobody owns.

It is separate from the [account commitments check](https://fullypowered.ai/workflows/account-commitments-check/), which lists what both sides promised across an account's meetings and emails, and from the [stale ticket sweep](https://fullypowered.ai/workflows/stale-ticket-sweep/), which looks at the whole queue of open tickets. When one follow-up needs a specialist, the [support escalation brief](https://fullypowered.ai/workflows/support-escalation-brief/) carries it on.

## What has to change for your company

- **Your working days and hours,** so that "by the end of the day" and "within 48 hours" read as the times your team means.
- **Your speaker labels,** exactly as your transcription service writes them, including any label for a second agent after a transfer.
- **Your owner map:** which team owns each kind of follow-up when the call names nobody.
- **Your record types and statuses,** exactly as your case, callback and billing systems export them.
- **Your promise limits,** such as the largest credit an agent may offer without approval.
- **The exports:** their column headings, and which customer details are removed before they leave your systems.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply; it needs no connection to your phone or case systems.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 11 November 2026. It was tried on its invented example in Claude on 11 November 2026, and the record of that run is published with it. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on calls your team leader has already listened to, plus hard cases written in advance, each with its expected result: a promise with vague timing, a callback booked for a later day than the one promised, a line from a speaker the transcription could not name, a promise the agent took back two lines later, a credit above the agent's limit. The team leader checks every line against the transcript before anyone relies on the list. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Stale ticket sweep](../stale-ticket-sweep/)
- [Support escalation brief](../support-escalation-brief/)
- [Account commitments check](https://fullypowered.ai/workflows/account-commitments-check/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
