# Trial: Help article from a resolved issue

- **Product:** Claude, run in Claude Code

Model: Claude Sonnet 5.5 (model ID claude-sonnet-5-5). Date: 2026-11-09.

The inputs are the invented example in `public/example.md` (Company H, Client W, tickets, articles and style guide all invented). No client data was used. I used its five inputs as given: the resolution record, the note from the person running it, the article list, the style guide HC-2 and the settings. I followed the instruction block and the output format in `member/template.md`. I did not write this template.

One flaw in the method, stated first: I was meant to read only the inputs before producing my output. My first file read printed the whole example, including most of its output, so I had seen that output before I wrote mine. My article and notes below were composed from the inputs and the instructions, but they are not a blind run, and the close match to the published example partly reflects that. The ambiguities listed at the end were found while following the instructions.

## What came out

```
HELP ARTICLE DRAFT: Invoices still show the old logo after you change it
Status: Draft for Ren, support lead. Not published. Ready for review
Source: Ticket 2318, resolved Thursday 5 November 2026. Fix confirmed by the customer, Thursday 5 November 2026 (message 5).
How often: Third ticket in two weeks (Sam's note: 2290, 2297, 2318).
Style: HC-2, 1 September 2026. Body: 168 words against a limit of 300.
Recommendation: New article. KB-104 and KB-131 are related and linked; see "Overlapping articles".

ARTICLE
Title: Invoices still show the old logo after you change it
Type: Troubleshooting
Category: Invoicing
Audience: Account admins
Tags: logo; invoice template; invoice PDF; branding; company details
Search terms: old logo on invoice; changed logo but invoices still show old one; invoice logo not updating; regenerate PDF. Exact error text: none in the record

# Invoices still show the old logo after you change it
Changed your company logo, but new invoices still carry the old one? This article is for account admins.
## What you see
You changed your logo under **Settings > Company**. Invoices you make afterwards still show the old logo.
## Why it happens
Each invoice template keeps its own copy of the logo. Changing the logo under **Settings > Company** does not change your templates.
## How to fix it
1. Go to **Settings > Invoice templates**. Only account admins can see this page.
2. Open the template you use.
3. Under **Logo**, choose **Use company logo**.
4. Select **Save**.
5. Repeat for each template you use.
New invoices made from that template now show the new logo.
## Invoices you made before the change
Earlier invoices keep the old logo. To update one, open it and choose **More > Regenerate PDF**.
## If that does not work
If an earlier invoice still shows the old logo after you regenerate it, contact support.
Need more help? Contact support from **Help > Contact us**.
## Related articles
- Add or change your company logo (KB-104)
- Create and edit invoice templates (KB-131)

TRACE
1. Title and opening: new invoices keep the old logo after the change - message 1, 4 Nov, customer.
2. Audience and "only account admins can see this page" - internal note, 5 Nov, support.
3. What you see - message 1, 4 Nov, customer.
4. Why it happens - message 2, 4 Nov, support.
5. Steps 1 to 4 (Settings > Invoice templates, open template, Use company logo, Save) - message 2, 4 Nov, support; confirmed working for new invoices in message 3, 4 Nov, customer.
6. Step 5, repeat for each template - message 2, 4 Nov, support; customer did both of theirs in message 3, 4 Nov, customer.
7. New invoices show the new logo - message 3, 4 Nov, customer.
8. Earlier invoices keep the old logo; More > Regenerate PDF - message 2, 4 Nov, support. The regenerate step is not confirmed on its own: see Check the steps.
9. If that does not work, contact support - message 3, 4 Nov, customer (regenerate still showed old logo); internal note, 4 Nov, support (only staff could fix it); message 5, 5 Nov, customer.
10. Closing line - style guide HC-2, rule 5.
11. Related articles - article list (KB-104, KB-131); person's note (KB-104 suggested).

CUSTOMER DETAILS REMOVED
- Customer's first name and job title: ticket header, messages 1 and 2. Not carried into the article.
- Company name: ticket header, message 1. Not carried.
- Email address and phone number: message 1. Not carried.
- Account number: ticket header, internal note of 4 Nov. Not carried.
- The customer's own client: message 1. Not carried.
- Invoice number: messages 1, 3 and 4. Not carried.
- Screenshot and its file name: message 1. Not carried.
- Ticket numbers: ticket header, Sam's note. Not carried.
- Dates of the case: every message. Not carried.

KEPT OUT OF THE ARTICLE
- Clearing the PDF cache from the admin console (internal note, 4 Nov; only staff can do it). The article says to contact support instead.
- Engineering's plan to make templates follow the company logo (internal note, 5 Nov; no date, and "do not tell customers").
- Support staff names and the name of the product specialist (messages 2 and 4, internal notes).

BEFORE PUBLISHING
Check the steps: A colleague who did not work on the ticket follows the steps once on a test account, from changing the logo under Settings > Company to regenerating an earlier invoice. Not confirmed: More > Regenerate PDF on its own. In the ticket the regenerated invoice still showed the old logo (message 3) until support cleared the cache, and showed the new one afterwards (message 5).
Expert review: Kai, product specialist (invoicing). The article explains why the old logo stays, and relies on a step the customer did not confirm on its own; the settings call for review in both cases.
Overlapping articles: KB-104, "Add or change your company logo": covers changing the logo, not why invoices keep the old one; link it, and consider one line in KB-104 pointing here. KB-131, "Create and edit invoice templates": where the fix is made; linked. Its text was not supplied, so whether it mentions Use company logo is unknown.
Screenshots: None required by HC-2. If one is added: the Logo option on Settings > Invoice templates, from a test account.
Sections left out: None
Questions for Kai, product specialist: Should More > Regenerate PDF show the new logo without staff clearing the cache? If yes, is the "If that does not work" section needed? If no, the steps change before publishing.
Questions for Ren, support lead: Add a line to KB-104 linking here? Does KB-131 need a mention of Use company logo? Is "Account admins" the right single audience, given that all users may meet the symptom?
Review date: Monday 10 May 2027, six months from Monday 9 November 2026 (Sunday 9 May 2027 moved to the next working day).
Approval: Ren, support lead, approves before the article is published.

Prepared for Sam, support agent. Nothing has been published, edited or sent by the assistant, and the ticket is unchanged.
Not completed, and what is needed: whether More > Regenerate PDF works without staff clearing the cache (Kai's answer).
```

