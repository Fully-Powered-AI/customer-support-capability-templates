# Follow-ups promised on service calls: an invented example

*Illustrative example with invented data.* The company, its customers, its agents, the calls, the records, the dates and the amounts below are all invented. An invented online retailer of kitchen appliances runs a phone queue for orders and deliveries. On Thursday morning the queue's team leader picks two of Monday afternoon's calls for review, one taken by Maya and one by Theo. The team leader exports the call list, the transcripts and the follow-up records, and runs the workflow template.

The inputs come first, in full, so the template can be run on them. The list it returned follows.

## The inputs

### 1. Run settings

```
Team: Orders and deliveries phone queue
For: Team leader, Orders and deliveries
Run at: Thursday 12 November 2026, 09:30
Working days and hours: Monday to Friday, 09:00 to 17:00
Speaker labels: Agent, Customer
Owner map:
  Callback, Send, Task: the agent on the call
  Refund or credit: Billing team
  Replacement or delivery: Fulfillment team
  Visit: Field scheduling
  Escalation: Team leader
Record types (kind: type):
  Callback: Callback; Send: Send; Refund or credit: Refund;
  Replacement or delivery: Delivery; Visit: Visit;
  Escalation: Escalation; Task: Task
Done statuses: Done, Closed
Promise limits: agents may offer a goodwill credit of up to $20 without
  approval. Anything above $20 needs the team leader's approval.
```

### 2. Call list

```
Call ID,Date,Start,Agent,Customer,Case,Wrap-up note
C-4471,2026-11-09,14:05,Maya,Customer A,88213,"Dishwasher delivered with dented door. Customer emailing photos tonight. Replacement once photos received. Callback booked for Thursday. Call summary emailed."
C-4486,2026-11-09,16:40,Theo,Customer B,88240,"Refund for returned kettle not received. Raised with billing, TK-5531. Refund due within 48 hours."
```

### 3. Transcripts

```
Call ID,Line,Time,Speaker,Text
C-4471,1,00:00,Agent,"Thanks for calling, this is Maya. How can I help?"
C-4471,2,00:05,Customer,My new dishwasher arrived this morning with a big dent in the door.
C-4471,3,00:14,Agent,I'm sorry about that. Could you send us a couple of photos of the dent?
C-4471,4,00:22,Customer,"Yes, I can email them tonight."
C-4471,5,00:27,Agent,"Thank you. Once the photos are in, we'll arrange a replacement for you."
C-4471,6,00:36,Customer,How long does that usually take?
C-4471,7,00:40,Agent,Replacements normally go out within five working days.
C-4471,8,00:48,Customer,I had to take the morning off work for that delivery.
C-4471,9,00:55,Agent,I understand. I'll put a $25 credit on your account for the trouble.
C-4471,10,01:03,Customer,Thank you. Will someone let me know when the new one is coming?
C-4471,11,01:09,Agent,"Yes, I'll call you back by Thursday to confirm the delivery date."
C-4471,12,01:17,Customer,Could I have all of this in writing as well?
C-4471,13,01:21,Agent,Of course. I'll email you a summary of today's call by the end of the day.
C-4471,14,01:29,Customer,"Great, thanks."
C-4471,15,01:32,Agent,Thanks for calling. Goodbye.
C-4486,1,00:00,Agent,You're through to Theo. How can I help?
C-4486,2,00:04,Customer,I sent a kettle back three weeks ago and I still haven't had my refund.
C-4486,3,00:12,Agent,Let me look. The return reached our warehouse on 23 October.
C-4486,4,00:31,Agent,I'm going to raise this with our billing team now.
C-4486,5,01:02,Agent,"Right, that's raised with billing, reference TK-5531."
C-4486,6,01:08,Customer,So when do I get my money?
C-4486,7,01:12,Agent,The refund should be with you within 48 hours.
C-4486,8,01:18,Customer,And if it isn't?
C-4486,9,01:21,Agent,"If it's not there by then, I'll email you myself with an update."
C-4486,10,01:28,Customer,"OK, thanks."
C-4486,11,01:30,Agent,Thanks for calling. Goodbye.
```

### 4. Follow-up records, exported Thursday 12 November 2026, 09:15

