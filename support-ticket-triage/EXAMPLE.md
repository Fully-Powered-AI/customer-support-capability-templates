# Support ticket triage: an invented example

*Illustrative example with invented data.* The company, its customers, the tickets, the rules and the known issues below are all invented. An invented 45-person company sells booking software to salons and studios. On Monday 9 November 2026 its queue manager exports the ten unassigned tickets that arrived since Thursday and runs the capability before the team picks anything up.

The inputs come first, in full, so the template can be run on them. The triage sheet follows.

## The inputs

### The time of the export and working hours

```
Queue: Unassigned
Export taken: Monday 9 November 2026, 09:15
Working hours: Monday to Friday, 08:00 to 18:00. One working day is 10 working hours.
A ticket that arrives outside working hours starts its clock at the next 08:00.
```

### The triage rules

```
SUPPORT TRIAGE RULES, version 6 (owner: support lead)

CATEGORIES. One per ticket. Follow the cause, not the first symptom. If a
ticket holds a fault and a request, the fault is the category and the
request is noted.
- Fault: something in our product that worked and has stopped, or behaves wrongly.
- How-to: the customer wants to know how to do something the product does.
- Billing: charges, refunds, invoices, plan changes.
- Account access: cannot sign in, locked out, staff permissions.
- Integration: connecting or syncing with an outside calendar or accounting tool.
- Data: imports, exports, missing or wrong records.
- Request: the customer wants something the product does not do.
- Security: unauthorised access, or one customer's information shown to another.

PRIORITIES AND FIRST-REPLY TARGETS
- P1, 1 working hour: a business cannot take bookings or payments at all;
  records lost; one customer's information shown to another; any security report.
- P2, 4 working hours: a main function (booking, payment, reminders) is
  broken with no workaround, but the business can still operate another way.
- P3, 1 working day: something broken that has a workaround; a problem
  outside the main functions; a billing problem on one account.
- P4, 2 working days: questions, requests, cosmetic faults.
Raise one level, once only, when either is true:
- the ticket is past its first-reply target at the time of the export;
- the same fault appears in three or more open tickets.
A raised ticket takes the first-reply target of its raised level, counted
from when it arrived, not from when it was raised.

ROUTES
- Frontline: how-to questions; any ticket that matches a known issue with
  a posted workaround or answer.
- Senior support: faults that need investigating, integration, account
  access, data.
- Billing desk: refunds, double charges, invoice changes.
- Product inbox: requests. A request inside another ticket is copied there
  by the agent who takes the ticket.
Engineering on-call and the security lead are reached only through an
escalation, never by routing.

ESCALATION CONDITIONS. The queue manager decides each one.
- E1 Security: any report of unauthorised access, or of one customer's
  information shown to another. First call: security lead.
- E2 Outage: a business cannot take bookings or payments at all.
  First call: engineering on-call.
- E3 Pattern: the same fault in three or more open tickets. Raised as one
  item. First call: engineering on-call.
- E4 Customer at risk: the customer asks for a manager, or says they may
  cancel or move to another system. First call: support lead.
```

### The known issues

```
KNOWN ISSUES, as of Friday 6 November 2026

KI-14. Since release 4.12 (3 November), new bookings can take several
hours to appear in a connected outside calendar. Workaround: Settings >
Calendar > Sync now. Fix in progress. Posted to the help centre 5 November.

KI-15. Receipt PDFs show our previous logo. Cosmetic; receipts remain
valid. Fix scheduled for release 4.13. Posted answer: corrected copies can
be downloaded again after the release.
```

### The queue export

