# Complaint and refund request handling: trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Opus 5.5 (model ID claude-opus-5-5)
- **Date:** 2026-11-09

The inputs were the invented example's own: Shop H, the customer Marta, order H-20931, policy RP-3, the complaint log, tone guide TG-1, the settings and Dev's notes. No client data was used. The run followed the instruction block and the output format of version 0.1.0, as revised after an earlier run, on the seven inputs in [the example](example.md).

This run was done by the model that made those revisions to the template and the example, so it is not an independent check. The example's published output was then set to this run's output, wrapped to the example's line width, so the two agree by construction. The useful comparison is with the earlier run, described below.

## What came out

```
COMPLAINT AND REFUND REQUEST: Marta, order H-20931, email of Monday 2 November 2026
Status: Prepared for Dev. Not sent, not refunded. Decision needed first from Ana (owner): Marta asks for something for the trouble, which R6 leaves to the owner.
Received: email, Monday 2 November 2026, 09:05. Policy: RP-3, 1 August 2026. Order record as of Monday 2 November 2026, 10:15. Today: Monday 2 November 2026.
Customer: returning: 1 earlier order in the record (H-19877); 0 earlier complaints in the log, matched by order id.

WHAT THE CUSTOMER REPORTS AND ASKS FOR
1. "The large serving bowl has a big chip on the rim, photo attached." Confirmed in part by Dev's note on the photo: a chip about 2 cm long on the rim. That it was there on arrival rests on Marta's account.
2. "The mugs are a much darker green than on your website, nothing like the photos." Not shown in the inputs.
3. "A full refund for the whole order, shipping included." Asks for: refund of USD 139.50.
4. "Something for the trouble." Asks for: a goodwill gesture.

THE ORDER
Matched by: order number in the message.
Speckled mug (set of 4), qty 1, USD 72.00, delivered 28 October 2026, refunded so far USD 0.00
Large serving bowl, qty 1, USD 58.00, delivered 28 October 2026, refunded so far USD 0.00
Shipping, qty 1, USD 9.50, delivered 28 October 2026, refunded so far USD 0.00
Paid by: card ending 4417. Open card dispute: no.

POLICY CHECK
R2, bowl: damaged on arrival, reported within 14 days of delivery, with a photo. Delivered Wednesday 28 October, reported Monday 2 November: day 5 of 14, last day Wednesday 11 November (order record; message). Photo supplied (Dev's note). That the chip was there on arrival is Marta's account; R2 asks for no more than the report and the photo. Met.
R4, mugs: colour that differs from the photos is not a fault. The complaint about the mugs is their colour against the website photos (message). Met, so R2 does not apply to the mugs; R4 points them to R1.
R1, mugs: unused, returned within 30 days of delivery. Delivered 28 October, so the last day is Friday 27 November 2026 (order record). Not known: whether the mugs are unused; they have not been returned.
R3, shipping: refunded only when the whole order is refunded under R2. Only the bowl falls under R2. Not met.
R5, bowl: a refund goes to the original payment method. Card ending 4417 (order record). Met.
R6, something for the trouble: goodwill is decided by the owner. Not known: Ana has not seen this complaint (Dev's note).
Result: Partly within policy.
Remedy allowed: refund of the bowl in full, or a replacement, at Marta's choice; she asks for a refund (R2, Large serving bowl).
Alternative offered by the policy: return the mugs unused by Friday 27 November 2026 for a refund of USD 72.00, Marta paying the return postage (R1 and R4, Speckled mug set).

AMOUNT
Large serving bowl USD 58.00 - refunded so far USD 0.00 = USD 58.00
Not included: Shipping, USD 9.50 (R3). Speckled mug (set of 4), USD 72.00 (R1: only once returned unused; not proposed now). Something for the trouble (R6: the owner's decision).

FOR APPROVAL (NOT ISSUED)
Refund: USD 58.00, order H-20931, to card ending 4417, under R2 and R5. Approver: Dev (service lead, up to USD 100.00 per order).
Exception: None proposed. The owner may choose one; the reply is then redrafted.

DRAFT REPLY
Subject: Re: Order H-20931 - chipped bowl, wrong colour mugs

Hi Marta,

I've refunded the USD 58.00 for the large serving bowl to your card ending 4417. I'm sorry it reached you chipped. You don't need to send it back.

On the mugs: our glazes are mixed by hand, so their colour can differ from the photos on our website, and we don't treat that as a fault. If they're unused, you can return them by Friday 27 November for a refund of USD 72.00. The return postage is yours to cover. [Note: the return address and how to start a return are not in the inputs. Add them here before sending.]

Shipping is refunded only when a whole order is refunded as damaged or faulty on arrival, so the USD 9.50 stays as it is.

Dev, Shop H

BEFORE SENDING
Do first: Dev approves and issues the USD 58.00 refund on order H-20931 to card ending 4417. The reply says it has been refunded.
Confirm: Monday 2 November is day 5 after delivery on Wednesday 28 October 2026, inside R2's 14 days; Friday 27 November 2026 is day 30, the last day under R1. Check the delivery date in the shop. The return address and the way to start a return, for the bracketed note.
Questions for Ana: Marta asks for "something for the trouble". R6 leaves goodwill to you. Do you want to offer anything? If so, say what, and the reply is redrafted before it goes.
Not said, and why: anything for the trouble (R6, waiting on Ana); the replacement bowl R2 also allows (Marta asks for a refund); how long the refund takes to reach the card (RP-3 gives no period).
Tone check: TG-1. Rule 1: first name, signed "Dev, Shop H". Rule 2: the refund opens the reply. Rule 3: one apology, for the chipped bowl. Rule 4: no barred words, no exclamation marks. Rule 5: 109 words from the greeting to the sign-off, not counting the subject line or the bracketed note, against a limit of 170.

REPEAT CHECK
Damaged in transit: 3 in the 30 days to 2 November 2026, including this one (H-20544, H-20702, H-20931). Question for Ana: all three are serving bowls (chipped at the rim, cracked, chipped at the rim). Is it worth looking at how serving bowls are packed?
Colour not as pictured: 2 in the 30 days to 2 November 2026, including this one (H-20811, H-20931). No repeat flagged.

AFTER SENDING
Complaint log line for the handler to add: 2026-11-02, H-20931, Damaged in transit, Large serving bowl chipped at rim; refund USD 58.00 under R2.
Complaint log line for the handler to add: 2026-11-02, H-20931, Colour not as pictured, Mugs darker than photos; return under R1 offered.
Follow-up: Ana's answer on goodwill, then a redraft if she offers anything (Dev). If the mugs come back by Friday 27 November 2026, Dev checks they are unused and prepares the USD 72.00 refund under R1 for approval (Dev).

Prepared for Dev. Nothing has been sent, refunded, credited or recorded by the assistant.
Not completed, and what is needed: the return address and how to start a return (from Dev); whether to offer anything for the trouble (Ana's decision).
```

