# Customer feedback themes

Each month your support lead sees what customers keep telling you: tickets, disputes, reviews and survey comments grouped into themes with counts and quotations, the three issues most worth fixing with a proposed fix and owner, and a note for customers once a fix ships. A person decides every fix.

*Capability template · Customer support and service · version 0.1.0 · [Capabilities Directory](https://fullypowered.ai/capabilities/customer-feedback-themes/)*

## The outcome

Once a month the scattered complaints turn into one picture. Every ticket, card dispute, review and survey comment from the month is read, and items about the same experience are put together, so three customers describing one dented parcel in three different ways land in one theme. Each theme is counted by customer as well as by message, so one person who writes five times is still one customer, and each carries its impact and a few quotations in the customers' own words, with names and contact details taken out.

The report ends with three issues to fix. Each comes with what the feedback shows about its cause, one proposed change, the role that would own it, and the count that will tell you next month whether it worked. When a fix from an earlier month ships, a short "you told us, we changed" note is ready for customers. The person you name decides which fixes go ahead and approves every note before it is shared anywhere. Anything that cannot wait for a monthly report, such as a customer who was hurt, goes to the top on its own.

## Who starts the work, and when

The support lead runs it in the first days of each month, once the month's exports are in. It takes the month's feedback, last month's report and the list of fixes already under way. The support lead checks the counts, then takes the report to whoever decides fixes: the operations manager, the owner or the managing director. Fixes are agreed there, with the role that owns each area.

The assistant prepares the report and the draft notes. It closes no ticket, settles no dispute, answers no review and sends nothing.

## What they supply

- **The month's feedback export.** One row per ticket, dispute, review or survey comment: its number, date, source, customer and text, and a star rating where there is one. The template lists the default column headers; a header that does not match stops the work until someone says what the column holds.
- **The owner list.** The areas of your business, such as delivery, website and billing, and the role that owns each.
- **Last month's report and the fix list.** Each fix with its status (planned, in progress, shipped or declined) and, for a shipped fix, what changed and from which date.
- **What changed this month.** Packaging, prices, a promotion, a new supplier: anything with a date that might explain a theme.
- **Who approves notes to customers,** and how customers can reach you.

## What comes out

One report in a fixed order:

1. **Needs a person now.** Items that report an injury, a safety risk, a legal threat, a data exposure or abuse of staff, lifted out with who decides.
2. **Themes.** Each with its area, customers, items by source, impact, score, last month's count and up to three quotations.
3. **Single mentions and items not placed,** so nothing read is lost.
4. **Three issues to fix,** each with evidence, cause as far as the feedback shows it, a proposed fix, a proposed owner and the count to watch.
5. **The fix list,** set against this month's counts.
6. **You told us, we changed.** Draft notes for fixes that have shipped, marked as not sent.
7. **Questions for the support lead.**

Good looks like this: every count can be traced to item numbers, every item read appears in the report exactly once, and the person deciding fixes can see in two minutes what customers are telling you and what it would take to stop it.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Customer support and service](https://fullypowered.ai/functions/customer-support-and-service/): the team that hears every complaint first and is best placed to say which ones keep coming back.
- [Product management](https://fullypowered.ai/functions/product-management/): the themes about the product itself become evidence for what to change next.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/): delivery, packaging, checkout and refund feedback arrives in volume across tickets, reviews and card disputes.
- [Consumer brands](https://fullypowered.ai/industries/consumer-brands/): reviews and surveys show what buyers think of the product as well as the service.
- [Software technology](https://fullypowered.ai/industries/software-technology/): tickets, app reviews and survey comments point to the same faults in different words.
- [Hospitality](https://fullypowered.ai/industries/hospitality/): guest reviews, complaints and post-stay surveys repeat the same few problems.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/): the business has outgrown the one person who used to read every complaint.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/): the same issues have quietly come back for years and nobody has counted them.

## What has to change for your company

- **Your export.** Decide which systems feed it and map your column headers to the defaults once. Remove anything customers would not expect to leave your systems.
- **Your areas and owners.** List the parts of the business a fix can land in and the role that owns each.
- **Your impact rules.** The defaults rate a theme high when money is at stake or a customer cannot use what they bought; change them if your business weighs things differently.
- **What needs a person now.** Name the matters that cannot wait and who decides each.
- **Who decides fixes and who approves notes,** and where approved notes appear: your help centre, a newsletter or a reply to the customers who raised it.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini from files you supply; it needs no connection to your help desk or payment provider.

## What has been checked

Fully Powered AI wrote this capability template. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026 in two runs; the record of the second, made on the instructions as revised after the first, is published with it. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past month your support lead remembers well, plus hard cases written in advance: one customer writing five times about the same thing, a review that reports an injury, a fix that shipped halfway through the month, a column header the template does not know. The support lead checks every count against the export before anyone decides a fix. [Pilot acceptance-test preparation](https://fullypowered.ai/capabilities/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete capability template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the capability drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related capabilities

- [Support ticket triage](../support-ticket-triage/)
- [Churn risk and save plan](https://fullypowered.ai/capabilities/churn-risk-and-save-plan/)
- [Customer interview synthesis](https://fullypowered.ai/capabilities/customer-interview-synthesis/)

## Make it yours

This is the starting version. Fully Powered AI adapts capabilities to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
