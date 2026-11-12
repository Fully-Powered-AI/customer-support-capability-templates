# Complaint and refund request handling: an invented example

*Illustrative example with invented data.* The shop, the customer, the people, the orders, the policy and every document below are invented. Shop H is an invented online shop that sells handmade ceramic tableware; Ana owns it and Dev is its service lead. First come the inputs Dev supplied, in full, then what the workflow template returned.

## The inputs

### 1. The customer's message

```
Channel: email. Received Monday 2 November 2026, 09:05.
From: Marta <marta@example.com>
Subject: Order H-20931 - chipped bowl, wrong colour mugs

Hi,

My order came on Wednesday. The large serving bowl has a big chip on the
rim, photo attached. And the mugs are a much darker green than on your
website, nothing like the photos.

I'd like a full refund for the whole order, shipping included. Honestly
I think something for the trouble would be fair too.

Marta
```

### 2. The order record (shop export, taken Monday 2 November 2026, 10:15)

```
order_id,order_date,customer_email,item,quantity,line_total,payment_method,delivered_date,refunded_to_date,dispute_open
H-19877,2026-07-02,marta@example.com,Small plate,2,36.00,card ending 4417,2026-07-06,0.00,no
H-19877,2026-07-02,marta@example.com,Shipping,1,6.50,card ending 4417,2026-07-06,0.00,no
H-20931,2026-10-24,marta@example.com,Speckled mug (set of 4),1,72.00,card ending 4417,2026-10-28,0.00,no
H-20931,2026-10-24,marta@example.com,Large serving bowl,1,58.00,card ending 4417,2026-10-28,0.00,no
H-20931,2026-10-24,marta@example.com,Shipping,1,9.50,card ending 4417,2026-10-28,0.00,no
```

### 3. The refund and return policy (RP-3, dated 1 August 2026)

```
R1. Change of mind. Return unused items within 30 days of delivery for a
    refund of the item price. You pay the return postage.
R2. Damaged or faulty on arrival. Tell us within 14 days of delivery and
    send a photo. We refund the item in full or send a replacement, your
    choice. You don't need to send it back.
R3. Shipping is refunded only when a whole order is refunded under R2.
R4. Our glazes are mixed by hand. Colour that differs from the photos is
    not a fault; those items can be returned under R1.
R5. Refunds go back to the original payment method.
R6. Goodwill gestures, and anything this policy does not list, are
    decided by the owner.
```

### 4. The complaint log (export, last 40 days)

```
date,order_id,category,summary
2026-09-28,H-20390,Damaged in transit,Mug handle broken
2026-10-09,H-20544,Damaged in transit,Serving bowl chipped at rim
2026-10-15,H-20612,Late delivery,Arrived 4 days after estimate
2026-10-21,H-20702,Damaged in transit,Large serving bowl cracked
2026-10-27,H-20811,Colour not as pictured,Mugs darker than photos
```

### 5. The tone guide (TG-1, dated 1 September 2026)

```
1. First names. Sign off "Dev, Shop H".
2. The outcome first.
3. When we got it wrong, apologize once, for the specific thing.
4. Never "unfortunately" or "any inconvenience". No exclamation marks.
5. Email: under 170 words.
```

### 6. Settings

```
Today: Monday 2 November 2026. Currency: USD.
Approvals: Dev (service lead) may approve refunds up to USD 100.00 per
  order. Above that, Ana (owner).
Escalation role and safety role: Ana (owner). A holding acknowledgement
  may be drafted.
Repeat window: 30 days. Repeat count: 3.
```

### 7. Dev's notes

```
Photo came with the email: it shows a chip about 2 cm long on the rim of
the bowl. Nothing issued yet. Ana hasn't seen this one.
```

## The output

