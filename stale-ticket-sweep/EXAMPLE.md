# Stale ticket sweep: an invented example

*Illustrative example with invented data.* The company, its customers, its team, the tickets and the dates below are all invented. An invented 40-person company sells and supports till systems for cafés and restaurants. Its support team is four people, Ben, Carla, Dev and Erin, led by a support lead. On Monday 9 November 2026 the support lead exports every open ticket in the Support queue and runs the workflow template before the team plans its week.

The inputs come first, in full, so the template can be run on them. The sweep follows.

## The inputs

### The time of the export

```
Export taken: Monday 9 November 2026, 08:30. All open tickets in the Support queue.
```

### The sweep settings

```
SWEEP SETTINGS, Support (owner: support lead)
Working days: Monday to Friday. Office closed: Wednesday 4 November 2026.
Status groups:
  Open, In progress: Working
  New: Unassigned when no one is assigned; Working when someone is
  Pending customer: Waiting on the customer
  Waiting on supplier: Waiting on a third party
Limits, in working days without real activity:
  Working 3. Unassigned 1. Waiting on the customer 5. Waiting on a third party 7.
Waiting on the customer: at most 2 reminders. A ticket may be closed after
  2 reminders and 10 working days in the status with no reply, once the
  support lead confirms.
Duplicates: same customer, same problem, opened within 5 working days.
Size points: S 1, M 2, L 3. A ticket with no size counts as M.
Age factors, working days since created: 0 to 5, x1; 6 to 15, x1.5; over 15, x2.
Heavy: above 1.5 times the team average. Light: below 0.5 times.
```

### The team this week

```
Ben, Carla, Dev, Erin. Erin is away on Monday 9 and Tuesday 10 November.
```

### Last week's sheet

```
LAST WEEK'S SHEET (Monday 2 November 2026), ticket numbers by section
Stale: T-296, T-301, T-310
Waiting on the customer too long: T-298
Status out of date: none
Could not be placed: none
```

### The open-ticket export

```
Ticket,Subject,Customer,Contact,Status,Priority,Assignee,Size,Created,Status since,Last team note or reply,Last customer reply,Reminders sent,Updated
T-301,Card reader drops its connection at lunchtime,Customer A,A-1,In progress,P2,Carla,L,2026-10-13,2026-10-14,2026-10-23,2026-10-22,,2026-11-07
T-302,Add a second till to the account,Customer C,C-1,Open,P3,Ben,S,2026-11-05,2026-11-05,2026-11-06,2026-11-05,,2026-11-06
T-303,Change the logo on printed receipts,Customer E,E-1,Open,P4,Ben,S,2026-11-03,2026-11-03,2026-11-06,2026-11-03,,2026-11-06
T-304,Staff log-in screen shows the wrong site name,Customer G,G-1,Open,P3,Ben,S,2026-11-02,2026-11-02,2026-11-03,2026-11-02,,2026-11-03
T-305,End-of-day report missing card totals,Customer F,F-2,Pending customer,P3,Dev,M,2026-10-15,2026-10-20,2026-10-29,2026-10-19,2,2026-10-29
T-306,Refunds not appearing in the weekly sales report,Customer H,H-1,Pending customer,P2,Erin,M,2026-10-26,2026-10-28,2026-10-28,2026-10-27,0,2026-10-28
T-307,Question about exporting sales to a spreadsheet,Customer C,C-2,Pending customer,P4,Dev,S,2026-10-29,2026-10-30,2026-10-30,2026-10-29,0,2026-10-30
T-308,Discount button greyed out for some staff,Customer E,E-2,Pending customer,P3,Ben,S,2026-10-27,2026-10-28,2026-10-28,2026-11-05,0,2026-11-05
T-309,Loyalty points not adding up after an update,Customer G,G-2,Pending customer,P3,Carla,M,2026-10-19,2026-10-21,2026-10-26,2026-10-20,1,2026-10-26
T-310,Replacement cash drawer not yet received,Customer B,B-1,Waiting on supplier,P2,Dev,M,2026-10-12,2026-10-16,2026-10-16,2026-10-15,,2026-10-16
T-311,Kitchen printer swap under warranty,Customer A,A-2,Waiting on supplier,P3,Carla,L,2026-10-26,2026-10-29,2026-10-29,2026-10-28,,2026-10-29
T-312,Receipt printer printing blank receipts,Customer D,D-2,New,P3,,,2026-11-05,2026-11-05,,2026-11-05,,2026-11-05
T-313,How do I add a new staff member,Customer H,H-2,New,P4,,,2026-11-06,2026-11-06,,2026-11-06,,2026-11-06
T-314,Printer gives blank receipts since this morning,Customer D,D-1,Open,P3,Ben,S,2026-11-05,2026-11-05,2026-11-06,2026-11-05,,2026-11-06
T-315,Menu changes not reaching the second site,Customer F,F-1,Open,P2,Carla,L,2026-10-07,2026-10-08,2026-11-05,2026-11-06,,2026-11-06
T-316,Gift card balance shows twice,Customer B,B-2,In progress,P3,Dev,,2026-11-02,2026-11-02,2026-11-03,2026-11-02,,2026-11-03
T-317,Table plan resets after closing,Customer D,D-1,In progress,P3,Erin,M,2026-10-28,2026-10-29,2026-10-30,2026-10-29,,2026-11-06
T-318,Change the tax rate on menu items,Customer B,B-1,Open,P4,Ben,S,2026-10-29,2026-10-29,2026-11-05,2026-11-05,,2026-11-05
T-319,How to set a new tax rate for takeaway orders,Customer B,B-3,Open,P3,Ben,S,2026-10-19,2026-10-19,2026-11-03,2026-11-03,,2026-11-03
T-320,Till app closes when splitting a bill,Customer F,F-1,In progress,P1,Dev,L,2026-11-06,2026-11-06,2026-11-06,2026-11-06,,2026-11-06
T-321,Install visit for a second till,Customer E,E-1,Scheduled,P3,Carla,M,2026-10-27,2026-11-03,2026-11-03,2026-10-28,,2026-11-03
```

