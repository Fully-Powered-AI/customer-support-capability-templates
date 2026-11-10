# Customer feedback themes: an invented example

*Illustrative example with invented data.* The shop, its customers, the feedback, the owner list, the fixes and every number below are invented. Shop A is an invented online shop with 14 staff that sells loose-leaf tea, tea subscriptions and teaware. On Tuesday 3 November 2026 its support lead runs the capability on October's feedback, before taking the report to the operations manager.

The inputs come first, in full, so the template can be run on them. The report follows.

## The inputs

### The settings

```
REPORT SETTINGS
Month: October 2026. Prepared: 3 November 2026. Report for: support lead.
Sources expected: Ticket, Dispute, Review, Survey, Marketplace review.
Periods covered: tickets, disputes and reviews 1 to 31 October 2026;
survey 30 September to 31 October 2026 (the survey tool's fixed range).
Theme minimum, impact rules, matters that need a person now: the defaults.
Fix decider: operations manager. Approver for notes to customers:
operations manager. Contact route for notes: reply to any email from us.
Outside our control: none listed. Column mapping: none; the export uses
the default headers.
```

### The owner list

```
Product: buying lead
Delivery and packing: warehouse lead
Website and checkout: ecommerce manager
Billing and refunds: finance lead
Service: support lead
```

### What changed this month

```
1 October 2026: every order is now packed in one standard box, the large
size, to cut the number of box types we hold.
1 October 2026: code AUTUMN10 emailed to the mailing list. 10% off, valid
to 31 October 2026, excludes gift sets and teaware.
21 October 2026: fix F-07 shipped (see the fix list).
```

### Last month's report and the fix list

```
SEPTEMBER 2026 THEMES (customers)
No tracking after dispatch: 6
Surprised by subscription renewal: 4
Late delivery: 3
Tins arrive dented: 2
Asked for gift wrap: 2

FIX LIST
F-06 | Gift wrap option | Theme: Asked for gift wrap | Owner: warehouse lead
       Declined 15 October 2026. Reason: "Adds packing time; revisit in January."
F-07 | Carrier tracking link in every dispatch email | Theme: No tracking
       after dispatch | Owner: ecommerce manager | Shipped 21 October 2026.
       What changed: "Every dispatch email now includes the carrier's
       tracking link. Applies to orders dispatched from 21 October 2026."
F-08 | Renewal reminder three days before each subscription charge, and
       "subscription" shown on the checkout button | Theme: Surprised by
       subscription renewal | Owner: ecommerce manager | In progress,
       target 15 November 2026.
```

### The feedback export

```
ID,Date,Source,Customer,Rating,Text
SV-1119,2026-09-30,Survey,C-2088,4,"Quick delivery."
TK-5501,2026-10-03,Ticket,C-2041,,"My order shipped on Monday and I still have no tracking number. Can you tell me where it is?"
TK-5502,2026-10-04,Ticket,C-2055,,"Second tin this month that's arrived dented. The tin was rattling around in a huge box with no padding. Can I get a replacement?"
RV-0901,2026-10-05,Review,C-2055,2,"Lovely tea but the tin came dented again. Packaging needs work."
DP-0311,2026-10-06,Dispute,C-2078,,"Reason given: not recognised. Customer note: I didn't know the subscription renewed automatically. I want this charge reversed."
TK-5503,2026-10-06,Ticket,C-2078,,"I've been charged $18 for a subscription I didn't know renewed. I've asked my bank to reverse it."
SV-1120,2026-10-07,Survey,C-2090,3,"Tin was dented and the brewing guide made no sense to me. How long am I meant to steep the oolong?"
TK-5504,2026-10-08,Ticket,C-2102,,"Your code AUTUMN10 says invalid at checkout. Can you apply it manually? Call me on 555-0148."
TK-5505,2026-10-09,Ticket,C-2110,,"Discount code from your email isn't working. It says the code has expired but the email says it runs to the end of the month."
RV-0902,2026-10-10,Review,C-2117,5,"Best breakfast tea I've found. Fast delivery too."
TK-5506,2026-10-12,Ticket,C-2123,,"Order dispatched last Thursday, no tracking info in the email. Is it on its way?"
DP-0312,2026-10-13,Dispute,C-2131,,"Reason given: not recognised. Customer note: Didn't realise I'd signed up for monthly deliveries."
TK-5507,2026-10-13,Ticket,C-2144,,"I emailed on Friday about changing my delivery address and nobody has replied. It's now Tuesday."
SV-1121,2026-10-14,Survey,C-2139,4,"The tin had a dent in the lid but the tea was fine."
RV-0903,2026-10-16,Review,C-2150,1,"Tin arrived crushed on one side, tea everywhere in the box. Asked for a refund."
TK-5508,2026-10-17,Ticket,C-2158,,"The code WELCOME15 won't apply to my first order. Tried three times."
SV-1122,2026-10-18,Survey,C-2163,3,"Steeping times on the pack are tiny and hard to read."
RV-0904,2026-10-19,Review,C-2170,2,"The glass teapot's handle got so hot I burned my hand pouring. Be careful."
TK-5509,2026-10-20,Ticket,C-2176,,"AUTUMN10 code rejected. Says not valid for items in my basket, but nothing says which items are excluded."
SV-1123,2026-10-21,Survey,C-2181,4,"Would love a decaf option."
TK-5510,2026-10-22,Ticket,C-2185,,"Still waiting on a reply to my email from last week about my order."
SV-1124,2026-10-24,Survey,C-2190,2,"Box was massive for one tin of tea, and the tin was dented anyway."
SV-1125,2026-10-26,Survey,C-2194,5,"Lovely as always."
RV-0905,2026-10-27,Review,C-2199,3,"Good tea. The brewing card in the box didn't say how much tea to use per cup."
SV-1126,2026-10-29,Survey,C-2203,,"n/a"
TK-5511,2026-10-30,Ticket,C-2207,,"Why was I charged again? I thought the tea was a one-off order."
```

