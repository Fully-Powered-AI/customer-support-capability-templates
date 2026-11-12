# Product recall customer contact plan

Workflow template, version 0.1.0.

## Purpose

Prepare the customer side of a recall or corrective notice the business has already decided to issue: the list of affected customers drawn from the order export, the approved notice carried word for word into an email or letter draft and a phone script for the care team, the remedies the business operates and no others, and a tracker that marks a customer done only when every affected unit is confirmed back with the business or repaired. The assistant prepares; people decide and make every contact. It never sends a message, calls anyone, changes the approved wording, advises on the hazard, books a collection, issues a refund or marks anything done.

## When to use it and when not to

Use it once the business has issued a recall or corrective notice, the wording has been approved by a named person, and the remedies on offer are written down. Run it first to build the list and the drafts, then again whenever the care team has new entries in its contact log or the warehouse has new entries in its returns log, to bring the tracker up to date.

Do not use it:

- to decide whether to recall, which units are affected, or what the notice should say. Those decisions, and every regulatory or legal duty that comes with a recall, belong to the business and its advisers;
- to write a notice to a regulator, a press statement, a public announcement or a notice for retailers;
- to judge how dangerous a product is, whether it can stay in use, or how a customer should handle or dispose of it. The approved notice says all the business has cleared on that;
- for a single customer's complaint or refund request that is not about the recall; Complaint and refund request handling covers that;
- for any message whose real purpose is selling something or chasing a debt.

## Roles

- **Care lead** (runs it, checks the list, approves the drafts, decides who is contacted and when, and takes every item passed on to someone else or thrown away, every request not to be contacted and every remedy asked for that the record does not list): the customer care lead or service lead.
- **Approver of the notice** (approved the notice text; answers any question about what the notice covers or says): the role named in the recall record.
- **Care team** (makes each contact, by email, letter or phone, and keeps the contact log): the people the care lead names.
- **Confirms returns and repairs** (records each unit received or repaired, with their name or role): the warehouse, workshop or returns lead.
- **Escalation role** (takes injuries, damage claims, disputes, mentions of a lawyer or regulator, and anything the approved answers do not cover): the role named in the recall record.

## Inputs

1. **The recall record.** The notice reference; the product and its identifiers (model, SKU, lot, batch or serial range, and any sale-date range); the approved notice wording exactly as signed off, with the approver's role and the date; the remedies the business runs, each with how it works; how customers respond (reply address, phone number and hours); the approved short message for an unanswered call, if one exists; the approved answers to expected questions, if any; and the escalation role. If the notice wording, its approver or the list of remedies is missing, stop and ask the care lead. Draft nothing.
2. **The order export** for every order that contains the product, one row per order line. Default column headers: `order_id`, `order_date`, `customer_ref`, `customer_name`, `email`, `phone`, `sku`, `lot_or_serial`, `quantity`, `do_not_contact`. If a header does not match these and the settings give no mapping for it, stop and ask the care lead which column holds each field before reading any row; never guess a mapping. If the export is missing, stop.
3. **The contact log,** on every run after the first. Default column headers: `customer_ref`, `date`, `channel`, `contact_by`, `outcome`, `remedy_chosen`, `note`. `outcome` is one of: sent, bounced, no answer, message left, reached, replied, asked not to be contacted. The same header rule applies. If missing, every customer is "not contacted" and the tracker says "contact log not supplied".
4. **The returns log,** on every run after the first. Default column headers: `order_id`, `customer_ref`, `lot_or_serial`, `quantity`, `event`, `date`, `confirmed_by`. `event` is one of: collection booked, item received, repair completed. The same header rule applies. If missing, no unit is confirmed and the tracker says "returns log not supplied".
5. **Settings:** today's date; the care lead's role; the channels in order (for example email first, then phone); [your attempt limit] per customer and [your gap between attempts] in working days, with any public holidays to skip; calling hours; any column mapping for headers that differ from the defaults; and who approves the drafts before anything is sent. If the attempt limit or the gap is missing, list no next contacts and say so.

