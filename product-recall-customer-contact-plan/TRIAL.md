# Product recall customer contact plan: trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Opus 5.5 (model ID claude-opus-5-5) for the recorded run; the first run used Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The template was run four times on 10 November 2026 on its invented example in `public/example.md` (Business R, the FS-2 folding stool, notice FS2-0926): the recall record, the order export, the contact log, the returns log and the settings. No client data was used in any run. The pasted instructions, the output format and the example were revised after the first run, the sorting rule and two lines of the pasted instructions after the second, and, following an independent review, a few lines of the instructions, the output format and the example after the third. This record gives a short account of the first three runs and the fourth in full.

## The first run

Claude Sonnet 5.5, a model that had not written the template, followed the instruction block and the output format and read the example's output only after producing its own. Its output was complete and its arithmetic held: the same three questions, the same sorting of all nine rows, the same customer lines, tracker statuses, six counts, first follow-up item and single next contact as the example. It differed in two places. It gave C-201's "Last" as the outgoing email of 30 September, where the example gave the customer's reply of 1 October, because the template said a reply is not an attempt but did not say what "Last" meant. It sent C-240's passed-on stool to the operations manager, where the example sent it to the customer care lead, because the template said only "to the role that handles it". It also noted that the example's phone script added "May I read it to you?" and "please keep to the notice", which no input supplies.

It listed nine points the template left open: whether the count "Attempted" covers every customer with an attempt or only those in the Attempted status; whether Done customers count under "Remedy chosen"; that a damage report from a customer who had chosen a remedy showed only in the follow-up list; that a `do_not_contact` flag from the export never reaches the follow-up list; whether a returns entry's quantity covers that many units; whether "repair completed" should close a customer before the repaired stool is delivered back; that "character for character" cannot apply to line breaks; that calling hours had no place in the output and the export no time zone; and that the working-day gap ignored public holidays.

It found a defect in the template itself: the pasted instruction block named the statuses Needs a person and Attempts used up without their rules, did not say to write the Questions section or set the question count in the status line, and checked the headers of the export only, not the two logs. It also noted that the version notes still said the template had not been tried.

Changes made after the first run:

- The pasted instructions now carry the rule for every tracker status, in an order of precedence (Done, Held, Needs a person, Remedy chosen, Reached, Attempts used up, Attempted, Not contacted), what happens when either log is missing, the instruction to write the numbered questions and the count in the status line, and the header check for the contact log and the returns log as well as the export.
- Each of the nine open points is settled in the procedure and the pasted instructions: each count's base is defined whatever the status, Done customers count as having chosen a remedy, "Last attempt" is the latest outgoing entry, a returns entry counts as many units as its quantity, a tracker line ends "Follow-up: section 10." when the customer has a follow-up item, a `do_not_contact` flag shows as Held rather than as a follow-up, only typed line breaks in the notice may be joined, the calling hours are printed under the next contacts with the time zone left to the care team, and the gap skips holidays the settings list. "What to customize" now says how a business can require a repaired item to be delivered back before it counts.
- Passed-on or thrown-away items, stop requests and unlisted remedies go to the care lead; injuries, damage, claims, lawyers, regulators and unanswered questions go to the escalation role.
- The example's tracker now gives C-201's last attempt as 30 September 2026, both C-201 and C-240 point to the follow-up list, the calling hours are printed under section 11, and the phone script no longer says "May I read it to you?" or "please keep to the notice".

## The second run

Claude Opus 5.5 ran the revised template in a fresh Claude Code session with every tool switched off. It was given only the pasted instruction block and the output format as its instructions, and the example's five inputs as the message; it did not see the procedure or the example's output. The model is the one that made the revisions, in a separate session.

Its tracker, all six counts, both follow-up items with their roles, and the next contact matched the example. It differed in sorting: it put R-5266 (batch B26, sold 12 August, inside the dates) under possibly affected and asked the approver about it, giving four questions and no row not affected. That followed the pasted rule as then written, "one stated condition met and another failed", which a readable batch outside the range meets. Its phone script also asked the customer to confirm the email address or delivery details on the order, and it wrote a sentence about the date before the plan.

Changes made after the second run:

