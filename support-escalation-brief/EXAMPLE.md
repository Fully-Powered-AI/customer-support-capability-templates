# Support escalation brief: an invented example

*Illustrative example with invented data.* The company, its customers, the team, the ticket and every date below are invented. Company X is an invented 25-person business that sells coffee beans to cafés through an online ordering portal. Its support team is led by a support lead; Marta is the support agent who holds the case. On Monday 2 November 2026 the support lead asks for a brief on one unresolved ticket, to hand to the platform team.

The inputs come first, in full, so the template can be run on them. The brief follows.

## The inputs

### The date of the brief

```
Brief date: 2026-11-02
```

### The ticket's details

```
Ticket: S-2041
Customer: Customer A
Plan: Business account
Priority: P2
Status: Open
Owner: Marta
```

### The ticket history export

```
Ticket,Date,Who,Kind,Entry
S-2041,2026-10-21,Customer A (A-1),Customer message,"Our standing order for the three sites did not come on Tuesday 20 October and there is no order in the portal for that day. Two sites ran out of beans on Tuesday afternoon and Wednesday morning. I logged out and back in and the portal still shows no order. [attachment: portal-orders-21-oct.png]"
S-2041,2026-10-21,System,Automatic,"Acknowledgement sent to customer."
S-2041,2026-10-21,System,Assignment,"Unassigned to Marta."
S-2041,2026-10-21,Marta,Team reply,"Sorry about that. The standing order shows as Active but no order was generated for 20 October. I have placed a manual order for delivery on Thursday 22 October. Please check the three site addresses on it."
S-2041,2026-10-22,Customer A (A-1),Customer message,"Addresses were right and the delivery arrived this morning. We bought beans from a shop to cover the gap. Please make sure it does not happen again."
S-2041,2026-10-22,Marta,Internal note,"Audit log for standing order SO-889 shows an edit on 2026-10-16 by contact A-2: site 3 delivery day changed from Tuesday to Wednesday, then back to Tuesday in the same hour. Possible cause; not confirmed."
S-2041,2026-10-22,Marta,Internal note,"Re-saved SO-889 with no changes to see whether the next run generates."
S-2041,2026-10-22,Marta,Status change,"Open to Solved. Manual order delivered; cause still being checked."
S-2041,2026-10-28,Customer A (A-1),Customer message,"Nothing came on Tuesday 27 October and there is no order in the portal. A third site ran out on Wednesday. This is the second week. Nobody at our end has changed anything on the order. We are thinking of moving our order to another supplier."
S-2041,2026-10-28,System,Status change,"Solved to Open (customer reply)."
S-2041,2026-10-28,System,Automatic,"Acknowledgement sent to customer."
S-2041,2026-10-28,Marta,Team reply,"I am sorry. The standing order did not run again on 27 October. I have placed a manual order for delivery on Thursday 29 October and I will update you by Friday 30 October on the cause."
S-2041,2026-10-29,Customer A (A-1),Customer message,"The delivery arrived. Please tell us what is going wrong. We review our suppliers on Wednesday 4 November."
S-2041,2026-10-30,Marta,Internal note,"Asked the platform team in the support channel at 10:15 why SO-889 did not run. No reply yet."
S-2041,2026-10-30,Marta,Team reply,"I do not have a cause yet and I am still chasing it. I will place a manual order each week until it is fixed."
S-2041,2026-11-02,Customer A (A-1),Customer message,"Any news? Our review is on Wednesday."
S-2041,2026-11-02,Marta,Internal note,"Placed manual order for delivery on Tuesday 3 November."
```

### The escalation policy

```
ESCALATION POLICY, Company X support (owner: support lead)
Destinations:
  Platform team: faults in our own systems (orders, portal, integrations).
    Criteria: the fault has happened on 2 or more occasions, or a customer
    deadline falls within 5 days.
  Accounts manager: commercial risk.
    Criteria: the customer says they may leave, or names a review of
    their suppliers.
Rules: the support lead chooses the destination. The receiving owner
confirms in the ticket within 1 working day. A brief carries impact,
timeline, evidence, fixes tried, workaround and the decision needed.
```

### Related reports

```
Reference,Date,Customer,Summary,Status
S-2058,2026-10-30,Customer B,"Weekly order not created for Tuesday 27 October; customer placed it by hand",Open
Known-issues list: no entry about standing orders, checked by the support lead on 2 November 2026.
```

### The support lead's choice

```
Destination: Platform team. Receiving owner: the platform team's on-call lead, confirmed by the support lead on 2 November 2026.
```

