# Product recall customer contact plan: an invented example

*Illustrative example with invented data.* The business, the product, the notice, the customers, the people and every record below are invented, and contact details use made-up addresses and numbers. Business R is an invented online shop that sells small furniture for the home. It has recalled one of its folding stools, and its managing director has approved the notice. Eight days into contacting customers, the customer care lead runs the workflow template again with the care team's contact log and the warehouse's returns log. First come the inputs the care lead supplied, in full, then the plan the workflow template returned.

## The inputs

### 1. The recall record

```
Notice reference: FS2-0926
Product: FS-2 two-step folding stool. SKUs FS2-OAK (oak finish) and
  FS2-WHT (white finish).
Affected: batches B24 and B25, sold between 1 June and 15 August 2026.
  The batch number is printed under the top step.
Approved by: Managing director, 28 September 2026.

Approved notice wording:
Business R is recalling the FS-2 two-step folding stool from batches B24
and B25, sold between 1 June and 15 August 2026. The hinge under the top
step can crack, and the stool may fold while someone is standing on it.
Stop using the stool straight away and keep it folded. You can find the
batch number printed under the top step. We will collect the stool at no
cost to you and either refund what you paid or fit a new hinge and bring
it back.

Remedies we run:
1. Collection and refund. Our courier collects the stool from your home
   at no cost. We refund the price you paid to your original payment
   method within 5 working days of the stool reaching our warehouse.
2. Collection and hinge repair. Our courier collects the stool at no
   cost. Our workshop fits a new hinge and we deliver the stool back to
   you within 10 working days of collection.

How customers respond: reply to our email, or call 555-0100, Monday to
  Friday, 9:00 to 17:00.

Approved short message (for voicemail, or when someone else answers):
Hello, this is Business R with a message for [customer name]. Please call
us on 555-0100, Monday to Friday, 9 to 5. Thank you.

Approved answers:
Q: Do I have to be at home for the collection?
A: Yes, or someone you trust. The courier agrees a two-hour slot with you
   first.
Q: Is my stool affected if it comes from a different batch?
A: Only stools from batches B24 and B25 sold between 1 June and 15 August
   2026 are part of this recall.
Q: How soon is the refund paid?
A: Within 5 working days of the stool reaching our warehouse.

Escalation role: Operations manager.
```

### 2. The order export (every order containing an FS-2, taken Wednesday 7 October 2026)

```
order_id,order_date,customer_ref,customer_name,email,phone,sku,lot_or_serial,quantity,do_not_contact
R-5101,2026-06-04,C-201,Rosa T.,rosa.t@example.com,555-0111,FS2-OAK,B24,1,no
R-5133,2026-06-19,C-214,Imran K.,imran.k@example.com,555-0112,FS2-WHT,B24,2,no
R-5160,2026-07-02,C-229,Jo P.,jo.p@example.com,,FS2-OAK,B25,1,no
R-5188,2026-07-15,C-233,Dana M.,dana.m@example.com,555-0114,FS2-OAK,,1,no
R-5190,2026-07-16,C-201,Rosa T.,rosa.t@example.com,555-0111,FS2-WHT,B25,1,no
R-5215,2026-07-29,C-240,Theo B.,,555-0115,FS2-WHT,B25,1,no
R-5242,2026-08-09,C-251,Mina S.,mina.s@example.com,555-0116,FS2-OAK,B25,1,yes
R-5266,2026-08-12,C-258,Sam W.,sam.w@example.com,555-0117,FS2-OAK,B26,1,no
R-5290,2026-08-20,C-262,Lee A.,lee.a@example.com,555-0118,FS2-OAK,B25,1,no
```

### 3. The contact log (kept by the care team, as of Wednesday 7 October 2026)

```
customer_ref,date,channel,contact_by,outcome,remedy_chosen,note
C-201,2026-09-30,email,Care team member A,sent,,
C-201,2026-10-01,email,Care team member A,replied,Collection and refund,"Wants both stools collected. Asks: will you pay for the scratch the stool left on my kitchen floor?"
C-214,2026-09-30,email,Care team member A,sent,,
C-214,2026-10-05,phone,Care team member B,reached,Collection and hinge repair,Asked for collection as soon as possible.
C-229,2026-09-30,email,Care team member A,sent,,
C-229,2026-10-05,email,Care team member A,sent,,Second email. No phone number on file.
C-240,2026-10-01,phone,Care team member B,message left,,Approved short message left.
C-240,2026-10-06,phone,Care team member B,reached,,Says he gave the stool to his brother in August. Did not choose a remedy.
```

### 4. The returns log (kept by the warehouse, as of Wednesday 7 October 2026)

```
order_id,customer_ref,lot_or_serial,quantity,event,date,confirmed_by
R-5101,C-201,B24,1,collection booked,2026-10-02,
R-5190,C-201,B25,1,collection booked,2026-10-02,
R-5133,C-214,B24,2,collection booked,2026-10-06,
R-5101,C-201,B24,1,item received,2026-10-06,Warehouse lead
R-5190,C-201,B25,1,item received,2026-10-06,
R-5133,C-214,B24,2,repair completed,2026-10-07,Workshop lead
```