- The sorting rule in the procedure and the pasted instructions now says a readable lot, batch or serial outside the stated range is not affected whatever the sale date, and possibly affected means a blank or unreadable identifier, or an identifier inside the range with another stated condition failing. Acceptance test 5 gained the matching case.
- The phone script, in the procedure and the pasted instructions, asks for the customer by name and for no other detail to prove who they are.
- The pasted instructions say to write nothing before the output format.

## The third run

The same set-up as the second run, on the template as it then stood. Its output, exactly as returned, is kept here because the record of every later change starts from it:

```
PRODUCT RECALL CUSTOMER CONTACT PLAN: FS-2 two-step folding stool, notice FS2-0926
Status: Draft for Customer care lead. Nothing has been sent and nobody has been contacted by the assistant. Questions to settle first: 3
Notice approved by Managing director on 28 September 2026. Order export as of 7 October 2026. Contact log as of 7 October 2026. Returns log as of 7 October 2026. Today: 7 October 2026.

1. QUESTIONS TO SETTLE
1. For approver: Order R-5188 (C-233, Dana M.) is for an FS2-OAK, quantity 1, sold 2026-07-15. That date is inside the sale-date range, but the export has no batch number for it. Is this order part of the recall? Nobody will contact this customer until you rule.
2. For approver: Order R-5290 (C-262, Lee A.) is for an FS2-OAK from batch B25, quantity 1. B25 is an affected batch, but the order was sold on 2026-08-20. That is after the sale-date range ends on 15 August 2026. Is this order part of the recall? Nobody will contact this customer until you rule.
3. For returns lead: Order R-5190 (C-201, Rosa T.), batch B25, quantity 1, has an "item received" entry dated 2026-10-06, but the confirmed_by field is blank. This unit is not counted as back until someone confirms it. Can it be confirmed, and by whom?

2. AFFECTED CUSTOMERS
Rows read: 9. Affected: 6. Possibly affected: 2. Not affected: 1.
C-201, Rosa T.: R-5101 FS-2 two-step folding stool (FS2-OAK), batch B24 x 1; R-5190 FS-2 two-step folding stool (FS2-WHT), batch B25 x 1. Units: 2. Contact: email and phone. Ready
C-214, Imran K.: R-5133 FS-2 two-step folding stool (FS2-WHT), batch B24 x 2. Units: 2. Contact: email and phone. Ready
C-229, Jo P.: R-5160 FS-2 two-step folding stool (FS2-OAK), batch B25 x 1. Units: 1. Contact: email. Ready
C-240, Theo B.: R-5215 FS-2 two-step folding stool (FS2-WHT), batch B25 x 1. Units: 1. Contact: phone. Ready
C-251, Mina S.: R-5242 FS-2 two-step folding stool (FS2-OAK), batch B25 x 1. Units: 1. Contact: email and phone. Held: marked do_not_contact in the export.
Possibly affected, for the approver to rule on:
C-233, R-5188, FS-2 two-step folding stool (FS2-OAK), identifier blank: no batch number in the export. Sold 2026-07-15, which is inside the sale-date range.
C-262, R-5290, FS-2 two-step folding stool (FS2-OAK), batch B25: the batch is in the affected range, but it was sold 2026-08-20, after the range ends on 15 August 2026.
Not affected: R-5266
Held for the care lead's decision: C-251: marked do_not_contact in the export.

3. APPROVED NOTICE, WORD FOR WORD (approved by Managing director, 28 September 2026)
"Business R is recalling the FS-2 two-step folding stool from batches B24 and B25, sold between 1 June and 15 August 2026. The hinge under the top step can crack, and the stool may fold while someone is standing on it. Stop using the stool straight away and keep it folded. You can find the batch number printed under the top step. We will collect the stool at no cost to you and either refund what you paid or fit a new hinge and bring it back."

4. REMEDIES THE BUSINESS RUNS
1. Collection and refund: Our courier collects the stool from your home at no cost. We refund the price you paid to your original payment method within 5 working days of the stool reaching our warehouse.
2. Collection and hinge repair: Our courier collects the stool at no cost. Our workshop fits a new hinge and we deliver the stool back to you within 10 working days of collection.
No other remedy is offered.

5. EMAIL OR LETTER DRAFT (for the care lead's approval; not sent)
Subject: Recall notice FS2-0926: FS-2 two-step folding stool, batches B24 and B25

Dear [customer name],

We are writing about the FS-2 two-step folding stool you bought from us:
[order number], [order date], FS-2 two-step folding stool ([SKU]), batch [batch number], quantity [quantity]
[repeat the line for each affected order]

Business R is recalling the FS-2 two-step folding stool from batches B24 and B25, sold between 1 June and 15 August 2026. The hinge under the top step can crack, and the stool may fold while someone is standing on it. Stop using the stool straight away and keep it folded. You can find the batch number printed under the top step. We will collect the stool at no cost to you and either refund what you paid or fit a new hinge and bring it back.

You can choose one of these two options:

1. Collection and refund: Our courier collects the stool from your home at no cost. We refund the price you paid to your original payment method within 5 working days of the stool reaching our warehouse.
2. Collection and hinge repair: Our courier collects the stool at no cost. Our workshop fits a new hinge and we deliver the stool back to you within 10 working days of collection.

To choose, reply to this email or call us on 555-0100, Monday to Friday, 9:00 to 17:00. Please tell us which option you would like and which days suit you for the collection.

Questions customers often ask:

Do I have to be at home for the collection?
Yes, or someone you trust. The courier agrees a two-hour slot with you first.

Is my stool affected if it comes from a different batch?
Only stools from batches B24 and B25 sold between 1 June and 15 August 2026 are part of this recall.

How soon is the refund paid?
Within 5 working days of the stool reaching our warehouse.

Our care team will be in touch to settle the details. We will keep this matter open until your stool is back with us or has been repaired.

Kind regards,
[care team member name]
Customer care, Business R
555-0100, Monday to Friday, 9:00 to 17:00

6. PHONE SCRIPT (read by a person on the care team)
1. Who is calling: "Hello, this is [your name] calling from Business R customer care."
2. Confirm the customer: "May I speak to [customer name], please?" Ask for no other detail to prove who they are: no address, date of birth, order number or payment details. Say nothing about the stool, the recall or the problem until the person confirms they are [customer name]. If someone else answers, or you reach voicemail, leave only the message in section 7, word for word, and record "message left". If you cannot leave it, record "no answer".
3. The notice: "Thank you. I'm calling about the FS-2 two-step folding stool you bought from us, order [order number], [SKU], batch [batch number]. I'd like to read you our notice." Read section 3 word for word. Add nothing and leave nothing out.
4. Item status: "Do you still have the stool?" Record one of: with them, sent back, handed on, thrown away. If it was handed on or thrown away, note what the customer says in their own words and pass it to the Customer care lead. Give no further advice.
5. Remedies: "We can offer two options." Read both from section 4, in that order, word for word, and do not favour either one. Ask: "Which would you prefer?" Record the choice and the days and times that suit them for the collection.
6. Questions: Answer only with the approved answers in section 8, word for word. For any other question say: "I'll pass that to our Operations manager, who will get back to you." Write the question down in the customer's own words.
7. Safety, handling or disposal questions: Read the notice in section 3 again. Add nothing, give no opinion and offer no reassurance.
8. Injury, damage, a claim, a lawyer, a regulator, or a customer who is upset: "Thank you for telling me. Our Operations manager will be in touch with you about this." Write down what they said in their own words. Do not argue, do not accept or deny blame, and offer nothing. Close the call politely.
9. Stop requests: If the customer asks not to be contacted again, say "I've noted that." Record "asked not to be contacted" and pass it to the Customer care lead. Make no further attempts.
10. No payment details: Do not ask for or write down card or bank details. If the customer starts to give them, stop them politely. The refund in option 1 goes to the original payment method, as the remedy sets out.
11. Close: "Our care team will be in touch to settle the details. We'll keep this open until the stool is back with us or repaired. If you need us before then, call 555-0100, Monday to Friday, 9:00 to 17:00. Thank you for your time." Record the outcome in the contact log yourself.

7. MESSAGE IF THE CUSTOMER IS NOT THE ONE WHO ANSWERS, OR FOR VOICEMAIL
"Hello, this is Business R with a message for [customer name]. Please call us on 555-0100, Monday to Friday, 9 to 5. Thank you."

8. APPROVED ANSWERS
Q: Do I have to be at home for the collection? A: Yes, or someone you trust. The courier agrees a two-hour slot with you first.
Q: Is my stool affected if it comes from a different batch? A: Only stools from batches B24 and B25 sold between 1 June and 15 August 2026 are part of this recall.
Q: How soon is the refund paid? A: Within 5 working days of the stool reaching our warehouse.
Anything else goes to Operations manager.

9. CONTACT TRACKER
C-201, Rosa T.: Remedy chosen: Collection and refund. Attempts 1. Last attempt: 2026-09-30, email, Care team member A. Units confirmed back or repaired: 1 of 2 (R-5101, item received, 2026-10-06, Warehouse lead). Follow-up: section 10.
C-214, Imran K.: Done. Attempts 2. Last attempt: 2026-10-05, phone, Care team member B. Units confirmed back or repaired: 2 of 2 (R-5133, repair completed, 2026-10-07, Workshop lead).
C-229, Jo P.: Attempted. Attempts 2. Last attempt: 2026-10-05, email, Care team member A. Units confirmed back or repaired: 0 of 1.
C-240, Theo B.: Needs a person. Attempts 2. Last attempt: 2026-10-06, phone, Care team member B. Units confirmed back or repaired: 0 of 1. Follow-up: section 10.
C-251, Mina S.: Held. Attempts 0. Last attempt: none. Units confirmed back or repaired: 0 of 1.
Counts:
Customers on the list: 5
Attempted: 4 of 5 on the list
Reached: 3 of 4 attempted
Remedy chosen: 2 of 3 reached
Done: 1 of 5 on the list
Units confirmed back or repaired: 3 of 7 affected units

10. FOLLOW-UP FOR A PERSON
C-201: 2026-10-01, by email reply: "Asks: will you pay for the scratch the stool left on my kitchen floor?" (damage and possible claim) → Operations manager
C-240: 2026-10-06, by phone: "Says he gave the stool to his brother in August. Did not choose a remedy." (item handed on) → Customer care lead

11. NEXT CONTACTS DUE
C-229: email, on or after 2026-10-08, attempt 3 of 3
Calling hours: Monday to Friday, 9:00 to 17:00, in each customer's own time zone. The export holds no time zone: the care team applies each customer's own, and any holiday the settings do not list.

Draft for Customer care lead. Nothing has been sent, no customer has been contacted, and no record has been changed by the assistant. A customer is done only when every affected unit is confirmed back or repaired. The decision to recall, the notice and every regulatory or legal duty stay with the business and its advisers.
```

