# Follow-ups promised on service calls: trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-11

This is the second recorded run. The first run (also 2026-11-11) was by a separate assistant and led to changes in the instruction block, the output format and the example's run settings; this record replaces it. Because the same model that made those changes ran this one, it is a check that the changed block and format can be followed to the example's result, not an independent trial.

The inputs are the invented example, and no client data was used. The run settings, the call list (C-4471 and C-4486), the transcripts and the five follow-up records are those under "The inputs" in `public/example.md`. The run used the template's changed instruction block and output format and those inputs only. The published example's output was read after the list below was produced, not before. Claude Sonnet 5.5 made the edits to the block and format before this run.

## What came out

The assistant produced the full list. Every part the format asks for was produced. It found six promises (five firm, one hedged), five of them flagged, one expectation and one action completed during the call. It stopped for nothing: all headers matched, no call was missing from either file, and no line held card details, a customer name, a lawyer or an instruction aimed at the assistant.

```
FOLLOW-UPS PROMISED ON SERVICE CALLS: Orders and deliveries phone queue, run of Thursday 12 November 2026, 09:30

For: Team leader, Orders and deliveries. Calls read: 2 (C-4471, C-4486). Agents: Maya, Theo.
Promises found: 6 (5 firm, 1 hedged). Flagged: 5. Expectations set, not promises: 1. Completed during the call: 1.
Deadlines read using: Monday to Friday, 09:00 to 17:00 (your settings).
Follow-up records: 5 supplied, exported Thursday 12 November 2026, 09:15; used for these calls: 4; for other calls, not used: 1.
Promise limits: agents may offer a goodwill credit of up to $20 without approval; anything above $20 needs the team leader's approval.
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
- Words: "Yes, I'll call you back by Thursday to confirm the delivery date."
- Deadline as said: "by Thursday", read as Thursday 12 November 2026, 17:00 (rule 4)
- Condition: none
- Owner as said: Maya ("I'll")
- Follow-up record: CB-3120, Callback, owner Maya, due 13 November 2026, status Open
- Wrap-up note: mentions it
- Flags: RECORD LATER THAN PROMISED
- Question 3 below.

P4 | Line 13, 01:21 | Send | firm
- Words: "Of course. I'll email you a summary of today's call by the end of the day."
- Deadline as said: "by the end of the day", read as Monday 9 November 2026, 17:00 (rule 2)
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
- Deadline as said: "within 48 hours", read as Wednesday 11 November 2026, 16:40 (rule 6)
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
- Condition: "If it's not there by then" (line 9); depends on a time, read as Wednesday 11 November 2026, 16:40 (rule 6, as for line 7); not met by the end of the call
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

1. C-4471 P1: Maya said "we'll arrange a replacement" once the photos are in. No owner and no date were named, the photos were not in by the end of the call, and no delivery record was found. Your owner map proposes the Fulfillment team. Have the photos arrived since, and who owns the replacement, by when?
2. C-4471 P2: Maya said she would put a $25 credit on the account. Your limit is $20 without approval. No date was given, no refund or credit record was found, and the wrap-up note does not mention it. Is the credit approved, who applies it, and by when?
3. C-4471 P3: Maya promised a callback by Thursday, read as Thursday 12 November 2026, 17:00. Record CB-3120 is due Friday 13 November 2026. Does the callback move to Thursday, or is the customer told of a different date?
4. C-4486 P5: Theo said the refund should be with the customer within 48 hours, read as Wednesday 11 November 2026, 16:40. Record RF-7702 (Billing team) is due Friday 13 November 2026 and is Open. Who confirms where the refund stands, and is the customer told of a different date?
5. C-4486 P6: Theo said he would email an update if the refund had not arrived by then. That time has passed on the run date and RF-7702 is Open. No send record was found and the wrap-up note does not mention it. Has the refund arrived since, and if not, does Theo send the update, and by when?

COULD NOT BE READ

None.

Prepared for the team leader. Nothing has been booked, assigned, changed or sent.
No customer has been contacted. This list is not proof a promise was kept or broken.
```

## What was observed

Against the published example output:

- The promises, kinds, strengths, deadline readings, flags, owners, record matches, numbering and counts are the same. The six promises, the five flagged ones, the Thursday 12 November 17:00 reading for P3 and the Wednesday 11 November 16:40 reading for P5 and P6 all agree. The customer's own timing ("tonight") appears on P1's condition line, and P6's condition carries its rule in brackets, as the format now asks.
- The differences are wording. This run quoted the whole agent line where the example starts the quote at the promise, which the checklist allows; it wrote out the full promise limit; it left out the longer explanation of the rule in brackets; and its five questions are worded differently. For P5 this run asks who confirms where the refund stands rather than whether it has been paid.
- Nothing in either output is missing from the inputs. Every date, record number, amount and name can be found in the inputs, and the dates follow from them by the rules.

Points from the first run and where they stand:

1. **Kind and record type** are now paired in the record types setting, and this run matched Refund and Delivery from the pairs, not by guessing. Fixed.
2. **The customer's own timing** is now quoted on the condition line and left unread when no rule fits. Fixed.
3. **"By then" in P6** still depends on the assistant resolving a reference to an earlier line. The rule says to give the rule in brackets; this run wrote "as for line 7". Left as it was.
4. **A conditional promise with no record** is still flagged NO RECORD FOUND (P6, and P1). The format now asks every conditional promise's question to ask whether the condition has since been met, which is the only change. Here P6's condition time had already passed, so the flag is a fair one; for a condition that is still open it may read oddly to a team leader.
5. **Deadline not stated on a conditional promise** is unchanged and follows step 7.
6. **"Should" as a promise** is unchanged: hedged promise.
7. **The instruction block** now carries the both-files check, the second agent label rule, "not known" for an unclear speaker, the no-owner wording, "can't promise", "this afternoon" and "straight away", the stated-date rule and the same-weekday reading. This run did not need most of them, because the example has no such cases.
8. **Where the per-call sections sit** is unchanged: under each call.
9. **The order of lines in the P-block** is unchanged and shown once in the format.

The same-weekday reading was not exercised by the example, whose Thursday deadline comes from a Monday call.

This is one run in one product on invented data. It shows the changed template can be followed to a complete list. It is not a test in a real company's systems.