## The output

The sheet is plain text. It is set here with bold section titles and bullets so it reads well on a page; the words and their order are the template's.

**STALE TICKET SWEEP: Support, export of Monday 9 November 2026, 08:30**

Open tickets in the export: 21. Stale: 4. Waiting on the customer too long: 3. Status out of date: 1. Could not be placed: 1. Healthy, not listed: 12.
Likely duplicate pairs: 1. Possibly related pairs: 1.
Limits, in working days without real activity: Working 3, Unassigned 1, Waiting on the customer 5, Waiting on a third party 7 (team's settings).
Working days: Monday to Friday. Closed: Wednesday 4 November 2026. Activity measured from: replies, notes and status changes.
Compared with: last week's sheet of Monday 2 November 2026.
Settings taken as default: none.

**STALE**

T-310 | Waiting on a third party (Waiting on supplier) | Dev | P2 | 15 working days without real activity (limit 7, over by 8)
- Subject: Replacement cash drawer not yet received
- Last real activity: 16 October 2026, team note or reply and status change.
- On last week's sheet.
- Question for the lead: The ticket has had no note since it was set to wait on the supplier on 16 October; who asks the supplier for a delivery date, and by when?

T-301 | Working (In progress) | Carla | P2 | 10 working days without real activity (limit 3, over by 7)
- Subject: Card reader drops its connection at lunchtime
- Last real activity: 23 October 2026, team note or reply. Updated 7 November 2026: not real activity.
- On last week's sheet.
- Question for the lead: This ticket was on last week's sheet as well, and the customer last wrote on 22 October; does Carla update the customer this week, or does the ticket need another person's help?

T-317 | Working (In progress) | Erin | P3 | 5 working days without real activity (limit 3, over by 2)
- Subject: Table plan resets after closing
- Last real activity: 30 October 2026, team note or reply. Updated 6 November 2026: not real activity.
- Question for the lead: Erin is away today and tomorrow; does someone else pick this ticket up while Erin is away?

T-312 | Unassigned (New) | unassigned | P3 | 2 working days without real activity (limit 1, over by 1)
- Subject: Receipt printer printing blank receipts
- Last real activity: 5 November 2026, customer reply and status change.
- Question for the lead: Nobody owns this ticket, and it looks like a duplicate of T-314, which Ben holds; is it linked or merged with T-314, or assigned to someone?

**WAITING ON THE CUSTOMER TOO LONG**

T-309 | Carla | P3 | 9 working days since the team last acted (limit 5) | 12 working days in the status | Reminders sent: 1
- Subject: Loyalty points not adding up after an update
- Reminder: 1 of 2 reminders left.
- Take it back: a working status, with a named owner who checks for the answer.
- Close: closing rule not met: needs 2 reminders and 10 working days in the status; has 1 reminder and 12 working days. A person confirms before anything is closed.
- The team's rules point to: reminder, because Carla is at work today and 1 reminder is left.

T-306 | Erin | P2 | 7 working days since the team last acted (limit 5) | 7 working days in the status | Reminders sent: 0
- Subject: Refunds not appearing in the weekly sales report
- Reminder: 2 of 2 reminders left.
- Take it back: a working status, with a named owner who checks for the answer.
- Close: closing rule not met: needs 2 reminders and 10 working days in the status; has 0 reminders and 7 working days. A person confirms before anything is closed.
- The team's rules point to: take it back, because Erin, the assignee, is away on the export date.

T-305 | Dev | P3 | 6 working days since the team last acted (limit 5) | 13 working days in the status | Reminders sent: 2
- Subject: End-of-day report missing card totals
- Reminder: 0 of 2 reminders left.
- Take it back: a working status, with a named owner who checks for the answer.
- Close: closing rule met: needs 2 reminders and 10 working days in the status; has 2 reminders and 13 working days, with no customer reply since 19 October. A person confirms before anything is closed.
- The team's rules point to: close, once a person confirms, because Dev is at work today, no reminders are left and the closing rule is met.

**STATUS OUT OF DATE**

T-308 | Ben | P3 | Status says waiting on the customer since 28 October 2026; the customer replied on 5 November 2026 | 2 working days since that reply (Working limit 3)
- Subject: Discount button greyed out for some staff
- Question for the lead: The customer answered on 5 November but the ticket still shows as waiting on them; who sets it back to a working status and replies?

**LIKELY DUPLICATES AND RELATED TICKETS**

T-312 and T-314: likely duplicate. Customer D; different contacts; opened 5 November 2026 and 5 November 2026, 0 working days apart (window 5).
- Why: "Receipt printer printing blank receipts" and "Printer gives blank receipts since this morning" describe the same printer fault. T-312 is unassigned and listed under Stale; T-314 is with Ben and healthy.
- Options: link or merge. The lead picks which stays; nothing has been linked or merged.

T-319 and T-318: possibly related. Customer B; different contacts; opened 19 October 2026 and 29 October 2026, 8 working days apart (window 5).
- Why: "How to set a new tax rate for takeaway orders" and "Change the tax rate on menu items" both ask about changing a tax rate. Both are with Ben and healthy.
- Options: link or merge. The lead picks which stays; nothing has been linked or merged.

**WORKLOAD ACROSS THE TEAM**

Carla: in hand 2, load 12, heavy. Also held: 1 waiting on the customer, 1 waiting on a third party, 1 not placed.
- Weights: T-301: L 3 x 2 (18 working days old) = 6; T-315: L 3 x 2 (22 working days old) = 6.
- Listed on this sheet: T-301 (Stale); T-309 (Waiting on the customer too long); T-321 (Could not be placed).

Ben: in hand 7, load 8.5, within range. Also held: 0 waiting on the customer, 0 waiting on a third party.
- Weights: T-302: S 1 x 1 (2 working days old) = 1; T-303: S 1 x 1 (3 working days old) = 1; T-304: S 1 x 1 (4 working days old) = 1; T-308: S 1 x 1.5 (8 working days old) = 1.5; T-314: S 1 x 1 (2 working days old) = 1; T-318: S 1 x 1.5 (6 working days old) = 1.5; T-319: S 1 x 1.5 (14 working days old) = 1.5.
- Listed on this sheet: T-308 (Status out of date).

Dev: in hand 2, load 5, within range. Also held: 2 waiting on the customer, 1 waiting on a third party.
- Weights: T-316: no size, counted as M 2 x 1 (4 working days old) = 2; T-320: L 3 x 1 (1 working day old) = 3.
- Listed on this sheet: T-310 (Stale); T-305 (Waiting on the customer too long).

Erin (away Monday 9 and Tuesday 10 November): in hand 1, load 3, light. Also held: 1 waiting on the customer, 0 waiting on a third party.
- Weights: T-317: M 2 x 1.5 (7 working days old) = 3.
- Listed on this sheet: T-317 (Stale); T-306 (Waiting on the customer too long).

Team load 28.5 across 4 people; average 7.1. Heavy above 10.7; light below 3.6. Unassigned: 2 (T-312, T-313).
Observation: Ben holds the most tickets in hand (7), all small, yet Carla, with 2 large tickets each more than 15 working days old, carries the heaviest load (12 against Ben's 8.5); Erin, the lightest, is away today and tomorrow and holds T-317 and T-306, both listed on this sheet. Who moves what is the lead's decision.

**COULD NOT BE PLACED**

T-321 | Scheduled | Carla: the status "Scheduled" is not in the team's status groups. Question for the lead: Is Scheduled a working status, a waiting status, or one the sweep should leave out?

**FROM LAST WEEK'S SHEET, NO LONGER IN THE EXPORT**

T-296, T-298

Prepared for the support lead. No ticket has been changed and no one has been contacted.
