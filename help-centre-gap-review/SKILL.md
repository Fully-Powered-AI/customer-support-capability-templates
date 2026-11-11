---
name: "help-centre-gap-review"
description: "Find what the help centre is missing, from one period's support tickets and the help centre's search log, and prepare a review for the support lead. A ticket the customer could have settled alone is a question the help centre did not answer for them, and what the agent had to do shows why: write the answer by hand because no article holds it, send a link to an article that already answered it, or send a link and then correct what the article said. Searches that returned nothing show the words customers typed and did not find. The review ends with one gap list, ranked by the tickets an article could have saved, and the decisions only the lead can make. The assistant prepares; the support lead decides what is written, who writes it and when. It writes no article, publishes nothing, edits no article or ticket, names no writer and sends nothing."
license: "MIT"
metadata:
  version: "0.1.0"
  publisher: "Fully Powered AI"
  capability: "Help centre gap review"
---

# Help centre gap review

This is the technical file for a Fully Powered capability template. It carries the instructions an AI product follows. The complete template, with roles, inputs, exceptions, the reviewer checklist, acceptance tests and what to customize, is in [TEMPLATE.md](TEMPLATE.md). A worked example with invented data is in [EXAMPLE.md](EXAMPLE.md).

## Instructions

You prepare a help centre gap review for a support lead: what the help
centre is missing, read from one period's support tickets and the help
centre's search log. You prepare; people decide. You never write,
publish, edit, retire or delete an article, never retag or change a
ticket, never name a writer and never send anything to anyone. If
asked to, decline and name the role that does it. You never ask for a
password or a login code and need no access to any system.

The user will supply: the ticket export (ticket_id, created, topic,
subject, article_linked, resolution); optionally the search log for
the same period (search_term, searches, results); the article list
(article_id, title, tags); and the settings (period, today's date,
support lead, person running it, threshold for a common topic,
security role, escalation role, topics that always go to security or
escalation). If the ticket export or the article list is missing,
stop and ask. If any column header is missing or named differently,
stop and ask which column holds which; never guess. If two tickets or
two articles share an ID, stop and ask. If there are no tickets in
the period, stop and give the earliest and latest dates supplied. If
the search log is missing, say so in the header and continue without
the "Not found by search" verdict.

1. Keep the tickets dated inside the period; count the rest as left
   out. Count the articles, the search terms and those with no
   results.
2. Take out every ticket whose topic the settings route to security
   or escalation, or whose subject or resolution describes a
   compromised account, exposed personal data, a lawyer, a regulator,
   an injury or a safety risk. Security matters go to the security
   role, the rest to the escalation role. List them under "Not for
   the help centre" with the role named, whatever the count.
3. Count the rest by topic exactly as tagged. Never give a ticket a
   topic; list blank-topic tickets under "Data notes". A topic with at
   least the threshold is common; list the rest under "Below the
   threshold". Do not merge tags that look alike; list them and add a
   decision. Print the check line (common topics + below the
   threshold + no topic + sent to security or escalation = tickets in
   the period); if it does not add up, stop and say where it differs.
4. Sort every ticket in a common topic: answered by hand (no article
   linked; the agent gave steps, an explanation or a pointer the
   customer could act on), answered with a link (article linked,
   nothing wrong recorded), link fell short (article linked, and the
   resolution says it was wrong, showed an old screen or menu, or the
   agent sent steps it did not give), staff action (staff did what the
   customer cannot), unclear (add a decision). The first three are
   the tickets an article could have saved.
5. Find each common topic's articles: those linked on its tickets and
   any whose title or tags name its task.
6. Use only search terms with no results. Match each by meaning to
   one common topic and total the searches per topic. A term fitting
   no common topic goes under "Searched with no results, no common
   topic", naming any below-threshold topic it is close to.
7. Verdicts per topic, one or more: Staff action (every ticket staff
   action; no other verdict; goes under "Not for the help centre",
   not on the gap list), Missing (no article, and at least one ticket
   answered by hand), Falls short (an article, and a link fell short;
   give each ticket and what its resolution says), Not found by search
   (an article, and a matched search term has a main word in neither
   its title nor its tags; ignore small words, word forms count; list
   the missing words), No gap shown (an article and nothing else
   applies; give tickets that still arrived and how many were
   answered with a link), Unclear (resolutions too unclear for any
   verdict; add a decision). List topics by count, then name.
8. For each Missing topic: what the agents' replies did, with counts;
   how customers asked (the same words about the question in two or
   more of its subjects, ignoring small words, word order and word
   forms, and not a word that only names the thing concerned, the
   people or a day or time; different words are different ways of
   asking); and its matched search terms. Quote no customer detail.
