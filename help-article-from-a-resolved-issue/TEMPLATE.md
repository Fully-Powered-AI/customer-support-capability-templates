# Help article from a resolved issue

Workflow template, version 0.1.0.

## Purpose

Turn one resolved support issue into one draft help article that other customers can find and follow. The draft is written in the words customers use, carries no detail of the customer who raised the issue, and traces every statement and step to the resolution record or an approved source. It comes with a record of the customer details left out, what was kept internal and why, the steps someone still has to try, and a recommendation on whether this is a new article or an update to an existing one. The assistant prepares; the knowledge-base owner approves and publishes. It never publishes an article, edits the live help centre or changes a ticket.

## When to use it and when not to

Use it once an issue is closed and other customers are likely to run into it too. Good candidates: a fix customers can apply themselves, a setting people overlook, a question several customers have asked, or a way round a fault engineering has not fixed yet.

Do not use it:

- when the issue is not resolved, or the record does not say what fixed it;
- when the fix was something only your staff can do, such as a refund, a credit, a manual change in an admin tool or a policy exception. That is not something another customer can follow;
- for a security weakness, exposed personal data or a compromised account. Those go to the role you name, not to a public page;
- for an outage notice, a release note or a message to many customers at once;
- to audit or reorganize the whole help centre. This workflow template writes one article from one issue;
- for anything touching a lawyer, a regulator, an injury or a safety risk.

## Roles

- **Runs it:** the support agent who resolved the issue, or the knowledge-base owner.
- **Approves and publishes** (decides whether the article goes live, and where): the knowledge-base owner.
- **Checks technical accuracy** (where the settings call for it): the subject expert for that product area.
- **Follows the steps once before publishing:** a colleague who did not work on the issue.

## Inputs

1. **The resolution record.** The complete ticket thread, with the date and the author's role on each message (customer or support), and every internal note. It must say what fixed the issue. If it is missing, or it ends without a resolution, stop.
2. **A note from the person running it:** why this deserves an article, how often it comes up (a count or other ticket references), and any article they think it updates. If there is no note, the header says "How often: not stated".
3. **The list of existing articles,** exported with these column headers: `article_id`, `title`, `category`, `tags`, `last_updated`, `owner`. Tags may be separated by semicolons. If a header is missing or named differently, stop and ask which column holds which; never guess. If no list is supplied, the recommendation line says overlap was not checked. If an update is recommended, the full text of that article is needed to draft the update; without it, the draft gives only what to add.
4. **The help-centre style guide:** voice, headings, how menu paths are written, the standard closing line, the length limit. If missing, use the defaults in step 7 and say so in the header.
5. **Approved product facts,** where you keep them: the names of screens and menus, plan limits, and anything about future changes that customers may be told. A statement that is not in the record needs one of these behind it.
6. **Settings:** the knowledge-base owner; the subject expert for each product area and when one must review; the audiences and categories your help centre uses; [your review interval]; today's date; any details beyond the defaults in step 8 that count as customer details; [your security role] and [your escalation role].

## The procedure

1. **Check the inputs.** Confirm the record is present and contains a resolution. Check the article list's headers against the defaults. Note the style guide's identifier and date.
2. **State the case from the record.** In one short paragraph for yourself: the problem as the customer described it, what fixed it, who it applies to (for example, only account admins, or only one plan), and how often it comes up. Then say how the fix was confirmed: the customer wrote that it worked, support checked it, or nothing in the record confirms it. An unconfirmed fix makes the status "Not ready". When the main fix is confirmed and only a secondary step is not, the status stays "Ready for review" and that step goes under "Check the steps".
3. **Decide whether it belongs in the help centre.** Split what fixed the issue into what a customer can do and what only staff can do. If nothing is left for the customer, stop: there is no self-service article to write. If part is left, the article covers that part, and the staff-only part becomes "contact support" at the point where it would be needed.
4. **Check for overlap.** Compare the problem, the task and the customer's words with each title, category and tags in the list. Same problem or same task: recommend an update to that article and say what changes. Related: link to it and name it under "Overlapping articles". Neither: recommend a new article. The "Recommendation" line gives the one main outcome; a line to be added to a related article goes under "Overlapping articles". The recommendation is the owner's to accept.
5. **Choose one article type.**
   - **How-to:** the customer wants to get something done.
   - **Troubleshooting:** something goes wrong and there is a fix the customer can apply.
   - **Question and answer:** a reply of one to three sentences. Anything the reader has to carry out in order belongs in a how-to.
   - **Known issue:** a fault that is still open. Its status, who it affects and any workaround come from the record; a fix date appears only if an approved product fact gives one for customers.
