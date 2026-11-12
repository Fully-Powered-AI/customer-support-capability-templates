# Customer satisfaction detractor follow-up: an invented example

*Illustrative example with invented data.* The business, its customers, its staff, the survey responses, the tickets, the log and every number below are invented. Firm A is an invented IT support company with 25 staff that looks after the computers, networks and printers of small offices. Every ticket it closes sends a one-question satisfaction survey (CSAT, 1 to 5), and some customers also answer a recommendation survey (NPS, 0 to 10). On Monday 9 November 2026 its support lead runs the workflow template on the week of 2 to 8 November.

The inputs come first, in full, so the template can be run on them. The report follows.

## The inputs

### The settings

```
REPORT SETTINGS
Week: Monday 2 November to Sunday 8 November 2026. Prepared: 9 November 2026.
Report for: support lead. Dates in the exports are in our own time zone.
CSAT scale and cut-offs, small sample, comparison minimum, change worth
naming, repeat window, matters that need a person now: the defaults.
Sign-off for messages: [Name], [owner's role], Firm A
Column mapping: none; the exports use the default headers.

OWNER LIST
Service desk team: service desk lead
Field team: field lead
Billing: accounts lead

ACCOUNT LIST
Client C: account manager
Client H: account manager
```

### The survey export

```
Response,Date,Survey,Score,Comment,Ticket,Customer
R-4398,2026-11-01,CSAT,5,,T-1180,Client A
R-4399,2026-11-02,CSAT,5,"Quick and friendly.",T-1184,Client A
R-4402,2026-11-02,CSAT,1,"Third time this month the second-floor printer has dropped off the network. Each time someone fixes it and a week later it's back.",T-1187,Client C
R-4404,2026-11-02,CSAT,4,,T-1189,Client L
R-4407,2026-11-03,CSAT,5,,T-1192,Client M
R-4410,2026-11-03,NPS,9,"Reliable.",,Client N
R-4413,2026-11-03,CSAT,3,"Fixed, but it took a while.",T-1196,Client E
R-4417,2026-11-03,CSAT,2,"Waited from Friday morning until Monday for a reply to a simple account lockout.",T-1203,Client F
R-4419,2026-11-03,CSAT,5,,T-1205,Client D
R-4421,2026-11-04,CSAT,4,,T-1207,Client A
R-4423,2026-11-04,CSAT,5,"Sorted in ten minutes.",T-1209,Client P
R-4425,2026-11-04,NPS,8,,,Client Q
R-4427,2026-11-04,CSAT,4,,T-1212,Client L
R-4429,2026-11-05,CSAT,5,,T-1215,Client M
R-4431,2026-11-05,CSAT,1,"We are seriously thinking about moving to another provider. The laptop for our new starter still isn't set up after a week.",T-1219,Client H
R-4433,2026-11-05,CSAT,4,,T-1220,Client R
R-4435,2026-11-05,NPS,10,"Always there when we need you.",,Client S
R-4437,2026-11-05,CSAT,5,,T-1222,Client G
R-4440,2026-11-06,CSAT,2,"The invoice charged us for a call-out that our plan covers.",T-1224,Client J
R-4442,2026-11-06,CSAT,4,,T-1225,Client N
R-4445,2026-11-06,NPS,4,"Support is fine, but you never tell us about an outage until we ring you.",,Client B
R-4447,2026-11-06,CSAT,5,,T-1227,Client P
R-4449,2026-11-07,NPS,6,,T-1230,Client K
R-4450,2026-11-07,CSAT,3,,T-1231,Client T
R-4451,2026-11-07,CSAT,5,,T-1232,Client E
R-4452,2026-11-08,CSAT,,"Fixed in the end, but nobody told us the engineer would be two hours late.",T-1233,Client D
R-4453,2026-11-08,NPS,9,,,Client U
R-4454,2026-11-08,CSAT,4,,T-1234,Client R
R-4455,2026-11-08,CSAT,5,,T-1235,Client V
R-4456,2026-11-08,CSAT,4,,T-1236,Client W
```

### The ticket export

The tickets named by this week's low-score and comment-only responses.

```
Ticket,Customer,Team,Handled by,Opened,Closed,Subject,Notes
T-1187,Client C,Service desk,Tech 2,2026-10-30,2026-11-02,"Second-floor printer offline","30 Oct: printer not on the network; restarted, back online. 2 Nov: no further report; closed. Earlier tickets for the same printer: T-1102 (9 Oct) and T-1151 (21 Oct), each closed after a restart."
T-1203,Client F,Service desk,Tech 4,2026-10-30,2026-11-02,"Account locked out","30 Oct 08:50: email received. 2 Nov 08:15: assigned. 2 Nov 08:40: account unlocked; customer confirmed. 2 Nov 09:05: closed."
T-1219,Client H,Field,Tech 6,2026-10-28,2026-11-04,"New starter laptop","28 Oct: laptop ordered. 29 Oct: setup visit booked for 3 Nov. 30 Oct: laptop received at our office. 2 Nov: visit moved by us to 6 Nov, engineer unavailable. 4 Nov: laptop delivered to site; this ticket closed; setup moved to T-1226."
T-1224,Client J,Field,Tech 5,2026-11-03,2026-11-05,"Monitor flickering","3 Nov: remote check, cable suspected. 5 Nov: site visit, cable replaced, monitor working. Closed."
T-1230,Client K,Service desk,Tech 1,2026-11-06,2026-11-06,"VPN not connecting","6 Nov 14:05: reported by phone. 6 Nov 14:45: settings corrected; customer connected. Closed."
T-1233,Client D,Field,Tech 5,2026-11-06,2026-11-07,"Network switch replacement","6 Nov: visit booked for 7 Nov 09:00. 7 Nov 11:10: engineer on site; switch replaced; network checked. Closed."
```