```
Ticket,Arrived,Customer,Plan,Channel,Replies sent,Subject,Message
T-4181,Fri 6 Nov 16:40,Customer A,Standard,Email,0,"Bookings not reaching my calendar","Bookings made this morning still are not in my outside calendar. It used to take a minute. I keep double-checking by hand."
T-4182,Sat 7 Nov 10:05,Customer B,Standard,Email,0,"Charged twice for November","My card statement shows two charges of $49 on 1 November. Please refund one."
T-4183,Mon 9 Nov 08:02,Customer C,Multi-site,Email,0,"Nobody can book: payment error","Since about 7:45 this morning every client who tries to book at any of our four locations gets 'Something went wrong (code 5031)' at the payment step. We take no phone bookings, so right now we cannot take bookings at all."
T-4184,Mon 9 Nov 08:20,Customer D,Standard,Email,0,"Payment step error 5031","Clients tell me they cannot pay online this morning. The page shows code 5031. Phone bookings still work."
T-4185,Mon 9 Nov 08:41,Customer E,Standard,Chat,0,"Online checkout down?","Is there an outage? Getting code 5031 when a client tries to check out."
T-4186,Sat 7 Nov 14:30,Customer F,Standard,Email,0,"Adding a staff member","We have hired a second stylist. How do I add her so clients can book with her?"
T-4187,Thu 5 Nov 11:15,Customer G,Multi-site,Email,0,"Export missing clients, still waiting","This is the third time I have written about this. The client export I ran on 4 November left out every client added since 1 October. We have a mailing going out this week and need the full list. If this is not sorted by Wednesday we will start looking at other systems."
T-4188,Mon 9 Nov 08:55,Customer H,Standard,Email,0,"Wrong client on my screen","When I opened a booking at about 8:50 this morning, the client panel showed a name, phone number and card ending that do not belong to any client of mine, and another salon's name was at the top of the page. I refreshed and it went back to normal. Screenshot attached."
T-4189,Sun 8 Nov 19:20,Customer B,Standard,Email,0,"Double charge: any update?","Following up on my message from Saturday about the two $49 charges on 1 November."
T-4190,Mon 9 Nov 09:01,Customer J,Standard,Chat,0,"Gift cards?","Would love to sell gift cards through the booking page. Is that coming? Also, the receipt PDF still shows your old logo."
```

## The output

The sheet is plain text. It is set here with bold type and bullets so it reads well on a page; the words and their order are the template's.

**TICKET TRIAGE: Unassigned, export of Monday 9 November 2026, 09:15**

Tickets in the export: 10. Stopped for a decision: 5, in 3 items. Ready to route: 4. Duplicates: 1. Could not be triaged: 0.

Rules: version 6. Known issues: as of Friday 6 November 2026.

**STOPPED FOR A DECISION**

**1. T-4183, T-4184, T-4185: payment step fails with code 5031 at three businesses**

- **Condition met:** E3 Pattern, the same fault in three open tickets. T-4183 also meets E2 Outage on its own: “we cannot take bookings at all”.
- **Decides:** the queue manager. First call under the rules: engineering on-call, for E3 and for E2.
- **Category:** Fault, all three.
- **Priority:** T-4183 is P1: the business cannot take bookings at all. T-4184 is P2 by its own facts (payment is broken, but “Phone bookings still work”) and is raised to P1 because the same fault is in three open tickets. T-4185 is P1: the ticket does not say whether the business can take bookings another way, so the higher of P1 and P2 is taken. P1 is the top level, so the raising rules change nothing for T-4183 or T-4185.
- **Who is affected:** Customer C (Multi-site, all four locations), Customer D, Customer E.
- **Since:** about 07:45 today (T-4183); “this morning” (T-4184); not stated (T-4185).
- **Known:** Code 5031 at the payment step in all three tickets. Customer C takes no phone bookings (T-4183). Customer D’s phone bookings still work (T-4184). The known-issue list has no entry for code 5031.
- **Not known:** Whether other businesses are affected. Whether Customer E can take bookings another way. Whether anything changed in the product this morning.
- **First reply due:** T-4183 at 09:02 (P1), past target by 13 minutes. T-4184 at 09:20, not yet due: under the rules a raised ticket takes its raised level’s target from arrival, so this is the P1 target (its starting P2 target was 12:20). T-4185 at 09:41 (P1), not yet due.

**2. T-4188: Customer H saw another business’s client details**

