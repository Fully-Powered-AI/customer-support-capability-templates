# Customer reply drafting: trial runs on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Fable 5.2
- **Date:** 2026-11-09

This is a record of two runs of the capability template on its own invented example: one on the template as first written, and one after the template and the example were revised in answer to what the first run and an independent review found. The company, the customer, the people and the charges are all invented, and no client data was used. It shows what the template produced on one set of inputs. It is not a test in any company's environment.

## First run: the template as first written

### The inputs used

The inputs were those then in [the worked example](example.md), under "The inputs": Priya's email on ticket 4471, the earlier thread, the account record checked by Jo, tone guide TG-2, approved answers AA-7 (A1 to A6), and the sender settings with Jo's note. At that point the settings gave no review period and no send day. The template's instructions for an AI assistant and its output format were pasted in first, then the inputs. The example's own output was not read until the run was finished.

### What came out

The complete output, as returned:

```
CUSTOMER REPLY DRAFT: Priya, Studio M, ticket 4471
Status: Draft for Jo. Not sent. Review needed first: Ren, support lead,
under A5, because Priya writes "I'll be looking at other options".
Channel: email. Situation: billing issue, with a complaint, two product
questions and a request above the sender's limit. Tone: TG-2; rules 2
(answer first), 3 (one specific apology) and 5 (day-and-date dates) lead.
Sources: TG-2, 1 September 2026; AA-7, reviewed 20 October 2026; account
facts checked by Jo, Thursday 5 November 2026, 09:40.

WHAT THE CUSTOMER RAISED
1. "I upgraded to the Plus plan on Monday." Answered from the account
   record: Plus since Monday 2 November 2026.
2. "You've charged my card twice, $89 each time." Answered from the
   account record: $89.00 at 10:02 and at 10:03 on 2 November, the
   second a duplicate.
3. "This is the second billing problem this year." Answered from the
   thread: a charge taken twice on 3 March 2026, corrected the same day.
4. "I want the extra charge back." Answered from A1: full refund of the
   duplicate, within Jo's $200 limit. The refund is not yet issued.
5. "Frankly a free month for the hassle." For the support lead to decide
   (A2). Nothing offered or hinted at.
6. "Can I export class attendance to a spreadsheet?" Held: A6 covers the
   class schedule only. No approved answer covers attendance.
7. "When is the waitlist feature coming?" Answered from A3: not
   available today, no date, notify list offered.
8. "You told me 'soon' back in the summer." Answered from the thread:
   Sam's reply of 15 July 2026 used that word.
9. "If this isn't sorted this week I'll be looking at other options."
   For the support lead to read before the reply goes (A5). The reply
   does not answer it.

DRAFT REPLY
Subject: Your duplicate $89 charge: refunded today

Hi Priya,

I've refunded the duplicate $89 charge from Monday 2 November in full.
It will reach your card in 5 to 7 business days, so between Thursday
12 November and Monday 16 November. I'm sorry we charged you twice, and
you're right that it is the second time this year, after the one in
March.

On your other points:

- A free month: I've passed your request to Ren, our support lead, who
  decides these. You'll hear from me by Monday 9 November.
- Attendance export: the class schedule exports to a spreadsheet file
  from Settings, then Export. I'm confirming whether attendance can be
  exported as well and will tell you by Monday 9 November.
- Waitlist: it isn't available today, and I don't have a date to give
  you. We told you in July it was coming, without a date. We keep a
  notify list for it; reply "yes" and I'll add you.

Jo
Company T support

BEFORE SENDING
Do first: (1) Issue the $89 refund. The draft says "I've refunded" and
the account record says the refund is not yet issued. (2) Pass the
free-month request to Ren. The draft says "I've passed your request"
and Jo's note says Ren has not been asked.
Review first: Ren, support lead, reads the draft before it goes (A5).
Confirm: that the refund is issued on Thursday 5 November; the arrival
dates in the draft are counted from that day and move if it is issued
later. That no public holiday falls in the count. That the reply goes
on Thursday 5 November; if Ren's reading moves it to Friday, "Monday
9 November" becomes Tuesday 10 November.
Promises in this draft:
- The refund reaches the card between Thursday 12 November and Monday
  16 November, owned by Jo. Allowed by A1 (5 to 7 business days).
- A reply on the free month by Monday 9 November, owned by Jo. Allowed
  by A2 (say when she will hear) and A4 (two business days). Record it
  on ticket 4471.
- A reply on attendance export by Monday 9 November, owned by Jo.
  Allowed by A4. Record it on ticket 4471.
- Adding Priya to the waitlist notify list if she says yes, owned by
  Jo. Allowed by A3.
Not said, and why:
- No free month offered or hinted at (A2).
- Nothing says attendance can or cannot be exported (no approved
  answer; A6 is the schedule only).
- No date for the waitlist, and the word from the July reply is not
  repeated (A3; TG-2 rule 5).
- No comment on the July reply being wrong. The thread shows what was
  said; no approved answer says how to describe it.
- Nothing about her looking at other options, and nothing about "this
  week". The refund is issued this week but reaches the card next week.
Questions for Ren (support lead):
- Does Priya get a free month? Can you decide in time for Jo's reply
  on Monday 9 November?
- Can class attendance be exported? If so, who writes the approved
  answer?
- Do you want the reply to say anything about her looking at other
  options, or about the July reply?
Tone guide check: rule 1, first names, "I" and "we": applied. Rule 2,
answer first: the refund opens the reply. Rule 3: one apology, for the
double charge. Rule 4: no exclamation marks, no barred words. Rule 5:
every date as day and date. Rule 6: 159 words against a limit of 180.
Rule 7: signed "Jo", then "Company T support".
After sending: Jo records the three promises on ticket 4471 (A4) and
writes to Priya by Monday 9 November with the answers on the free
month and attendance export. Jo adds her to the notify list only if
she says yes.

Prepared for Jo. Nothing has been sent, refunded or recorded by the
assistant.

What I could not complete, and what I need:
- Whether attendance can be exported: an approved answer is needed.
- The free month: Ren's decision is needed.
- The settings give no review period for approved answers. AA-7 was
  reviewed 16 days before the message and I treated it as current.
```