The assistant works from files and text the care lead supplies. It needs no connection to an order system, a mailbox or a phone system, and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm the recall record holds the wording, the approver and at least one remedy, and that every header of the export, the contact log and the returns log matches the defaults or a mapping given in the settings. Note the date of each log.
2. **Sort every row of the order export** against the affected identifiers in the recall record, one row at a time:
   - **Affected:** the SKU or model matches and the lot, batch or serial falls inside the stated range, and any sale-date range stated is met.
   - **Possibly affected:** the SKU or model matches but the lot or serial is blank or unreadable, or the lot or serial is inside the range but another stated condition fails (for example an affected batch sold after the stated end date). Never decide these; list each with what is missing or in conflict.
   - **Not affected:** the SKU or model does not match, or the lot, batch or serial is readable and falls outside the stated range, whatever the sale date.
   Count each group; the three counts add up to the rows read.
3. **Build one line per affected customer,** joined on `customer_ref`: every affected order, each product and identifier with its quantity, the total affected units, and the contact routes on file (email, phone, both or none).
4. **Hold, without dropping,** any affected customer who is marked `do_not_contact`, who has no email and no phone, or who shares an email or phone with a different `customer_ref`. Each is listed for the care lead with the reason. Whether and how a held customer is reached is the care lead's decision, with the business's advisers where the reason is a contact preference.
5. **Copy the approved notice exactly,** character for character, into section 3 and into the email or letter draft. Change nothing: not a word, not spelling, not punctuation, not length. Only line breaks that come from how the record was typed or wrapped may be joined into paragraphs. If something in it looks wrong (a typo, a date that conflicts with the identifiers, a remedy the recall record does not list), keep the text as approved and write a question for the approver.
6. **List the remedies** exactly as the recall record sets them out, with how each works. Nothing else is offered: no draft mentions any remedy, payment or gesture the record does not list.
7. **Draft the email or letter once,** with the personal fields in square brackets for the care team to fill: the customer's name, their order numbers, and the product and identifier they bought. No other personal detail goes in. Then the approved notice word for word; then the remedies as listed, with how to choose one (the reply route from the recall record); then, only if approved answers exist, a short list of them. Close by saying the care team will be in touch to settle the details, and that the matter stays open until the item is back with the business or repaired. Add nothing about the hazard beyond the notice.
8. **Write the phone script** for a person on the care team to read:
   - Say who is calling and from which business. Ask for the customer by name, and ask for no other detail to prove who they are. Mention no product, order or problem until that person confirms who they are.
   - If someone else answers, or the call goes to voicemail, leave only the approved short message. If there is none, leave no message and record "no answer". Never describe the product or the problem to anyone but the customer.
   - Read the approved notice word for word. Find out what has become of the item (still with them, already sent back, handed on, or binned) and note the answer as given.
   - Go through each listed remedy in turn without favouring one; note the customer's pick and when suits them.
   - Use the approved answers and nothing else. Any other question is written down in the customer's own words and passed to the escalation role, and the customer is told who will get back to them.
   - On any question about safety, handling or disposal, read the relevant sentence of the notice again and stop there, with no reassurance and no opinion of your own.
   - If they mention an injury, damage to property, a claim, a lawyer or a regulator, or are upset: say you are sorry to hear it and that the escalation role will be in touch, write it down, and bring the call to a courteous close without debating the point or accepting blame.
   - Someone who wants no further contact hears that their wish is noted and passed to the care lead, and the call ends there. The script promises nothing more either way: the care lead decides what happens next.
   - Payment goes only by the remedy as written, so the care team never takes card or bank details, a password or an ID number, even when a customer starts to read them out.
   - Close with what happens next and who will confirm it. The matter stays open until the item is back or repaired, and the script never tells the customer otherwise.
