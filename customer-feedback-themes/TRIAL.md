# Customer feedback themes: one trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Opus 5.5 (model ID claude-opus-5-5), the model that revised the template after review; not an independent run
- **Date:** 2026-11-10

The inputs are the invented example in `public/example.md` (the settings, the owner list, what changed this month, last month's report and fix list, and the 26-row feedback export). No client data was used. The run followed the instruction block and the output format from the workflow template, applied to the example's inputs.

This is the second run on the same example. An earlier run the same day, by a different model that had not written the template, showed where the instructions left room to guess; the instructions and the example's output were revised after review, and the run recorded here was made on the revised instructions. Because it was made by the model that made those revisions, which had already read the example's output and the earlier run, it is not an independent run. What the earlier run found, and what was changed, is at the end.

## What came out

The report, as produced on the revised instructions. It is plain text.

```
CUSTOMER FEEDBACK THEMES: October 2026

For: support lead. Prepared 3 November 2026. Rows in the export: 26.
Outside the month, left out: 1 (SV-1119).
Sources read: Ticket 11 items, covering 1 to 31 October 2026; Dispute 2 items, covering 1 to 31 October 2026; Review 5 items, covering 1 to 31 October 2026; Survey 7 items, covering 30 September to 31 October 2026.
Sources not supplied: Marketplace review. Their customers are not counted this month.
Items read: 25. Needs a person now: 1. In themes: 20. Single mentions: 1.
Not placed: 3. Items in two themes: 1.
Last report: September 2026. Known changes: supplied.

NEEDS A PERSON NOW

RV-0904 (Review, 2026-10-19): the customer says they burned their hand on the handle of a glass teapot while pouring.
- Matter: an injury or a risk to someone's safety
- Decides: support lead

THEMES

1. Tins arrive dented | Delivery and packing | Customers 5 | Items 6: Ticket 1, Review 2, Survey 3 | Impact High | Score 15 | Last month: 2
- What customers ran into: Tins of tea arrive dented or crushed.
- Impact: High, because TK-5502 asks for a replacement and RV-0903 says the customer asked for a refund.
- In their words: "The tin was rattling around in a huge box with no padding. Can I get a replacement?" (TK-5502, Ticket); "Tin arrived crushed on one side, tea everywhere in the box." (RV-0903, Review, 1 of 5); "The tin had a dent in the lid but the tea was fine." (SV-1121, Survey, 4 of 5)
- On the fix list: No.

2. Surprised by subscription renewal | Billing and refunds | Customers 3 | Items 4: Ticket 2, Dispute 2 | Impact High | Score 9 | Last month: 4
- What customers ran into: Customers were charged for a subscription renewal they did not know about.
- Impact: High, because DP-0311 and DP-0312 are disputes.
- In their words: "I didn't know the subscription renewed automatically. I want this charge reversed." (DP-0311, Dispute); "Didn't realise I'd signed up for monthly deliveries." (DP-0312, Dispute); "Why was I charged again? I thought the tea was a one-off order." (TK-5511, Ticket)
- On the fix list: F-08, renewal reminder and "subscription" on the checkout button, in progress.

3. Discount codes rejected at checkout | Website and checkout | Customers 4 | Items 4: Ticket 4 | Impact Medium | Score 8 | Last month: new
- What customers ran into: Discount codes customers were given are rejected at checkout, and they write in to get the discount.
- Impact: Medium, because all four items are tickets (TK-5504, TK-5505, TK-5508, TK-5509), and none is a dispute, asks for money back or says the customer gave up.
- In their words: "Your code AUTUMN10 says invalid at checkout. Can you apply it manually? Call me on [removed]." (TK-5504, Ticket); "It says the code has expired but the email says it runs to the end of the month." (TK-5505, Ticket); "AUTUMN10 code rejected. Says not valid for items in my basket, but nothing says which items are excluded." (TK-5509, Ticket)
- On the fix list: No.

4. No tracking after dispatch | Delivery and packing | Customers 2 | Items 2: Ticket 2 | Impact Medium | Score 4 | Last month: 6
- What customers ran into: Customers had no tracking for dispatched orders and wrote in to ask where they were.
- Impact: Medium, because both items are tickets (TK-5501, TK-5506).
- In their words: "My order shipped on Monday and I still have no tracking number." (TK-5501, Ticket); "Order dispatched last Thursday, no tracking info in the email. Is it on its way?" (TK-5506, Ticket)
- On the fix list: F-07, carrier tracking link in every dispatch email, shipped 21 October 2026.

5. Slow replies to emails | Service | Customers 2 | Items 2: Ticket 2 | Impact Medium | Score 4 | Last month: new
- What customers ran into: Customers who emailed heard nothing for days and wrote again to chase a reply.
- Impact: Medium, because both items are tickets that chase an unanswered email (TK-5507, TK-5510).
- In their words: "I emailed on Friday about changing my delivery address and nobody has replied. It's now Tuesday." (TK-5507, Ticket); "Still waiting on a reply to my email from last week about my order." (TK-5510, Ticket)
- On the fix list: No.

6. Brewing instructions unclear | Product | Customers 3 | Items 3: Review 1, Survey 2 | Impact Low | Score 3 | Last month: new
- What customers ran into: The brewing guidance with the tea is hard to read or leaves out the steeping time or the amount to use.
- Impact: Low, because no item meets the High or Medium rule (SV-1120, SV-1122, RV-0905).
- In their words: "How long am I meant to steep the oolong?" (SV-1120, Survey, 3 of 5); "Steeping times on the pack are tiny and hard to read." (SV-1122, Survey, 3 of 5); "The brewing card in the box didn't say how much tea to use per cup." (RV-0905, Review, 3 of 5)
- On the fix list: No.

Last month's themes not seen this month: Late delivery (3 customers last month); Asked for gift wrap (2 customers last month).

SINGLE MENTIONS

SV-1123 (Survey): asks for a decaf option.

NOT PLACED

Praise only: 2 (RV-0902, SV-1125). No matter raised: 1 (SV-1126). Could not be read: 0 (none).

THREE ISSUES TO FIX

1. Tins arrive dented: Tins reach customers dented or crushed.
- Evidence: customers 5, items 6, score 15; TK-5502, RV-0901, SV-1120, SV-1121, RV-0903, SV-1124
- Cause: TK-5502 says the tin "was rattling around in a huge box with no padding", and SV-1124 says the "Box was massive for one tin of tea". Known change: from 1 October 2026 every order is packed in the large standard box.
- Proposed fix: Pad single tins packed in the large standard box so they cannot move.
- Proposed owner: warehouse lead
- How you will know: customers in this theme next month (5 this month), and replacement or refund requests about dented tins (2 this month: TK-5502, RV-0903).

2. Discount codes rejected at checkout: Customers are refused a discount at checkout with a code they were given.
- Evidence: customers 4, items 4, score 8; TK-5504, TK-5505, TK-5508, TK-5509
- Cause: Partly shown. AUTUMN10 excludes gift sets and teaware (known change, 1 October 2026), and TK-5509 says "nothing says which items are excluded". TK-5505 was told the code had expired although the email ran it to the end of the month; the feedback does not show why. TK-5504 and TK-5508 give no cause.
- Proposed fix: When checkout rejects a code, show the reason, including any items the code excludes.
- Proposed owner: ecommerce manager
- How you will know: customers in this theme next month (4 this month).

3. Slow replies to emails: Customers who email wait days for a reply and write again to chase it.
- Evidence: customers 2, items 2, score 4; TK-5507, TK-5510
- Cause: Not shown in the feedback.
- Proposed fix: Start each day by answering the oldest unanswered emails first, recording how many were waiting, so the cause can be found.
- Proposed owner: support lead
- How you will know: customers in this theme next month (2 this month).

Not chosen: Surprised by subscription renewal: on the fix list (F-08, in progress).
Not chosen: No tracking after dispatch: fix F-07 shipped 21 October 2026, before every item in the theme.
Not chosen: Brewing instructions unclear: below the three chosen (score 3).

FIX LIST

F-06 | Gift wrap option | Asked for gift wrap | Declined 15 October 2026 | Customers this month 0 (last month 2)
- Reason recorded: "Adds packing time; revisit in January."
F-07 | Carrier tracking link in every dispatch email | No tracking after dispatch | Shipped 21 October 2026 | Customers this month 2 (last month 6)
- Items dated on or after the ship date: none.
F-08 | Renewal reminder three days before each subscription charge, and "subscription" shown on the checkout button | Surprised by subscription renewal | In progress, ecommerce manager, target 15 November 2026 | Customers this month 3 (last month 4)
- Not yet shipped.

YOU TOLD US, WE CHANGED (drafts, not sent)

F-07: Carrier tracking link in every dispatch email
Draft: "You told us that after your order left us you could not see where it was. Every dispatch email now includes the carrier's tracking link, for orders dispatched from 21 October 2026. If a dispatch email reaches you without the link, reply to any email from us and let us know."
For approval by: operations manager. Where it appears: the approver decides.

QUESTIONS FOR THE SUPPORT LEAD

1. Marketplace reviews are expected each month but were not supplied. Is there an October export to add before the report goes to the operations manager?

Prepared for the support lead. Nothing has been sent, posted or changed.
```

## What was observed

The report was produced in full, with every part the output format asks for. The checks in the instructions hold: 26 rows less 1 outside the month is 25 items; 1 + 20 + 1 + 3 = 25; each theme's items by source add up to its item count; the six themes hold 21 item places, which is In themes (20) plus Items in two themes (1), because SV-1120 is in both "Tins arrive dented" and "Brewing instructions unclear"; every score is customers times weight. Nothing made it stop: the headers were the defaults, no required column was missing and no source value was unknown. No item held a card number, password or sign-in detail. TK-5504 held a phone number, which appears as "[removed]". The draft note is 51 words.

Points the revised instructions settled in this run:

- **Who decides the injury item:** the support lead, because the settings name no other role. No question was needed.
- **The area of the renewal theme:** Billing and refunds, the area where the customer noticed the problem (the charge).
- **The Low rating:** its reason is that no item meets the High or Medium rule, as the format now says.
- **SV-1120's question about steeping:** a question in a survey, so not a contact; the brewing theme stays Low.
- **The survey period:** printed as stated (30 September to 31 October 2026), with SV-1119 listed as left out.
- **Gift wrap in the fix list:** 0 customers this month, as the instructions now say.
- **SV-1126 ("n/a"):** no matter raised.
- **Which fixes get a note:** F-07 shipped on 21 October 2026, after the last day of September, the month last month's report covered.
- **Third place:** "No tracking after dispatch" and "Slow replies to emails" are equal on score, impact, customers and items, but the first is skipped (its fix shipped before every item), so third place was not decided by name and no tie was shown.

Compared with the published example output, the two reports agree on every count, impact level, score, the order of the themes, the three issues chosen, the "Not chosen" lines, the fix list and the single draft note. The differences are in wording: the names of two new themes ("Discount codes rejected at checkout", "Slow replies to emails"), some quotations (a different third quotation for dented tins, and a shorter part of SV-1120), and the wording of the proposed fixes, of which the second differs in substance (showing the reason at checkout here; checking the code against the email before it goes out in the example). Each run's proposed fix is a single change.

Where the instructions still left room to choose:

1. **Naming a new theme.** There is a rule for reusing last month's name, none for a new one.
2. **Whether the oversized box is its own theme.** Two customers mention the box size alongside a dented tin. This run kept one theme and used the box as the cause.
3. **The area for "No tracking after dispatch".** The customers noticed the gap in the dispatch email; this run read that as part of delivery and kept Delivery and packing. "Where the customer noticed the problem" still calls for judgment.
4. **The closing line and the Questions heading name the support lead** even though the report reader is a setting; here they are the same role, so nothing turned on it.
5. **The check that theme item counts equal In themes plus Items in two themes** assumes no item sits in three themes.

No fact appears in this report that is not in the inputs. The proposed fixes are proposals, not claims about the shop.

This was one run on one invented example, by the model that revised the instructions. It shows the revised instructions can be followed to a complete, consistent report. It does not show the template works in a real business.

## The earlier run, and what was changed

The earlier run was made the same day with Claude Sonnet 5.5 (model ID claude-sonnet-5-5), run in Claude Code, by an assistant that was given only the instruction block, the output format and the example's inputs and did not read the example's output until its own report was finished. Its report agreed with the example on every count, impact level, score, the order of the themes, the three issues chosen, the fix list and the draft note. It wrote "[owner to confirm]" for who decides the injury item and asked a second question about it, chose Website and checkout for the renewal theme, and gave a single proposed fix where the example's first fix offered two options.

It listed these points where it had to guess: the tie rule for third place could never apply, because the order of themes ends in theme name A to Z; the instruction block did not say who decides an item under Needs a person now; how to choose an area when two fit; whether the oversized box is a separate theme; whether a survey question counts as a contact; that the Low rating has no rule to cite; which period to print when a source's range is wider than the month; what "Customers this month" is for a fix whose theme is absent; whether "n/a" is no matter raised or could not be read; what "the period of last month's report" means for the notes; how to name a new theme; and whether a quotation may be part of the text. It noted that both its own and the example's proposed fixes for slow replies picked a waiting time the inputs do not give, and that the example's second fix mentioned "first-order limits", which the inputs touch only through WELCOME15 failing on a first order.

After review, these were changed: the tie for third place now applies only when two themes are equal on everything but name; who decides an item under Needs a person now is the support lead unless the settings name another role; the report reader is a setting, defaulting to the support lead; the area is the one where the customer noticed the problem, then the first on the owner list; a survey or review question is not a contact; the reason for Low is that no item meets the High or Medium rule; the period is printed as stated, or "(from the rows)"; a fix whose theme is absent shows 0; a blank or "n/a" answer is no matter raised; the notes cover fixes shipped after the last day of the month last month's report covered; a quotation may be the whole item or one continuous part of it; a proposed fix is a single change, not a choice; and the instruction block now carries the rules on the period, missing ratings and the fuller arithmetic checks. In the example's output, the first and second proposed fixes were reduced to one change each, the third no longer names a waiting time, and the Low reason follows the new wording.