The output followed the output format from the first line to the closing lines, with nothing before it, and the arithmetic held. Against the published example as it then stood, it was the same in the sorting of all nine rows, the three questions (in a different order), the customer lines and the held customer, every tracker status, attempt count, last attempt and unit count, all six counts, both follow-up items and their roles, the single next contact and the calling-hours line. The notice, the remedies and the short message were the same text, and the approved answers the same apart from "Operations manager" without "the" in the last line. The subject line, greeting, sign-off and close of the email differed, as the format allows, and the email's bracketed fields added "[order date]" and "[quantity]". Its phone script mentioned the order number, SKU and batch once the customer had confirmed who they were, where the example mentioned only the product. Its stop-request line said "Make no further attempts", which went a little further than the template's "the care lead decides", although it also passed the request to the care lead, and its close told the care team member to record the outcome in the contact log themselves, which is a person's action. Two lines of the example went beyond the run and beyond the output format: the example's Held line added a sentence about whether and how the customer is reached, and its tracker line for C-201 added a note about the unconfirmed R-5190 receipt inside the bracket the format keeps for confirmed units. The run's Held line and C-201 bracket were shorter, as the format has them. No facts outside the inputs appeared beyond dates worked out from them.

Changes made after the third run, following an independent review:

- A customer whose status is Reached (spoken to, no listed remedy chosen, no follow-up item) appeared in neither the follow-up list nor the next contacts. The procedure, the pasted instructions and the output format now name every such customer under the next contacts, for the care lead to decide the next step, and the example's section 11 carries that line ("None", since its one reached customer without a remedy has a follow-up item).
- The count of customers reached is out of those attempted; the procedure and the pasted instructions now say that a customer who got in touch before any attempt counts as attempted for the counts only, so the reached count never exceeds its base.
- The stop-request line of the phone script, in the procedure, the pasted instructions and the example, now says the wish is noted and passed to the care lead, the call ends, and nothing more is promised either way.
- The lines on safety questions, on remedies the record does not list and on keeping the counts apart were reworded in the procedure and the pasted instructions, with the same meaning; the example's safety line was reworded to match.
- The example's Held line and its C-201 tracker bracket were trimmed to what the output format provides for.

