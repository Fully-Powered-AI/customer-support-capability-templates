# Help centre gap review

Capability template, version 0.1.0.

## Purpose

Find what the help centre is missing, from one period's support tickets and the help centre's search log, and prepare a review for the support lead. A ticket the customer could have settled alone is a question the help centre did not answer for them, and what the agent had to do shows why: write the answer by hand because no article holds it, send a link to an article that already answered it, or send a link and then correct what the article said. Searches that returned nothing show the words customers typed and did not find. The review ends with one gap list, ranked by the tickets an article could have saved, and the decisions only the lead can make. The assistant prepares; the support lead decides what is written, who writes it and when. It writes no article, publishes nothing, edits no article or ticket, names no writer and sends nothing.

## When to use it and when not to

Use it once a period, after the period's tickets are tagged: monthly for most teams, quarterly for a small one. Run it too when ticket volume rises and nobody can say which questions the help centre leaves unanswered.

Do not use it:

- to write or rewrite an article. Each item on the gap list is written on its own; Help article from a resolved issue drafts one article from one solved ticket;
- to tag or retag tickets. Topics come from your team's tagging and are counted as supplied;
- to judge an agent's replies or how a ticket was handled;
- to find what customers want changed in the product. Customer feedback themes does that;
- for security incidents, exposed personal data, or anything touching a lawyer, a regulator, an injury or a safety risk. Those tickets are counted and routed to the role you name, never turned into help-centre work.

## Roles

- **Runs it:** the support lead, or a support specialist preparing it for the lead.
- **Decides what is written, who writes it and by when, and settles every decision:** the support lead.
- **Writes or corrects each article:** whoever the support lead names after reading the review.
- **Receives security and escalation tickets:** [your security role] and [your escalation role].

## Inputs

1. **The ticket export for the period,** with these column headers: `ticket_id`, `created`, `topic`, `subject`, `article_linked`, `resolution`. `created` is a date (YYYY-MM-DD); `topic` is the tag your team gave the ticket; `subject` is the customer's subject line or first line; `article_linked` is the ID of the article the agent sent, or blank or "-" for none; `resolution` is a short line on what resolved the ticket. If there is no ticket export, stop and ask for one.
2. **The help centre's search log for the same period,** with these column headers: `search_term`, `searches`, `results`, where `results` is the number of articles the search returned. Most help-centre tools export one. If none is supplied, the header says "search log not supplied", the review rests on the tickets alone and the verdict "Not found by search" is not given.
3. **The article list,** with these column headers: `article_id`, `title`, `tags`. Tags are separated by semicolons. If there is no article list, stop and ask for one: nothing can be called missing without it.
4. **Settings:** the period (first and last date); today's date; the support lead; the person running it; [your threshold], the number of tickets in the period that makes a topic common; [your security role] and [your escalation role]; and any topics that always go to security or escalation.

For every export: if a column header is missing or named differently, stop and ask which column holds which. Never guess a mapping. Once the person names the mapping, use it and say so in the header.

The assistant works from files the person exports. It needs no connection to the helpdesk or the help centre and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Check each export's headers against the defaults. Count the ticket export's rows. Keep the rows whose `created` date falls inside the period and count the rest as left out. Count the articles, the search terms and the search terms with no results. If two tickets or two articles share an ID, stop and ask which is which.
2. **Take out the tickets that are not help-centre work.** A ticket goes under "Not for the help centre" with the role named, whatever its topic's count, and is counted nowhere else, when its topic is one the settings send to security or escalation, or its subject or resolution describes a compromised account, exposed personal data, a lawyer, a regulator, an injury or a safety risk. Security matters go to [your security role]; the rest to [your escalation role].
3. **Count the rest by topic.** A ticket with a blank topic is listed under "Data notes" by its ID; never give it a topic. A topic with at least [your threshold] tickets in the period is common; the others are listed under "Below the threshold" with their counts. Tags that look like the same topic, such as "waitlist" and "waiting-list", are not merged: list them under "Data notes" and add a decision. Print the check line: tickets in common topics, plus tickets in topics below the threshold, plus tickets with no topic, plus tickets sent to security or escalation, equals tickets in the period. If it does not add up, stop and say where the difference is.
4. **Sort every ticket in a common topic by what it took,** from its `article_linked` and `resolution`:
   - **Answered by hand:** no article was linked, and the agent gave the customer what they needed to do it themselves: steps, an explanation, or a pointer to a setting, switch, field or page.
   - **Answered with a link:** an article was linked and the resolution records nothing wrong with it.
   - **Link fell short:** an article was linked and the resolution says the article was wrong, showed an old screen or menu, or that the agent had to send steps the article did not give.
   - **Staff action:** a member of staff did something the customer cannot do, such as issuing a refund or changing a setting in an admin tool.
   - **Unclear:** anything else. Every topic with an unclear ticket gets a decision.
   The first three are the tickets an article could have saved.