```
Record,Call ID,Case,Type,Owner,Due,Created,Status,Description
CB-3099,C-4460,88190,Callback,Maya,2026-11-10,2026-11-09 11:02,Done,Call back about warranty registration
CB-3120,C-4471,88213,Callback,Maya,2026-11-13,2026-11-09 14:19,Open,Call to confirm replacement delivery date
SE-2208,C-4471,88213,Send,Maya,2026-11-09,2026-11-09 14:22,Done,Email summary of call
TK-5531,C-4486,88240,Task,Theo,2026-11-09,2026-11-09 16:41,Done,Raise refund delay with billing
RF-7702,,88240,Refund,Billing team,2026-11-13,2026-11-09 16:52,Open,Refund for returned kettle
```

## The output

The list as the workflow template returned it, in plain text.

```
FOLLOW-UPS PROMISED ON SERVICE CALLS: Orders and deliveries phone queue, run of Thursday 12 November 2026, 09:30

For: Team leader, Orders and deliveries. Calls read: 2 (C-4471, C-4486). Agents: Maya, Theo.
Promises found: 6 (5 firm, 1 hedged). Flagged: 5. Expectations set, not promises: 1. Completed during the call: 1.
Deadlines read using: Monday to Friday, 09:00 to 17:00 (your settings).
Follow-up records: 5 supplied, exported Thursday 12 November 2026, 09:15; used for these calls: 4; for other calls, not used: 1.
Promise limits: agents may offer a goodwill credit of up to $20 without approval.
Settings taken as default: none.

CALL C-4471 | Monday 9 November 2026, 14:05 | Agent: Maya | Customer: Customer A | Case: 88213

P1 | Line 5, 00:27 | Replacement or delivery | firm
- Words: "Once the photos are in, we'll arrange a replacement for you."
- Deadline as said: not stated
- Condition: "Once the photos are in" (line 5); depends on the customer; not met by the end of the call; customer's own timing: "Yes, I can email them tonight." (line 4)
- Owner as said: not stated on the call
- Proposed owner from your owner map: Fulfillment team.
- Follow-up record: none found
- Wrap-up note: mentions it
- Flags: OWNER MISSING, DEADLINE NOT STATED, CONDITIONAL, NO RECORD FOUND
- Question 1 below.

P2 | Line 9, 00:55 | Refund or credit | firm
- Words: "I'll put a $25 credit on your account for the trouble."
- Deadline as said: not stated
- Condition: none
- Owner as said: Maya ("I'll")
- Follow-up record: none found
- Limit: a $25 credit; your limit is $20 without approval.
- Wrap-up note: does not mention it
- Flags: DEADLINE NOT STATED, NEEDS APPROVAL UNDER YOUR LIMITS, NO RECORD FOUND
- Question 2 below.

P3 | Line 11, 01:09 | Callback | firm
- Words: "I'll call you back by Thursday to confirm the delivery date."
- Deadline as said: "by Thursday", read as Thursday 12 November 2026, 17:00 (rule 4: the first Thursday after the call date, at the end of working hours)
- Condition: none
- Owner as said: Maya ("I'll")
- Follow-up record: CB-3120, Callback, owner Maya, due 13 November 2026, status Open
- Wrap-up note: mentions it
- Flags: RECORD LATER THAN PROMISED
- Question 3 below.

P4 | Line 13, 01:21 | Send | firm
- Words: "I'll email you a summary of today's call by the end of the day."
- Deadline as said: "by the end of the day", read as Monday 9 November 2026, 17:00 (rule 2: the call date, at the end of working hours)
- Condition: none
- Owner as said: Maya ("I'll")
- Follow-up record: SE-2208, Send, owner Maya, due 9 November 2026, status Done
- Wrap-up note: mentions it
- Flags: none

Expectations set, not promises:
- Line 7, 00:40: "Replacements normally go out within five working days."

Completed during the call:
None.

CALL C-4486 | Monday 9 November 2026, 16:40 | Agent: Theo | Customer: Customer B | Case: 88240

P5 | Line 7, 01:12 | Refund or credit | hedged
- Words: "The refund should be with you within 48 hours."
- Deadline as said: "within 48 hours", read as Wednesday 11 November 2026, 16:40 (rule 6: 48 clock hours after the call's start)
- Condition: none
- Owner as said: not stated on the call; record RF-7702 names Billing team
- Follow-up record: RF-7702, Refund, owner Billing team, due 13 November 2026, status Open
- Wrap-up note: mentions it
- Flags: HEDGED, RECORD LATER THAN PROMISED, DEADLINE PASSED
- No record supplied shows it done. This is not proof it was broken.
- Question 4 below.

P6 | Line 9, 01:21 | Send | firm
- Words: "If it's not there by then, I'll email you myself with an update."
- Deadline as said: not stated
- Condition: "If it's not there by then" (line 9); depends on a time, read as Wednesday 11 November 2026, 16:40 (rule 6, as for line 7: 48 clock hours after the call's start); not met by the end of the call
- Owner as said: Theo ("I'll")
- Follow-up record: none found
- Wrap-up note: does not mention it
- Flags: DEADLINE NOT STATED, CONDITIONAL, NO RECORD FOUND
- Question 5 below.

Expectations set, not promises:
None.

Completed during the call:
- Line 4, done at line 5: raised with the billing team, reference TK-5531 said on the call.

QUESTIONS FOR THE TEAM LEADER

1. C-4471 P1: Maya said a replacement would be arranged once the customer's photos are in. The call names no owner and no date, the photos had not arrived by the end of the call, and no delivery record was found. Your owner map proposes the Fulfillment team. Have the photos arrived since, and who arranges the replacement, by when?
2. C-4471 P2: Maya offered a $25 credit; your limit for agents is $20 without approval. No date was given, no refund or credit record was found, and the wrap-up note does not mention it. Do you approve the credit, and who applies it, by when?
3. C-4471 P3: Maya promised a callback by Thursday 12 November 2026, read as 17:00; record CB-3120 is due Friday 13 November 2026. Does the callback move to Thursday, or is the customer told of the later day?
4. C-4486 P5: Theo said the refund should be with the customer within 48 hours, read as Wednesday 11 November 2026, 16:40. Record RF-7702, owned by the Billing team, is due Friday 13 November 2026 and is still Open. Has the refund been paid, and is the customer told of the later date?
5. C-4486 P6: Theo said he would email the customer himself if the refund had not arrived by then. That time, read as Wednesday 11 November 2026, 16:40, has passed and RF-7702 is still Open; no send record was found and the wrap-up note does not mention the email. Has the refund arrived since, and if not, does Theo send the email, and by when?

COULD NOT BE READ

None.

Prepared for the team leader. Nothing has been booked, assigned, changed or sent.
No customer has been contacted. This list is not proof a promise was kept or broken.
```