### 5. Settings

```
Today: Wednesday 7 October 2026
Care lead: Customer care lead
Channels: email first, then phone. A customer with one route gets that
  route again.
Attempt limit: 3 per customer
Gap between attempts: 3 working days (Monday to Friday)
Calling hours: Monday to Friday, 9:00 to 17:00, in each customer's own time zone
Drafts approved by: Customer care lead
```

## The output

**PRODUCT RECALL CUSTOMER CONTACT PLAN: FS-2 two-step folding stool, notice FS2-0926**

- **Status:** Draft for the customer care lead. Nothing has been sent and nobody has been contacted by the assistant. Questions to settle first: 3.
- Notice approved by the managing director on 28 September 2026. Order export as of 7 October 2026. Contact log as of 7 October 2026. Returns log as of 7 October 2026. Today: Wednesday 7 October 2026.

**1. Questions to settle**

1. For the approver: R-5290, Lee A. (C-262), FS2-OAK, batch B25, sold 20 August 2026. The notice covers batches B24 and B25 sold between 1 June and 15 August 2026. This stool is from an affected batch but was sold after the end date. Is it covered?
2. For the approver: R-5188, Dana M. (C-233), FS2-OAK, sold 15 July 2026, inside the dates. The export records no batch for this order, so whether the stool is from B24 or B25 cannot be told. Is this customer in scope?
3. For the returns lead: R-5190, Rosa T. (C-201), batch B25, 1 unit, "item received" on 6 October 2026 with no name or role in `confirmed_by`. Who confirmed it? Until that is recorded, the unit is not counted as back.

**2. Affected customers**

Rows read: 9. Affected: 6. Possibly affected: 2. Not affected: 1.

- C-201, Rosa T.: R-5101 FS2-OAK, B24 x 1; R-5190 FS2-WHT, B25 x 1. Units: 2. Contact: email and phone. Ready.
- C-214, Imran K.: R-5133 FS2-WHT, B24 x 2. Units: 2. Contact: email and phone. Ready.
- C-229, Jo P.: R-5160 FS2-OAK, B25 x 1. Units: 1. Contact: email. Ready.
- C-240, Theo B.: R-5215 FS2-WHT, B25 x 1. Units: 1. Contact: phone. Ready.
- C-251, Mina S.: R-5242 FS2-OAK, B25 x 1. Units: 1. Contact: email and phone. Held: marked do not contact.

Possibly affected, for the approver to rule on:

- C-262, R-5290, FS2-OAK, B25: an affected batch, sold 20 August 2026, after the stated end date (question 1).
- C-233, R-5188, FS2-OAK, identifier blank: no batch recorded, so it cannot be matched to B24 or B25 (question 2).

Not affected: R-5266 (batch B26).

Held for the care lead's decision: C-251: marked do not contact in the order export.

**3. Approved notice, word for word (approved by the managing director, 28 September 2026)**

"Business R is recalling the FS-2 two-step folding stool from batches B24 and B25, sold between 1 June and 15 August 2026. The hinge under the top step can crack, and the stool may fold while someone is standing on it. Stop using the stool straight away and keep it folded. You can find the batch number printed under the top step. We will collect the stool at no cost to you and either refund what you paid or fit a new hinge and bring it back."

**4. Remedies the business runs**

1. Collection and refund: Our courier collects the stool from your home at no cost. We refund the price you paid to your original payment method within 5 working days of the stool reaching our warehouse.
2. Collection and hinge repair: Our courier collects the stool at no cost. Our workshop fits a new hinge and we deliver the stool back to you within 10 working days of collection.

No other remedy is offered.