## The fourth run, in full

The same set-up as the second and third runs, on the template as it now stands: Claude Opus 5.5 in a fresh Claude Code session with every tool switched off, given only the pasted instruction block and the output format as its instructions, and the example's five inputs as the message. It did not see the procedure or the example's output. The model is the one that made the changes after the third run, in a separate session. Its output, exactly as returned:

```
PRODUCT RECALL CUSTOMER CONTACT PLAN: FS-2 two-step folding stool, notice FS2-0926
Status: Draft for Customer care lead. Nothing has been sent and nobody has been contacted by the assistant. Questions to settle first: 3
Notice approved by Managing director on 28 September 2026. Order export as of 7 October 2026. Contact log as of 7 October 2026. Returns log as of 7 October 2026. Today: Wednesday 7 October 2026.

1. QUESTIONS TO SETTLE
1. For approver: Order R-5188 (C-233, Dana M., FS2-OAK, ordered 2026-07-15, quantity 1) has no batch number. The order date is inside the sale-date range of 1 June to 15 August 2026, but there is no batch to place inside or outside B24–B25. Is this customer in scope?
2. For approver: Order R-5290 (C-262, Lee A., FS2-OAK, batch B25, ordered 2026-08-20, quantity 1) is from an affected batch. But it was sold after the stated end of the sale-date range, 15 August 2026. Is this customer in scope?
3. For returns lead: The returns log has "item received" for R-5190 (C-201, Rosa T., B25, quantity 1) on 2026-10-06, but confirmed_by is blank. This unit is not counted as confirmed back. Can the receipt be confirmed, and by whom?

2. AFFECTED CUSTOMERS
Rows read: 9. Affected: 6. Possibly affected: 2. Not affected: 1.
C-201, Rosa T.: R-5101 FS2-OAK, B24 x 1; R-5190 FS2-WHT, B25 x 1. Units: 2. Contact: email and phone. Ready
C-214, Imran K.: R-5133 FS2-WHT, B24 x 2. Units: 2. Contact: email and phone. Ready
C-229, Jo P.: R-5160 FS2-OAK, B25 x 1. Units: 1. Contact: email. Ready
C-240, Theo B.: R-5215 FS2-WHT, B25 x 1. Units: 1. Contact: phone. Ready
C-251, Mina S.: R-5242 FS2-OAK, B25 x 1. Units: 1. Contact: email and phone. Held: marked do_not_contact in the order export
Possibly affected, for the approver to rule on:
C-233, R-5188, FS2-OAK, identifier blank: ordered 2026-07-15, inside the sale-date range, but no batch is recorded (question 1)
C-262, R-5290, FS2-OAK, B25: the batch is inside the range, but the order date 2026-08-20 is after the sale-date range ends on 15 August 2026 (question 2)
Not affected: R-5266
Held for the care lead's decision: C-251: marked do_not_contact in the order export

3. APPROVED NOTICE, WORD FOR WORD (approved by Managing director, 28 September 2026)
"Business R is recalling the FS-2 two-step folding stool from batches B24 and B25, sold between 1 June and 15 August 2026. The hinge under the top step can crack, and the stool may fold while someone is standing on it. Stop using the stool straight away and keep it folded. You can find the batch number printed under the top step. We will collect the stool at no cost to you and either refund what you paid or fit a new hinge and bring it back."

4. REMEDIES THE BUSINESS RUNS
1. Collection and refund: Our courier collects the stool from your home at no cost. We refund the price you paid to your original payment method within 5 working days of the stool reaching our warehouse.
2. Collection and hinge repair: Our courier collects the stool at no cost. Our workshop fits a new hinge and we deliver the stool back to you within 10 working days of collection.
No other remedy is offered.

5. EMAIL OR LETTER DRAFT (for the care lead's approval; not sent)
Subject: Recall notice FS2-0926: your FS-2 two-step folding stool

Dear [customer name],

Our records show that you bought the following from us: order [order number], [product: FS-2 two-step folding stool, finish], batch [batch number], quantity [quantity] [; repeat for each further order].

Business R is recalling the FS-2 two-step folding stool from batches B24 and B25, sold between 1 June and 15 August 2026. The hinge under the top step can crack, and the stool may fold while someone is standing on it. Stop using the stool straight away and keep it folded. You can find the batch number printed under the top step. We will collect the stool at no cost to you and either refund what you paid or fit a new hinge and bring it back.

You can choose either of these two remedies:

1. Collection and refund. Our courier collects the stool from your home at no cost. We refund the price you paid to your original payment method within 5 working days of the stool reaching our warehouse.

2. Collection and hinge repair. Our courier collects the stool at no cost. Our workshop fits a new hinge and we deliver the stool back to you within 10 working days of collection.

To tell us which remedy you would like, reply to this email, or call 555-0100, Monday to Friday, 9:00 to 17:00.

Questions customers often ask:

Do I have to be at home for the collection?
Yes, or someone you trust. The courier agrees a two-hour slot with you first.

Is my stool affected if it comes from a different batch?
Only stools from batches B24 and B25 sold between 1 June and 15 August 2026 are part of this recall.

How soon is the refund paid?
Within 5 working days of the stool reaching our warehouse.

Our care team will be in touch to settle the details with you. This matter stays open until your stool is back with us or has been repaired.

Yours sincerely,
[Name]
Customer care team, Business R

6. PHONE SCRIPT (read by a person on the care team)
1. Who is calling: "Hello, this is [your name] calling from Business R."
2. Confirm the customer: "May I speak to [customer name], please?" Ask for no other detail to prove who they are. Say nothing about the product, the stool, the batch or the recall until the person confirms they are [customer name].
   - If someone else answers, or you reach voicemail, leave only the message in section 7, word for word, and nothing more. Record "message left".
   - If you cannot leave a message, record "no answer".
3. Orders: "Thank you. I'm calling about [order number(s)], the [product] from batch [batch number] that you bought from us. I'd like to read you a recall notice about it."
4. The notice: read section 3 word for word, without adding to it or shortening it.
5. Item status, for each unit: "Can I ask where the stool is now? Do you still have it, have you sent it back to us, have you passed it on to someone else, or has it been thrown away?"
   - Note the answer for each unit in the customer's words.
   - If the stool was passed on or thrown away, give no advice. Note it, and it goes to the Customer care lead.
6. Remedies: "We offer two remedies." Read both from section 4, in that order, with equal weight. Do not recommend either one.
   - Then ask: "Which would you prefer?"
   - Then ask: "What days or times would suit you for the courier to agree a collection slot?"
   - Note the pick and the times. Do not book anything on the call.
7. Questions:
   - If the question matches section 8, give that answer word for word.
   - For any other question, say: "I don't have an answer to that, so I'll pass your question to our Operations manager." Write the question down in the customer's own words.
8. Safety, handling or disposal questions: reread the notice from section 3 and stop there. Give no reassurance and no opinion of your own.
9. Injury, damage, a claim, a lawyer, a regulator, or the customer is distressed:
   - Say: "Thank you for telling me. Our Operations manager will be in touch with you about this."
   - Note what was said in their words.
   - Do not debate it and do not accept blame. Close the call courteously.
10. Stop requests: if the customer asks not to be contacted again, say: "I've noted that, and I'll pass it to our Customer care lead."
    - End the call.
    - Promise nothing more either way.
11. No payment details: "We don't need any card or bank details from you, and I can't take them on this call." If the customer starts to give them, stop them politely and write nothing down.
12. Close: "Thank you for your time. Our care team will be in touch to settle the details. Your case stays open until the stool is back with us or has been repaired. If you need us, reply to our email or call 555-0100, Monday to Friday, 9:00 to 17:00." Record the outcome in the contact log yourself. The assistant does not update any log.

7. MESSAGE IF THE CUSTOMER IS NOT THE ONE WHO ANSWERS, OR FOR VOICEMAIL
"Hello, this is Business R with a message for [customer name]. Please call us on 555-0100, Monday to Friday, 9 to 5. Thank you."

8. APPROVED ANSWERS
Q: Do I have to be at home for the collection? A: Yes, or someone you trust. The courier agrees a two-hour slot with you first.
Q: Is my stool affected if it comes from a different batch? A: Only stools from batches B24 and B25 sold between 1 June and 15 August 2026 are part of this recall.
Q: How soon is the refund paid? A: Within 5 working days of the stool reaching our warehouse.
Anything else goes to Operations manager.

9. CONTACT TRACKER
C-201, Rosa T.: Remedy chosen: Collection and refund. Attempts 1. Last attempt: 2026-09-30, email, Care team member A. Units confirmed back or repaired: 1 of 2 (R-5101, item received, 2026-10-06, Warehouse lead). Follow-up: section 10.
C-214, Imran K.: Done. Attempts 2. Last attempt: 2026-10-05, phone, Care team member B. Units confirmed back or repaired: 2 of 2 (R-5133, repair completed, 2026-10-07, Workshop lead).
C-229, Jo P.: Attempted. Attempts 2. Last attempt: 2026-10-05, email, Care team member A. Units confirmed back or repaired: 0 of 1.
C-240, Theo B.: Needs a person. Attempts 2. Last attempt: 2026-10-06, phone, Care team member B. Units confirmed back or repaired: 0 of 1. Follow-up: section 10.
C-251, Mina S.: Held. Attempts 0. Last attempt: none. Units confirmed back or repaired: 0 of 1.
Counts:
Customers on the list: 5
Attempted: 4 of 5 on the list
Reached: 3 of 4 attempted
Remedy chosen: 2 of 3 reached
Done: 1 of 5 on the list
Units confirmed back or repaired: 3 of 7 affected units

10. FOLLOW-UP FOR A PERSON
C-201: Damage or claim, logged 2026-10-01 (customer's reply by email): "Asks: will you pay for the scratch the stool left on my kitchen floor?" → Operations manager
C-240: Item passed on, logged 2026-10-06 (phone): "Says he gave the stool to his brother in August. Did not choose a remedy." → Customer care lead

11. NEXT CONTACTS DUE
C-229: email, on or after Thursday 8 October 2026, attempt 3 of 3
Reached, no listed remedy chosen, for the care lead to decide the next step: None
Calling hours: Monday to Friday, 9:00 to 17:00, in each customer's own time zone. The export holds no time zone: the care team applies each customer's own, and any holiday the settings do not list.

Draft for Customer care lead. Nothing has been sent, no customer has been contacted, and no record has been changed by the assistant. A customer is done only when every affected unit is confirmed back or repaired. The decision to recall, the notice and every regulatory or legal duty stay with the business and its advisers.
```