## The output

The report is plain text, exactly as the template sets it out.

```
CUSTOMER FEEDBACK THEMES: October 2026

For: Support lead. Prepared 3 November 2026. Rows in the export: 26.
Outside the month, left out: 1 (SV-1119).
Sources read: Ticket 11 items, covering 1 to 31 October 2026; Dispute 2 items, covering 1 to 31 October 2026; Review 5 items, covering 1 to 31 October 2026; Survey 7 items, covering 30 September to 31 October 2026.
Sources not supplied: Marketplace review. Their customers are not counted this month.
Items read: 25. Needs a person now: 1. In themes: 20. Single mentions: 1.
Not placed: 3. Items in two themes: 1.
Last report: September 2026. Known changes: supplied.

NEEDS A PERSON NOW

RV-0904 (Review, 2026-10-19): the customer says the glass teapot's handle became hot enough to burn their hand while pouring.
- Matter: an injury or a risk to someone's safety
- Decides: Support lead

THEMES

1. Tins arrive dented | Delivery and packing | Customers 5 | Items 6: Ticket 1, Review 2, Survey 3 | Impact High | Score 15 | Last month: 2
- What customers ran into: Tins of tea arrive dented or crushed.
- Impact: High, because TK-5502 asks for a replacement and RV-0903 says the customer asked for a refund.
- In their words: "The tin was rattling around in a huge box with no padding." (TK-5502, Ticket); "Tin arrived crushed on one side, tea everywhere in the box." (RV-0903, Review, 1 of 5); "Box was massive for one tin of tea, and the tin was dented anyway." (SV-1124, Survey, 2 of 5)
- On the fix list: No.

2. Surprised by subscription renewal | Billing and refunds | Customers 3 | Items 4: Ticket 2, Dispute 2 | Impact High | Score 9 | Last month: 4
- What customers ran into: Customers were charged for a subscription renewal they did not know they had signed up for.
- Impact: High, because DP-0311 and DP-0312 are disputes.
- In their words: "I didn't know the subscription renewed automatically." (DP-0311, Dispute); "Didn't realise I'd signed up for monthly deliveries." (DP-0312, Dispute); "Why was I charged again? I thought the tea was a one-off order." (TK-5511, Ticket)
- On the fix list: F-08, renewal reminder and "subscription" on the checkout button, in progress.

3. Discount codes refused at checkout | Website and checkout | Customers 4 | Items 4: Ticket 4 | Impact Medium | Score 8 | Last month: new
- What customers ran into: Discount codes customers were sent are refused at checkout.
- Impact: Medium, because all four items are tickets (TK-5504, TK-5505, TK-5508, TK-5509) and none asks for money back or says the customer gave up.
- In their words: "Your code AUTUMN10 says invalid at checkout. Can you apply it manually? Call me on [removed]." (TK-5504, Ticket); "It says the code has expired but the email says it runs to the end of the month." (TK-5505, Ticket); "Says not valid for items in my basket, but nothing says which items are excluded." (TK-5509, Ticket)
- On the fix list: No.

4. No tracking after dispatch | Delivery and packing | Customers 2 | Items 2: Ticket 2 | Impact Medium | Score 4 | Last month: 6
- What customers ran into: Customers had no tracking for orders already dispatched and wrote in to ask where they were.
- Impact: Medium, because both items are tickets (TK-5501, TK-5506).
- In their words: "My order shipped on Monday and I still have no tracking number." (TK-5501, Ticket); "Order dispatched last Thursday, no tracking info in the email." (TK-5506, Ticket)
- On the fix list: F-07, carrier tracking link in every dispatch email, shipped 21 October 2026.

5. Slow replies from support | Service | Customers 2 | Items 2: Ticket 2 | Impact Medium | Score 4 | Last month: new
- What customers ran into: Customers who emailed waited days for a reply and wrote again to chase it.
- Impact: Medium, because both items are tickets that chase an earlier email (TK-5507, TK-5510).
- In their words: "I emailed on Friday about changing my delivery address and nobody has replied. It's now Tuesday." (TK-5507, Ticket); "Still waiting on a reply to my email from last week about my order." (TK-5510, Ticket)
- On the fix list: No.

6. Brewing instructions unclear | Product | Customers 3 | Items 3: Review 1, Survey 2 | Impact Low | Score 3 | Last month: new
- What customers ran into: The brewing guidance that comes with the tea is hard to read or leaves out the steeping time or the amount to use.
- Impact: Low, because no item meets the High or Medium rule (SV-1120, SV-1122, RV-0905).
- In their words: "the brewing guide made no sense to me. How long am I meant to steep the oolong?" (SV-1120, Survey, 3 of 5); "Steeping times on the pack are tiny and hard to read." (SV-1122, Survey, 3 of 5); "The brewing card in the box didn't say how much tea to use per cup." (RV-0905, Review, 3 of 5)
- On the fix list: No.

Last month's themes not seen this month: Late delivery (3 customers last month); Asked for gift wrap (2 customers last month).

SINGLE MENTIONS

SV-1123 (Survey): asks for a decaf option.

NOT PLACED

Praise only: 2 (RV-0902, SV-1125). No matter raised: 1 (SV-1126). Could not be read: 0 (none).

THREE ISSUES TO FIX

1. Tins arrive dented: Tins reach customers dented or crushed, and customers connect it with a large box that lets the tin move.
- Evidence: customers 5, items 6, score 15; TK-5502, RV-0901, SV-1120, SV-1121, RV-0903, SV-1124
- Cause: TK-5502 says the tin "was rattling around in a huge box with no padding"; SV-1124 says the "Box was massive for one tin of tea". Known changes: from 1 October 2026 every order is packed in the large standard box.
- Proposed fix: Pack small orders with padding that holds the tin still in the large box.
- Proposed owner: Warehouse lead
- How you will know: customers in this theme next month (5 this month), and replacement or refund requests about dented tins (2 this month: TK-5502, RV-0903).

2. Discount codes refused at checkout: Customers are refused at checkout by codes they were sent, and write in to get the discount.
- Evidence: customers 4, items 4, score 8; TK-5504, TK-5505, TK-5508, TK-5509
- Cause: Partly shown. AUTUMN10 excludes gift sets and teaware (known changes, 1 October 2026), and TK-5509 says "nothing says which items are excluded". TK-5505 was told the code from the email had expired, though the email gave the end of the month; the feedback does not show why. TK-5504 and TK-5508 give no cause.
- Proposed fix: Before each code email goes out, check the code in the store against what the email says: its end date and the items it excludes.
- Proposed owner: Ecommerce manager
- How you will know: customers in this theme next month (4 this month).

3. Slow replies from support: Customers who email wait several days for a reply and write again to chase it.
- Evidence: customers 2, items 2, score 4; TK-5507, TK-5510
- Cause: Not shown in the feedback.
- Proposed fix: Each morning, answer the oldest unanswered emails first and note how many were waiting, so the cause can be found.
- Proposed owner: Support lead
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
Draft: "You told us that once your order left us, you had no way to see where it was. Every dispatch email now includes the carrier's tracking link, for orders dispatched from 21 October 2026. If a dispatch email reaches you without one, reply to any email from us and tell us."
For approval by: Operations manager. Where it appears: the approver decides.

QUESTIONS FOR THE SUPPORT LEAD

1. Marketplace reviews are expected each month but were not supplied. Is there an October export to add before the report goes to the operations manager?

Prepared for the support lead. Nothing has been sent, posted or changed.
```

How the figures add up: 26 rows, less SV-1119 dated 30 September, leaves 25 items (11 tickets, 2 disputes, 5 reviews, 7 survey comments). Of these, 1 needs a person now, 20 sit in themes, 1 is a single mention and 3 are not placed. The six themes hold 21 item places because SV-1120 is in both "Tins arrive dented" and "Brewing instructions unclear". Customer C-2055 wrote a ticket and a review, and C-2078 opened a dispute and a ticket, so each counts once in its theme. The draft note has not been sent: the operations manager approves it and decides where it appears.
