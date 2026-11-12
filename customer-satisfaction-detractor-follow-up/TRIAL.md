# Customer satisfaction detractor follow-up: trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Opus 5.5 (model ID claude-opus-5-5)
- **Date:** 2026-11-10
- **Template version:** 0.1.0

This is a record of one run of the workflow template on its own invented example. The business, its customers, its staff, the responses, the tickets and the numbers are invented, and no client data was used. It shows what the template produced once, on one set of inputs. It is not a test in any company's environment. Nothing was sent, no customer was contacted and no record was changed.

This is the third run on the same example. The first, by a model that had not written the template, showed where the instructions left room to guess; the instructions were revised and a second run was made and recorded. An independent review then passed the template with minor points, the instructions and the output format were tightened again, and the run recorded here was made on that version. What the earlier runs found, and what was changed after each, is at the end.

Read this run for what it is. It was made in a fresh, non-interactive session with no tools and none of the account's or the project's standing instructions loaded. Its system prompt was the fenced instruction block followed by the output format, as the template says to paste them, and its one message was the example's inputs, under "The inputs" in [the worked example](example.md), with the line "Here are this week's inputs. Please prepare the report." The session saw nothing else: not the rest of the template, not the earlier runs or their observations, not the example's output. It is the same model that revised the template, and that model set the run up and wrote these observations, so the run is blind only in that its session had no other context.

## The inputs used

The inputs in [the worked example](example.md), under "The inputs", unchanged from the earlier runs: the settings for the week of 2 to 8 November 2026, the survey export of 30 rows, the ticket export of six tickets, the follow-up log of four entries covering 10 August to 8 November 2026, and last week's thirteen trend lines.

## What came out

The full report, as the run produced it:

```
LOW SCORE FOLLOW-UP: week of 2 Nov 2026 to 8 Nov 2026

For: support lead. Prepared 9 Nov 2026. Rows in the export: 30.
Outside the week, left out: 1 (R-4398).
Responses read: 29. CSAT with a score: 22 (satisfied 16, neutral 2, low 4). NPS with a score: 6 (promoters 3, passives 1, detractors 2). Comment only: 1.
Low scores this week: 6. Needs a person now: 0. Ready to follow up: 6.
Small samples this week: NPS (6 responses).
Follow-up log: supplied, covering 10 August to 8 November 2026. Earlier weeks for the trend: 13 supplied, 12 used.

NEEDS A PERSON NOW

None.

LOW SCORES TO FOLLOW UP

1. R-4402 | CSAT 1 of 5 | 2026-11-02 | Client C | Ticket T-1187
- Flags: repeat (earlier R-4290, 2026-10-13); account manager
- Handled by: Service desk, Tech 2
- In their words: "Third time this month the second-floor printer has dropped off the network. Each time someone fixes it and a week later it's back."
- What went wrong, as far as the ticket shows: 30 Oct: printer not on the network; restarted, back online. 2 Nov: closed with no further report. The notes list two earlier tickets for the same printer, T-1102 (9 Oct) and T-1151 (21 Oct), each closed after a restart. The notes do not record any check of why the printer keeps dropping off the network.
- Suggested owner: support lead | Copy: account manager | Why: rule 1, repeat low score from Client C inside the 90-day window (R-4290, 2026-10-13)
- Draft follow-up (not sent; for the support lead to edit and send):
  "Thank you for your feedback. I'm sorry the second-floor printer has dropped off the network again. Our records show it went offline on 9 October, 21 October and 30 October, and each time it was restarted and came back online, only for the problem to return. I will look into why it keeps happening and come back to you. Would you prefer a call or a reply by email to talk this through, and what time would suit you? [Name], support lead, Firm A"

2. R-4417 | CSAT 2 of 5 | 2026-11-03 | Client F | Ticket T-1203
- Flags: none
- Handled by: Service desk, Tech 4
- In their words: "Waited from Friday morning until Monday for a reply to a simple account lockout."
- What went wrong, as far as the ticket shows: 30 Oct 08:50: email received. No entry is recorded between then and 2 Nov 08:15: assigned. 2 Nov 08:40: account unlocked; customer confirmed. 2 Nov 09:05: closed.
- Suggested owner: service desk lead | Copy: none | Why: rule 5, ticket handled by the Service desk team
- Draft follow-up (not sent; for the service desk lead to edit and send):
  "Thank you for your feedback. I'm sorry you waited from Friday morning until Monday for a reply about your account lockout. Our records show your email arrived on Friday 30 October at 08:50 and your account was unlocked on Monday 2 November at 08:40. Would you prefer a call or a reply by email to talk this through, and when would suit you? [Name], service desk lead, Firm A"

3. R-4431 | CSAT 1 of 5 | 2026-11-05 | Client H | Ticket T-1219
- Flags: may leave; account manager
- Handled by: Field, Tech 6
- In their words: "We are seriously thinking about moving to another provider. The laptop for our new starter still isn't set up after a week."
- What went wrong, as far as the ticket shows: 28 Oct: laptop ordered. 29 Oct: setup visit booked for 3 Nov. 30 Oct: laptop received at the office. 2 Nov: visit moved to 6 Nov; the note gives the reason as engineer unavailable. 4 Nov: laptop delivered to site; ticket closed; setup moved to T-1226. The notes do not record the setup itself, which was moved to T-1226; T-1226 is not in the ticket export.
- Suggested owner: account manager | Copy: none | Why: rule 2, comment says they are thinking about moving to another provider; Client H has an account manager
- Draft follow-up (not sent; for the account manager to edit and send):
  "Thank you for your feedback. I'm sorry that the laptop for your new starter was still not set up after a week. Our records show the setup visit first booked for 3 November was moved to 6 November, and the laptop was delivered to your site on 4 November. I understand you are thinking about moving to another provider, and I would like to hear more about your experience. I will look into where the setup now stands and come back to you. Would you prefer a call or a reply by email, and when would suit you? [Name], account manager, Firm A"

4. R-4440 | CSAT 2 of 5 | 2026-11-06 | Client J | Ticket T-1224
- Flags: none
- Handled by: Field, Tech 5
- In their words: "The invoice charged us for a call-out that our plan covers."
- What went wrong, as far as the ticket shows: Nothing in the ticket shows what went wrong. The notes do not record the invoice, any call-out charge or what the customer's plan covers.
- Suggested owner: accounts lead | Copy: none | Why: rule 4, comment is about an invoice (Billing)
- Draft follow-up (not sent; for the accounts lead to edit and send):
  "Thank you for your feedback. I'm sorry to hear about the call-out charge on your invoice. I will look into the charge against what your plan covers and come back to you. Would you prefer a call or a reply by email, and when would suit you? [Name], accounts lead, Firm A"

5. R-4445 | NPS 4 of 10 | 2026-11-06 | Client B | Ticket none
- Flags: repeat (earlier R-4385, 2026-10-30); open follow-up (R-4385, Not started)
- Handled by: no ticket
- In their words: "Support is fine, but you never tell us about an outage until we ring you."
- What went wrong, as far as the ticket shows: No ticket: the comment is all there is.
- Suggested owner: support lead | Copy: none | Why: rule 1, repeat low score from Client B inside the 90-day window (R-4385, 2026-10-30)
- Draft follow-up (not sent; for the support lead to edit and send):
  "Thank you for your feedback, and I'm glad the support itself has been fine. I'm sorry you have only found out about outages when you rang us. I will look into how we let you know about outages and come back to you. Would you prefer a call or a reply by email, and when would suit you? [Name], support lead, Firm A"

6. R-4449 | NPS 6 of 10 | 2026-11-07 | Client K | Ticket T-1230
- Flags: none
- Handled by: Service desk, Tech 1
- In their words: No comment given.
- What went wrong, as far as the ticket shows: Nothing in the ticket shows what went wrong.
- Suggested owner: service desk lead | Copy: none | Why: rule 5, ticket handled by the Service desk team
- Draft follow-up (not sent; for the service desk lead to edit and send):
  "Thank you for taking the time to answer our survey. Our records show you rang us on 6 November because your VPN was not connecting, and the settings were corrected that afternoon so you could connect. I would like to understand what would have made the difference for you. Would you prefer a call or a reply by email, and when would suit you? [Name], service desk lead, Firm A"

COMMENT ONLY (counted in no figure)

R-4452 (CSAT, 2026-11-08) | Client D | Ticket T-1233
- In their words: "Fixed in the end, but nobody told us the engineer would be two hours late."
- What the ticket shows: 6 Nov: visit booked for 7 Nov 09:00. 7 Nov 11:10: engineer on site; switch replaced; network checked. Closed. The notes do not record whether the customer was told the engineer would arrive later than 09:00.
- Suggested owner if followed up: field lead. The support lead decides whether to follow up.

STILL OPEN FROM EARLIER WEEKS

R-4378 | 2026-10-29 | Client G | service desk lead | Message sent, 2026-10-30
R-4385 | 2026-10-30 | Client B | support lead | Not started, no date | Same customer as R-4445 this week.

TREND: 13 weeks to 8 Nov 2026

Week of 10 Aug 2026 | CSAT responses 24, satisfied 21, low 1, 88% | NPS responses 5, promoters 3, detractors 1, score 40 (small sample)
Week of 17 Aug 2026 | CSAT responses 21, satisfied 18, low 2, 86% | NPS responses 4, promoters 2, detractors 1, score 25 (small sample)
Week of 24 Aug 2026 | CSAT responses 26, satisfied 23, low 1, 88% | NPS responses 6, promoters 3, detractors 1, score 33 (small sample)
Week of 31 Aug 2026 | CSAT responses 9, satisfied 8, low 0, 89% (small sample) | NPS responses 2, promoters 1, detractors 0, score 50 (small sample)
Week of 7 Sep 2026 | CSAT responses 23, satisfied 20, low 1, 87% | NPS responses 5, promoters 3, detractors 1, score 40 (small sample)
Week of 14 Sep 2026 | CSAT responses 25, satisfied 22, low 2, 88% | NPS responses 6, promoters 4, detractors 1, score 50 (small sample)
Week of 21 Sep 2026 | CSAT responses 22, satisfied 19, low 1, 86% | NPS responses 4, promoters 2, detractors 1, score 25 (small sample)
Week of 28 Sep 2026 | CSAT responses 24, satisfied 21, low 1, 88% | NPS responses 5, promoters 3, detractors 1, score 40 (small sample)
Week of 5 Oct 2026 | CSAT responses 20, satisfied 16, low 2, 80% | NPS responses 7, promoters 3, detractors 2, score 14 (small sample)
Week of 12 Oct 2026 | CSAT responses 25, satisfied 19, low 3, 76% | NPS responses 5, promoters 2, detractors 2, score 0 (small sample)
Week of 19 Oct 2026 | CSAT responses 23, satisfied 18, low 3, 78% | NPS responses 6, promoters 3, detractors 1, score 33 (small sample)
Week of 26 Oct 2026 | CSAT responses 21, satisfied 15, low 4, 71% | NPS responses 4, promoters 1, detractors 2, score -25 (small sample)
Week of 2 Nov 2026 | CSAT responses 22, satisfied 16, low 4, 73% | NPS responses 6, promoters 3, detractors 2, score 17 (small sample)

Last four weeks against the four before:
- CSAT: 75% (91 responses) against 86% (91 responses): lower by 11 points
- NPS: 21 responses against 22: too few responses to compare (fewer than 40 scored responses in each four-week period).

QUESTIONS FOR THE SUPPORT LEAD

1. Client B scored low again this week (R-4445), and their earlier follow-up R-4385 (2026-10-30) is still Not started. Should one follow-up cover both? What was R-4385 about? The log does not hold its score or comment.
2. R-4431: the laptop setup for Client H was moved to T-1226, which is not in the ticket export. The account manager will need to know whether the 6 Nov setup visit took place and where the setup stands. Can T-1226 be supplied?
3. R-4440: the accounts lead will need the invoice, the call-out it charges for and Client J's plan terms. None of these are in the inputs.
4. The repeat flags for R-4402 (Client C, earlier R-4290) and R-4445 (Client B, earlier R-4385) assume that every follow-up log entry was a low score. The log does not show scores. Is that assumption right?

Prepared for the support lead. Nothing has been sent, offered or changed.
```