## What was observed

- **Every required part was produced.** The four header lines, all nine headed sections of the output format in order, and the two closing lines ending with "Not completed". Nothing in the instructions told the assistant to stop: the message, order record and policy were present, the export headers matched, one order matched by its number, no dispute was open and nothing was refunded. No lawyer, regulator, injury or card number appeared, and nothing in the message read as an order to the assistant.
- **The revised rules settled the points the earlier run left open.** The status line came out as "Decision needed first", because the goodwill request must be answered before the reply goes, and the repeat check's packaging question was not counted. The bowl's chip was marked "Confirmed in part", with its timing named as resting on Marta's account, and R2 was Met because the clause asks for the report and a photo, not more. Earlier complaints were matched through the order ids of Marta's two orders: none in the log. The 30-day window was counted from the day after delivery and ends on 27 November, listed under "Confirm". "Do first" lists both the approval and the issuing, because the reply says "I've refunded".
- **Facts not in the inputs.** None found. The reply's shipping sentence follows R3 (a whole order refunded as damaged or faulty on arrival, which is R2's test), and the mug return is stated as "for a refund of USD 72.00" with no timing, since RP-3 gives none.
- **Where the instructions still needed a judgment.**
  - Whether the reply should mention the replacement R2 lets the customer choose instead of a refund. This run left it out, because Marta asked for a refund, and listed it under "Not said". The template leaves that to the drafter.
  - R1's "returned within 30 days" is a condition that has not happened yet. Of the three results, "Not known" with what is needed was the closest fit.
  - The log's category "Damaged in transit" names a cause the inputs do not show; the chip could have happened before dispatch. The run used the log's own category, as the instructions say.
  - The reply could have said "I'm refunding" instead of "I've refunded", which would leave only the approval under "Do first". The template allows either.
- **The earlier run.** An earlier run on the same day, by Claude Sonnet 5.5 in the same product, used the previous instructions and a previous version of the example (the mug set at a different price, and the message ending "not what I picked at all"). It produced every section and the same refund for the bowl. It found these gaps, which were settled before this run: no rule for whether a pending owner question makes the status "Decision needed first"; the instruction block and the procedure listed "Do first" items differently; no stated end day for a 30-day window; no value for a problem that is confirmed but whose timing rests on the customer's account; no way to match earlier complaints, since the log has no customer column; "not what I picked" could mean a different colour was sent, which no clause covers (the example's message was reworded to remove that reading); and the example's reply had loosened R3's wording. Its record is replaced by this one.
- **Edited after this run (2026-11-09).** After review, the instruction block gained three lines the procedure already stated: with no order record, match no order and go no further than step 2; a message announcing changed bank details is held for the owner, like a request to pay a different card, account or person; and a problem that fits no log category is marked "new category". The procedure's step 8 also lost a reason clause, and the reviewer checklist now names "Confirmed in part". The output format is unchanged. None of these bears on the inputs above, and the run was not repeated.
- **Shortcomings.** This is one run, by one model, on one invented example, and that model also revised the template and wrote the published output, so the comparison is not independent. It shows the revised template can be followed on this input. It does not show how the template behaves with a different model, a messier message or a real order export.