### What was observed

**What worked**

- Every part of the output format was produced, including the status line, the sources line and the closing line.
- All nine things in the customer's message were numbered. Nothing was skipped, including the remark about looking at other options.
- The two traps in the example were caught. The refund not yet issued went first under "Do first", and the attendance question was held instead of stretching the schedule-export answer to cover it.
- The free month was neither offered nor hinted at, and the waitlist got no date.
- The mention of leaving put the support lead in the status line as second reader, with the rule.
- No stop condition applied. The inputs held no card number, password or login code, and the reply asks for none.
- The reply came to 159 words against the tone guide's limit of 180.
- Against the template's review checklist, items 1 to 3 and 5 to 7 hold on reading the draft. Items 4, 8 and 9 (the refund actually issued, the support lead's reading, the sending) are a person's steps and were not done by the run, as intended.

**Where the instructions were unclear or a guess was needed**

- The instructions ask for one of four results for every numbered point, but three of the nine points are statements of fact and one is a remark about leaving. None of the four results fits them well. The run marked confirmed statements "Answered from" the record or thread and marked the remark as one for the support lead to read. The published example at the time worded these differently ("Confirmed by the thread", "Not answered in the reply").
- The instructions refer to "[your review period]" for approved answers, and the example's settings do not give one. The run treated answers reviewed 16 days earlier as current and said so.
- The "Confirm" line is defined as the place for customer statements that cannot be checked. Here every statement could be checked, so the run used the line for the date assumptions instead. The format does not say what to write when there is nothing to confirm.
- "5 to 7 business days" had to be turned into dates because the tone guide asks for day-and-date dates. The run counted from the day of the refund and assumed no public holidays. The instructions do not say whether to convert a range like this or leave it as the approved answer words it.
- A2 says to tell the customer when they will hear, and A4 allows a promise of a reply in two business days. Whether the sender can promise the support lead's decision by that day is not settled by either. The run promised a reply, not a decision, and asked the support lead.
- Jo's note says Ren has not been asked about the free month, while the natural wording is "I've passed your request". The run treated this as a second action to do first. The instructions name only the refund as their example of such an action.

