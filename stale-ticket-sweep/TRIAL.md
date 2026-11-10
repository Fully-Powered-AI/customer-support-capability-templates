# Stale ticket sweep: tried once on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs are the template's own invented example. No client data was used. The run was made by an assistant that had not written the template. It read the template and the example's inputs first, produced the sheet by following the instruction block and the output format, and only then compared the result with the example's published sheet and the reviewer checklist.

## Inputs used

The inputs in `public/example.md`, under "The inputs": the time of the export (Monday 9 November 2026, 08:30), the sweep settings, the team this week, last week's sheet, and the open-ticket export of 21 tickets. Nothing else was supplied.

## What came out

The sheet follows. The run produced plain text; it is set here with bold titles so it reads on a page.

**STALE TICKET SWEEP: Support queue, export of Monday 9 November 2026, 08:30**

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
- Question for the lead: Nothing has happened on this ticket since 16 October; who chases the supplier, and by when?

T-301 | Working (In progress) | Carla | P2 | 10 working days without real activity (limit 3, over by 7)
- Subject: Card reader drops its connection at lunchtime
- Last real activity: 23 October 2026, team note or reply. Updated 7 November 2026: not real activity.
- On last week's sheet.
- Question for the lead: This ticket was on last week's sheet too; does Carla act on it this week, or does it need another person?

T-317 | Working (In progress) | Erin | P3 | 5 working days without real activity (limit 3, over by 2)
- Subject: Table plan resets after closing
- Last real activity: 30 October 2026, team note or reply. Updated 6 November 2026: not real activity.
- Question for the lead: Erin is away on 9 and 10 November; does someone else pick this up while she is away?

T-312 | Unassigned (New) | unassigned | P3 | 2 working days without real activity (limit 1, over by 1)
- Subject: Receipt printer printing blank receipts
- Last real activity: 5 November 2026, customer reply and status change.
- Question for the lead: Nobody owns this ticket; who is assigned to it? (It is a likely duplicate of T-314, see below.)

**WAITING ON THE CUSTOMER TOO LONG**

T-309 | Carla | P3 | 9 working days since the team last acted (limit 5) | 12 working days in the status | Reminders sent: 1
- Subject: Loyalty points not adding up after an update
- Reminder: 1 of 2 reminders left.
- Take it back: a working status, with a named owner who checks for the answer.
- Close: closing rule not met: needs 2 reminders and 10 working days in the status; has 1 reminder and 12 working days. A person confirms before anything is closed.
- The team's rules point to: reminder, because the assignee is at work and 1 reminder is left.

T-306 | Erin | P2 | 7 working days since the team last acted (limit 5) | 7 working days in the status | Reminders sent: 0
- Subject: Refunds not appearing in the weekly sales report
- Reminder: 2 of 2 reminders left.
- Take it back: a working status, with a named owner who checks for the answer.
- Close: closing rule not met: needs 2 reminders and 10 working days in the status; has 0 reminders and 7 working days. A person confirms before anything is closed.
- The team's rules point to: take it back, because the assignee, Erin, is away on the export date.

T-305 | Dev | P3 | 6 working days since the team last acted (limit 5) | 13 working days in the status | Reminders sent: 2
- Subject: End-of-day report missing card totals
- Reminder: 0 of 2 reminders left.
- Take it back: a working status, with a named owner who checks for the answer.
- Close: closing rule met: needs 2 reminders and 10 working days in the status; has 2 reminders and 13 working days. A person confirms before anything is closed.
- The team's rules point to: close, once a person confirms, because the assignee is at work, no reminders are left and the closing rule is met.

**STATUS OUT OF DATE**

T-308 | Ben | P3 | Status says waiting on the customer since 28 October 2026; the customer replied on 5 November 2026 | 2 working days since that reply (Working limit 3)
- Subject: Discount button greyed out for some staff
- Question for the lead: The customer replied on 5 November but the status still says waiting on them; who moves it back to a working status and answers?

**LIKELY DUPLICATES AND RELATED TICKETS**

T-312 and T-314: likely duplicate. Customer D; different contacts; opened 5 November 2026 and 5 November 2026, 0 working days apart (window 5).
- Why: "Receipt printer printing blank receipts" and "Printer gives blank receipts since this morning" describe the same fault. T-312 is listed under Stale; T-314 is healthy and held by Ben.
- Options: link or merge. The lead picks which stays; nothing has been linked or merged.

T-318 and T-319: possibly related. Customer B; different contacts; opened 29 October 2026 and 19 October 2026, 8 working days apart (window 5).
- Why: "Change the tax rate on menu items" and "How to set a new tax rate for takeaway orders" both concern changing a tax rate. Both are with Ben and healthy.
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
Observation: Ben holds the most tickets in hand (7) but all are small, while Carla holds only 2, both large and over 15 working days old, and carries the heaviest load (12 against 8.5); Erin, with the lightest load, is away on 9 and 10 November and holds T-317 and T-306, both listed on this sheet. Who moves what is the lead's decision.

**COULD NOT BE PLACED**