9. **Check the short message.** If the approved short message names the product, a model, a lot, a batch or the problem, keep it as approved and write a question for the approver, because a voicemail may be played to the whole household.
10. **Build the tracker** for every affected customer, held ones included, from the contact log and the returns log. If the contact log is missing, every customer is Not contacted (or Held) and the tracker says "Contact log not supplied."; if the returns log is missing, no unit is confirmed and it says "Returns log not supplied." Give each customer the first status in this order that fits:
    1. **Done:** every affected unit of that customer has a returns log entry of "item received" or "repair completed" with `confirmed_by` filled in. Nothing else makes a customer done: not a reply, not a chosen remedy, not "collection booked".
    2. **Held:** held at step 4, or any contact log entry is "asked not to be contacted".
    3. **Needs a person:** the customer has an item on the follow-up list (step 11) and has not chosen a listed remedy.
    4. **Remedy chosen:** the latest `remedy_chosen` entry names a remedy the recall record lists; show how many of their affected units are confirmed back or repaired.
    5. **Reached:** a "reached" or "replied" entry, with no listed remedy chosen.
    6. **Attempts used up:** [your attempt limit] attempts made and none "reached" or "replied"; the care lead decides what happens next.
    7. **Attempted:** at least one attempt, none "reached" or "replied", fewer than [your attempt limit].
    8. **Not contacted:** no entry in the contact log.
    Attempts are the care team's outgoing entries (sent, bounced, no answer, message left, reached); a reply from the customer is not an attempt, and a sent email, a bounce, a call with no answer and a message left never count as reaching the customer. "Last attempt" on a tracker line is the latest outgoing entry, never the customer's reply. A returns log entry counts as many units of its order line as its `quantity` says. An "item received" or "repair completed" entry with `confirmed_by` blank does not count; list it as a question for the returns lead. A customer with an item on the follow-up list keeps their status and their tracker line ends "Follow-up: section 10.", so a damage report from a customer who has chosen a remedy is not hidden. Then give the counts, each against its own base, whatever each customer's status: customers on the list; attempted (customers with at least one attempt), out of customers on the list; reached (customers with a "reached" or "replied" entry), out of those attempted; remedy chosen (customers who chose a listed remedy, Done included), out of those reached; done, out of customers on the list; and affected units confirmed back or repaired, out of all affected units. A customer who got in touch before the team made any attempt counts as attempted for these counts only, so the reached count never exceeds its base. Each count goes on its own line; none is combined with another into a single figure.
11. **Build the follow-up list** from the contact log, each item with its role: every mention of injury, damage, a claim, a lawyer or a regulator, listed first, and every question the approved answers do not cover, quoted as logged, to the escalation role; every customer who says the item was passed on to someone else or thrown away, every request not to be contacted, and every chosen remedy that is not one the record lists, to the care lead. A plain no-answer (no answer, message left, bounced) is not a follow-up item; it is an attempt. A `do_not_contact` flag in the order export is not a follow-up item either: that customer is shown as Held in sections 2 and 9.
12. **List the next contacts due** for customers who are Not contacted or Attempted (never Held, Attempts used up or any other status): the next channel in the settings order that the customer has a route for (a customer with only one route gets that route again), the earliest date (the last attempt plus [your gap between attempts] working days, skipping weekends and any holidays listed in the settings; for a customer not yet contacted, today), and the attempt number out of [your attempt limit]. Under the list, name every customer whose status is Reached (spoken to, no listed remedy chosen, no follow-up item), so the care lead can decide how to follow up; they are not given a next contact automatically. Print the calling hours from the settings under the list; the export carries no time zone, so the care team applies each customer's own time zone and any holiday the settings do not list.
13. **Write the questions** in section 1, numbered, for the care lead, the approver and the returns lead: anything missing from the recall record, every possibly affected row that needs a ruling on scope, every wording question from steps 5 and 9, and every unconfirmed returns entry. Set the status line to "Questions to settle first: [n]" with that number, or "No open questions" when there are none. Check the plan against the reviewer checklist and return it to the care lead.

## Exceptions and stop conditions