## The output

The brief is plain text. It is set here with bold section titles and bullets so it reads well on a page; the words and their order are the template's.

**SUPPORT ESCALATION BRIEF: S-2041, Customer A**

Prepared for: support lead. Brief date: 2026-11-02. History read to: 2026-11-02 (17 entries).
Destination: Platform team. Receiving owner: the platform team's on-call lead, confirmed by the support lead on 2026-11-02.
Internal. Nothing here has been sent to the customer or to the receiving owner.

**THE CASE**

S-2041 | Customer A | Business account | priority P2 | status Open | owner Marta
Problem: the customer says its standing order for the three sites did not come on Tuesday 20 October and no order shows in the portal for that day.
Opened 2026-10-21 (12 days before this brief). Reopened 1 time(s): 2026-10-28. Entries: 5 customer messages, 3 team replies, 4 internal notes, 3 status or assignment changes, 2 automatic.
Last customer message: 2026-11-02 (0 days ago), not yet answered. Last team reply to the customer: 2026-10-30 (3 days ago).

**IMPACT**

Stated by the customer:
- The standing order covers three sites (2026-10-21).
- Two sites ran out of beans, on "Tuesday afternoon and Wednesday morning" (2026-10-21).
- The customer bought beans from a shop to cover the gap (2026-10-22).
- A third site ran out of beans, on "Wednesday" (2026-10-28).
- The customer is thinking of moving its order to another supplier (2026-10-28).
- The customer reviews its suppliers on Wednesday 4 November (2026-10-29, repeated 2026-11-02).

Confirmed by the team:
- The standing order did not generate an order on 20 October (Marta, 2026-10-21) or on 27 October (Marta, 2026-10-28).
- Manual orders were placed for delivery on 22 October, 29 October and 3 November (Marta, 2026-10-21, 2026-10-28, 2026-11-02).

Not verified or not stated:
- That the sites ran out of beans: only the customer says so.
- The cost of the shop purchases: no amount is stated.
- The supplier review on 4 November: only the customer says so.

**TIMELINE**

2026-10-21 | Customer | A-1 says the standing order for Tuesday 20 October did not arrive and the portal shows no order; two sites ran out of beans. Screenshot attached.
2026-10-21 | System | Ticket assigned to Marta.
2026-10-21 | Team | Marta replied: the standing order shows Active but no order was generated for 20 October; manual order placed for delivery on Thursday 22 October.
2026-10-22 | Customer | A-1 says the delivery arrived and the addresses were right; says beans were bought from a shop to cover the gap; asks that it not happen again.
2026-10-22 | Internal note | Marta: audit log for SO-889 shows an edit on 16 October by contact A-2 (site 3 delivery day moved and moved back). Possible cause, not confirmed.
2026-10-22 | Internal note | Marta re-saved SO-889 with no changes, to see whether the next run generates.
2026-10-22 | Team | Marta changed the status from Open to Solved: manual order delivered, cause still being checked.
2026-10-28 | Customer | A-1 says nothing arrived on 27 October; a third site ran out; nobody at their end changed the order; they are thinking of moving to another supplier.
2026-10-28 | System | Status changed from Solved to Open, from the customer's reply.
2026-10-28 | Team | Marta replied: the standing order did not run again on 27 October; manual order placed for delivery on 29 October; promised an update on the cause by 30 October.
2026-10-29 | Customer | A-1 says the delivery arrived, asks what is going wrong, and says they review their suppliers on Wednesday 4 November.
2026-10-30 | Internal note | Marta: asked the platform team in the support channel at 10:15 why SO-889 did not run; no reply yet.
2026-10-30 | Team | Marta replied: no cause yet, still chasing it; will place a manual order each week until it is fixed.
2026-11-02 | Customer | A-1 asks for news and says the review is on Wednesday.
2026-11-02 | Internal note | Marta: placed a manual order for delivery on Tuesday 3 November.
2 automatic entries left out.

**EVIDENCE**

Found:
- Screenshot portal-orders-21-oct.png: attached to the customer message of 2026-10-21; the customer's message says the portal shows no order; the file has not been opened.
- Audit log reading for SO-889: in Marta's internal note of 2026-10-22; it reports an edit on 16 October by contact A-2. The log extract itself is not in the history.
- Status of the standing order: in Marta's reply of 2026-10-21; the entry says it shows Active with no order generated for 20 October.
Checklist:
- Exact error text or system log: not in the history
- Steps to reproduce: not in the history
- When it happened, date and time: date only (20 October and 27 October)
- Record identifiers: found, standing order SO-889 and contacts A-1 and A-2
- Screenshot or file: found, 1
Reproduction: no entry says it was tried.