```
COMPLAINT AND REFUND REQUEST: Marta, order H-20931, email of Monday
2 November 2026
Status: Prepared for Dev. Not sent, not refunded. Decision needed first
from Ana (owner): Marta asks for something for the trouble, which R6
leaves to the owner.
Received: email, Monday 2 November 2026, 09:05. Policy: RP-3, 1 August
2026. Order record as of Monday 2 November 2026, 10:15. Today: Monday
2 November 2026.
Customer: returning: 1 earlier order in the record (H-19877); 0 earlier
complaints in the log, matched by order id.

WHAT THE CUSTOMER REPORTS AND ASKS FOR
1. "The large serving bowl has a big chip on the rim, photo attached."
   Confirmed in part by Dev's note on the photo: a chip about 2 cm long
   on the rim. That it was there on arrival rests on Marta's account.
2. "The mugs are a much darker green than on your website, nothing like
   the photos." Not shown in the inputs.
3. "A full refund for the whole order, shipping included." Asks for:
   refund of USD 139.50.
4. "Something for the trouble." Asks for: a goodwill gesture.

THE ORDER
Matched by: order number in the message.
Speckled mug (set of 4), qty 1, USD 72.00, delivered 28 October 2026,
  refunded so far USD 0.00
Large serving bowl, qty 1, USD 58.00, delivered 28 October 2026,
  refunded so far USD 0.00
Shipping, qty 1, USD 9.50, delivered 28 October 2026, refunded so far
  USD 0.00
Paid by: card ending 4417. Open card dispute: no.

POLICY CHECK
R2, bowl: damaged on arrival, reported within 14 days of delivery, with
  a photo. Delivered Wednesday 28 October, reported Monday 2 November:
  day 5 of 14, last day Wednesday 11 November (order record; message).
  Photo supplied (Dev's note). That the chip was there on arrival is
  Marta's account; R2 asks for no more than the report and the photo.
  Met.
R4, mugs: colour that differs from the photos is not a fault. The
  complaint about the mugs is their colour against the website photos
  (message). Met, so R2 does not apply to the mugs; R4 points them to
  R1.
R1, mugs: unused, returned within 30 days of delivery. Delivered
  28 October, so the last day is Friday 27 November 2026 (order
  record). Not known: whether the mugs are unused; they have not been
  returned.
R3, shipping: refunded only when the whole order is refunded under R2.
  Only the bowl falls under R2. Not met.
R5, bowl: a refund goes to the original payment method. Card ending
  4417 (order record). Met.
R6, something for the trouble: goodwill is decided by the owner. Not
  known: Ana has not seen this complaint (Dev's note).
Result: Partly within policy.
Remedy allowed: refund of the bowl in full, or a replacement, at
  Marta's choice; she asks for a refund (R2, Large serving bowl).
Alternative offered by the policy: return the mugs unused by Friday
  27 November 2026 for a refund of USD 72.00, Marta paying the return
  postage (R1 and R4, Speckled mug set).

AMOUNT
Large serving bowl USD 58.00 - refunded so far USD 0.00 = USD 58.00
Not included: Shipping, USD 9.50 (R3). Speckled mug (set of 4),
  USD 72.00 (R1: only once returned unused; not proposed now).
  Something for the trouble (R6: the owner's decision).

FOR APPROVAL (NOT ISSUED)
Refund: USD 58.00, order H-20931, to card ending 4417, under R2 and R5.
Approver: Dev (service lead, up to USD 100.00 per order).
Exception: None proposed. The owner may choose one; the reply is then
redrafted.

DRAFT REPLY
Subject: Re: Order H-20931 - chipped bowl, wrong colour mugs

Hi Marta,

I've refunded the USD 58.00 for the large serving bowl to your card
ending 4417. I'm sorry it reached you chipped. You don't need to send
it back.

On the mugs: our glazes are mixed by hand, so their colour can differ
from the photos on our website, and we don't treat that as a fault. If
they're unused, you can return them by Friday 27 November for a refund
of USD 72.00. The return postage is yours to cover. [Note: the return
address and how to start a return are not in the inputs. Add them here
before sending.]

Shipping is refunded only when a whole order is refunded as damaged or
faulty on arrival, so the USD 9.50 stays as it is.

Dev, Shop H

BEFORE SENDING
Do first: Dev approves and issues the USD 58.00 refund on order H-20931
  to card ending 4417. The reply says it has been refunded.
Confirm: Monday 2 November is day 5 after delivery on Wednesday
  28 October 2026, inside R2's 14 days; Friday 27 November 2026 is day
  30, the last day under R1. Check the delivery date in the shop. The
  return address and the way to start a return, for the bracketed note.
Questions for Ana: Marta asks for "something for the trouble". R6
  leaves goodwill to you. Do you want to offer anything? If so, say
  what, and the reply is redrafted before it goes.
Not said, and why: anything for the trouble (R6, waiting on Ana); the
  replacement bowl R2 also allows (Marta asks for a refund); how long
  the refund takes to reach the card (RP-3 gives no period).
Tone check: TG-1. Rule 1: first name, signed "Dev, Shop H". Rule 2: the
  refund opens the reply. Rule 3: one apology, for the chipped bowl.
  Rule 4: no barred words, no exclamation marks. Rule 5: 109 words from
  the greeting to the sign-off, not counting the subject line or the
  bracketed note, against a limit of 170.

REPEAT CHECK
Damaged in transit: 3 in the 30 days to 2 November 2026, including this
  one (H-20544, H-20702, H-20931). Question for Ana: all three are
  serving bowls (chipped at the rim, cracked, chipped at the rim). Is it
  worth looking at how serving bowls are packed?
Colour not as pictured: 2 in the 30 days to 2 November 2026, including
  this one (H-20811, H-20931). No repeat flagged.

AFTER SENDING
Complaint log line for the handler to add: 2026-11-02, H-20931, Damaged
  in transit, Large serving bowl chipped at rim; refund USD 58.00 under
  R2.
Complaint log line for the handler to add: 2026-11-02, H-20931, Colour
  not as pictured, Mugs darker than photos; return under R1 offered.
Follow-up: Ana's answer on goodwill, then a redraft if she offers
  anything (Dev). If the mugs come back by Friday 27 November 2026, Dev
  checks they are unused and prepares the USD 72.00 refund under R1 for
  approval (Dev).

Prepared for Dev. Nothing has been sent, refunded, credited or recorded
by the assistant.
Not completed, and what is needed: the return address and how to start
a return (from Dev); whether to offer anything for the trouble (Ana's
decision).
```

The log entry of 28 September falls outside the 30-day window, so it is not counted. From here the decisions are people's: Ana decides on goodwill, and Dev adds the return address, approves and issues the bowl refund, and sends the reply himself.