- **No approved notice wording, no named approver, or no remedies in the recall record:** stop and ask. Draft nothing.
- **A header in the export, the contact log or the returns log does not match, and the settings give no mapping:** stop and ask which column holds each field.
- **Asked to rewrite, shorten, translate or soften the approved notice:** decline; write the request as a question for the approver.
- **Asked whether the product is safe, how dangerous it is, or how to handle, store, repair or dispose of it:** decline; the notice is the only guidance, and anything more goes to the escalation role.
- **Asked to offer a remedy the recall record does not list,** such as a voucher, a refund where only repairs are offered, or a goodwill payment: decline; write it as a question for the care lead.
- **Asked to decide whether a possibly affected customer is in scope:** decline; list the row and the conflict for the approver.
- **Asked to write a notice to a regulator, a press statement or any public announcement, or to judge the business's legal or regulatory duties:** decline; those stay with the business and its advisers.
- **Asked to send the emails, place calls, book collections, issue refunds, update a log or mark a customer done:** decline; those are people's actions, each after the care lead's approval.
- **A contact log entry reports an injury, damage to property, a claim, or a mention of a lawyer or regulator:** list it first in the follow-up list for the escalation role; the tracker marks the customer "Needs a person" until a listed remedy is chosen, and after that the tracker line still points to the follow-up list. Nothing in the plan comments on cause or fault.
- **An input contains a card number, bank details, a password or a login code:** do not repeat it anywhere; tell the care lead to remove it from the source.

## Output format

```
PRODUCT RECALL CUSTOMER CONTACT PLAN: [product], notice [reference]
Status: Draft for [care lead]. Nothing has been sent and nobody has been contacted by the assistant. [Questions to settle first: [n] | No open questions]
Notice approved by [role] on [date]. Order export as of [date]. Contact log as of [date | not supplied]. Returns log as of [date | not supplied]. Today: [date].

1. QUESTIONS TO SETTLE
[n]. For [care lead | approver | returns lead]: [question, with the facts]
[| None]

2. AFFECTED CUSTOMERS
Rows read: [n]. Affected: [n]. Possibly affected: [n]. Not affected: [n].
[customer ref], [name]: [order id] [product, identifier] x [qty][; next order...]. Units: [n]. Contact: [email | phone | email and phone | none]. [Ready | Held: [reason]]
Possibly affected, for the approver to rule on: [customer ref], [order id], [product, identifier | identifier blank]: [what is missing or in conflict] | None
Not affected: [order ids] | None
Held for the care lead's decision: [customer ref]: [reason] | None

3. APPROVED NOTICE, WORD FOR WORD (approved by [role], [date])
"[notice exactly as approved]"

4. REMEDIES THE BUSINESS RUNS
[n]. [Remedy]: [how it works, as the recall record sets it out]
No other remedy is offered.

5. EMAIL OR LETTER DRAFT (for the care lead's approval; not sent)
Subject: [subject]
[Greeting with the customer's name],
[Order numbers and the product and identifier they bought]
[Approved notice, word for word]
[Remedies as listed, and how to choose]
[Approved answers, if any]
[Care team will be in touch to settle the details; the matter stays open until the item is back or repaired]
[Sign-off]

6. PHONE SCRIPT (read by a person on the care team)
[Numbered lines: who is calling; confirm the customer; the notice; item status; remedies; questions; safety questions; injury, damage, claims or distress; stop requests; no payment details; close]

7. MESSAGE IF THE CUSTOMER IS NOT THE ONE WHO ANSWERS, OR FOR VOICEMAIL
"[approved short message]" | None approved: leave no message and record "no answer".

8. APPROVED ANSWERS
Q: [question] A: [answer as approved]
[| None approved: every question goes to [escalation role].]
Anything else goes to [escalation role].

9. CONTACT TRACKER
[customer ref], [name]: [Done | Held | Needs a person | Remedy chosen: [remedy] | Reached | Attempts used up | Attempted | Not contacted]. Attempts [n]. Last attempt: [date, channel, by whom | none]. Units confirmed back or repaired: [n] of [n] [(order id, event, date, confirmed by)].[ Follow-up: section 10.]
Counts:
Customers on the list: [n]
Attempted: [n] of [n] on the list
Reached: [n] of [n] attempted
Remedy chosen: [n] of [n] reached
Done: [n] of [n] on the list
Units confirmed back or repaired: [n] of [n] affected units
[Contact log not supplied. | Returns log not supplied.]

10. FOLLOW-UP FOR A PERSON
[customer ref]: [what was said or asked, as logged, with the date] → [role]
[| None]

11. NEXT CONTACTS DUE
[customer ref]: [channel], on or after [date], attempt [n] of [limit]
[| None | Attempt limit or gap not set: no next contacts listed.]
Reached, no listed remedy chosen, for the care lead to decide the next step: [customer refs] | None
Calling hours: [calling hours from the settings | not set]. The export holds no time zone: the care team applies each customer's own, and any holiday the settings do not list.

Draft for [care lead]. Nothing has been sent, no customer has been contacted, and no record has been changed by the assistant. A customer is done only when every affected unit is confirmed back or repaired. The decision to recall, the notice and every regulatory or legal duty stay with the business and its advisers.
```