**FIXES ALREADY TRIED**

2026-10-21 | Customer (A-1) | Logged out and back in | no effect: the customer says the portal still showed no order (2026-10-21 message)
2026-10-22 | Marta | Re-saved SO-889 with no changes | not recorded: no entry gives the result; the 27 October run was missed afterwards (2026-10-28 message and reply)
2026-10-30 | Marta | Asked the platform team in the support channel | not recorded: no reply recorded (2026-10-30 internal note)

**CURRENT WORKAROUND**

Marta places a manual order each week. In place since 2026-10-21 (first manual order; weekly since the 2026-10-30 promise), set by Marta. Customer confirmed it works: yes, for the deliveries of 22 and 29 October (2026-10-22 and 2026-10-29 messages); the 3 November delivery is not yet due. What it does not cover: the cause, and the standing order itself. Depends on: a person placing the order each week; Marta promised on 2026-10-30 to do so until it is fixed.

**PROMISES AND OPEN REQUESTS**

2026-10-22 | Customer asked | to make sure it does not happen again | not answered: the standing order was missed again on 27 October (2026-10-28 message and reply)
2026-10-28 | Marta promised | an update on the cause by Friday 30 October | not kept: a reply was sent on 2026-10-30, but it gave no cause
2026-10-29 | Customer asked | what is going wrong | answered without what was asked: the 2026-10-30 reply gave no cause
2026-10-30 | Marta promised | a manual order each week until it is fixed | kept so far: the order for 3 November was placed on 2026-11-02
2026-11-02 | Customer asked | for news before the review on Wednesday | not answered: no team reply since 2026-10-30

**CONFLICTS AND GAPS**

- Conflict: whether the order was changed. Customer, 2026-10-28: nobody at their end changed anything on the order. Marta's internal note, 2026-10-22: the audit log shows contact A-2 edited SO-889 on 16 October. Neither is verified.
- Gap: no run record for SO-889 on 20 or 27 October is in the history.
- Gap: no entry shows that the customer was asked about the 16 October edit.

**RELATED REPORTS**

S-2058 | 2026-10-30 | Customer B | Weekly order not created for Tuesday 27 October; customer placed it by hand | same symptom. Not verified that the cause is shared.
Known-issues list: no matching entry.

**POLICY CHECK**

Platform team: "the fault has happened on 2 or more occasions": met, the standing order did not generate on 20 October and 27 October, both confirmed by Marta (2026-10-21, 2026-10-28).
Platform team: "a customer deadline falls within 5 days": cannot tell, the customer names a review of its suppliers on Wednesday 4 November, 2 days after the brief date; whether that is a deadline in the policy's sense is for the support lead.
Accounts manager: "the customer says they may leave": met, the customer says it is thinking of moving its order to another supplier (2026-10-28).
Accounts manager: "names a review of their suppliers": met, the customer names a review on Wednesday 4 November (2026-10-29).
Policy asks the brief to carry: impact, timeline, evidence, fixes tried, workaround and the decision needed; all present.
The support lead chooses the destination.

**DECISION NEEDED**

From the platform team's on-call lead:
1. Why did SO-889 not generate an order on 20 and 27 October, and does the audit log for SO-889 support or rule out the 16 October edit by contact A-2 as the cause? Blocked: Marta has no cause to give the customer, and the support-channel request of 2026-10-30 has no reply.
2. Who in the platform team owns this fault? Blocked: no entry names anyone who owns it.
Needed by: Wednesday 4 November 2026, the customer's stated supplier review (2026-10-29); the policy gives the receiving owner 1 working day to confirm in the ticket.

**QUESTIONS FOR THE SUPPORT LEAD BEFORE IT GOES**

1. The customer's message of 2026-11-02 ("Any news?") has no reply and the customer's review is on 4 November. Who answers it, and with what? The brief writes nothing for the customer.
2. The Accounts manager's criteria also look met (2026-10-28 and 2026-10-29). Does the accounts manager receive a copy?
3. The request in the support channel on 2026-10-30 has no reply in the history. Does this brief replace it?
4. The run record for SO-889, the steps to reproduce and the time of the missed runs are not in the history. Can anyone supply them before the brief goes?
5. The history has two accounts of whether the order was changed. Does anyone ask the customer about the 16 October edit before the brief goes, or does the platform team check the audit log for SO-889 first?

Prepared for the support lead. Nothing has been sent, no ticket has been changed and no one has been contacted.