## What was observed

All parts of the output format were produced, and nothing in the instructions made me stop: the record had a resolution, part of the fix was something a customer can do, and there was no security, legal or safety matter. The staff-only cache clearing was correctly turned into "contact support" and listed under "Kept out". The review date landed on a Sunday and the weekend rule moved it to Monday 10 May 2027.

Differences from the published example:
- Mine has no Related-articles link to KB-150 ("Resend an invoice to a client") and no sentence about resending. The record does not mention resending; the example's link rests only on the article list. Neither is wrong, but the example's link has no support in the ticket.
- The example's "If that does not work" section adds "tell us which invoice it is" and "the rest of the fix is done on our side". Neither appears in the record as advice to the customer; I left both out under the rule that an untraced statement is removed.
- The example says "Invoices made before you changed the template keep the old logo"; the record says invoices made before the change. Wording only.
- Word count: the example says 196; mine says 168 for a shorter body. Counting rules are loose (see below), so the two figures cannot be compared exactly.
- Same status, type, category, audience, recommendation and review date. The example's questions for Ren and Kai match mine closely; I added one on the audience.

Facts not in the inputs: none in my output that I found. In the example's output, the closing sentence in "If that does not work" ("The rest of the fix is done on our side") and the KB-150 link are not backed by the ticket, though the second is backed by the article list. The example's trace entry 10 sources "the rest is done by support" correctly to the internal note, but the article tells customers something the note was written for staff to read.