## What was observed

**What held.** Every section of the output format came out, in order, and every end check held. The row outside the week (1) plus the responses read (29) equal the 30 rows. The CSAT groups (16, 2, 4) add up to 22, the NPS groups (3, 1, 2) add up to 6, and with the one comment-only response they give the 29 read. The six low scores each appear once, none under Needs a person now. Every trend figure agrees with its counts, and the twelve earlier figures agree with last week's lines. CSAT for the last four weeks is lower by 11 points (75% of 91 against 86% of 91); NPS is not compared, with 21 and 22 responses against a minimum of 40. The counts, flags, owners, trend and comparison are the same as the two earlier runs'.

**How the revised rules played out.**

- **Open follow-up flag.** R-4445 carries "open follow-up (R-4385, Not started)" beside its repeat flag, and the Still open line for R-4385 says "Same customer as R-4445 this week." Both lines say so, as step 5 now asks.
- **Something the business itself did.** R-4431's draft says the setup visit "was moved to 6 November", stating the event and not who caused it. The "What went wrong" line, which is for the support lead, gives the note's reason ("engineer unavailable").
- **Dates.** The heading, the TREND line and the week lines use day, short month and year. The run also wrote "Prepared 9 Nov 2026" in that style, while the follow-up log's period kept the log's own wording.
- **Reason for no comparison.** "fewer than 40 scored responses in each four-week period", one of the set forms.
- **The drafts.** All six offer a call or a reply by email and ask which suits and when; the longest is 103 words. Five say sorry for what the customer went through (R-4402, R-4417, R-4431, R-4440, R-4445); none admits fault or says whose fault it was. Four say the owner will look into something and come back (R-4402, R-4431, R-4440, R-4445), with no outcome and no date. Each fills in the owner's role in the sign-off and leaves "[Name]" for the owner. The weekdays in R-4417's draft (Friday 30 October, Monday 2 November) are worked out from the dates and are correct.