- **Condition met:** E1 Security, one customer’s information shown to another.
- **Decides:** the queue manager. First call under the rules: security lead.
- **Category:** Security.
- **Priority:** P1: one customer’s information shown to another, and a security report.
- **Who is affected:** Customer H, and an unnamed second business whose client’s details were shown.
- **Since:** about 08:50 today, once; back to normal after a refresh.
- **Known:** The panel showed a name, a phone number and a card ending that were not Customer H’s client, under another salon’s name. Customer H says a screenshot is attached.
- **Not known:** Which business the details belong to. Whether it has happened to anyone else. The screenshot is not in the export, and it may show another business’s client details.
- **First reply due:** 09:55 (P1); not yet due.

**3. T-4187: Customer G’s client export is incomplete, and they may move**

- **Condition met:** E4 Customer at risk: “we will start looking at other systems”.
- **Decides:** the queue manager. First call under the rules: support lead.
- **Category:** Data: an export with missing records.
- **Priority:** P3 by its own facts (a problem outside the main functions), raised to P2 because its P3 first reply was due Friday 6 November at 11:15 and none has gone out. The ticket reports clients missing from an export, not records lost from the account, so “records lost” (P1) is not applied.
- **Who is affected:** Customer G (Multi-site).
- **Since:** the export was run on 4 November.
- **Known:** The export left out every client added since 1 October. A mailing goes out this week. The customer has set Wednesday as their limit. Replies sent: 0.
- **Not known:** The customer says this is their third message; the two earlier ones are not in this export. Whether the missing clients are still in the account or only missing from the export.
- **First reply due:** Thursday 5 November, 15:15, the P2 target counted from arrival as the rules say for a raised ticket; past target by 14 working hours. Its starting P3 target, Friday 6 November at 11:15, was past by 8 working hours.

**READY TO ROUTE**

- **T-4181** | Integration | P3 | Frontline | First reply due Monday 9 November, 16:40
  - Why: “Bookings made this morning still are not in my outside calendar” is a problem syncing with an outside calendar (Integration). It also fits Fault, since “It used to take a minute”; the priority and the route are the same either way. A workaround exists, so P3. It matches a known issue with a posted workaround, so Frontline. Arrived Friday at 16:40: 1 hour 20 minutes counted on Friday, the other 8 hours 40 minutes from Monday at 08:00.
  - Known issue: KI-14. Posted workaround: Settings > Calendar > Sync now.
- **T-4182** | Billing | P3 | Billing desk | First reply due Monday 9 November, 18:00
  - Why: “two charges of \$49 on 1 November. Please refund one” is a billing problem on one account (Billing, P3). Refunds and double charges go to the Billing desk. Arrived Saturday, so the clock started Monday at 08:00.
  - See Duplicates: T-4189.
- **T-4186** | How-to | P4 | Frontline | First reply due Tuesday 10 November, 18:00
  - Why: “How do I add her so clients can book with her?” asks how to do something the product does (How-to; questions are P4). How-to questions go to Frontline. Arrived Saturday, so the clock started Monday at 08:00.
- **T-4190** | Fault | P4 | Frontline | First reply due Wednesday 11 November, 09:01
  - Why: the ticket holds a fault (“the receipt PDF still shows your old logo”) and a request (gift cards); under the rules the fault is the category. A cosmetic fault is P4. It matches a known issue with a posted answer, so Frontline.
  - Known issue: KI-15. Posted answer: corrected copies can be downloaded again after release 4.13.
  - Also in this ticket: a request to sell gift cards through the booking page. Under the rules, the agent who takes the ticket copies it to the Product inbox.

**DUPLICATES**

- **T-4189** repeats **T-4182**: same customer (Customer B), same two \$49 charges on 1 November. It asks for an update and adds nothing new. It is not routed separately; the queue manager decides whether to merge it.

**COULD NOT BE TRIAGED**

None.

Prepared for the queue manager. No ticket has been changed, assigned or answered.
