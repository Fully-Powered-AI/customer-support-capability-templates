# Complaint and refund request handling

A customer complains or asks for money back, and whoever handles it gets your policy's answer: the order matched, each condition checked, the amount worked out, any refund set out for a named person to approve, and a reply ready to edit and send.

*Workflow template · Customer support and service · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/complaint-and-refund-request-handling/)*

## The outcome

Every complaint is settled the way your written policy says, whoever picks it up. The handler sees which clause applies to each item, whether each condition is met, and the exact amount, with the arithmetic shown. Any refund, credit or replacement is written out as a request for the person allowed to approve it, and marked as not yet issued. The reply opens with the outcome. Where the policy says no, the reply says no too, names the clause, and puts forward the option the policy leaves open.

Nothing goes beyond the policy. A request it does not cover, such as a goodwill gesture, becomes a question for the owner rather than a promise. The AI assistant issues no refund, sends no reply and closes no ticket. It also checks your complaint log, so a problem that keeps coming back, such as one item that keeps arriving broken, reaches the owner while it is still a handful of orders.

## Who starts the work, and when

The owner, the service lead or a member of the service team starts it when a customer writes in about an order: something arrived damaged, late or not as expected, or they want a refund, a replacement or a credit. It runs once for each complaint, and again if the customer replies with something new. The handler checks the facts, edits the reply and sends it. Whoever your settings name approves any money before the reply says it has moved.

## What they supply

- The customer's message, and a description of any photo or attachment.
- The order rows from your shop or order system, as an export or pasted in.
- Your written refund and return policy, with its date.
- Your recent complaint log, if you keep one.
- Your tone guide, or two or three past replies the owner liked.
- Who may approve which amounts, and anything the owner has already decided about this complaint.

## What comes out

1. **What the customer reports and asks for,** point by point, each problem marked as confirmed by the inputs, confirmed in part, or not shown.
2. **The order and the policy check:** each condition, the fact behind it, and whether it is met, with one overall result.
3. **The amount,** worked from the order lines, and what is left out and why.
4. **For approval:** each refund, credit or replacement with its approver, not issued. A decline shows no approval request at all.
5. **The draft reply,** with any missing fact marked at the sentence it affects.
6. **Before and after sending:** what to do first, what to confirm, questions for the owner, the repeat check, and the line to add to the complaint log.

A good result can be checked against the policy and the order in two minutes.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Customer support and service](https://fullypowered.ai/functions/customer-support-and-service/), where refunds and complaints are the hardest messages in the queue.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), for damaged parcels, returns windows and items that do not match the photos.
- [Hospitality](https://fullypowered.ai/industries/hospitality/), where a guest asks for money back after a stay, a meal or a booking that went wrong.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), which have a written policy and want every complaint handled by it.

## What has to change for your company

Write the refund and return policy down, give each clause a number, and name its owner; the workflow template adds no terms of its own. Set who may approve which amounts, and who takes the complaints that mention a lawyer, a regulator, a card dispute or an injury. Keep a complaint log with a few fixed categories, and choose the window and the count that make a repeat worth raising. Check that your order export carries the default columns, or tell the assistant your own; for a stay, a meal or a booking, the order record is the booking or the bill, one row per charge, with the date of the stay or visit in place of the delivery date. Decide which customer details the assistant may be shown, on ChatGPT, Claude, Copilot or Gemini. It works from what you paste or upload and needs no connection to your payment system or shop.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 9 November 2026. It was tried twice on its invented example in Claude on 9 November 2026; the record of the second run, on the instructions as revised after the first, is published with the template. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on past complaints your team has already settled, plus hard cases written in advance, each with its expected behavior: a request outside the returns window, two orders that could be the one, an open card dispute, a request your policy says nothing about. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that test set, and [What we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) shows the record.

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

- [Customer reply drafting](../customer-reply-drafting/)
- [Support ticket triage](../support-ticket-triage/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
