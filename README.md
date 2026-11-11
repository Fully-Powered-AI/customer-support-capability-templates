# Fully Powered Capability Templates: Customer Support

Every customer answered the way your best agent would answer. These capability templates take the replies and triage that fill a support queue and give an AI assistant a precise way to prepare them from your own approved answers, so your people send faster and escalate sooner.

This repository holds 11 capability templates for support and service teams. Each one is a single piece of work with its own folder: what it is for and who starts it, the complete template an AI assistant follows, a worked example with invented data, what to change for your company, what has been checked, and its sources.

## The capabilities

- **[Complaint and refund request handling](complaint-and-refund-request-handling/)**: A customer complains or asks for money back, and whoever handles it gets your policy's answer: the order matched, each condition checked, the amount worked out, any refund set out for a named person to approve, and a reply ready to edit and send.
- **[Customer feedback themes](customer-feedback-themes/)**: Each month your support lead sees what customers keep telling you: tickets, disputes, reviews and survey comments grouped into themes with counts and quotations, the three issues most worth fixing with a proposed fix and owner, and a note for customers once a fix ships. A person decides every fix.
- **[Customer reply drafting](customer-reply-drafting/)**: Every customer gets the reply your best person would write. Hand over the customer's message, your tone guide and your approved answers, and get back a draft in your voice where every statement and every promise traces to something you approved. A person on your team reads it, edits it and sends it.
- **[Customer satisfaction detractor follow-up](customer-satisfaction-detractor-follow-up/)**: Every week your support lead gets each low satisfaction or recommendation score with the ticket behind it: the customer's own words, what went wrong as far as the ticket shows, a suggested owner and a draft message, plus the trend and a warning wherever the numbers are too thin to read. A person sends every message.
- **[Help article from a resolved issue](help-article-from-a-resolved-issue/)**: Turn every answer your team works out once into an article the next customer finds on their own. Hand over a resolved ticket and your list of articles; get back a draft in your customers' words, with their details removed and every step traced to the ticket. Your knowledge-base owner decides what goes live.
- **[Help centre gap review](help-centre-gap-review/)**: Once a period, your support lead sees what the help centre is missing, read from that period's tickets and search log: questions agents answered by hand, articles that fell short, articles search could not find, and one gap list ranked by the tickets an article could have saved. The lead decides what is written.
- **[Product recall customer contact plan](product-recall-customer-contact-plan/)**: Once your business has issued a recall, the customer care lead gets the contact plan: affected customers from the order export, the approved notice word for word, drafts that offer only the remedies you run, and a tracker that counts a customer done only when the item is back or repaired.
- **[Stale ticket sweep](stale-ticket-sweep/)**: Once a week the support lead gets one sheet of what the queue is hiding: tickets with no real activity past their limit, tickets left waiting on the customer with the three ways out of each, likely duplicates, and each person's load weighed by size and age. A person makes every move.
- **[Support escalation brief](support-escalation-brief/)**: When a support case must move to a specialist or manager, the support lead gets one brief: the customer's impact, a dated timeline from the ticket history, the evidence, the fixes tried, the workaround in place and the decision needed. Nothing goes to the customer.
- **[Support service level definition](support-service-level-definition/)**: The support lead gets reply and resolution targets for every priority level, worked out from the team's own ticket history and the hours the team really has. Each target shows how often the team already meets it, and every gap comes back as a question for the lead to settle.
- **[Support ticket triage](support-ticket-triage/)**: Your queue manager opens the morning’s tickets already sorted: each one with a category, a priority and a route, and the reason for all three in a line. The tickets that cannot wait sit at the top, stopped for a person to decide.

## How to use one

Open a folder and start with its README. Every folder stands alone, so copy the one you want and leave the rest. The templates are written for ChatGPT, Claude, Copilot and Gemini: paste the instruction block and the output format in as custom instructions, or load the folder in a product that reads `SKILL.md` packages.

In every template a person starts the work, supplies the inputs and decides. The template prepares and checks. Anything that sends, posts, pays or changes a record waits for a person to approve it.

## What SKILL.md is

Each folder holds a file named `SKILL.md`. It is the technical file: the same instructions and output format as the template, in the packaged form that AI products which load instructions from a folder read. It is generated from `TEMPLATE.md`, so the two always agree. The capability template is the whole folder; `SKILL.md` is one way of loading it. If your AI product does not read that format, use `TEMPLATE.md`.

## What "checked" means here

Each folder says exactly what was checked and when: who wrote it, that its sources and rights were reviewed, the date of its editorial review, and whether it has been tried on its invented example in a named AI product. Nothing is described as tested for a client unless it was. Test a template on your own past work before your team relies on it; each one comes with acceptance tests for that.

## More capabilities

The [Fully Powered Capabilities Directory](https://fullypowered.ai/capabilities/) lists every capability across functions and industries, with search. A machine-readable list of this repository is in [index.json](index.json).

## Licence and credits

MIT, in [LICENSE](LICENSE) and in every folder. Each folder's SOURCES.md names what the capability drew on. Published by [Fully Powered AI](https://fullypowered.ai/).
