# Product recall customer contact plan

Once your business has issued a recall, the customer care lead gets the contact plan: affected customers from the order export, the approved notice word for word, drafts that offer only the remedies you run, and a tracker that counts a customer done only when the item is back or repaired.

*Workflow template · Customer support and service · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/product-recall-customer-contact-plan/)*

## The outcome

Every affected customer is on one list, and nobody slips off it. Your care team works from one email draft and one phone script, both carrying the notice exactly as your business approved it and offering only the collection, return or repair you really operate. Nobody improvises an answer about the hazard, promises a refund you do not offer, or shares what a customer bought with a stranger who happens to answer.

The tracker tells the truth about progress. A reply, a chosen remedy or a booked collection moves a customer along, but only a unit confirmed back or repaired, by a named person, finishes them. Each count stands on its own base, so a busy week of emails never reads as a finished recall.

Questions the approved answers do not cover, reports of damage or injury, and items passed on to someone else go to the right person, quoted as the customer put them. The AI assistant sends nothing, calls nobody and marks nothing done. A person on your care team makes every contact.

## Who starts the work, and when

The customer care lead or service lead starts it once the decision to recall has been made, the notice wording has been signed off by a named person, and the remedies are written down. It runs first to build the list and the drafts, and again whenever the care team's contact log or the warehouse's returns log has moved on, to bring the tracker and the next contacts up to date. The care lead approves the drafts before anything goes out.

## What they supply

- **The recall record:** the affected product and its identifiers, the approved notice wording with who approved it and when, the remedies you run, how customers reply, the short message for a voicemail, any approved answers, and who takes escalations.
- **The order export** for every order containing the product, with the customer's contact details and the lot, batch or serial number.
- **The care team's contact log** and **the returns log,** once contact has started.
- **Your settings:** today's date, the order of channels, how many attempts per customer and how far apart, and your calling hours.

## What comes out

1. **Questions to settle** for the care lead, the person who approved the notice and the returns lead.
2. **The affected customers,** one line each. Any order whose scope is unclear is set aside for a ruling, and anyone who cannot simply be contacted is held with the reason.
3. **The approved notice and the remedies,** exactly as written.
4. **An email or letter draft and a phone script** for the care team.
5. **The tracker,** with each customer's status, units confirmed back or repaired, and separate counts.
6. **The follow-up list** and **the next contacts due.**

A good plan can be checked against the order export and the two logs in a few minutes.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Customer support and service](https://fullypowered.ai/functions/customer-support-and-service/), which carries the notice to customers and keeps the record of every contact.
- [Quality management](https://fullypowered.ai/functions/quality-management/), which owns the corrective action and needs to know how many units have actually come back.
- [Consumer brands](https://fullypowered.ai/industries/consumer-brands/), selling direct to households that expect a clear, calm notice.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where the order export already holds who bought what and how to reach them.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where affected units are traced by lot, batch or serial number.
- [Hardware and physical technology](https://fullypowered.ai/industries/hardware-and-physical-technology/), where a fix is often a repair or a part swap rather than a refund.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), with an order history long enough that a recall reaches customers from months back.

## What has to change for your company

Write the recall record down first: the identifiers, the notice exactly as approved, the remedies and the approved answers. The workflow template adds nothing to any of them. The decision to recall, the notice itself and every regulatory or legal duty stay with your business and its advisers; this prepares the customer contact list and the message drafts, and nothing is sent. Check that your order export, contact log and returns log carry the default columns, or give the assistant your own headers once. Decide how your business handles customers marked do not contact for a safety notice, who confirms returns and repairs, how many attempts the team makes and how far apart. It works in ChatGPT, Claude, Copilot or Gemini from the files you supply, with no connection to your order system, mailbox or phones.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example on 10 November 2026 in four runs: the instructions and the example were revised after each of the first three, and the fourth, on the current version, gave the same customer list, statuses, counts and follow-up as the example; the record is published with it, and no edits to the instructions or the example have been made since that run. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past recall or a rehearsal with your own order data, plus hard cases written in advance: a row with a blank batch number, a unit received with nobody's name against it, a customer who asks about damage, a request to offer a remedy you do not run. The care lead checks every count against the logs before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that test set, and [What we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) shows the record.

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

- [Complaint and refund request handling](../complaint-and-refund-request-handling/)
- [Customer reply drafting](../customer-reply-drafting/)
- [Support ticket triage](../support-ticket-triage/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