The example's output at the time also differed from this run and from the template's own format: it had no "Sources" or "Confirm" line and no closing note, it worded the results for statements its own way, and its reply called the July answer unfair and quoted the word the tone guide bars. Those were faults in the example, not in the run.

## What was changed after the first run

Each unclear point above led to a change in the template, and the example was rewritten to follow it.

- **Results for every kind of point.** A question, request or complaint is still Answered, Held, Declined or For a role to decide. A statement of fact is now Confirmed or Cannot be checked, and a passing remark is Noted, with the second reader named where a rule sends it to one.
- **No judgement, no barred word.** The reply says what a confirmed statement's source shows and no more, and a word the tone guide bars stays out of the reply even in a quotation.
- **Review period.** The example's settings now give one (90 days), and the template says what to do when none is set.
- **"Confirm" and the other notes** may say "None", and "Confirm" also takes dates the draft counted.
- **Periods and dates.** A period the sender does not control, such as "5 to 7 business days", stays in the approved answer's wording. A promise the sender will keep gets a day and date counted from the send day, listed under "Confirm".
- **A reply is not a decision.** Permission to promise a reply by a day is not permission to promise another role's decision by that day.
- **Every assumed action** goes under "Do first", including a request the reply says has been passed on.
- **A last line,** "Not completed, and what is needed", is now part of the output format.
- **Send day.** A run on the revised template, before the example gave a send day, counted the follow-up date from the date of the session instead of the date of the message. Its output is not reproduced here. The settings now carry the send day, and the template says what to count from when none is given.

## Second run: the revised template and example

### The inputs used

The inputs are exactly those now in [the worked example](example.md), under "The inputs", including the review period and the send day. The revised instructions for an AI assistant and the revised output format were pasted first, then the inputs, into a new session with no files and no tools. That session saw neither the example's output nor the first run.

### What came out

The complete output, as returned, with long lines wrapped for reading:

```
CUSTOMER REPLY DRAFT: Priya (Studio M), Ticket 4471
Status: Draft for Jo. Not sent. Review needed first: support lead (Ren),
rule A5, because the customer says she will be "looking at other
options".
Channel: email. Situation: duplicate $89 charge on the Plus upgrade,
confirmed and not yet refunded; second double charge reported this year;
customer upset, has waited since Thursday 5 November 09:12, and was told
on 15 July that the waitlist was "coming soon". Tone: TG-2, led by rules
2 (answer first), 3 (one specific apology) and 5 (day and date, barred
words).
Sources: TG-2, 1 September 2026; AA-7, reviewed 20 October 2026, inside
the 90-day review period (current to 18 January 2027); account facts
checked by Jo (support agent), Thursday 5 November 2026, 09:40.

WHAT THE CUSTOMER RAISED
1. Subject: "Charged twice AGAIN??" Complaint: Answered from the account
   record and A1 (duplicate confirmed; refund in full).
2. "I upgraded to the Plus plan on Monday." Statement of fact: Confirmed
   by the account record: Plus, $89 a month, since Monday 2 November
   2026.
3. "You've charged my card twice, $89 each time." Statement of fact:
   Confirmed by the account record: $89.00 at 10:02 and $89.00 at 10:03
   on 2 November, same card; the second is a duplicate.
4. "This is the second billing problem this year." Statement of fact:
   Confirmed by the earlier thread: on 3 March 2026 Priya reported a
   charge taken twice after a card update, and support corrected it the
   same day.
5. "I want the extra charge back." Request: Answered from A1 (refund the
   duplicate in full; $89 is within Jo's $200 limit; reaches the card in
   5 to 7 business days).
6. "Frankly a free month for the hassle." Request: For the support lead
   to decide (A2).
7. "Can I export class attendance to a spreadsheet?" Question: Held: A6
   covers class schedule export only; nothing covers attendance.
8. "When is the waitlist feature coming?" Question: Answered from A3
   (not available today; no date; a notify list exists).
9. "You told me 'soon' back in the summer." Statement of fact: Confirmed
   by the earlier thread: on 15 July 2026 Sam replied "It's on our list
   and coming soon."
10. "If this isn't sorted this week..." Request: Answered from A1 for
    the refund only (issued Thursday 5 November; arrival on the card is
    5 to 7 business days). The free month and attendance follow-up fall
    on Monday 9 November, after this week; see Questions for Ren.
11. "...I'll be looking at other options." Passing remark: Noted:
    support lead reads first (A5).

DRAFT REPLY
Subject: Your extra $89 charge

Hi Priya,

I've refunded the extra $89 charge in full today, Thursday 5 November. A
refund reaches your card in 5 to 7 business days.

You upgraded to Plus on Monday 2 November and we charged your card $89
at 10:02 and again at 10:03. The second charge was a duplicate, and I'm
sorry we charged you twice. You also reported a charge taken twice on 3
March, which we corrected the same day.

- Free month: Ren, our support lead, decides these. I've passed your
  request to Ren and I'll write to you by Monday 9 November with where
  it stands.
- Attendance export: I'm confirming whether class attendance exports to
  a spreadsheet and will tell you by Monday 9 November.
- Waitlist: it isn't available today and I can't give you a date. On 15
  July we told you it was on our list. There is a notify list for it;
  reply to this email and I'll add you.

You'll hear from me next by Monday 9 November.

Jo
Company T support

BEFORE SENDING
Do first: (1) Issue the $89 refund for the 10:03 charge on 2 November;
the draft says it is done. (2) Pass the free month request to Ren; the
draft says it has been passed on. (3) Record both Monday 9 November
follow-up promises on the ticket (A4).
Review first: Ren, support lead, rule A5 (customer mentions leaving).
Ren reads the message and this draft before it goes.
Confirm:
- The refund shows as issued in the account record before sending.
- Monday 9 November is two business days counted from the send day,
  Thursday 5 November (Friday 6, Monday 9). If the reply goes on a later
  day, change "today, Thursday 5 November" and recount both follow-up
  dates.
Promises in this draft:
- A reply on where the free month request stands, by Monday 9 November,
  owned by Jo. Allowed by A4 and A2. This is a reply, not Ren's
  decision.
- An answer or update on attendance export, by Monday 9 November, owned
  by Jo. Allowed by A4.
- Adding Priya to the waitlist notify list if she replies, no date
  because it depends on her reply, owned by Jo. Allowed by A3.
- The refund reaching the card in 5 to 7 business days is not Jo's to
  control; it is left in A1's wording.
Not said, and why:
- Any offer or hint of a free month or credit (A2).
- Any date or timing for the waitlist, and the quoted word from the 15
  July reply (A3; TG-2 rule 5 bars it even in a quotation).
- That the 15 July reply was wrong, or an apology for it (no checked
  fact or approved answer says so; raised with Ren below).
- That attendance can or cannot be exported, and the class schedule
  export in A6 (a nearby answer that does not cover attendance).
- Any response to "looking at other options" (A5 gives no wording; Ren
  reads first).
- Any promise that everything will be sorted this week (nothing allows
  it).
- Sam's name (fault is not passed to a colleague).
Questions for Ren:
1. Do you approve this draft going out under A5?
2. What is your decision on the free month, and will Jo have it before
   Monday 9 November?
3. Can class attendance be exported to a spreadsheet? A6 covers the
   class schedule only.
4. Should the reply say anything more about the 15 July "coming soon"
   reply, given A3 now bars that wording?
5. Priya asked for this to be sorted this week, and two follow-ups land
   on Monday 9 November. Do you want to answer any of them sooner?
Tone guide check:
- Rule 1: first names; "I" for Jo's actions, "we" for the company.
- Rule 2: the refund is the first sentence.
- Rule 3: one apology, for charging twice, which the account record
  confirms; no "any inconvenience".
- Rule 4: no exclamation marks; neither barred word used.
- Rule 5: every commitment has a day and date; "soon" and "shortly" do
  not appear.
- Rule 6: about 175 words including subject and sign-off, under the 180
  limit.
- Rule 7: signed "Jo", then "Company T support".
After sending:
- Reply to Priya on where the free month request stands, Monday 9
  November, Jo.
- Reply to Priya on attendance export, Monday 9 November, Jo.
- Add Priya to the waitlist notify list if she replies, on the day she
  replies, Jo.

Prepared for Jo. Nothing has been sent, refunded or recorded by the
assistant.
Not completed, and what is needed: (1) The attendance export question is
unanswered; it needs an approved answer or a checked fact from Ren. (2)
The free month is undecided; it needs Ren's decision, and Jo has not yet
asked. (3) The A5 read is outstanding; Ren must read this before it
goes.
```

