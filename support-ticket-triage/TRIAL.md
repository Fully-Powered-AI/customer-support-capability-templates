# Support ticket triage: a trial on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Fable 5.2
- **Date:** 2026-11-09

The inputs are the invented example published with this capability template. No client data was used, and this is not a test in any company's support system. It is one run of the template as it stood when the run was made, recorded as it happened, shortcomings included.

It was not the first run that day. Runs on earlier drafts showed where the instructions were unclear, and the template and the example were revised because of them. Those runs and what they changed are described at the end. The sheet below comes from the wording as it stood at the end of that day's runs.

**Edited after this run, 9 November 2026.** Following the editorial review, the template and the example were edited after the run recorded here, and the run was not repeated. The output and the observations below are left as recorded, so where they describe the template or the example they describe them as they were at the time of the run. The instruction block changed in four places: it now says to note what the customer has already tried; to mention in the reason any wording in a ticket that is addressed to the assistant; to write a target that ends exactly at closing time as that day's closing time, which is what the example does for T-4182 and not what this run did (difference 1 below); and to say once when a raising rule is true for a ticket already at the top level (unclear point 2). In the output format, the known-issue date is now described as the list's date. In the example, the sheet's known-issue date no longer begins "as of" (unclear point 3), the line "See Duplicates: T-4189" under T-4182 was removed because the format has no such line (difference 6), and one route in the invented rules was reworded from "faults that need investigating" to "faults not matched to a known issue"; no ticket in the example takes that route.

## The inputs used

The four inputs in [the invented example](example.md), exactly as written there: the export time and working hours, the triage rules (version 6), the known-issue list (as of Friday 6 November 2026) and the queue export of ten tickets, T-4181 to T-4190. The template's instruction block and its output format were given ahead of them, in one message, to a fresh session with no tools and no files. The session was not given the example's own triage sheet.

## What came out

The complete reply, as produced:

```
TICKET TRIAGE: Unassigned, export of Monday 9 November 2026, 09:15

Tickets in the export: 10. Stopped for a decision: 5, in 3 items.
Ready to route: 4. Duplicates: 1. Could not be triaged: 0.
Rules: version 6. Known issues: Friday 6 November 2026.

STOPPED FOR A DECISION

1. T-4183, T-4184, T-4185: code 5031 at the payment step for three different customers this morning
- Condition met: E3 Pattern, "the same fault in three or more open tickets"; all three tickets report code 5031 at payment or checkout. T-4183 also meets E2 Outage on its own: "right now we cannot take bookings at all".
- Decides: queue manager. First call under the rules: engineering on-call (E3). For T-4183 under E2, first call is also engineering on-call.
- Category: Fault
- Priority: T-4183: P1, "cannot take bookings at all". Both raising rules are true (past target; three or more open tickets), but there is no level above P1.
  T-4184: P1, raised from P2 because the same fault appears in three or more open tickets. Starting level P2: payment is broken but "Phone bookings still work".
  T-4185: P1. The ticket does not state whether the business has another way to take bookings or payments, so the higher of P1 and P2 is taken. The three-ticket rule would raise P2 to P1 in any case; there is no level above P1.
- Who is affected: Customer C (Multi-site, four locations), Customer D (Standard), Customer E (Standard), and their clients trying to pay online.
- Since: T-4183: "about 7:45 this morning". T-4184: "this morning". T-4185: not stated.
- Known: T-4183: every client who tries to book at any of the four locations gets "Something went wrong (code 5031)" at the payment step, and the business takes no phone bookings. T-4184: clients cannot pay online, the page shows code 5031, phone bookings still work. T-4185: code 5031 appears when a client tries to check out, and the customer asks "Is there an outage?". No known issue on the list of 6 November matches. No replies have been sent on any of the three.
- Not known: the cause. Whether Customer E can take bookings or payments another way, so E2 is not claimed for T-4185. Whether every client of Customer D and Customer E is affected or only some. Whether customers who have not written in are affected.
- First reply due: T-4183: Monday 9 November, 09:02 (P1 target); past target by 13 working minutes.
  T-4184: Monday 9 November, 09:20 (raised level's P1 target, counted from arrival at 08:20); not yet due. The starting P2 target was 12:20.
  T-4185: Monday 9 November, 09:41 (P1 target); not yet due.

2. T-4188: another business's client details and salon name appeared on the customer's screen
- Condition met: E1 Security, "one customer's information shown to another"; the ticket says the client panel showed details that "do not belong to any client of mine, and another salon's name was at the top of the page".
- Decides: queue manager. First call under the rules: security lead.
- Category: Security
- Priority: P1, "one customer's information shown to another; any security report". Not past target; the three-ticket rule does not apply; not raised.
- Who is affected: Customer H (Standard), plus an unnamed other salon and one of its clients whose details were shown.
- Since: "about 8:50 this morning", Monday 9 November.
- Known: it happened when the customer opened a booking. The panel showed personal and card-related details of someone who is not their client; the export carries the description. After a refresh "it went back to normal". No replies sent.
- Not known: which other salon and which client were shown. Whether it has happened more than once or to anyone else. Whether Customer H's own client information was shown elsewhere. The ticket says "Screenshot attached"; the screenshot is not in the export and may hold another person's personal details.
- First reply due: Monday 9 November, 09:55 (P1 target); not yet due.

3. T-4187: client export left out clients added since 1 October; customer says they may look at other systems
- Condition met: E4 Customer at risk, "says they may cancel or move to another system"; the ticket says "If this is not sorted by Wednesday we will start looking at other systems".
- Decides: queue manager. First call under the rules: support lead.
- Category: Data
- Priority: P2, raised from P3 because the ticket is past its first-reply target at the time of the export. Starting level P3: a problem outside the main functions (booking, payment, reminders).
- Who is affected: Customer G (Multi-site).
- Since: the export was run on 4 November; the missing clients are those "added since 1 October".
- Known: the customer says "This is the third time I have written about this". A mailing is going out this week and they need the full list. They give a deadline of "Wednesday". The ticket arrived Thursday 5 November, 11:15, and no replies have been sent.
- Not known: the two earlier messages are not in the export, so what they said and whether they were answered is not known. Whether the client records are missing from the account or only from the export file; the ticket states only the export. Which Wednesday is meant. Whether the customer has another way to get the list.
- First reply due: Thursday 5 November, 15:15 (raised level's P2 target, counted from arrival); past target by 14 working hours (1 working day and 4 working hours). The starting P3 target was Friday 6 November, 11:15; past by 8 working hours.

READY TO ROUTE

T-4181 | Integration | P3 | Frontline | First reply due Monday 9 November, 16:40
- Why: Syncing with an outside calendar is Integration: "Bookings made this morning still are not in my outside calendar". Fault also fits, but priority and route are the same either way. P3 because it is broken with a workaround, and it goes to Frontline as a ticket matching a known issue with a posted workaround. Arrived Friday 16:40: 1 hour 20 minutes on Friday plus 8 hours 40 minutes on Monday gives 16:40; not yet due.
- Known issue: KI-14. Workaround: Settings > Calendar > Sync now.

T-4182 | Billing | P3 | Billing desk | First reply due Tuesday 10 November, 08:00
- Why: "a billing problem on one account" is P3, and refunds and double charges go to the Billing desk: "two charges of $49 on 1 November. Please refund one." Arrived Saturday 10:05, outside working hours, so the clock starts Monday 08:00; one working day gives Tuesday 08:00; not yet due.

T-4186 | How-to | P4 | Frontline | First reply due Tuesday 10 November, 18:00
- Why: a question is P4, and how-to questions go to Frontline: "How do I add her so clients can book with her?" Arrived Saturday 14:30, outside working hours, so the clock starts Monday 08:00; two working days (20 working hours) gives Tuesday 18:00; not yet due.

T-4190 | Fault | P4 | Frontline | First reply due Wednesday 11 November, 09:01
- Why: the ticket holds a fault and a request, so the fault is the category: "the receipt PDF still shows your old logo". A cosmetic fault is P4, and it goes to Frontline as a ticket matching a known issue with a posted answer. Arrived Monday 09:01; two working days gives Wednesday 09:01; not yet due.
- Known issue: KI-15. Posted answer: corrected copies can be downloaded again after release 4.13.
- Also in this ticket: a request to "sell gift cards through the booking page". Under the rules, a request inside another ticket is copied to the Product inbox by the agent who takes the ticket.

DUPLICATES

T-4189 repeats T-4182: same customer (Customer B), same problem (two $49 charges on 1 November); it adds nothing new and asks for an update.
Not routed separately; the queue manager decides whether to merge it.

COULD NOT BE TRIAGED

None.

Prepared for the queue manager. No ticket has been changed, assigned or answered.
```

## What was observed