T-321 | Scheduled | Carla: the status "Scheduled" is not in the team's status groups. Question for the lead: Is Scheduled a working status, a waiting status, or one the sweep should leave out?

**FROM LAST WEEK'S SHEET, NO LONGER IN THE EXPORT**

T-296, T-298

Prepared for the support lead. No ticket has been changed and no one has been contacted.

## What was observed

- **Every required part was produced.** All sections of the output format were filled. The five groups add up: 4 + 3 + 1 + 1 + 12 = 21. No stop condition applied: all required headings matched, no ticket number repeated, the export time was given, and no subject held personal details, legal wording or instructions to the assistant. The one status the settings did not cover, "Scheduled", went to Could not be placed as the template says.
- **Same figures as the published example.** Every count, working-day figure, overrun, weight, load, average, mark, pair and "rules point to" choice matched the example's sheet. The working-day arithmetic across the weekend and the closed Wednesday came out the same.
- **Differences from the example are in wording and order only.**
  - The header says "Support queue"; the example says "Support".
  - The questions for the lead are worded differently. The example's question for T-312 asks whether it is linked or merged with T-314, and its T-317 question names Wednesday 11 November, a date worked out from Erin's absence and not stated in the inputs. This run asked who is assigned, and whether someone covers while Erin is away.
  - The example's T-305 close line adds "with no customer reply since 19 October"; this run left it out.
  - The pairs are written in a different order of ticket numbers (T-318 and T-319 here, T-319 and T-318 in the example). The template does not say which comes first.
  - The example's T-308 question proposes who does what ("does Ben set it back to a working status and reply?"). This run asked who, which is closer to the template's rule of proposing no move, but both are questions only.
- **No fact in either sheet is missing from the inputs,** apart from the example's "Wednesday 11 November", which is derived from the absence dates and the working calendar. The customer names ("Customer A" and so on) are the export's own labels.

## Where the instructions were unclear or needed a guess

- **Order of the two ticket numbers in a pair** is not specified.
- **Whether a listed waiting ticket counts in "Also held".** The template says tickets waiting on the customer are counted for the person; this run counted listed and unlisted ones alike (Dev holds T-305 and T-307, so 2). The example does the same.
- **A status-out-of-date ticket inside its Working limit.** T-308 is 2 working days past the customer's reply against a limit of 3, so it is not over. The template says to list it with the overrun "if there is one", so it was listed. A reader may expect only overdue tickets to be listed.
- **The export time of 08:30 on the Monday.** The template counts the export day as a whole working day. This run followed that, and it is the reason a ticket last active on Friday is 1 day old on Monday morning.
- **How to write a last activity that falls on two dates' worth of kinds.** T-312's status change and customer reply are on the same day, and the format says to join them with "and". That was clear. T-301's customer reply (22 October) is earlier than its team note, so only the note is named; the template does not say whether to mention an earlier customer reply.
- **What the question for the lead should do on a ticket that is also half of a pair.** The format says one question per ticket; the template does not say whether it should point to the pair.
- **The instruction block is shorter than the procedure.** It does not repeat the rule that an unreadable date, or a last activity later than the export time, puts a ticket under Could not be placed; that rule is only in the Exceptions section. It also does not say to give each pair's options. An assistant given only the pasted block, without the whole template, would miss the first of these.
- **Ordering inside Could not be placed and among pairs** is not specified; there was only one ticket here, so it made no difference.

## Changes made after this run

These were made on 10 November 2026, after the run above and after an independent review, and have not been run again. The output and observations above are left as the run produced them; where they compare this run with the published example, they describe the example as it stood at the time of the run. None of the changes alters a setting, a count, a working-day figure, a weight, a load, a mark, a pair or a "rules point to" choice on the example.

- The instruction block now carries the default settings itself, so an assistant given only the pasted block and the output format does not have to look them up. The example supplies every setting, so this run did not use them.
- The instruction block now says that a date that cannot be read, or a last activity later than the export time, puts the ticket under Could not be placed, as the Exceptions section already did. Nothing in the example triggers it.
- A pair is written with the earlier-opened ticket first, or the lower ticket number first when both were opened the same day. Likely duplicates come before possibly related pairs, and each kind is listed by the earlier opening date. This writes down the order the published example already used. The output above writes the related pair as "T-318 and T-319"; under the revised rule it would be "T-319 and T-318", a difference of order only.
- Could not be placed is listed by ticket number.
- When a ticket under Stale, Status out of date or Could not be placed is half of a pair, its question names the other ticket. Both this run and the example already did so for T-312.
- The example's T-317 question now asks whether someone picks the ticket up "while Erin is away", in place of naming Wednesday 11 November, and its T-308 question now asks who sets the ticket back to a working status and replies, in place of naming Ben. Both are now close to the wording this run used.
- The instruction block still does not repeat that each pair carries its options; the output format's Options line carries it, and this run wrote it for both pairs.

## What was not shown

This was one run, on one invented example, in one product, by one model. It does not show how the template behaves on a real export, with real column headings, on other models or products, or in a team's own environment. It was not tested in a client environment.