## Reviewer checklist

1. The notice in section 3 and in the email draft matches the approved wording character for character. (Care lead)
2. Every row of the export is counted once, and affected plus possibly affected plus not affected equals the rows read. (Care lead)
3. No possibly affected row has been placed in or out of scope by the assistant; each has gone to the approver. (Approver)
4. No held customer has been dropped, and each has a reason. (Care lead)
5. No draft offers a remedy, an answer or a word about the hazard that the recall record does not contain. (Care lead; approver)
6. The phone script mentions nothing about the product until the customer confirms who they are, and the short message names no product or problem. (Care lead)
7. Every customer marked Done has a confirmed receipt or repair for every affected unit, with the person who confirmed it. (Returns lead)
8. Every injury, damage claim, mention of a lawyer or regulator, and question outside the approved answers is in the follow-up list with its role. (Escalation role)
9. The drafts are approved by the care lead before anything is sent, and every contact is made by a person. (Care lead)

## Acceptance tests

Proposed tests. None has been run.

1. **First run.** A recall record, an order export of twenty rows, no logs. Expected: every row sorted and counted; every customer Not contacted; the tracker notes both logs not supplied; next contacts list the first channel for each ready customer.
2. **Header does not match.** The export has `Batch` instead of `lot_or_serial`. Expected: stops and asks which column holds the lot or serial; reads no row.
3. **No approver.** The recall record has wording but no approver. Expected: stops; drafts nothing.
4. **Blank lot.** A row with the right SKU and a blank lot. Expected: possibly affected, with "identifier blank"; a question for the approver; not on the contact list.
5. **Conflicting conditions.** An affected batch sold after the stated sale-date range. Expected: possibly affected, with the conflict stated; no ruling. A batch outside the range sold inside the dates is not affected.
6. **Do not contact.** An affected customer marked `do_not_contact`. Expected: held with the reason; still on the tracker as Held; not in next contacts.
7. **Chosen remedy is not done.** A customer replied and chose a collection, and the returns log shows "collection booked". Expected: Remedy chosen, 0 of 1 units; not Done.
8. **Partly back.** A customer with two units; one "item received" with `confirmed_by`, one with `confirmed_by` blank. Expected: Remedy chosen, 1 of 2 units; a question for the returns lead about the unconfirmed entry.
9. **Voicemail is not a follow-up.** A call logged "message left". Expected: an attempt; not in the follow-up list.
10. **Question outside the approved answers.** A customer asks whether the business will pay for floor damage. Expected: quoted in the follow-up list for the escalation role; no answer drafted.
11. **Asked to advise.** "Tell customers it is fine to keep using it until collection." Expected: declines; the notice stands as approved.
12. **Asked to add a voucher.** "Offer everyone a voucher as well." Expected: declines; a question for the care lead; no draft mentions a voucher.
13. **Asked to send.** "Email them all now." Expected: declines; returns the plan for the care lead's approval.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare the customer contact plan for a recall or corrective
notice that the business has already decided to issue. You prepare; people
decide and make every contact. You never send an email or letter, call
anyone, book a collection, issue a refund, update a log, change any record
or mark a customer done. You never ask for a password or a login code.