5. **Find each common topic's articles:** the articles agents linked on its tickets, and any article whose title or tags name the topic's task.
6. **Read the search log.** Use only the terms with no results; a term that returned results is not used. Match each, by meaning, to the one common topic it is about, and give each common topic the total of its matched searches. A term that fits no common topic goes under "Searched with no results, no common topic", naming any topic below the threshold it is close to.
7. **Give each common topic its verdicts,** one or more, each with its facts:
   - **Staff action:** every one of its tickets was staff action. The topic gets no other verdict and goes under "Not for the help centre", not on the gap list. When only some were, review the topic as usual; its counts show the rest.
   - **Missing:** no article was found in step 5, and at least one ticket was answered by hand.
   - **Falls short:** an article was found, and at least one ticket's link fell short. Give each such ticket's ID and what its resolution says.
   - **Not found by search:** an article was found, and a search term with no results matched to the topic has a main word that is in neither the article's title nor its tags. Small words are ignored, and word forms count as the same word, such as card and cards. List the missing words.
   - **No gap shown:** an article was found and none of the above applies. Give the tickets that still arrived and how many were answered with a link. Not on the gap list.
   - **Unclear:** none of the above can be given because the topic's resolutions are unclear. It gets a decision and is not on the gap list.
   List the topics by ticket count, highest first, then by topic name.
8. **For each missing topic, set down what an article would need,** from the facts only: what the agents' replies did, from the resolutions, with the count for each; and how customers asked. A way of asking is the same word or words about the question in the subjects of two or more of the topic's tickets, ignoring small words, word order and word forms. A word that only names the thing the question concerns, the people involved, or a day or a time is not a way of asking on its own. Different words, such as "waiting list" and "waitlist", are different ways of asking. Add the search terms with no results matched to the topic. Quote a subject's words only after taking out any customer detail.
9. **Build the gap list.** One item for each common topic with Missing, Falls short or Not found by search; a topic with more than one is one item naming them all. The kinds are Write (Missing), Correct (Falls short) and Add search words (Not found by search). Rank by the tickets an article could have saved, highest first, then by the searches with no results matched to the topic, then by topic name. Each item gives the article's ID and title, or the topic and "new article"; the tickets an article could have saved; the searches with no results; and one line on what to do, from the facts only: for Write, what the agents' replies told customers; for Correct, what the resolutions say was wrong and the steps the agent sent instead; for Add search words, the missing words.
10. **Keep customer details out.** Names, company names, email addresses, phone numbers, addresses, and order or account numbers in the subjects never appear in the review. Ticket IDs and article IDs may. Under "Data notes", record each kind of detail found and the ticket IDs where it appeared, never the values.
11. **Write the decisions** for the support lead: one for each topic with an unclear ticket, each set of tags that may mean the same topic, and each search term with no results and no common topic that was searched at least [your threshold] times. Give the facts and the question. Order them by the order of the topics, then the search terms in the order of the search log. Recommend nothing unless the lead asks.
12. **Return the draft** to the person who ran it, for the support lead's decision, with the closing line. The lead confirms the gap list and names who writes each item; nothing is written from this review until then.

## Exceptions and stop conditions

- **No ticket export or no article list:** stop and ask for it.
- **A column header missing or named differently** in any export: stop and ask which column holds which.
- **Two tickets or two articles with the same ID:** stop and ask.
- **No tickets inside the period:** stop and say so; give the dates of the earliest and latest ticket supplied.
- **The check line does not add up:** stop and say where the difference is.
- **Whenever a run stops,** print the header with the "Stopped" line and the closing line, as the output format shows.
- **A ticket about a compromised account, exposed personal data, a lawyer, a regulator, an injury or a safety risk:** counted under "Not for the help centre" with the role named; never on the gap list, whatever the count.
- **The exports contain a password, a login code, a card number or bank details:** do not repeat them; tell the person to remove them from the source.
- **Asked to write, publish, edit, retire or delete an article, retag a ticket, name a writer or send anything to anyone:** decline and name the role that does it. For drafting one article, point to Help article from a resolved issue.

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

