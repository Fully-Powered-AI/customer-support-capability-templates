# Help centre gap review: tried on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Opus 5.5 (model ID claude-opus-5-5)
- **Date:** 2026-11-10

This was one run of the template, version 0.1.0 as published, on its own invented example. The inputs are the invented Company V data in [the example](example.md), sections 1 to 4 (settings, ticket export, search log and article list). No client data was used.

**This run was not blind.** The same session rewrote the template and wrote the example's inputs, then ran the instruction block on those inputs. There was no separate published output to compare with: the output below is the run's, and it was copied unchanged into the example as its published output. To check it, every count was recomputed afterward by a short script that read the three input files (tickets in and out of the period, the check line, each topic's tickets and sort, the searches with no results matched to each topic, and the words missing from each article's title and tags). Every figure agreed. An independent run by a model that has not seen the output is still to be done.

An earlier draft of this template, with a different method, was tried on an earlier version of this example on the same day. That draft was withdrawn and rewritten, so its record no longer describes this template and is not kept here.

## What came out

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

## What was observed

- **Nothing stopped the run.** Both required exports and the search log were present, every header matched the defaults, no ID was repeated, and there were tickets in the period.
- **Every section of the output format was produced,** in order, and the check line added up (23 + 2 + 1 + 1 = 27). One ticket (T-4099, 30 September) was outside the period and left out.
- **Each verdict but Unclear occurred once or more:** Missing, Falls short, Not found by search, No gap shown and Staff action. The example has no unclear resolution and no tags that look alike, so those paths were not exercised.
- **Customer details stayed out.** The subjects carry two invented studio names and two first names; none appears in the output, and the data notes record the kinds and ticket IDs.
- **Facts not in the inputs.** None found on a line-by-line read. "Monday" comes from the settings.

## Where the run had to choose

- **T-4107** records both that the customer updated the card after the link and that the article showed an old menu. The run sorted it as "link fell short", because step 4 counts a resolution saying the article showed an old screen or menu.
- **T-4130** had no article linked although KB-210 covers the topic, so it was "answered by hand". The template gives that no verdict of its own; it shows only in the topic's counts.
- **Matching search terms by meaning** is a judgement. "card expired" was matched to billing-card-update (two subjects mention an expired card), "upload clients" and "import contacts" to member-import, "waiting list" to class-waitlist, and "gift cards" to no topic. "cancel class" and "opening hours" returned results and were not used.
- **Ways of asking for class-waitlist.** "class" appears in three subjects but only names what the question concerns, so it was not counted on its own. "Class is full" and "full classes" were counted as one way of asking ("full class"), and "waiting list" and "waitlist" as two, as step 8 says.
- **Main words in "card expired".** "card" is in KB-210's title and tags; only "expired" is missing, which is enough for the verdict.

## Unchecked by this run

It covers one invented example in one product, run by the session that wrote the template. The thirteen other acceptance tests (a header named differently, no search log, unclear resolutions, alike tags, requests to write or assign, no tickets in the period, and so on) were not run.