### The follow-up log

```
FOLLOW-UP LOG, covering 10 August to 8 November 2026
Response,Date,Customer,Owner,Status,Status date
R-4290,2026-10-13,Client C,service desk lead,Called back,2026-10-14
R-4361,2026-10-27,Client E,field lead,Called back,2026-10-28
R-4378,2026-10-29,Client G,service desk lead,Message sent,2026-10-30
R-4385,2026-10-30,Client B,support lead,Not started,
```

### Last week's trend lines

```
TREND: 13 weeks to 1 November 2026
Week of 3 Aug 2026 | CSAT responses 22, satisfied 19, low 1, 86% | NPS responses 5, promoters 2, detractors 1, score 20 (small sample)
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
```

## The output

The report is plain text, exactly as the template sets it out.

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
- What went wrong, as far as the ticket shows: 30 Oct: printer not on the network; restarted, back online. 2 Nov: no further report; closed. The notes list two earlier tickets for the same printer, T-1102 (9 Oct) and T-1151 (21 Oct), each closed after a restart. The notes do not record any check of why the printer keeps dropping off the network.
- Suggested owner: support lead | Copy: account manager | Why: rule 1, repeat low score from Client C inside the 90-day window (R-4290, 2026-10-13)
- Draft follow-up (not sent; for the support lead to edit and send):
  "Thank you for your feedback. I'm sorry the second-floor printer has dropped off the network again. Our records show it was restarted on 30 October, and that two earlier tickets for it, from 9 and 21 October, were each closed after a restart. I will look into why it keeps happening and come back to you. Would you prefer a call or a reply by email to talk this through, and what time would suit you? [Name], support lead, Firm A"

2. R-4417 | CSAT 2 of 5 | 2026-11-03 | Client F | Ticket T-1203
- Flags: none
- Handled by: Service desk, Tech 4
- In their words: "Waited from Friday morning until Monday for a reply to a simple account lockout."
- What went wrong, as far as the ticket shows: 30 Oct 08:50: email received. 2 Nov 08:15: assigned. 2 Nov 08:40: account unlocked; customer confirmed. 2 Nov 09:05: closed. The notes do not record why the email waited from 30 Oct to 2 Nov before it was assigned.
- Suggested owner: service desk lead | Copy: none | Why: rule 5, ticket handled by the Service desk team
- Draft follow-up (not sent; for the service desk lead to edit and send):
  "Thank you for your feedback. I'm sorry you waited from Friday morning until Monday for a reply about your account lockout. Our records show your email arrived on Friday 30 October at 08:50 and your account was unlocked on Monday 2 November at 08:40. Would you prefer a call or a reply by email to talk this through, and when would suit you? [Name], service desk lead, Firm A"

3. R-4431 | CSAT 1 of 5 | 2026-11-05 | Client H | Ticket T-1219
- Flags: may leave; account manager
- Handled by: Field, Tech 6
- In their words: "We are seriously thinking about moving to another provider. The laptop for our new starter still isn't set up after a week."
- What went wrong, as far as the ticket shows: 28 Oct: laptop ordered. 29 Oct: setup visit booked for 3 Nov. 30 Oct: laptop received at our office. 2 Nov: visit moved to 6 Nov; the note gives the reason as engineer unavailable. 4 Nov: laptop delivered to site; this ticket closed; setup moved to T-1226. The notes do not record the setup itself, which was moved to T-1226; T-1226 is not in the ticket export.
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

How the figures add up: 30 rows, less R-4398 dated 1 November, leaves 29 responses: 22 CSAT with a score, 6 NPS with a score and 1 with a comment only. The 22 CSAT scores split 16 satisfied (4 or 5), 2 neutral (R-4413 and R-4450) and 4 low (R-4402, R-4417, R-4431, R-4440). The 6 NPS scores split 3 promoters (R-4410, R-4435, R-4453), 1 passive (R-4425) and 2 detractors (R-4445, R-4449). This week's CSAT is 16 ÷ 22 = 73%, and NPS is (3 − 2) ÷ 6 = 17. The last four weeks (12 October to 8 November) pool 91 CSAT responses with 68 satisfied, 75%; the four before (14 September to 11 October) pool 91 with 78 satisfied, 86%. Last week's lines cover thirteen weeks; the week of 3 August is dropped because the trend keeps the twelve most recent earlier weeks, so the header reads "13 supplied, 12 used". Client E's 3 this week (R-4413) is neutral, not low, so its earlier follow-up (R-4361) does not make it a repeat. No message has been sent: each owner edits and sends their own once the support lead confirms them.