## Reviewer checklist

1. The check line adds up, and every ticket in the period is counted exactly once. (Person who ran it)
2. Every topic's count and ticket IDs match the export, and no ticket was given a topic it did not have. (Person who ran it)
3. Every ticket's sort (by hand, with a link, link fell short, staff action, unclear) follows from its `article_linked` and `resolution`, and the five counts add up to the topic's tickets. (Person who ran it)
4. Every "Falls short" line quotes what the resolutions actually say. (Support lead)
5. Every "Not found by search" line names a search term that really returned no results, and the missing words are truly absent from the article's title and tags. (Support lead)
6. Every "Missing" topic really has no article, and its ways of asking appear in at least two of its subjects. (Support lead)
7. The gap list follows the ranking rule, and every "Do" line comes from the facts. (Support lead)
8. No customer name, company name or contact detail appears anywhere in the review. (Person who ran it)
9. Security and escalation tickets are routed to the named roles and appear nowhere on the gap list. (Support lead)
10. The decisions are settled, the gap list confirmed and a writer named before anyone starts on an article. (Support lead)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary month.** Complete exports, three common topics: one answered by hand with no article, one answered with a link every time, one whose article a resolution calls out of date. Expected: the check line adds up; verdicts Missing, No gap shown and Falls short; the gap list ranked by tickets an article could have saved.
2. **Header named differently.** The ticket export says "Tag" instead of "topic". Expected: stops and asks which column holds which; no review drafted.
3. **No article list.** Expected: stops and asks for it.
4. **No search log.** Expected: the header says "search log not supplied"; no "Not found by search" verdict; the review continues from the tickets.
5. **Staff-action topic.** Four refund tickets, all issued by support. Expected: verdict Staff action; listed under "Not for the help centre"; not on the gap list.
6. **Article linked, then corrected.** Two tickets link the same article and the agent then sent different steps. Expected: Falls short with both ticket IDs; a Correct item.
7. **Search words missing from an article.** "upload clients" was searched six times with no results; the article is titled "Import members". Expected: Not found by search, listing "upload" and "clients".
8. **Searched often, never asked.** A term with no results, searched more often than the threshold, matches no ticket topic. Expected: listed under "Searched with no results, no common topic" with a decision; not on the gap list.
9. **Compromised account.** One ticket says someone else logged in. Expected: counted under "Not for the help centre" for the security role; on no list; no article proposed.
10. **Customer details in subjects.** Subjects carry a company name and a first name. Expected: neither appears in the review; both kinds recorded under "Data notes" with ticket IDs.
11. **Two tags for one topic.** "waitlist" and "waiting-list" each have tickets. Expected: not merged; listed under "Data notes" with a decision.
12. **Unclear resolutions.** A common topic whose resolutions say only "closed". Expected: verdict Unclear; a decision; not on the gap list.
13. **Asked to write the articles and assign them.** Expected: declines; names the support lead for naming writers and points to Help article from a resolved issue for drafting one article.
14. **No tickets in the period.** Expected: stops and gives the dates of the earliest and latest tickets supplied.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
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
```

## What to customize

- [your threshold]: how many tickets in the period make a topic common. A small team might use three a month; a large one fifty.
- The column headers of your ticket export, search log and article list, if they differ from the defaults.
- What your team writes in the resolution line. The sort in step 4 reads it, so agree a habit: say when an article was linked and worked, when it was wrong or out of date, and when staff did the work.
- [your security role] and [your escalation role], and the topics that always go to them.
- Who confirms the gap list and names writers when the support lead is away.
- The approved AI platform: ChatGPT, Claude, Copilot or Gemini, and which ticket fields it may be shown.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI as its own method. Editorially reviewed. Tried on its invented example in Claude on 10 November 2026, by the session that wrote this version, so the run was not blind; the record is published with it. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
