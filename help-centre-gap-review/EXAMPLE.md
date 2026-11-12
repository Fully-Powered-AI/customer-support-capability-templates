# Help centre gap review: an invented example

*Illustrative example with invented data.* The company, its customers, the staff, the tickets, the searches, the articles and every figure below are invented. Company V is an invented 25-person company that sells class-booking software to independent fitness and dance studios; its customers are the studios' owners and managers. First come the inputs the support specialist supplied, in full, then the review the workflow template returned.

## The inputs

### 1. Settings

```
Period: 1 October 2026 to 31 October 2026
Today: Monday 9 November 2026
Support lead: Lena, support lead
Run by: Omar, support specialist
Common topic: 4 or more tickets in the period
Security role: operations manager
Escalation role: operations manager
Topics that always go to security: account-security
```

### 2. Ticket export

```
ticket_id,created,topic,subject,article_linked,resolution
T-4099,2026-09-30,billing-card-update,update card,KB-210,Customer updated card after link
T-4101,2026-10-02,billing-card-update,How do I change the card we pay with?,KB-210,Customer updated card after link
T-4103,2026-10-03,class-waitlist,Class is full - can people join a waiting list?,-,Agent pointed to the Waitlist switch on the class's Capacity tab
T-4105,2026-10-04,member-import,Upload my client list from old system,KB-118,Customer imported members after link
T-4107,2026-10-05,billing-card-update,Card expired - Studio P,KB-210,Customer updated card after link; said the article showed an old menu
T-4108,2026-10-06,cancel-class,cancel tonight's class,KB-130,Customer followed article after link
T-4110,2026-10-07,refund-request,Refund for last month please,-,Support issued a refund
T-4111,2026-10-08,class-waitlist,waitlist for Saturday class,-,Agent pointed to the Waitlist switch on the class's Capacity tab
T-4113,2026-10-09,member-import,import contacts from spreadsheet - Ana at Studio K,KB-118,Customer imported members after link
T-4114,2026-10-09,app-notifications,members not getting reminder texts,-,Agent turned on reminder texts in the admin console
T-4115,2026-10-09,billing-card-update,new credit card for our subscription,KB-210,Customer updated card after link
T-4117,2026-10-12,cancel-class,How to cancel a class and tell people,KB-130,Customer followed article after link
T-4119,2026-10-13,class-waitlist,how do waitlists work,-,Agent explained how members join the waitlist once the Waitlist switch is on
T-4120,2026-10-13,refund-request,charged twice,-,Support issued a refund of the duplicate charge
T-4122,2026-10-14,billing-card-update,can't find where to update card,KB-210,Article's menu did not match the screen; agent sent steps for Settings > Billing and plans > Payment methods
T-4123,2026-10-15,,Question about your API,-,Agent answered by email
T-4124,2026-10-16,member-import,moving clients over,KB-118,Customer followed article after link
T-4126,2026-10-18,cancel-class,cancelling a class at short notice,KB-130,Customer followed article after link
T-4127,2026-10-19,class-waitlist,Members asking to queue for full classes,-,Agent pointed to the Waitlist switch on the class's Capacity tab
T-4128,2026-10-19,account-security,Someone else may have logged in to our account,-,Passed to the operations manager
T-4129,2026-10-20,refund-request,want refund after cancelling,-,Support issued a refund
T-4130,2026-10-20,billing-card-update,card expired and payment failed,-,Agent sent steps for Settings > Billing and plans > Payment methods
T-4131,2026-10-21,app-notifications,Reminder emails going to spam,-,Customer added the sending address to their mail settings
T-4133,2026-10-22,member-import,upload clients excel,KB-118,Customer followed article after link
T-4135,2026-10-24,class-waitlist,waiting list not showing for members,-,Agent pointed to the Waitlist switch on the class's Capacity tab
T-4136,2026-10-25,cancel-class,Cancel class,KB-130,Customer followed article after link
T-4137,2026-10-26,refund-request,Refund - Studio P,-,Support issued a refund
T-4138,2026-10-27,billing-card-update,Change card on file (Maria),KB-210,Customer updated card after link
```

### 3. Help-centre search log, October 2026

```
search_term,searches,results
card expired,9,0
upload clients,6,0
waiting list,5,0
gift cards,4,0
cancel class,4,2
import contacts,3,0
opening hours,1,1
```

### 4. Article list

```
article_id,title,tags
KB-101,Add your studio's opening hours,opening hours; studio details
KB-118,Import members from a spreadsheet,import; members; CSV
KB-130,Cancel a class and tell booked members,cancel class; notify members
KB-145,Set up class packs,class packs; credits; pricing
KB-210,Update your payment card,payment card; billing; update card
```

## The output

