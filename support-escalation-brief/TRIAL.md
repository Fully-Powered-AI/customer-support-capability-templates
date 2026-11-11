# Support escalation brief: trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs for this trial are the invented example in `public/example.md` (the date of the brief, the ticket's details, the 17-entry history export, the escalation policy, the related report and the support lead's choice). No client data was used.

This is the second run. The first run, made earlier the same day, was on the instruction block as first written. After an independent review the instruction block was brought into line with the procedure (results shown only by later entries, promises and requests in date order, the customer's own date as "needed by", the stops for a missing export and a missing brief date) and the procedure gained four rules (stopgaps such as manual orders belong under the workaround, criteria joined by "or" are set out one line per alternative, the source label of a status or assignment entry, and a log described but not quoted). The first run's output was replaced by this one, because the instruction block it followed no longer exists in that form.

Independence is weaker here than in the first run. The model that ran this one is the model that edited the template and the example in this pass, and it had read the example's output before running. It followed the instruction block and the output format line by line on the inputs, without copying from the example's output. Where this run's output matches the example, that is not independent confirmation; the differences below are the more useful evidence.

## What came out

The run produced every section of the output format. It did not stop: the headings matched, every kind was on the list, there was one ticket, the ticket number matched the details, the brief date was supplied and no entry was dated after it. The output follows as produced.

```
SUPPORT ESCALATION BRIEF: S-2041, Customer A

Prepared for: the support lead. Brief date: 2026-11-02. History read to: 2026-11-02 (17 entries).
Destination: Platform team. Receiving owner: the platform team's on-call lead, confirmed by the support lead on 2026-11-02.
Internal. Nothing here has been sent to the customer or to the receiving owner.

THE CASE
S-2041 | Customer A | Business account | priority P2 | status Open | owner Marta
Problem: the customer says its standing order for the three sites did not come on Tuesday 20 October and that no order shows in the portal for that day.
Opened 2026-10-21 (12 days before this brief). Reopened 1 time(s): 2026-10-28. Entries: 5 customer messages, 3 team replies, 4 internal notes, 3 status or assignment changes, 2 automatic.
Last customer message: 2026-11-02 (0 days ago), not yet answered. Last team reply to the customer: 2026-10-30 (3 days ago).

IMPACT
Stated by the customer:
- The standing order covers three sites (2026-10-21).
- Two sites ran out of beans, on "Tuesday afternoon and Wednesday morning" (2026-10-21).
- The customer bought beans from a shop to cover the gap (2026-10-22).
- The customer asked that it not happen again (2026-10-22).
- A third site ran out on "Wednesday" (2026-10-28).
- The customer is "thinking of moving our order to another supplier" (2026-10-28).
- The customer reviews its suppliers on Wednesday 4 November (2026-10-29, repeated 2026-11-02).
Confirmed by the team:
- The standing order showed as Active but no order was generated for 20 October (Marta, 2026-10-21).
- The standing order did not run on 27 October (Marta, 2026-10-28).
- Manual orders were placed for delivery on 22 October, 29 October and 3 November (Marta, 2026-10-21, 2026-10-28, 2026-11-02).
Not verified or not stated:
- That the sites ran out of beans: only the customer says so.
- The cost of the beans bought from the shop: no amount is stated.
- The supplier review on 4 November, and whether it concerns this fault: only the customer says there is a review.
- The customer's intention to leave: it says it is thinking of moving, no decision is stated.

TIMELINE
2026-10-21 | Customer | A-1 says the standing order for Tuesday 20 October did not come and the portal shows no order; two sites ran out; logging out and in changed nothing. Screenshot attached.
2026-10-21 | System | Assignment entry, worded in the history as "Unassigned to Marta."
2026-10-21 | Team | Marta replied: the order shows Active but none was generated for 20 October; manual order placed for delivery on Thursday 22 October; asked A-1 to check the addresses.
2026-10-22 | Customer | A-1 says the addresses were right and the delivery arrived; bought beans from a shop to cover the gap; asks that it not happen again.
2026-10-22 | Internal note | Marta: audit log for SO-889 shows a 16 October edit by contact A-2 (site 3 day moved and moved back). "Possible cause; not confirmed."
2026-10-22 | Internal note | Marta re-saved SO-889 with no changes, to see whether the next run generates.
2026-10-22 | Team | Marta changed status from Open to Solved: manual order delivered, cause still being checked.
2026-10-28 | Customer | A-1 says nothing came on Tuesday 27 October and no order is in the portal; a third site ran out; says nobody changed the order; thinking of moving supplier.
2026-10-28 | System | Status changed from Solved to Open, on the customer's reply.
2026-10-28 | Team | Marta replied: the order did not run again on 27 October; manual order placed for 29 October; promised an update on the cause by Friday 30 October.
2026-10-29 | Customer | A-1 says the delivery arrived, asks what is going wrong, and says the supplier review is on Wednesday 4 November.
2026-10-30 | Internal note | Marta asked the platform team in the support channel at 10:15 why SO-889 did not run. No reply yet.
2026-10-30 | Team | Marta replied: no cause yet, still chasing it; will place a manual order each week until it is fixed.
2026-11-02 | Customer | A-1 asks "Any news?" and says the review is on Wednesday.
2026-11-02 | Internal note | Marta placed a manual order for delivery on Tuesday 3 November.
2 automatic entries left out.

EVIDENCE
Found:
- Screenshot portal-orders-21-oct.png: customer message of 2026-10-21; the message says it shows the portal with no order; the file has not been opened.
- Audit log for SO-889: Marta's internal note of 2026-10-22; the note says it shows a 16 October edit by contact A-2 (site 3 delivery day changed from Tuesday to Wednesday and back in the same hour). The log itself is not in the history.
Checklist:
- Exact error text or system log: described in an entry, not quoted (the audit log, in the note of 2026-10-22)
- Steps to reproduce: not in the history
- When it happened, date and time: date only (20 October and 27 October; the 16 October edit has no time)
- Record identifiers: found, standing order SO-889 and contacts A-1 and A-2
- Screenshot or file: found, 1
Reproduction: no entry says it was tried.

FIXES ALREADY TRIED
2026-10-21 | Customer (A-1) | Logged out and back in | no effect: the customer says the portal still showed no order (message of 2026-10-21)
2026-10-22 | Marta | Re-saved SO-889 with no changes | not recorded: no entry gives the result; later entries are the customer message and Marta's reply of 2026-10-28
2026-10-30 | Marta | Asked the platform team in the support channel | not recorded: no reply recorded (internal note of 2026-10-30)

CURRENT WORKAROUND
A manual order placed by Marta for each delivery day. In place since 2026-10-21 (first manual order; weekly since the 2026-10-30 promise), set by Marta. Customer confirmed it works: yes, for the deliveries of 22 and 29 October (messages of 2026-10-22 and 2026-10-29); not confirmed for 3 November. What it does not cover: the standing order itself still has no recorded cause or fix; the customer's request to know the cause. Depends on: a person placing each order by hand; Marta promised on 2026-10-30 to do so until it is fixed.

PROMISES AND OPEN REQUESTS
2026-10-21 | Marta promised | a manual order for delivery on 22 October | kept so far: the customer says the delivery arrived (2026-10-22)
2026-10-22 | Customer asked | to make sure it does not happen again | not answered: the order was missed again on 27 October (2026-10-28 message and reply)
2026-10-28 | Marta promised | a manual order for delivery on 29 October | kept so far: the customer says the delivery arrived (2026-10-29)
2026-10-28 | Marta promised | an update on the cause by Friday 30 October | kept so far: a reply was sent on 2026-10-30, but it gives no cause
2026-10-29 | Customer asked | what is going wrong | answered without what was asked: the 2026-10-30 reply gives no cause
2026-10-30 | Marta promised | a manual order each week until it is fixed | kept so far: the order for 3 November was placed on 2026-11-02
2026-11-02 | Customer asked | for news before the review on Wednesday | not answered: no team reply since 2026-10-30

CONFLICTS AND GAPS
- Conflict: whether anything was changed on the order. Customer, 2026-10-28: nobody at their end changed anything. Marta's internal note, 2026-10-22: the audit log shows contact A-2 edited SO-889 on 16 October. Neither is verified.
- Gap: the cause; no entry says why SO-889 did not run on 20 or 27 October.
- Gap: the audit log text and any run record for SO-889.
- Gap: which sites ran out, and the cost of the shop purchase.
- Gap: whether contact A-2 works for the customer.
- Gap: a reply to the support-channel request of 2026-10-30.

RELATED REPORTS
S-2058 | 2026-10-30 | Customer B | Weekly order not created for Tuesday 27 October; customer placed it by hand | same symptom. Not verified that the cause is shared.
Known-issues list: no matching entry.

POLICY CHECK
Platform team: "the fault has happened on 2 or more occasions": met, no order was generated on 20 October and 27 October, both stated by Marta (2026-10-21, 2026-10-28).
Platform team: "a customer deadline falls within 5 days": cannot tell, the customer names a review of its suppliers on Wednesday 4 November, 2 days after the brief date (2026-10-29); whether a review is a deadline in the policy's sense is for the support lead.
Accounts manager: "the customer says they may leave": met, the customer says it is thinking of moving its order to another supplier (2026-10-28).
Accounts manager: "names a review of their suppliers": met, the customer names a review on Wednesday 4 November (2026-10-29).
Policy asks the brief to carry: impact, timeline, evidence, fixes tried, workaround and the decision needed; all present.
The support lead chooses the destination.

DECISION NEEDED
From the platform team's on-call lead:
1. Why did SO-889 not generate an order on 20 and 27 October, and does the audit log for SO-889 support or rule out the 16 October edit by contact A-2 as the cause? Blocked: Marta has no cause to give the customer, and the support-channel request of 2026-10-30 has no recorded reply.
2. Who in the platform team owns this fault? Blocked: no entry names anyone who owns it.
Needed by: Wednesday 4 November 2026, the customer's own date for its supplier review (message of 2026-10-29).

QUESTIONS FOR THE SUPPORT LEAD BEFORE IT GOES
1. The customer's message of 2026-11-02 ("Any news?") has no reply and its review is on 4 November. Who answers it, and with what? The brief writes nothing for the customer.
2. The accounts manager's criteria also look met (2026-10-28, 2026-10-29). Does the accounts manager receive a copy?
3. Checklist items not found: steps to reproduce, and the audit log text, which is described but not quoted. Can the log extract and the run record for SO-889 be attached before this goes?
4. The history has two accounts of whether the order was changed. How is the 16 October edit to be raised with the customer?
5. The support-channel request of 2026-10-30 has no reply in the history. Is it to be treated as unanswered?

Prepared for the support lead. Nothing has been sent, no ticket has been changed and no one has been contacted.
```

## What was observed

**Every required part was produced.** All twelve sections are present, in the order of the format, with the closing line. Counts and day counts were worked out from the export and match the example: 17 entries (5 customer messages, 3 team replies, 4 internal notes, 3 status or assignment changes, 2 automatic), opened 12 days before the brief, reopened once on 2026-10-28, last customer message unanswered, last team reply 3 days ago.

**The changes made after review took effect in this run.**
- The re-save of SO-889 was marked "not recorded", with the later entries named and nothing said about what they suggest. The first run had marked it "no effect".
- "Needed by" gave 4 November, labelled as the customer's own date. The first run had written "no date stated".
- The manual orders were put under the workaround and not under fixes, so the fixes list has three lines, as in the example. The first run had six.
- The policy's two "or" sentences were set out one line per alternative, four lines in all.
- The audit log, described in a note and not quoted, took the checklist value "described in an entry, not quoted".
- Promises and requests are in date order. The status change by Marta took the source Team and the system's took System.

**Nothing was stopped for.** The inputs were clean, so none of the stop conditions, including the two added to the instruction block (no export; no brief date), was tested here. The assistant was not asked to choose a destination, write to the customer or change anything.

**Where the instructions still left room to guess.**
- Whether a team statement made without saying what was checked ("the standing order did not run again on 27 October") counts as confirmed by the team. The run put it under Confirmed. This is the same call as the example and the first run.
- Whether Marta's update on 30 October, which gave no cause, keeps her promise of 28 October "an update on the cause". The run marked it "kept so far" with the basis that it gives no cause; the example marks it "not kept". The output format allows both marks, so this is a judgment the support lead checks.
- Whether the manual-order promises of 21 and 28 October are promises to list. The run listed them; the example lists only the weekly promise and the update. Both are defensible.
- Whether the policy's one-working-day confirmation starts from the support lead's choice on 2 November; the history shows no confirmation in the ticket. The run left it out of the brief.
- The history entry "Unassigned to Marta." reads oddly. The run reported it as written, with the source System, and did not list it as a gap this time.

**Differences from the published example.**
- The run's Impact lists the customer's request that it not happen again; the example does not.
- The run's Evidence lists two found items; the example lists the Active status of SO-889 as a third. The run put that under Confirmed by the team, as the review suggested.
- The run's Promises and open requests has seven lines; the example has five.
- The run's gaps list is shorter than the first run's and does not include the example's gap that nobody asked the customer about the 16 October edit; it asked that as a question for the support lead instead.
- Several timeline lines in the run run close to the 30-word limit; they were counted and none passes it.

**Facts in the output that are not in the inputs.** None was found on a line-by-line check of this output against the export. The first run's error, a line saying the customer confirmed the addresses "held for SO-889", was not repeated; this run says the manual orders are what the customer confirmed.

**Against the reviewer checklist.** Items 1 to 11 hold for the run's output on the checks made here. A person still has to read the output against the ticket, as the checklist says.

**What this does and does not show.** The template can be followed on a clean, invented ticket and gives a brief that matches the example in structure and in every count. It was run twice, in one product, on one set of inputs, and the second run was made by the model that edited the template. It does not show how the template behaves on messy exports, on the stop conditions or on a real ticket, and none of the acceptance tests was run.
