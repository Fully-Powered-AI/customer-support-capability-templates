# Help article from a resolved issue

Turn every answer your team works out once into an article the next customer finds on their own. Hand over a resolved ticket and your list of articles; get back a draft in your customers' words, with their details removed and every step traced to the ticket. Your knowledge-base owner decides what goes live.

*Workflow template · Customer support and service · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/help-article-from-a-resolved-issue/)*

## The outcome

An agent solves a tricky problem on Wednesday, and by the following week the fix is a help article any customer can find by typing what they see. The draft arrives with the title, the steps and the search terms already in your customers' language, the customer who raised it nowhere in sight, and each statement linked back to the message in the ticket it came from.

Beside the draft sit the notes your knowledge-base owner needs: which steps someone still has to try, what was kept internal and why, which existing articles overlap, and whether this should be a new article or an update to one you already have. One solved ticket becomes an answer that keeps working, and your team stops solving the same problem over and over.

## Who starts the work, and when

The support agent who resolved the issue starts it once the ticket is closed and the fix is confirmed, usually when the same question has come in more than once. A knowledge-base owner can also start it from a ticket they spot in the queue. It runs once per resolved issue. The knowledge-base owner reads the draft, sends it to a subject expert where your rules call for one, has a colleague follow the steps, and decides whether and where it is published.

## What they supply

- The resolution record: the ticket thread with its internal notes, showing what fixed the problem.
- A short note on why it deserves an article and how often it comes up.
- Your list of existing articles, exported with its titles, categories and tags.
- Your help-centre style guide, if you have one.
- Your settings: who owns the knowledge base, who checks each product area, your audiences and categories, and how often articles are reviewed.

## What comes out

1. **A recommendation:** a new article, or an update to a named one, with what changes.
2. **The draft article:** title, type, category, audience, tags and search terms, then the article itself in one of four shapes: how-to, troubleshooting, question and answer, or known issue.
3. **A trace** linking every statement and step to its source.
4. **The customer details removed,** by kind and where they appeared, without repeating them.
5. **What was kept internal,** such as staff-only tools or plans with no approved date, and why.
6. **Notes before publishing:** steps to try, the review needed, overlapping articles, screenshots to take from a test account, questions, the review date and the approval line.

A good draft can be checked against the ticket in a few minutes, and a customer who never saw the ticket can follow it to the end.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Customer support and service](https://fullypowered.ai/functions/customer-support-and-service/), where the same question arriving three times means an article is missing.
- [Marketing and content](https://fullypowered.ai/functions/marketing-and-content/), where the help centre is writing your customers go looking for.
- [Software technology](https://fullypowered.ai/industries/software-technology/), where settings, error messages and workarounds change with every release.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), for orders, deliveries and accounts that customers would rather sort out themselves.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where client portals and billing questions repeat across every client.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where years of answers sit in closed tickets instead of the help centre.

## What has to change for your company

Write down your help-centre style, even a short one: how menu paths look, the closing line, the length limit. Name the knowledge-base owner who approves every article, and the product areas that need a subject expert's review. Export your article list with the column headers the template expects, or tell it yours. Decide which customer details count beyond the usual ones, such as project names your customers use. Name who handles a security issue, because those never become public articles. Decide which ticket content the AI assistant may be shown, on ChatGPT, Claude, Copilot or Gemini. Your team keeps control of everything published in your name.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 9 November 2026. It was tried on its invented example in Claude on 9 November 2026, and the record of that run is published with it. The run was not blind: the example's output had been seen before the run's own output was written. Small clarifications made after the run, listed in the record, have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on tickets your team has already turned into articles, plus hard cases written in advance, each with its expected behavior: a fix only staff could apply, a step that did not work for the customer on its own, an error message that contains the customer's file name, an issue that touches exposed personal data. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that test set, and [What we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) shows the record.

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
- [Write an SOP from how the work is done](https://fullypowered.ai/workflow templates/sop-from-how-the-work-is-done/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