**Where the run departed from the template.**

1. R-4402's draft says the printer "went offline on 9 October, 21 October and 30 October, and each time it was restarted and came back online". The notes give 9 and 21 October only as the dates of two earlier tickets, each "closed after a restart"; reading them as the days it went offline and came back is beyond the notes. The independent review found the same kind of reading in an earlier example.
2. R-4417's "What went wrong" line puts a reading among the events ("No entry is recorded between then and 2 Nov 08:15") instead of the one sentence on what the notes do not record, here the reason for the wait.
3. Three lines paraphrase the notes rather than keeping their terms: "2 Nov: closed with no further report" (R-4402; the note reads "no further report; closed"), "laptop received at the office" and "ticket closed" (R-4431; the note reads "at our office" and "this ticket closed").

**Where the instructions still leave room to guess.**

1. The pasted instructions do not say that the follow-up log holds only earlier low scores; the template's Inputs section does. The run asked about it (question 4), which is a fair question from the block alone.
2. Whether "Prepared [date]" in the header follows the short date style. The run used it.
3. Whether a draft repeats back a customer's word that they may leave. R-4431's draft does ("I understand you are thinking about moving to another provider").
4. A ticket that the notes refer to but the export lacks (T-1226). The "[ticket] not found in the ticket export" wording is for the ticket a response names; the run used a sentence on what the notes do not record and a question, as the second run did.
5. Whether a draft for a score with no comment may recount the ticket's events. R-4449's draft does, from the ticket.

**What was not exercised.** No header was unknown, no required column or export missing, no score out of its scale and no time zone stated, so no stop was reached. No response met a matter that needs a person now, no comment held a card number or wording addressed to the assistant, no response ID appeared twice, and the follow-up log, the account list and the ticket export were all supplied. The refusals (asked to send, to offer a credit, to rank or blame staff) were not tried.

## The example's output

The output published in the worked example is this run's output with five corrections, each to make a line follow the template, and nothing else changed:

- R-4402, "What went wrong": "2 Nov: closed with no further report." became "2 Nov: no further report; closed.", the note's own words.
- R-4402, the draft: "Our records show it went offline on 9 October, 21 October and 30 October, and each time it was restarted and came back online, only for the problem to return." became "Our records show it was restarted on 30 October, and that two earlier tickets for it, from 9 and 21 October, were each closed after a restart."
- R-4417, "What went wrong": "No entry is recorded between then and" was removed from the events, and the sentence "The notes do not record why the email waited from 30 Oct to 2 Nov before it was assigned." was added.
- R-4431, "What went wrong": "at the office" became "at our office", and "ticket closed" became "this ticket closed", the note's own words.

## The earlier runs, and what was changed

### The first run

The first run, on 10 November 2026 in Claude Code, used Claude Sonnet 5.5 (model ID claude-sonnet-5-5), a model that had not written the template. It read the template and only the example's inputs, produced the report, and only then read the example's own output and the reviewer checklist. Its counts, flags, owners and rules, trend figures, comparison, still-open list and three questions all agreed with the example then published. It differed from that example, and recorded these points:

- The example said "12 supplied" for earlier weeks; the run wrote "13 supplied". The format did not say whether to count the lines given or the weeks used.
- The example's "What went wrong" lines added readings that were not dated events ("This is the third ticket for the same printer in a month", "The notes record no cause", "The notes do not say why it waited", "The notes do not record the customer being told of the delay"). The run kept to dated events and used "Nothing in the ticket shows what went wrong." for R-4440 and R-4449; the example had listed R-4449's events and then added that sentence.
- The example's drafts apologised and conceded ("I am sorry it has kept happening", "You are right that this is the third time"); the run's drafts acknowledged what the customer said without apologising. The template was silent on both.
- The example's R-4440 draft said "I am going to check the charge against your plan and will come back to you with what I find" and offered no call or reply. The template neither allowed nor banned such a promise.
- The example's drafts offered a call; the run's offered a call or a reply by email and asked which suited, as the instruction said.
- In the example's output, "Your score tells us we could have done better" (R-4449's draft) was an inference, and "we did not pick it up until Monday morning" and "delivered ... without being set up" were readings of the notes rather than their words. The independent review added that R-4402's draft read the dates of the two earlier tickets as restart dates ("restarted on 9, 21 and 30 October").
- Its record named as open: whether the assistant fills the name in the sign-off; whether to list events or write the "Nothing in the ticket" sentence when the events show nothing wrong; apology and admitting fault; promising to look into something; repeating back a threat to leave; date styles; the free reason after "too few responses to compare"; and what "Responses read" means.
- Its record named two defects in the template: the version notes and the public page said it had not been tried, which the run superseded; and the instruction block said to paste it "followed by the output format above", so a reader who pasted only the block got "use the output format exactly" with no format.

Changed after the first run, before the second:

- **The version notes** were changed to say the template was tried, in two runs, and that the second was recorded.
- **The paste note** says to paste the output format directly after the block, because the block refers to it, and the block's closing paragraph now points to the format pasted after it.
- **Responses read** is defined in the procedure, the pasted instructions and the note under the output format: the rows dated inside the week, each response ID counted once, comment-only responses included.
- **The trend count.** The header line now reads "[n] supplied, [n] used", and the pasted instructions ask for both.
- **What went wrong.** The dated events that bear on the score or the comment; "Nothing in the ticket shows what went wrong." in place of the events when none shows anything going wrong; and one plain sentence on what the notes do not record where the comment raises something they do not cover. The comment-only section follows the same rule.
- **The drafts.** They offer a call or a reply and ask which suits and when. They may say sorry for what the customer went through but may not admit fault or say whose fault it was. They may say the owner will look into a question the comment raises and come back, with no outcome and no date. The sign-off fills in the owner's role and leaves any name for the owner. The reviewer checklist checks these.
- **The example's output** was replaced with the output of the second run.
- **An acceptance test** uses a column headed `Technician` for the unknown-header case.

### The second run

The second run, on 10 November 2026 in Claude Code, used Claude Opus 5.5 (model ID claude-opus-5-5), the model that had revised the template, in a working session with the whole template, the first run and its observations in view, so it was not blind. Its output was published as the example's output until this revision. Its counts, flags, owners and rules, trend, comparison, still-open list and three questions matched the first run's. It recorded these points as still open:

1. R-4431's draft repeats the ticket note that the visit was "moved by us". It is a fact from the ticket, which the drafts may use, but it sits close to the admission of fault they may not make, and the template does not say which wins when a note records the business's own action.
2. Whether a draft tells the customer who is copied. The run did so once, in R-4402.
3. Whether a draft repeats back a customer's word that they may leave. The run did not.
4. A ticket that the notes refer to but the export lacks (T-1226). The format's "not found in the ticket export" is for the ticket a response names; the run used a sentence on what the notes do not record and a question.
5. The reason after "too few responses to compare" is still free wording.
6. The report heading has no set date style; the run wrote dates in full.

After the second run, the public page's line on what has been checked was changed to say the same as the version notes, and the credits line was shortened.

### Changed after the independent review, before the run recorded above

- **The pasted instructions** now carry the handling that sat only in the prose: stop and ask if the survey export or the ticket export is missing; "[ticket] not found in the ticket export" for one missing ticket, with a question; a response ID that appears twice is counted once, and if the rows differ the assistant asks which is right; "Not checked: no follow-up log." under Still open; "Earlier weeks not supplied; nothing compared." in place of the comparison; and "Account list not supplied." in the header.
- **Something the business itself did.** Where a ticket note records something the business did, such as moving a visit, a draft states the event, not who caused it. The reviewer checklist checks it. (Second run, point 1.)
- **Open follow-ups on both lines.** A new flag, "open follow-up ([Response], [status])", on a low score whose customer has a log entry still Not started or Message sent, to match "Same customer as [Response] this week." on the Still open line.
- **Set wording.** The reason after "too few responses to compare" is one of four set forms, and dates in the heading, the TREND line and the week lines are day, short month and year. (Second run, points 5 and 6.)
- **Columns to ignore.** The column mapping may list columns to ignore, and "What to customize" says to list them, since a typical survey export has many more columns than the defaults.
- **The example's output** was replaced as described above. Its inputs are unchanged.