The user will supply: the recall record (notice reference, product and
affected identifiers, the approved notice wording with its approver and
date, the remedies the business runs, how customers respond, the approved
short message, approved answers, escalation role); the order export with
headers order_id, order_date, customer_ref, customer_name, email, phone,
sku, lot_or_serial, quantity, do_not_contact; on later runs the contact
log (customer_ref, date, channel, contact_by, outcome, remedy_chosen,
note) and the returns log (order_id, customer_ref, lot_or_serial,
quantity, event, date, confirmed_by); and settings (today's date, the
care lead, channel order, attempt limit, gap between attempts in working
days, any holidays, calling hours, any column mapping). If the notice
wording, its approver or the remedies are missing, stop and ask; draft
nothing. If any header of the export, the contact log or the returns log
does not match and the settings give no mapping for it, stop and ask
which column holds each field before reading any row; never guess.

1. Sort every export row: affected (lot, batch or serial inside the
   stated range and any sale-date range met); possibly affected (the
   product matches but the identifier is blank or unreadable, or the
   identifier is inside the range and another stated condition fails);
   not affected (the product does not match, or the identifier is
   readable and outside the range, whatever the sale date). Never rule
   on a possibly affected row; list it with the conflict for the
   approver. The three counts must add up to rows read.
2. One line per affected customer by customer_ref: orders, identifiers,
   quantities, total units, contact routes. Hold, never drop, anyone
   marked do_not_contact, with no email and no phone, or sharing contact
   details with another customer_ref, with the reason.
3. Copy the approved notice exactly, character for character, into
   section 3 and the email draft: not a word, spelling or punctuation
   mark changed. Only line breaks from how the record was typed may be
   joined into paragraphs. If it looks wrong, keep it and ask the
   approver.
4. Offer only the remedies the recall record lists, as it describes them.
   No draft offers any remedy, payment or gesture the record does not
   list.
5. Email or letter draft, written once with the personal fields in
   square brackets: customer's name, their orders, product and
   identifier; the notice word for word; the remedies and how to choose;
   approved answers if any; the care team will be in touch to settle the
   details, and the matter stays open until the item is back or repaired.
6. Phone script for a person: say who is calling; ask for the customer
   by name and ask for no other detail to prove who they are; mention
   nothing about the product until the customer confirms who they are; to anyone else
   or a voicemail leave only the approved short message, or none; read
   the notice word for word; note what became of the item (with them,
   sent back, handed on, binned); go through each remedy without
   favouring one and note the pick and when suits them; use the
   approved answers only and pass every other question, in the
   customer's words, to the escalation role; on safety, handling or
   disposal, reread the notice and stop there, with no reassurance and
   no opinion; on injury, damage, a claim, a lawyer, a regulator or
   distress, say the escalation role will be in touch, note it, and
   close courteously without debating or accepting blame; on a wish for
   no further contact, say it is noted and passed to the care lead, end
   the call, and promise nothing more either way, since the care lead
   decides what happens next; take no card or bank details; close with
   what happens next, keeping the matter open until the item is back or
   repaired.
7. If the approved short message names the product, a model, a lot or
   the problem, keep it and ask the approver.
8. Tracker for every affected customer, held ones included. Attempts
   are the care team's outgoing entries (sent, bounced, no answer,
   message left, reached); a customer's reply is not one, and only
   "reached" or "replied" counts as reaching the customer. "Last
   attempt" is the latest outgoing entry, never a reply. Give each
   customer the first status that fits, in this order:
   Done: every affected unit has "item received" or "repair completed"
     with confirmed_by filled in. A reply, a chosen remedy or a booked
     collection is never done.
   Held: held in step 2, or any log entry "asked not to be contacted".
   Needs a person: an item on the follow-up list (step 9) and no listed
     remedy chosen.
   Remedy chosen: the latest remedy_chosen names a listed remedy.
   Reached: a "reached" or "replied" entry, no listed remedy chosen.
   Attempts used up: the attempt limit reached, never reached or
     replied; the care lead decides what next.
   Attempted: one or more attempts, under the limit, never reached.
   Not contacted: no contact log entry.
   A returns entry counts as many units of its order line as its
   quantity says. An entry with confirmed_by blank does not count; ask
   the returns lead. A customer with a follow-up item keeps their status
   and their line ends "Follow-up: section 10." If the contact log is
   missing, every customer is Not contacted or Held and the tracker says
   "Contact log not supplied."; if the returns log is missing, no unit
   is confirmed and it says "Returns log not supplied." Give each count
   against its own base, whatever the status: on the list; attempted
   (any attempt) of on the list; reached (any reached or replied) of
   attempted; remedy chosen (a listed remedy, Done included) of
   reached; done of on the list; units confirmed of units affected. A
   customer who got in touch before any attempt counts as attempted
   for these counts only, so reached never exceeds its base. Each count
   on its own line; never combine them.
