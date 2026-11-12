# Customer satisfaction detractor follow-up

Every week your support lead gets each low satisfaction or recommendation score with the ticket behind it: the customer's own words, what went wrong as far as the ticket shows, a suggested owner and a draft message, plus the trend and a warning wherever the numbers are too thin to read. A person sends every message.

*Workflow template · Customer support and service · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/customer-satisfaction-detractor-follow-up/)*

## The outcome

Every unhappy customer reaches someone who can put it right. Each Monday the support lead sees every low score from the week before, joined to the ticket it came from. Each one carries the customer's comment exactly as they wrote it, the events in the ticket that explain it (a wait over a weekend, a visit moved, a third ticket for the same fault), the person best placed to call back and why, and a short message that person can edit and send.

A customer who scored low a few weeks ago and has done so again goes to the support lead. A customer who says they are thinking of leaving goes to their account manager. A comment about a bill goes to whoever owns billing. Nobody is asked to call back about their own work, and no draft names a member of staff, argues with the customer, or offers money, credit or a fix nobody has agreed.

Below the list sits the thirteen-week trend, with the response count beside every figure. Weeks with too few answers are marked, and the report says plainly when there are not enough responses to tell whether satisfaction has changed. Follow-ups still open from earlier weeks are listed, so a promised call does not quietly lapse.

## Who starts the work, and when

The support lead runs it on the first working day of each week, once the week's survey export is in. They supply the survey export, the tickets the low scores name, the follow-up log and last week's trend lines, check the list, confirm each owner, and hand it on. Each owner edits and sends their own message or makes the call, and the support lead records what happened in the log.

The assistant prepares the list and the drafts. It sends nothing, contacts no customer, changes no survey or ticket record, and offers no refund or credit.

## What they supply

- **The week's survey export.** One row per response: its number, date, survey (CSAT or NPS), score, comment, ticket and customer. The template lists the default column headers; a header that does not match stops the work until someone says what the column holds.
- **The ticket export,** with the notes for every ticket a low score names.
- **The follow-up log:** earlier low scores, who owned each and where it stands.
- **Last week's trend lines,** so the trend runs over thirteen weeks.
- **The owner list and account list:** the lead of each support team, the owner of areas such as billing, and the customers who have an account manager.
- **The sign-off** your people use on messages.

## What comes out

One report in a fixed order:

1. **The header,** with every count that has to add up, and any survey with too few answers this week.
2. **Needs a person now.** Comments that report an injury, a legal threat, a data exposure or abuse of staff, lifted out with who decides.
3. **Low scores to follow up,** each with its flags, the customer's words, what the ticket shows, the suggested owner, who is copied, the rule that chose them, and a draft marked not sent.
4. **Comment only.** Responses with words and no score, kept out of every figure, for the support lead to decide on.
5. **Still open from earlier weeks.**
6. **The trend,** week by week, and the last four weeks set against the four before.
7. **Questions for the support lead.**

Good looks like this: every low score in the export appears once, every line about what went wrong points to a dated event in the ticket, and each owner can send their message after a light edit.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Customer support and service](https://fullypowered.ai/functions/customer-support-and-service/): the team that sends the surveys and is first to see who is unhappy.
- [Customer success and account management](https://fullypowered.ai/functions/customer-success-and-account-management/): account managers take the follow-ups for customers who say they might leave.
- [Software technology](https://fullypowered.ai/industries/software-technology/): IT support and software providers that survey customers when each ticket closes.
- [Professional services](https://fullypowered.ai/industries/professional-services/): firms whose service desk or client team asks for a score after each piece of work.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/): shops that survey after each support conversation and need the unhappy answers seen quickly.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/): too many survey answers for one person to read and route each week.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/): the survey has run for years and nobody owns what happens after a low score.

## What has to change for your company

- **Your exports.** Map your survey tool's and help desk's column headers to the defaults once, and list the columns to ignore, since most survey exports carry many more than the template needs.
- **Your scales.** Set the CSAT scale and the scores you count as low and satisfied if you do not use 1 to 5.
- **Your owners.** List the lead of each support team, the owner of billing and any other area a low score can be about, and the customers who have an account manager. Change the order of the owner rules if you route follow-ups differently.
- **Your thresholds.** How few answers make a week a small sample, how many a four-week comparison needs, how big a change is worth naming, and how far back a repeat counts.
- **What needs a person now,** and who decides each.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini from files you supply; it needs no connection to your survey tool or help desk.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026 in three runs: the first, by a model that had not written it, found places where the instructions were open; they were closed, and the second run was made on the revised version by the model that revised it; after an independent review the instructions were tightened again, and the third run, recorded with it, was made by that same model in a fresh session that saw only the instructions, the output format and the example's inputs. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past week your support lead remembers well, plus hard cases written in advance: a customer who scored low twice in a month, a comment that says they are leaving, a complaint about a bill the ticket says nothing about, a score with no comment, a week with only a handful of answers, a column header the template does not know. The support lead checks every count and every owner before any message goes out. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Customer feedback themes](../customer-feedback-themes/)
- [Complaint and refund request handling](../complaint-and-refund-request-handling/)
- [Churn risk and save plan](https://fullypowered.ai/workflows/churn-risk-and-save-plan/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