Ambiguities and defects in the template, where I had to guess or decide:
1. **Which words count toward the limit.** Step 7 says to count headings but not list numbers or ">". It does not say whether the title heading counts, or whether the bold markers and "#" marks count. I counted the title and all headings, ignored "#" and "**" marks, and got 168 (158 without the title).
2. **Status when a step is unconfirmed.** Step 2 makes an unconfirmed fix "Not ready", but an unconfirmed step is only listed under "Check the steps". The Regenerate PDF step did not work for the customer until staff acted, which is close to "the record shows two different outcomes". I chose "Ready for review" with the step flagged, because the main fix was confirmed. The template does not say where the line is.
3. **Update or new article.** Sam suggested KB-104. The test is "same problem or same task", which can be read either way. The recommendation line allows only one outcome, so a "new article plus a line added to an existing one" has to go in the notes.
4. **Audience.** The settings list "All users" and "Account admins". Only admins can reach the settings page, but the symptom affects anyone who sees invoices. The template says to choose from the settings and gives no rule for choosing.
5. **Ticket number in the header.** The article must carry no ticket numbers, but the Source and Trace lines name the ticket and customer messages. This is sensible, since those lines are for the owner, but the template does not say that the header and trace are exempt.
6. **A staff-only step that customers can see failing.** "If that does not work" has to say something without revealing the staff step. The template says "contact support" and nothing about what the article may say about why. I kept it to one sentence.
7. **Dates in the trace.** The trace asks for the date and author's role but the rule against case dates applies to the article, not the trace. This is clear on a careful read but easy to misapply.
8. **Style guide numbering.** The instruction block refers to defaults "in step 6" and the procedure refers to them in step 7; each is correct inside its own list, but the two numberings differ, which could confuse someone reading both.
9. **Closing line and Related articles.** The format puts the closing line above Related articles, and HC-2 agrees. When "If that does not work" is the last section, the closing line sits alone after it; fine, but the format's note "[Any further case...]" sections come before "If that does not work", which I followed.
10. **Approved product facts: none supplied.** The statement "Only account admins can see this page" comes from an internal note, not an approved fact. The template permits sources including internal notes in the trace, but also says a statement not in the record needs an approved fact. A support note counts as the record here, so it passed, but the line between the two is thin.

Nothing in the template was wrong enough to stop the run. The acceptance tests were not run as part of this trial; only the one scenario in the invented example.

## Changed after this run

Changed on 9 November 2026 after an independent review of the published template, and not run again. The output and the observations above are as recorded and describe the template and the example as they stood at the run:

- **The example's "If that does not work" section** now says only "contact support". The two untraced clauses noted above ("tell us which invoice it is" and "the rest of the fix is done on our side") were cut, as the run had left them out. Its trace entry now cites message 3, the internal note and message 5. The example's body count was recomputed from 196 to 179 words under the counting rule below.
- **Ambiguity 1, the word count.** The procedure and the pasted instructions now say that the title is not counted, nor are list numbers, the ">" in menu paths or markup marks such as "#" and "**". By that rule the run's body is 158 words, the figure it gave without the title.
- **Ambiguity 2, the status.** Step 2 and the pasted instructions now say that when the main fix is confirmed and only a secondary step is not, the status stays "Ready for review" and that step goes under "Check the steps", as the run chose.
- **Ambiguity 3, update or new article.** Step 4 and the pasted instructions now say that the "Recommendation" line gives one main outcome and that a line to be added to a related article goes under "Overlapping articles". The run also put a pointer on the Recommendation line itself; under the new wording that line would read "New article".
- **Ambiguity 4, the audience.** Step 10 and the pasted instructions now say that when the symptom reaches more readers than can apply the fix, the audience is the one that can carry out the steps, as the run chose.
- **Ambiguities 5 and 7, ticket numbers and dates.** Step 8 and the pasted instructions now say that the header, the trace and the notes for the owner may name the ticket, its dates and its message numbers, and the article, tags and search terms may not.
- **Three long lines** in the pasted instructions were rewrapped. Their wording is unchanged.

Ambiguities 6, 8, 9 and 10 are unchanged.