9. Follow-up list from the contact log, each to its role: injury,
   damage, claims, lawyers or regulators, listed first, and questions
   outside the approved answers, quoted, to the escalation role; items
   passed on or thrown away, stop requests and any remedy chosen that is
   not listed, to the care lead. A plain no-answer is an attempt, not a
   follow-up. A do_not_contact flag from the export shows as Held in
   sections 2 and 9, not here.
10. Next contacts due: for Not contacted or Attempted customers only,
    the next channel they have a route for (with one route, that route
    again), the earliest date (last attempt plus the gap in working
    days, skipping weekends and listed holidays; today if not yet
    contacted), attempt n of the limit. If the limit or gap is not set,
    list none and say so. Under the list, name every customer whose
    status is Reached, for the care lead to decide the next step, or
    write None; they get no next contact automatically. Print the
    calling hours under the list; the care team applies each customer's
    time zone.
11. Questions to settle, numbered in section 1, each for the care lead,
    the approver or the returns lead: anything missing from the recall
    record, every possibly affected row, every wording question from
    steps 3 and 7, every received or repaired entry with confirmed_by
    blank. The status line says "Questions to settle first: n" with that
    number, or "No open questions".
12. Use the output format exactly, with nothing written before it.
    Print "None" in any empty section. End with the closing lines.

Decline to: rewrite or soften the notice; judge the hazard or say
whether the item is safe; add a remedy; rule on scope; write to a
regulator, the press or the public; judge any legal or regulatory duty;
send, call, book, refund, update a log or mark anyone done. If an input
holds a card number, bank details, a password or a login code, do not
repeat it; tell the user to remove it.
```

## What to customize

- The recall record: your notice reference, identifiers, approved wording, approver, remedies, reply routes, short message, approved answers and escalation role. The template adds nothing of its own to any of them.
- The headers of your order export, contact log and returns log, if they differ from the defaults; tell the assistant the mapping once, in the settings.
- Which channels the care team uses, in what order, [your attempt limit] and [your gap between attempts].
- Your calling hours, set in each customer's own time zone, and the public holidays the working-day gap should skip.
- When a repair counts as finished. As written, "repair completed" with a named person closes that unit, even if the repaired item has not yet reached the customer again. If your business wants a repaired item delivered back first, add an event such as "delivered back" to the returns log and tell the assistant that only "item received" or "delivered back" makes a unit count.
- Who takes each kind of follow-up. As written, injuries, damage, claims, lawyers, regulators and questions outside the approved answers go to the escalation role; items passed on or thrown away, stop requests and unlisted remedies go to the care lead.
- How your business handles customers marked do not contact for a safety notice. That is a decision for the business and its advisers; the template only holds those customers for it.
- Who confirms receipts and repairs, and how they record their name or role in the returns log.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini, and which customer details it may be shown.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried on its invented example on 10 November 2026 in four runs: the pasted instructions, the output format and the example were revised after the first, the sorting rule and two lines of the pasted instructions after the second, and, following an independent review, a few lines of the instructions, the output format and the example after the third (Reached customers named for the care lead, the base of the reached count, the stop-request line, and two example lines trimmed to the format); the fourth, on the current version, is the run recorded in full. No edits to the instructions, the output format or the example have been made since that run; the trial record says so. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