```
HELP CENTRE GAP REVIEW: 1 October 2026 to 31 October 2026
For: Lena, support lead. Prepared Monday 9 November 2026 for Omar, support specialist.
Tickets: 28 in the export; 27 in the period; 1 outside the period, left out.
Articles: 5. Search log: 7 terms, 5 with no results.
Common topic: 4 or more tickets in the period.
Check: 23 in common topics + 2 in topics below the threshold + 1 with no topic + 1 sent to security or escalation = 27 tickets in the period.

TOPICS REVIEWED
1. billing-card-update: 6 tickets (T-4101, T-4107, T-4115, T-4122, T-4130, T-4138). Answered by hand 1; answered with a link 3; link fell short 2; staff action 0; unclear 0. Articles: KB-210. Searches with no results: 9. Verdict: Falls short, Not found by search.
2. class-waitlist: 5 tickets (T-4103, T-4111, T-4119, T-4127, T-4135). Answered by hand 5; answered with a link 0; link fell short 0; staff action 0; unclear 0. Articles: none. Searches with no results: 5. Verdict: Missing.
3. cancel-class: 4 tickets (T-4108, T-4117, T-4126, T-4136). Answered by hand 0; answered with a link 4; link fell short 0; staff action 0; unclear 0. Articles: KB-130. Searches with no results: 0. Verdict: No gap shown.
4. member-import: 4 tickets (T-4105, T-4113, T-4124, T-4133). Answered by hand 0; answered with a link 4; link fell short 0; staff action 0; unclear 0. Articles: KB-118. Searches with no results: 9. Verdict: Not found by search.
5. refund-request: 4 tickets (T-4110, T-4120, T-4129, T-4137). Answered by hand 0; answered with a link 0; link fell short 0; staff action 4; unclear 0. Articles: none. Searches with no results: 0. Verdict: Staff action.

MISSING
- class-waitlist, 5 tickets answered by hand (T-4103, T-4111, T-4119, T-4127, T-4135). The agents' replies: pointed to the Waitlist switch on the class's Capacity tab (4 tickets); explained how members join the waitlist once the Waitlist switch is on (1 ticket). Customers asked: "waiting list" (2 tickets); "waitlist" (2 tickets); "full class" (2 tickets). Searched "waiting list" 5 times, no results.

FALLS SHORT
- KB-210, "Update your payment card", for billing-card-update: T-4107: the customer said the article showed an old menu; T-4122: the article's menu did not match the screen, and the agent sent steps for Settings > Billing and plans > Payment methods.

NOT FOUND BY SEARCH
- KB-210, "Update your payment card", for billing-card-update: searched "card expired" 9 times, no results. Not in the title or tags: expired.
- KB-118, "Import members from a spreadsheet", for member-import: searched "upload clients" 6 times and "import contacts" 3 times, no results. Not in the title or tags: upload, clients, contacts.

NO GAP SHOWN
- cancel-class, KB-130: 4 tickets still arrived; 4 answered with a link.

SEARCHED WITH NO RESULTS, NO COMMON TOPIC
- "gift cards" (4 searches); see decision 1.

NOT FOR THE HELP CENTRE
- refund-request, 4 tickets (T-4110, T-4120, T-4129, T-4137): staff action, support issued a refund on each.
- account-security, 1 ticket (T-4128): security, for the operations manager.

GAP LIST (ranked by tickets an article could have saved)
1. Correct, Add search words: KB-210, "Update your payment card". Tickets an article could have saved: 6. Searches with no results: 9. Do: correct the menu the article shows (T-4107: an old menu; T-4122: did not match the screen; the agent's steps were Settings > Billing and plans > Payment methods), and add "expired" to the title or tags.
2. Write: class-waitlist, new article. Tickets an article could have saved: 5. Searches with no results: 5. Do: an article on the Waitlist switch on a class's Capacity tab and how members join the waitlist once it is on, for customers who ask about a "waiting list", a "waitlist" or a "full class".
3. Add search words: KB-118, "Import members from a spreadsheet". Tickets an article could have saved: 4. Searches with no results: 9. Do: add "upload", "clients" and "contacts" to the title or tags.

DECISIONS FOR LENA, SUPPORT LEAD
1. "gift cards". Searched 4 times in October with no results; no ticket in the period is about it and no article covers it. Add it to the gap list, find out more first, or leave it?

BELOW THE THRESHOLD
app-notifications (2)

DATA NOTES
Tickets with no topic: 1 (T-4123).
Customer details kept out: company names: T-4107, T-4113, T-4137; first names: T-4113, T-4138.
Tags that may mean the same topic: None.

Draft for Lena, support lead's decision. Nothing has been written, published, edited or sent, no writer has been named, and no ticket or article has been changed.
```