## How the figures were worked out

- **Promises:** six. Lines 5, 9, 11 and 13 of C-4471 and lines 7 and 9 of C-4486. Five are firm; P5 is hedged by "should". Line 7 of C-4471 says how replacements "normally" go, so it is an expectation. Line 4 of C-4486 was done on the call, at line 5. Line 3 of C-4471 and line 3 of C-4486 are a request and a statement about the past.
- **Flagged:** five, every promise but P4.
- **Records:** five supplied. CB-3099 belongs to call C-4460, which is not in this run. The other four belong to these calls: CB-3120 and SE-2208 by Call ID, TK-5531 by Call ID (the action done on the call), and RF-7702 by its case, 88240, since its Call ID is blank. Each was created after its call started (14:19 and 14:22 after 14:05; 16:41 and 16:52 after 16:40).
- **P3:** Monday 9 November to the first Thursday after it is Thursday 12 November, read as 17:00. CB-3120 is due Friday 13 November, read as 17:00, one day later. Thursday 17:00 is after the run at Thursday 09:30, so the deadline has not passed.
- **P4:** the call date, Monday 9 November, read as 17:00. SE-2208 is due the same day and is Done.
- **P5:** 16:40 on Monday 9 November plus 48 clock hours is 16:40 on Wednesday 11 November, a working day within working hours. RF-7702 is due Friday 13 November, later than promised, and is Open, not a done status. Wednesday 16:40 is before the run at Thursday 09:30, so the deadline has passed.
- **P2:** a $25 credit against a $20 limit is $5 over, so it needs approval.
- **P6:** the condition's time is P5's reading. The email itself has no deadline.

Nothing was booked, assigned, changed or sent; the team leader settles each question in the company's own systems.