### What was observed

**What worked**

- Every line of the output format was produced, including "Sources", "Confirm" and the new last line.
- Each point got a result of the right kind. The four statements of fact were marked Confirmed with the record or the thread named, and the remark about other options was marked Noted with the support lead and rule A5.
- Both actions the wording assumes went under "Do first": issuing the refund, and passing the free-month request to Ren.
- The attendance question was held, and the schedule-export answer was kept out of the reply so it could not be read as a yes.
- The free month was neither offered nor hinted at. The reply promises word on "where it stands", and the notes say this is a reply, not Ren's decision.
- The reply says what was said in July without the barred word and without calling that answer right or wrong; both are raised as a question for Ren.
- "5 to 7 business days" was left in the approved answer's wording. "Monday 9 November" was counted from the send day and listed under "Confirm" with the day it was counted from.
- No stop condition applied. The inputs held no card number, password or login code, and the reply asks for none.
- The reply body is 171 words by our count, 176 with the subject line, against the tone guide's limit of 180. The run's own figure was "about 175".

**Where the instructions were still unclear or the run fell short**

- The run wrote the kind of point ("Statement of fact:", "Request:") in front of each result. The output format lists the results by kind and does not say whether the kind is printed. Either reading is usable.
- The run split Priya's last sentence in two: "sorted this week" as a request, and "looking at other options" as a remark. It marked the first "Answered from A1 for the refund only", which stretches Answered; Held, with the question it did put to Ren, would have been the stricter result. It also listed the subject line as a point of its own.
- Tone guide rule 5 asks for dates as day and date. The reply gives "3 March" and "15 July" without the weekday, and the run's tone check reports only that commitments carry a day and date. The sender would need to add the weekdays or drop the dates.
- "Do first" includes recording the follow-up promises on the ticket. A4 requires the record, but the wording of the reply does not assume it, so it belongs under "After sending".
- The notes for the sender quote the barred word when describing the July reply. The rule covers the reply to the customer, and the reply does not use it.

## Differences between the second run and the published example

Both follow the same format and reach the same results on the refund, the free month, the attendance question, the waitlist and the second reader. They differ in these ways:

- The run lists eleven points and prints the kind of each; the example lists nine and does not.
- The run's reply restates the two charge times and the March correction and is 171 words; the example's is 135 and says only that this is the second billing problem this year.
- The run's reply says "I've refunded the extra $89 charge in full today, Thursday 5 November"; the example gives no day for the refund.
- On the waitlist the run says "we told you it was on our list"; the example says "we told you it was coming, without a date". The run asks Priya to reply to be added to the notify list; the example asks whether she would like that.
- The run puts recording the promises under "Do first"; the example puts it under "After sending".
- The run lists the refund period as a note under the promises; the example lists it as a promise allowed by A1.
- The run asks Ren five questions, including whether the draft may go and whether anything can be answered sooner than Monday; the example asks three.
- The run's reply gives two past dates without a weekday; the example's reply has none of that kind.

## Shortcomings of these trials

- Two runs, one model, one product, on the inputs the template's own example was written around. They say nothing about messier inputs.
- The second run tried a template that had been revised to answer the first run, on the same example. Agreement between the two is expected and is weaker evidence than a run on new inputs.
- None of the stop conditions (a lawyer, an injury, exposed personal data, a card number in the message) was exercised, and neither was the case of missing approved answers, a statement that cannot be checked, or a missing review period.
- The instructions and output format were followed as written text in a session, not installed as a packaged version.
- Nobody played the sender or the support lead, so the review steps that belong to people were not carried out.