**5. Email or letter draft (for the customer care lead's approval; not sent)**

Subject: Important notice about your FS-2 folding stool (FS2-0926)

Dear [customer name],

Our records show that you bought [product and batch] from us, on order [order numbers].

Business R is recalling the FS-2 two-step folding stool from batches B24 and B25, sold between 1 June and 15 August 2026. The hinge under the top step can crack, and the stool may fold while someone is standing on it. Stop using the stool straight away and keep it folded. You can find the batch number printed under the top step. We will collect the stool at no cost to you and either refund what you paid or fit a new hinge and bring it back.

You can choose either of these:

1. Collection and refund: Our courier collects the stool from your home at no cost. We refund the price you paid to your original payment method within 5 working days of the stool reaching our warehouse.
2. Collection and hinge repair: Our courier collects the stool at no cost. Our workshop fits a new hinge and we deliver the stool back to you within 10 working days of collection.

To choose, reply to this email or call 555-0100, Monday to Friday, 9:00 to 17:00.

Answers to common questions:

- Do I have to be at home for the collection? Yes, or someone you trust. The courier agrees a two-hour slot with you first.
- Is my stool affected if it comes from a different batch? Only stools from batches B24 and B25 sold between 1 June and 15 August 2026 are part of this recall.
- How soon is the refund paid? Within 5 working days of the stool reaching our warehouse.

Once you have chosen, our care team will be in touch to settle the details. This matter stays open until your stool is back with us or has been repaired.

Customer care, Business R

**6. Phone script (read by a person on the care team)**

1. "Hello, this is [your name] from Business R. May I speak with [customer name], please?" Say nothing about the stool, the order or the recall until that person confirms who they are.
2. If someone else answers, or the call goes to voicemail, leave only the message in section 7, and log "message left".
3. Once the customer confirms who they are: "We're calling about a notice for the FS-2 folding stool you bought from us." Then read the notice in section 3 word for word.
4. "Is the stool still with you?" If not, note where it went: already sent back, handed on, or thrown out. Log the answer as given.
5. Go through both remedies in section 4 without favouring either. Log their pick and when suits them.
6. Use the approved answers in section 8 and nothing else. For any other question: "That's one for our operations manager, who will be in touch with you about it." Log the question in their words.
7. If they ask whether the stool is safe, how to store it or how to get rid of it, read the relevant sentence of the notice again and stop there. Offer no reassurance, such as "don't worry", and no opinion of your own.
8. If they mention an injury, damage to their home or belongings, a claim, a lawyer or a regulator, or they are upset: "I'm sorry to hear that. Our operations manager will be in touch with you about it." Log it and close the call courteously, without debating the point or accepting blame.
9. If they want no further contact: "Understood, I've noted that, and I'll pass it to our customer care lead." Log it and end the call. Promise nothing more either way; the customer care lead decides what happens next.
10. Refunds go back to the original payment method, so take no card or bank details, password or ID number, even if the customer starts to read them out.
11. Close: "Our care team will be in touch about the [collection date | details]. This stays open until your stool is back with us or has been repaired. Thank you for your time." Do not suggest the matter is closed.

**7. Message if the customer is not the one who answers, or for voicemail**

"Hello, this is Business R with a message for [customer name]. Please call us on 555-0100, Monday to Friday, 9 to 5. Thank you."

**8. Approved answers**

- Q: Do I have to be at home for the collection? A: Yes, or someone you trust. The courier agrees a two-hour slot with you first.
- Q: Is my stool affected if it comes from a different batch? A: Only stools from batches B24 and B25 sold between 1 June and 15 August 2026 are part of this recall.
- Q: How soon is the refund paid? A: Within 5 working days of the stool reaching our warehouse.

Anything else goes to the operations manager.

**9. Contact tracker**

- C-201, Rosa T.: Remedy chosen: Collection and refund. Attempts 1. Last attempt: 30 September 2026, email, Care team member A. Units confirmed back or repaired: 1 of 2 (R-5101, item received, 6 October 2026, confirmed by the warehouse lead). Follow-up: section 10.
- C-214, Imran K.: Done. Attempts 2. Last attempt: 5 October 2026, phone, Care team member B. Units confirmed back or repaired: 2 of 2 (R-5133, repair completed, 7 October 2026, confirmed by the workshop lead).
- C-229, Jo P.: Attempted. Attempts 2. Last attempt: 5 October 2026, email, Care team member A. Units confirmed back or repaired: 0 of 1.
- C-240, Theo B.: Needs a person. Attempts 2. Last attempt: 6 October 2026, phone, Care team member B. Units confirmed back or repaired: 0 of 1. Follow-up: section 10.
- C-251, Mina S.: Held. Attempts 0. Last attempt: none. Units confirmed back or repaired: 0 of 1.

Counts:

- Customers on the list: 5
- Attempted: 4 of 5 on the list
- Reached: 3 of 4 attempted
- Remedy chosen: 2 of 3 reached
- Done: 1 of 5 on the list
- Units confirmed back or repaired: 3 of 7 affected units

**10. Follow-up for a person**

- C-201: on 1 October 2026 asked, "will you pay for the scratch the stool left on my kitchen floor?" Damage to property, outside the approved answers. → Operations manager.
- C-240: on 6 October 2026 said he gave the stool to his brother in August, and chose no remedy. Item passed on. → Customer care lead.

**11. Next contacts due**

- C-229: email (the only route on file), on or after Thursday 8 October 2026, attempt 3 of 3.

Reached, no listed remedy chosen, for the care lead to decide the next step: None.

Calling hours: Monday to Friday, 9:00 to 17:00, in each customer's own time zone. The export holds no time zone: the care team applies each customer's own, and any holiday the settings do not list.

Draft for the customer care lead. Nothing has been sent, no customer has been contacted, and no record has been changed by the assistant. A customer is done only when every affected unit is confirmed back or repaired. The decision to recall, the notice and every regulatory or legal duty stay with the business and its advisers.