**Every required part was produced.** All ten tickets appear exactly once and the counts add up (5 stopped in 3 items, 4 ready to route, 1 duplicate, 0 not triaged). Each stopped entry names a condition from the rules with the ticket's words. No ticket that met an escalation condition was given a route. Each raised priority shows both levels, and each raised ticket's due time says which level it is counted at. The due times that depend on out-of-hours arrival show their arithmetic in the reason. The sheet is plain text with the format's lines and no others. No reply was drafted and no fix suggested. The card ending and phone number mentioned in T-4188 were not repeated, and the missing screenshot was flagged.

**What the template stopped for.** Three items, five tickets: the code 5031 pattern (E3, with E2 for T-4183 named in the same entry), the security report (E1) and the customer who may leave (E4). None of the stops before triage applied: the export, the rules, the known-issue list, the export time and the working hours were all there.

**Compared with the published example.** The same three stopped items in the same order, the same categories, starting and raised priorities, routes and duplicate, and the same due time for nine of the ten tickets, including T-4184 at 09:20 and T-4187 at Thursday 5 November, 15:15, past target by 14 working hours. The differences:

1. T-4182's due time. The example gives Monday 9 November, 18:00; the run gives Tuesday 10 November, 08:00. Counted in working hours these are the same moment, the end of one working day and the start of the next, but a reader sees two different days. The instructions do not say which to write when a target ends exactly at closing time.
2. T-4183's lateness is given as "13 working minutes"; the example says 13 minutes.
3. Under Not known, the run listed more than the example does: the cause, which Wednesday Customer G means, whether Customer H's own client details were shown elsewhere. All are questions the tickets do not answer. The example's lists are shorter.
4. The run quoted the rules as well as the tickets in most places; the example quotes the ticket and names the rule in its own words.
5. The run showed the arithmetic for all four routed tickets, including T-4190, which arrived in working hours. The example shows it for the three that did not.
6. The example cross-refers T-4182 to its duplicate under Ready to route; the run lists the duplicate only under Duplicates, as the format does.
7. The example is set with bold type and bullets for the page, and says so; the run is plain text.

**Where the instructions were unclear or a guess was needed.**

1. A target that ends exactly at closing time (difference 1). The run chose the next morning; the example chose the evening.
2. T-4183 is past its target and already at the top level. The run said both raising rules were true and that there is no level above P1. The instructions do not say whether a raise that cannot happen should be mentioned.
3. The known-issue date. The run wrote "Friday 6 November 2026" where the example writes "as of Friday 6 November 2026". The format says only "date".

**Shortcomings of this trial.** One recorded run, by one model, on ten invented tickets written to exercise the template, so the rules and the tickets fit each other more neatly than a real queue would. The example's sheet was corrected after the earlier runs and before this one, by the same writer who revised the template, so the close agreement between this run and the example is not independent evidence. The stops for missing inputs, a legal threat, a card number in a message, an instruction inside a ticket, a missing pattern threshold, a partial known-issue match and a request to act after the sheet were not exercised. A support team has not checked the sheet.

## The earlier runs and what they changed

Three runs came before this one, all in the same product on the same inputs, each in a session that had not seen the example's sheet.

The first, on the first draft, differed from the example as it then stood in four ways. Each has since been settled:

1. T-4185. The example set it at P2 and raised it for the pattern; the run set it at P1 because the ticket does not say whether the business can take bookings another way. The example now gives P1 for that reason.
2. T-4187's due time. The example's rules could be read two ways, and the example gave the P3 time for T-4187 while giving T-4184 its raised P1 time. The rules now say a raised ticket takes its raised level's target from arrival, and both tickets follow that.
3. The example left out the line for the rules version and the known-issue date. It is there now.
4. The example said "past target" for T-4187 without saying by how much. It now gives both figures.

That run also found the instructions silent on a ticket in a pattern that meets a second condition, on the order of the due time and the raising rules, on how far "take the higher level" reaches, on a ticket that fits two categories with the same result, on the local settings, and on an attachment that is referred to but not in the export. The template now covers each.

The second and third runs were on a revised draft. They agreed with the example on every route, stop and due time, and showed three further things. They split on T-4185: one took P1 directly, the other started it at P2 and raised it, because the new limit on taking the higher level ("do not assume a fact the ticket does not raise") could be read against it. One used bold type and nested bullets, and one added a line of its own for the arithmetic and a remark about a setting that had not been supplied. The instructions were tightened on all three points, and the run recorded above followed them.