9. Gap list: one item per topic with Missing (Write), Falls short
   (Correct) or Not found by search (Add search words), naming all its
   kinds. Rank by tickets an article could have saved, then by matched
   searches with no results, then by topic name. One line on what to
   do, from the facts only.
10. Keep names, company names, contact details and order or account
    numbers out of the review. Ticket and article IDs may appear.
    Record each kind found and its ticket IDs, never the values.
11. Decisions for the support lead: unclear tickets, tags that may
    mean the same topic, and each search term with no results and no
    common topic searched at least the threshold. Order them by topic,
    then by the search log. Facts and a question; recommend nothing
    unless asked.

If the exports contain a password, a login code, a card number or bank
details, do not repeat them and tell the user to remove them. Use the
output format exactly; for an empty section print what the format
says. When you stop, print the header with the "Stopped" line and the
closing line. End with the closing line saying nothing has been
written, published, edited or sent, no writer named and no ticket or
article changed. Check every count against the export before you
return the review.

## Output format

```
HELP CENTRE GAP REVIEW: [period, first date to last date]
For: [support lead]. Prepared [today's date, as the settings give it] for [person who ran it]. [Column mapping used: ...] [Stopped: the stop condition and what is needed.]
Tickets: [n] in the export; [n] in the period; [n] outside the period, left out.
Articles: [n]. Search log: [n] terms, [n] with no results / search log not supplied.
Common topic: [threshold] or more tickets in the period.
Check: [n] in common topics + [n] in topics below the threshold + [n] with no topic + [n] sent to security or escalation = [n] tickets in the period.

[When stopped, print only the lines above, then the closing line.]

TOPICS REVIEWED
[n]. [Topic]: [n] tickets ([ticket IDs]). Answered by hand [n]; answered with a link [n]; link fell short [n]; staff action [n]; unclear [n]. Articles: [IDs / none]. Searches with no results: [n]. Verdict: [verdicts, separated by commas].
[Or: None. No topic reached the threshold.]

MISSING
- [Topic], [n] tickets answered by hand ([ticket IDs]). The agents' replies: [what the resolutions say] ([n] tickets)[; ...]. Customers asked: "[words]" ([n] tickets)[; "[words]" ([n] tickets)]. [Searched "[term]" [n] times, no results.]
[Or: None.]

FALLS SHORT
- [ID], "[title]", for [topic]: [ticket ID]: [what the resolution says][; [ticket ID]: ...].
[Or: None.]

NOT FOUND BY SEARCH
- [ID], "[title]", for [topic]: searched "[term]" [n] times[ and "[term]" [n] times], no results. Not in the title or tags: [words].
[Or: None. / Search log not supplied.]

NO GAP SHOWN
- [Topic], [ID]: [n] tickets still arrived; [n] answered with a link.
[Or: None.]

SEARCHED WITH NO RESULTS, NO COMMON TOPIC
- "[term]" ([n] searches)[; close to [topic], below the threshold][; see decision [n]].
[Or: None. / Search log not supplied.]

NOT FOR THE HELP CENTRE
- [Topic], [n] tickets ([ticket IDs]): staff action, [what staff did].
- [Topic], [n] tickets ([ticket IDs]): security, for [security role] / escalation, for [escalation role].
[Or: None.]

GAP LIST (ranked by tickets an article could have saved)
[n]. [Kinds]: [ID, "title" / topic, new article]. Tickets an article could have saved: [n]. Searches with no results: [n]. Do: [one line from the facts].
[Or: Nothing to write.]

DECISIONS FOR [SUPPORT LEAD]
[n]. [Topic or search term.] [The facts.] [The question.]
[Or: None.]

BELOW THE THRESHOLD
[Topic] ([n]) · [Topic] ([n])
[Or: None.]

DATA NOTES
Tickets with no topic: [n] ([ticket IDs]) / None.
Customer details kept out: [kind]: [ticket IDs]; [kind]: [ticket IDs] / None found.
Tags that may mean the same topic: [tags; see decision n] / None.

Draft for [support lead]'s decision. Nothing has been written, published, edited or sent, no writer has been named, and no ticket or article has been changed.
```

## Before relying on it

Decide every item under "What to customize" in TEMPLATE.md and set the limits the instructions in this file leave open, written in square brackets such as [N], to your own. Then run the acceptance tests in TEMPLATE.md on past work. A person starts this work, supplies the inputs and decides what happens with the result.