## What was observed

The output follows the output format from the first line to the closing lines, with nothing before it, and the arithmetic holds: the three row groups add to nine, and every count sits on its own base. Nothing made the run stop: all three files' headers matched the defaults, the notice, approver and remedies were present, and no input held card details or a password.

Against the published example:

- **Same:** the sorting of all nine rows, with R-5266 not affected; the three questions (in a different order); the customer lines, the held customer and the Held line; every tracker status, attempt count, last attempt and unit count, including C-201's last attempt on 30 September, its bracket naming only the confirmed unit, and the follow-up pointer on C-201 and C-240; all six counts; both follow-up items and their roles (C-201's damage question to the operations manager, C-240's passed-on stool to the customer care lead); the single next contact, on Thursday 8 October 2026; the new Reached line, "None"; and the calling-hours line. The notice, the remedies and the short message are the same text, and the approved answers are the same apart from "Operations manager" without "the" in the last line.
- **Wording of the drafts.** The subject line, the opening line, the sign-off and the phrasing of the close differ from the example's, as the format allows. The email's bracketed fields add "[quantity]" and the finish beside the order, product and batch the template names, and the email sets out the remedies with a full stop after each name where section 4 uses a colon.
- **Phone script.** It mentions the order number, product and batch once the customer has confirmed who they are, where the example mentions only the product. It asks which days or times would suit a collection and says not to book anything on the call; the template asks the care team to note when suits the customer, and the example does not put it as a question. Its stop-request line now follows the template's wording: noted, passed to the customer care lead, call ended, nothing more promised. Its payment line tells the customer that no card or bank details are needed. Its close again tells the care team member to record the outcome in the contact log themselves, which is a person's action, and adds that the assistant does not update any log.
- **Facts not in the inputs.** None beyond dates worked out from the inputs. The tracker gives dates as 2026-10-06 where the example writes them out.

Edits made after this run: none to the pasted instructions, the output format, the procedure or the example. Only the version notes in the template, the "What has been checked" paragraph of the public page and this record were written afterward.

The thirteen acceptance tests in the template are proposed and have not been run; this trial covers the invented example only.
