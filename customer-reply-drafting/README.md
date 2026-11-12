# Customer reply drafting

Every customer gets the reply your best person would write. Hand over the customer's message, your tone guide and your approved answers, and get back a draft in your voice where every statement and every promise traces to something you approved. A person on your team reads it, edits it and sends it.

*Workflow template · Customer support and service · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/customer-reply-drafting/)*

## The outcome

A customer writes in, and minutes later the person handling it has a reply ready to read: the answer first, in your company's voice, at the right length for the channel, with each next step dated and owned. Beside it sits a short list of what to confirm, what the draft promises and which of your rules allows each promise.

Nothing in the draft is made up. A question your approved answers do not cover is left unanswered and raised with the right person. A refund, credit or exception the sender cannot grant is never offered. The newest member of the team replies the way your best one does, and that is how a small team gives service that feels ten times its size.

## Who starts the work, and when

A support agent, an account manager or the owner starts it when a customer message needs a considered reply: a question, a complaint, a billing problem, a request you have to decline, or bad news you have to deliver. It runs once per message. The same person reads the draft, changes what needs changing and sends it. Where your rules call for a second reader, such as a customer who says they may leave, the draft names that role and waits.

## What they supply

- The customer's message, and the earlier thread if there is one.
- What is known and checked about the account: plan, order, charges, anything already promised.
- Your tone guide.
- Your approved answers: the policies, explanations and limits your team may state to customers.
- Who is sending, on which channel, and what that person may grant without asking.

## What comes out

1. **What the customer raised.** Every point in the message, numbered. Each question or request is marked as answered, held, declined or for a named role to decide, with its source. Each thing the customer says happened is marked as confirmed or not checkable.
2. **The draft reply.** Written to your tone guide and sized to the channel.
3. **Before sending.** Facts and actions to confirm, each promise with its date, owner and the rule that allows it, what was left out and why, and questions for colleagues.

A good draft answers the first thing the customer asked in its first lines, promises only what the sender can keep, and can be checked against your approved answers in a minute.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Customer support and service](https://fullypowered.ai/functions/customer-support-and-service/), for the everyday queue and the hard message alike.
- [Customer success and account management](https://fullypowered.ai/functions/customer-success-and-account-management/), where one careless promise costs a renewal.
- [Software technology](https://fullypowered.ai/industries/software-technology/), where billing, bugs and feature questions arrive in the same message.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), for orders, returns and delivery problems under a published policy.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where the reply comes from the person who holds the relationship.
- [Hospitality](https://fullypowered.ai/industries/hospitality/), where a guest's complaint deserves a personal answer the same day.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), which already have the policies and want every reply to follow them.

## What has to change for your company

Put your approved answers in one place, each with a review date and an owner; they are the only things a draft may state. Write down your tone guide, even one page of it. Set the limits: what an agent may refund or promise without asking, and how far ahead they may commit to a reply. Name the situations a second person reads before a reply goes, and who that person is. Decide which customer details the AI assistant may be shown, on ChatGPT, Claude, Copilot or Gemini. Your organization keeps control of what is said in its name.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 9 November 2026. It was tried on its invented example in Claude on 9 November 2026, and the record of those runs is published with the template. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on past messages your team has already answered, plus hard cases written in advance, each with its expected behavior: a question no approved answer covers, a request above the sender's limit, a customer who mentions leaving. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that test set, and [What we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) shows the record.

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

- [Client-status update preparation](https://fullypowered.ai/workflow templates/client-status-update-preparation/)
- [Inquiry handoff](https://fullypowered.ai/workflow templates/inquiry-handoff/)
- [Account handoff](https://fullypowered.ai/workflow templates/account-handoff/)
- [Support ticket triage](../support-ticket-triage/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