6. **Keep internal matters internal.** Internal notes, staff-only tools, staff names, other ticket numbers, engineering plans and any date not approved for customers stay out of the article. List each under "Kept out of the article" with the reason.
7. **Write the article.** Follow the style guide. Where it is silent, use these defaults:
   - The title names the symptom or the task in the customer's own words, and includes the exact error text when there is one.
   - The first sentence tells the reader, in their terms, what the article helps with and which readers it applies to.
   - Each numbered step is one action. Give the menu path in full, in bold, with ">" between levels. Where the record shows what appears on screen afterwards, say so.
   - Error messages are copied character for character, in code format.
   - Short paragraphs, a new heading whenever the subject changes, and the reader addressed as "you".
   - No more than 400 words in the body.
   Use the sections for the chosen type in the output format. An optional section with nothing behind it in the record is left out, and "Sections left out" says which and why. Count the body from the first sentence to the closing line, headings included; the title is not counted, nor are list numbers, the ">" in menu paths or markup marks such as "#" and "**". Give the count against the limit on the "Style" line.
8. **Remove the customer's details.** By default these count: names, email addresses, phone numbers, postal addresses, company names, account, order, invoice and ticket numbers, the customer's own clients or customers, file names, screenshots, dates that belong to their case, and quoted wording that would identify them; add any your settings list. Nothing of the kind goes into the article. Where an example value helps the reader, use a neutral placeholder such as "[your invoice number]". Record each kind of detail found and where it appeared, without repeating the value. The header, the trace and the notes for the owner are for staff and may name the ticket, its dates and its message numbers; the article, the tags and the search terms may not.
9. **Trace every statement.** Number each statement and each step in the article and give its source: a message in the thread (date and author's role), an internal note, the person's note, an approved product fact or an existing article's title. A statement with no source is taken out, or becomes a question. A step the record does not show working, for this customer or by a support check, goes under "Check the steps".
10. **Add the search details.** Tags and search terms come from the customer's own words, the exact error text and the categories and tags already in the article list. Choose the category and the audience from the settings. When the symptom reaches more readers than can apply the fix, choose the audience that can carry out the steps. If the record holds no error text, say "none in the record".
11. **Write the notes for the owner.** The steps to be tried once by a colleague who did not work on the issue, and any step not confirmed; the subject expert review, if the settings call for one, and why; overlapping articles; screenshots needed, to be taken from a test account and never from the customer's; questions for each role; the review date, counted from today by [your review interval]; and the approval line. A line with nothing to report says "None".
12. **Check and return.** Run the reviewer checklist, set the status line and return the draft to the person who ran it. End with the "Not completed" line. On a request to revise (shorter, another audience, another type), redo the article and every note together; a new statement goes through step 9 again.

## Exceptions and stop conditions

- **No resolution record, or it ends without a fix:** stop and ask.
- **Whenever a run stops,** print the header with the "Stopped" status, the case summary and the closing lines, as the output format shows.
- **Only staff could apply the fix,** or it was an exception made for one customer: stop. Say there is no self-service article, and why.
- **A security weakness, exposed personal data or a compromised account:** write no public article. Return the case summary and name [your security role].
- **A lawyer, a regulator, a claim, an injury or a safety risk is mentioned:** write no article on the matter; name [your escalation role].
- **The record gives two different fixes, or the customer's last message says it still fails:** status "Not ready"; draft nothing that depends on the disputed step; ask the agent who resolved it.
- **The issue depends on one customer's own setup,** so their details cannot be removed without losing the answer: stop and ask the owner whether a general article is possible.
- **Never a step:** a fix in which customers would share a password or login code, or switch off a security setting. Raise it as a question for the owner and the subject expert.
- **A release date or fix date not approved for customers:** left out of the article and listed under "Kept out".
- **The article list's headers do not match:** stop and ask which column is which.
- **Asked to publish the article, edit the live help centre, or update or close the ticket:** decline; those belong to the owner and the agent.

## Output format

```
HELP ARTICLE DRAFT: [working title]
Status: Draft for [knowledge-base owner]. Not published. [Ready for review | Not ready: reason | Stopped: the stop condition and the role named]
Source: [ticket reference], resolved [date]. Fix confirmed by [the customer, date | a support check, date | nothing in the record].
How often: [from the person's note | not stated]
Style: [style guide identifier and date | defaults used]. Body: [n] words against a limit of [limit].
Recommendation: [New article | Update to [article id], "[title]": what changes | New article; overlap not checked, no article list supplied | None: stopped]

[When stopped, print only the lines above, then this section, then the two closing lines:]
CASE SUMMARY
[The problem, what fixed it, who it applied to, and why no article is drafted.]

ARTICLE
Title: [title]
Type: [How-to | Troubleshooting | Question and answer | Known issue]
Category: [from the settings]
Audience: [from the settings]
Tags: [tags]
Search terms: [the customer's words; other phrasings]. Exact error text: [text | none in the record]

[Body, using the sections for the type. Sections marked (optional) are left out when the record holds nothing for them.]

How-to:
# [Title]
[First sentence: what this helps with, and which readers it applies to.]
## Before you start (optional)
## Steps
1. [Action, with the menu path, and what you should see next.]
## Check it worked
## If something goes wrong (optional)
[Style guide closing line]
## Related articles (optional)

Troubleshooting:
# [Title]
[First sentence.]
## What you see
## Why it happens (optional)
## How to fix it
1. [Action.]
## [Any further case the record covers, such as items made before the fix] (optional)
## If that does not work
[Style guide closing line]
## Related articles (optional)

Question and answer:
# [The question, as a customer would ask it]
[The answer in one to three sentences.]
## More detail (optional)
[Style guide closing line]
## Related articles (optional)

Known issue:
# Known issue: [what customers see]
Status: [from the record]. Who is affected: [from the record]. Last updated: [date].
## What you see
## What to do for now
[Steps, or "There is no way round this yet."]
## What happens next
[Only what an approved product fact allows customers to be told.]
[Style guide closing line]

TRACE
[n]. [Statement or step, shortened] — [source: thread message, date and author's role | internal note, date | person's note | approved fact | article list]

CUSTOMER DETAILS REMOVED
- [Kind of detail]: [where it appeared in the record]. [Not carried into the article | Replaced with "[placeholder]"]
[Or: None found.]

KEPT OUT OF THE ARTICLE
- [Item] ([reason]).
[Or: None.]

BEFORE PUBLISHING
Check the steps: [who follows them, and any step the record does not confirm | None]
Expert review: [subject expert role and why | None]
Overlapping articles: [article id, title: what overlaps and what to do | None | Not checked]
Screenshots: [what is needed, from a test account | None]
Sections left out: [section and why | None]
Questions for [role]: [question | None]
Review date: [date], [your review interval] from [today's date].
Approval: [knowledge-base owner] approves before the article is published.

Prepared for [person who ran it]. Nothing has been published, edited or sent by the assistant, and the ticket is unchanged.
Not completed, and what is needed: [item and what would settle it | Nothing outstanding]
```

## Reviewer checklist

1. The article describes the problem or task the way the customer did, and the title would match what a customer types. (Knowledge-base owner)
2. Every statement and step appears in the trace with a source, and nothing is stretched beyond what the record shows. (Knowledge-base owner)
3. No customer detail is in the article, the tags or the search terms, and "Customer details removed" names each kind found. (Person who ran it)
4. Nothing internal is in the article: no staff names, staff-only tools, engineering plans or dates not approved for customers. (Knowledge-base owner)
5. A colleague who did not work on the issue has followed the steps, and every step under "Check the steps" is settled. (The colleague)
6. Where the settings call for it, the subject expert has confirmed the cause and the steps. (Subject expert)
7. The recommendation on new or update fits the article list, and overlapping articles are linked or updated. (Knowledge-base owner)
8. The article follows the style guide and its length limit. (Knowledge-base owner)
9. The decision to publish, and the publishing. (Knowledge-base owner)

## Acceptance tests

Proposed tests. None has been run.

1. **Complete record, customer confirmed the fix.** Expected: status "Ready for review"; every statement traced; no customer detail anywhere in the article.
2. **No resolution in the record.** Expected: stops and asks.
3. **Staff-only fix.** Support issued a credit to close the ticket. Expected: stops; says there is no self-service article.
4. **Mixed fix.** The customer changed a setting, then support cleared a cache in an admin tool. Expected: the setting is a step; the cache step is kept out and replaced by "contact support"; listed under "Kept out" with the reason.
5. **Unconfirmed step.** One step did not work for the customer until support acted. Expected: listed under "Check the steps"; a question for the subject expert.
6. **Customer details in the error text.** The error message includes the customer's file name. Expected: the error text is kept with the file name replaced by a placeholder; recorded under "Customer details removed" without the value.
7. **Article list headers differ.** The export uses "Name" instead of "title". Expected: stops and asks which column is which.
8. **Existing article covers the same task.** Expected: "Update to [id]" with what changes; no second article drafted on the same task.
9. **No article list.** Expected: "New article; overlap not checked, no article list supplied".
10. **Engineering note with a release plan.** Expected: no date or plan in the article; listed under "Kept out".
11. **Exposed personal data in the issue.** Expected: no public article; [your security role] named.
12. **Login code in the fix.** In the record, the customer read a login code out to support. Expected: no step involves a login code; raised as a question.
13. **Asked to publish.** "Post it to the help centre and close the ticket." Expected: declines both and returns the draft.
14. **Asked for a question and answer, but the answer needs steps.** Expected: written as a how-to, with a line under "Questions for" asking the owner to confirm the change of type.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You turn one resolved support issue into one draft help article for
the knowledge-base owner. You prepare; people decide. You never publish
an article, edit the live help centre, or update or close a ticket. If
asked to, decline and return the draft.

You will receive: the resolution record (the ticket thread with dates,
each author's role and internal notes); a note on why the article is
wanted and how often the issue comes up; the existing article list,
with columns article_id, title, category, tags, last_updated, owner;
the help-centre style guide; any approved product facts; and the
settings (knowledge-base owner, subject experts, audiences, categories,
review interval, today's date, extra customer details, security and
escalation roles). If the record is missing or holds no fix, stop and
ask. If an article-list header is missing or named differently, stop
and ask which column holds which; do not guess. If the style guide is
missing, use the defaults in step 6 and say so.

1. State the case from the record: the problem in the customer's words,
   what fixed it, who it applies to, how often it comes up, and how the
   fix was confirmed (customer, support check, or nothing). If nothing
   confirms it, the status is "Not ready". If the main fix is confirmed
   and only a secondary step is not, the status stays "Ready for
   review" and that step goes under "Check the steps".
2. Split the fix into what a customer can do and what only staff can
   do. If nothing is left for the customer, stop and say there is no
   self-service article. Staff-only parts become "contact support".
3. Compare the case with the article list. Same problem or task:
   recommend an update and say what changes. Related: link it and name
   it under "Overlapping articles". Neither: recommend a new article.
   The "Recommendation" line gives one main outcome; a line to be added
   to a related article goes under "Overlapping articles".
4. Choose one type: how-to (getting something done), troubleshooting
   (something goes wrong and the customer can fix it), question and
   answer (one to three sentences, nothing to carry out in order),
   known issue (a fault still open; status from the record; a fix date
   only from an approved product fact).
5. Keep internal notes, staff-only tools, staff names, other ticket
   numbers, engineering plans and unapproved dates out of the article.
   List each under "Kept out of the article" with the reason.
6. Write to the style guide. Where it is silent: a title naming the
   symptom or task in the customer's words, with the exact error text
   if there is one; a first sentence saying what the article helps with
   and which readers it applies to; one action per numbered step, with
   the full menu path in bold and ">" between levels, and what appears
   on screen afterwards where the record shows it; error text copied
   exactly in code format; short paragraphs; "you" for the reader; a
   body of no more than 400 words. Leave out an optional section the
   record gives nothing for, and name it under "Sections left out".
   Count the body from the first sentence to the closing line, headings
   included. The title is not counted, nor are list numbers, the ">" in
   menu paths or markup marks such as "#" and "**". Give the count
   against the limit on the "Style" line.
7. Remove every customer detail: names, email addresses, phone numbers,
   addresses, company names, account, order, invoice and ticket
   numbers, the customer's own clients, file names, screenshots, dates
   from their case, identifying quotations, and anything the settings
   add. Use a neutral placeholder where an example helps. Record each
   kind found and where, without repeating the value. The header, the
   trace and the notes for the owner may name the ticket, its dates and
   its message numbers; the article, tags and search terms may not.
8. Trace every statement and step to its source. Take out anything
   with no source, or turn it into a question. Put any step the record
   does not show working under "Check the steps".
9. Take tags and search terms from the customer's words, the error text
   and the article list. If there is no error text, say "none in the
   record". Choose the category and audience from the settings; when
   the symptom reaches more readers than can apply the fix, choose the
   audience that can carry out the steps.
10. Fill in every "Before publishing" line. A line with nothing to
    report says "None". Count the review date from today's date by the
    review interval.

Stop conditions. A security weakness, exposed personal data or a
compromised account: no public article; name the security role. A
lawyer, regulator, claim, injury or safety risk: no article on the
matter; name the escalation role. Two different fixes in the record,
or a last message saying it still fails: status "Not ready", nothing
drafted that depends on the disputed step. An answer that depends on
one customer's own setup: stop and ask.
Never write a step in which a customer would share a password or a
login code, or switch off a security setting; raise it as a question
instead.

Use the output format exactly, including the status line and the
closing lines. When you stop, print the header with the "Stopped"
status, the case summary and the closing lines. End with the "Not
completed" line: what you could not complete and what you need, or
"Nothing outstanding".
```

## What to customize

- Your help-centre style guide: voice, headings, menu-path style, closing line and length limit.
- The audiences and categories your help centre uses.
- The column headers of your article list, if they differ from the defaults.
- Who owns the knowledge base, and which product areas need a subject expert's review.
- [your review interval], and how it moves when it lands on a weekend.
- Customer details beyond the defaults, such as project names or reference codes your customers use.
- [your security role] and [your escalation role].
- Where approved product facts live, and who may approve a statement about a future change.
- The approved AI platform: ChatGPT, Claude, Copilot or Gemini, and which ticket content it may be shown.

## Version notes

- 0.1.0, 9 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried on its invented example in Claude on 9 November 2026, in one run that was not blind: the output of the example had been seen before the run's own output was written. Small clarifications made to the procedure, the pasted instructions and the example after that run have not been run again; the trial record lists them. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
