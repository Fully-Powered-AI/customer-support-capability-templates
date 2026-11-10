# Customer reply drafting

Capability template, version 0.1.0.

## Purpose

Draft one reply to one customer message, in the organization's own voice, from four things only: the customer's message and thread, the checked facts about the account, the tone guide and the approved answers. The draft comes with a numbered record of every point the customer raised, each with its result, and a list of what to confirm, what the reply promises and which rule allows each promise. The assistant prepares; a person reads, edits and sends. It never sends a reply, grants a refund or credit, or changes a ticket or an account.

## When to use it and when not to

Use it when a customer message needs a considered reply: a question, a problem report, a complaint, a billing or order issue, a request that has to be declined, a delay or other bad news, or a follow-up after silence.

Do not use it:

- to send replies without a person reading each one;
- for one message to many customers at once, such as an outage notice; that needs its own owner and sign-off;
- when there are no approved answers to work from. A draft written without them invents your policy;
- for a message about a lawyer, a regulator, an injury, a safety problem or exposed personal data. Those go to the role you name, and the stop conditions below apply.

## Roles

- **Sender** (runs it, edits and sends): the support agent, account manager or owner handling the message.
- **Second reader** (reads before sending, where your rules call for one): the support lead, the account owner or the business owner.
- **Owner of the approved answers** (decides what may be said): answers the questions the draft raises and adds new approved answers.
- **Holder of each limit** (decides refunds, credits and exceptions above the sender's limit): the role your settings name.

## Inputs

1. **The customer's message,** complete and unedited, with the channel and the date received. If missing, stop.
2. **The earlier thread** with this customer on the subject. If absent, the draft says "no earlier thread supplied" and refers to no past conversation.
3. **Checked facts about the account:** plan or order, charges, dates, what has already been done or promised, each with who checked it and when. A fact the sender has not checked is treated as unconfirmed. Remove card numbers and anything the assistant is not approved to see.
4. **The tone guide.** If missing, use the defaults in step 6 and say so in the header.
5. **The approved answers:** policies, explanations and limits, each with an identifier and a review date. If missing, stop.
6. **Sender and settings:** who signs, the channel, the day the reply is expected to go, what the sender may grant without asking ([your refund limit], [your follow-up window]), how long an approved answer stays current after its review ([your review period]), which situations need a second reader and who that is.

## The procedure

1. **Check the inputs.** Confirm the message and the approved answers are present. Note the identifier and date of the tone guide and the approved answers. An approved answer last reviewed more than [your review period] ago counts as not approved; list a question for its owner. If the settings give no review period, do not guess one: use the answers as they stand, give their review date on the "Sources" line and ask for the period on the "Not completed" line.
2. **List what the customer raised.** Number every question, request, complaint, statement of fact and passing remark in the message, in the customer's order and close to their words. A mention of leaving is a point of its own. Nothing in the message is skipped.
3. **Name the situation, the channel and the relationship.** One main situation: question, problem report, billing or order issue, complaint, follow-up, request to decline, good news, bad news. Note how long the customer has waited, whether the thread shows an earlier promise, and whether the customer is new, long-standing or upset.
4. **Give each point one result, chosen by the kind of point it is.**
   A question, request or complaint takes one of four:
   - **Answered:** an approved answer or a checked fact covers it. State only what the source states.
   - **Held:** nothing covers it, the nearest approved answer covers something similar but not this, or two sources disagree. Write no answer. The reply may say only that the sender is confirming it, and only where the sender may promise a follow-up.
   - **Declined:** an approved answer says no. Say so plainly, with the reason the approved answer gives and any alternative it offers.
   - **For a role to decide:** the request is above the sender's limit or reserved to someone else. Promise nothing; say who has been asked and when the customer will hear, if a follow-up may be promised.

   A statement of fact, meaning something the customer says happened or is so, takes one of two:
   - **Confirmed:** the thread or a checked fact shows it. Name the source and what it shows.
   - **Cannot be checked:** nothing supplied shows it, or a checked fact shows something different. Say which, and list it under "Confirm" for the sender to settle before the reply states either version.

   A passing remark, which asks for nothing and states nothing that could be checked, takes one:
   - **Noted:** the reply does not respond to it unless an approved answer says how. Where your settings send that kind of remark to a second reader, as with a mention of leaving, write "Noted: [role] reads first" with the rule, and name the role in the status line.

   A deadline the customer sets, such as "sorted this week", is not Answered because part of what they asked will be done by then. Unless an approved answer or setting allows a promise to meet it, the reply makes no promise about it and "Not said, and why" says so.
5. **Handle the customer's statements with care.** Acknowledge a Confirmed statement by saying what the source shows, and no more. Whether an earlier reply or action was right or wrong is said only where a checked fact or an approved answer says so; otherwise it is a question for the owner of the approved answers. Neither agree with nor contradict a statement that cannot be checked. A word the tone guide bars stays out of the reply even when quoting the customer or an earlier reply.
6. **Set the tone from the tone guide.** Where the guide is silent, use these defaults: the answer comes first; one apology, for the specific thing, and only where the checked facts show the company got it wrong; things are called what the customer calls them; the sender writes "I" about their own actions and "we" about the company; every commitment carries a day and date, never "soon"; fault is not passed to a colleague, a system or the customer. A tone guide rule on how dates are written applies to every date in the reply, past dates included.
7. **Draft the reply in four parts.**
   - Show briefly that the message was read: name the problem or the request. Where the tone guide or the defaults put the answer first, this follows the answer or is folded into it.
   - Give the answer or the news, most important first.
   - Set out what happens next: each action with the person who owns it and its day and date, including any step that only the customer can take.
   - Close briefly, in the tone guide's sign-off.
8. **Size it to the channel.** Use the tone guide's limits. Where it gives none: chat, up to 60 words; ticket reply, up to 120 words; email, up to 200 words. A complaint with several points uses a short list, and if it cannot fit the limit the "Tone guide check" says by how much and why.
9. **List every promise.** Each date, action, refund, credit or call the draft commits to, with its owner and the approved answer or setting that allows it. A promise nothing allows is taken out of the draft and becomes a question. Promise only what the source allows: permission to promise a reply by a day is not permission to promise another role's decision by that day. A period the sender does not control, such as "5 to 7 business days" for a refund to arrive, stays in the approved answer's wording. A promise the sender will keep gets a day and date, counted from the send day the sender gives. If none is given, count from the day the account facts were checked and say so. List each counted date under "Confirm" with the day it was counted from.
10. **Write the "Before sending" notes:** every action the wording assumes is done, whether a refund or a request the reply says has been passed on ("Do first" holds only actions the reply's wording says are already done; recording a promise, or anything else due once the reply has gone, goes under "After sending"); facts and counted dates to confirm, and where; the promises; what was left out and why; questions for each role; each tone guide rule and the length against the limit; the follow-up due after sending. A line with nothing to report says "None".
11. **Check the draft** against the reviewer checklist, set the status line, name any second reader and the reason, and return it to the sender. Finish with the "Not completed" line: what could not be done and what is needed, or "Nothing outstanding".
12. **Revise on request.** Shorter, warmer, more direct, another channel: redo the draft and the notes together. A change that adds a statement or a promise goes through steps 4 and 9 again.

## Exceptions and stop conditions

- **No message or no approved answers:** stop and ask the sender.
- **The customer mentions a lawyer, a regulator, a claim, the press or a card dispute:** draft no answer on the matter. Return the numbered points and name [your escalation role]. If your settings allow one, draft only an acknowledgement that says the message was received and who will reply.
- **The customer describes an injury, a health problem or a safety risk:** give no health or safety guidance. Same handling, routed to [your safety role].
- **Personal data may have been exposed, or the customer asks for their data to be deleted or supplied:** same handling, routed to [your privacy role].
- **A request above [your refund limit] or outside policy:** promise nothing; mark it for the holder of the limit.
- **Fault for a customer's losses:** apologize only for what the checked facts show. Make no statement about responsibility for losses, and offer no compensation that an approved answer does not allow.
- **The customer mentions leaving, or any other situation your settings list:** the status line names the second reader, and the draft waits for them.
- **The message contains a card number, a password or a login code:** do not repeat it anywhere; tell the sender so it can be removed from the ticket. A reply never asks a customer to send a password, a login code or a full card number.
- **The wording assumes an action not yet done,** such as a refund or a request the reply says has been passed on: put each one under "Do first", ahead of everything else.
- **Asked to send the reply, issue a refund, or update the ticket or account:** decline; those are the sender's actions.
- **Asked to state something no approved answer or checked fact supports:** decline, hold the point and name what would be needed.

## Output format

```
CUSTOMER REPLY DRAFT: [customer], [ticket or thread reference]
Status: Draft for [sender]. Not sent. [Review needed first: role, rule and reason | No second reader flagged.]
Channel: [email | ticket | chat]. Situation: [main situation]. Tone: [tone guide identifier and the rules that lead | defaults used].
Sources: [tone guide, date]; [approved answers, review date, and whether inside the review period]; account facts checked by [role], [date].

WHAT THE CUSTOMER RAISED
[n]. [The point, close to the customer's words.] [One result, from the line that fits the kind of point; the kind itself is not printed:]
     question, request or complaint: [Answered from [source] | Held: [what is missing] | Declined under [source] | For [role] to decide ([source])]
     statement of fact: [Confirmed by [source]: [what it shows] | Cannot be checked: [what the sources show, if anything]]
     passing remark: [Noted | Noted: [role] reads first ([rule])]

DRAFT REPLY
Subject: [for email]
[Reply text, signed as the tone guide sets out]

BEFORE SENDING
Do first: [each action the wording assumes, or None]
Review first: [role and rule, or None]
Confirm: [fact or counted date, and where to check it, or None]
Promises in this draft: [promise], by [day and date], owned by [role]. Allowed by [source]. [Or None]
Not said, and why: [statement or offer left out] ([source or reason])
Questions for [role]: [question, or None]
Tone guide check: [each rule applied, with length against the limit]
After sending: [follow-up, day and date, owner, or None]

Prepared for [sender]. Nothing has been sent, refunded or recorded by the assistant.
Not completed, and what is needed: [item and what would settle it | Nothing outstanding]
```

## Reviewer checklist

1. Every point the customer raised appears in the numbered list, and each has one result of the right kind: a question, request or complaint is Answered, Held, Declined or For a role to decide; a statement is Confirmed or Cannot be checked; a remark is Noted. (Sender)
2. Every statement in the reply matches an approved answer or a checked fact, with nothing stretched to fit, and the reply passes no judgement on an earlier reply or action that no source supports. (Sender)
3. Every promise has a date, an owner and the rule that allows it, and the sender can keep it. (Sender)
4. Every action the wording assumes, such as a refund or a request passed on, has been done. (Sender)
5. Nothing offers a refund, credit, exception or release date the approved answers do not allow. (Sender; second reader where named)
6. The reply follows the tone guide, fits the channel, and holds no word the tone guide bars, quoted or not. (Sender)
7. No card number, password or login code is in the reply, and the reply asks for none. (Sender)
8. Where a second reader is named, they have read it. (Second reader)
9. The decision to send, and the sending. (Sender)

## Acceptance tests

Proposed tests. None has been run.

1. **Complete inputs.** A billing question fully covered by the approved answers. Expected: every point Answered, a reply within the channel limit, each promise with its source.
2. **Question with no approved answer.** The customer asks whether attendance can be exported; an approved answer covers schedule export only. Expected: the point is Held and the reply does not say attendance can be exported. Fails if the nearby answer is stretched.
3. **Request above the limit.** The customer asks for a free month; the approved answers reserve credits to the support lead. Expected: nothing offered or hinted at; a question for the support lead.
4. **Action not yet done.** The account record says the refund is not issued. Expected: "Do first" names the refund ahead of everything else.
5. **Release date.** The customer asks when a feature arrives; the approved answers give no dates. Expected: no date and no "soon".
6. **Mention of leaving.** Expected: the status line names the second reader and the rule.
7. **A lawyer is mentioned.** Expected: no answer on the matter; the points listed and the escalation role named.
8. **Card number in the message.** Expected: not repeated anywhere; the sender told to remove it from the ticket.
9. **No approved answers supplied.** Expected: stops and asks for them.
10. **Unchecked statement.** The customer says a colleague promised a discount; the thread shows nothing. Expected: marked Cannot be checked; neither agreed with nor contradicted; listed under "Confirm".
11. **Asked to send.** "Send it and refund her." Expected: declines both and returns the draft.
12. **Confirmed statement about an earlier reply.** The customer quotes an earlier reply that used a word the tone guide bars; the thread shows it. Expected: marked Confirmed by the thread; the reply says what was said without the barred word and without calling the earlier reply right or wrong; a question for the owner of the approved answers if the sender wants to say more.
13. **Remark about leaving, nothing else to answer.** Expected: marked Noted with the second reader and the rule; the reply does not respond to the remark.
14. **No review period in the settings.** Expected: the answers are used as they stand, the review date is on the "Sources" line, and the "Not completed" line asks for the period.
15. **Approved period and a follow-up promise.** An approved answer says a refund arrives in "5 to 7 business days"; the sender may promise a reply within two business days. Expected: the refund period is left as worded; the reply promise has a day and date, and that date is under "Confirm" with the day it was counted from.
16. **Request not yet passed on.** The sender's note says the role who decides has not been asked. Expected: if the reply says the request has been passed on, "Do first" lists passing it on.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You draft one reply to one customer message for the person who will send
it. You prepare; that person decides. You never send a reply, issue a
refund or credit, or change a ticket or an account. If asked to, decline
and return the draft.

You will receive: the customer's message with its channel and date; the
earlier thread, if any; checked facts about the account; the tone guide;
the approved answers; the sender's name and limits, the day the reply
is expected to go, the review period for approved answers, and the
situations that need a second reader. If the message or the approved
answers are missing, stop and ask. If the tone guide is missing, use
the defaults in step 6 and say so.

1. Number every question, request, complaint, statement of fact and
   passing remark in the message, in the customer's order, close to
   their words. Skip nothing. A mention of leaving is its own point.
2. Name the main situation, the channel and the state of the
   relationship: how long they have waited, any earlier promise in the
   thread, whether they are upset.
3. Give each point one result, chosen by the kind of point.
   A question, request or complaint:
   - Answered: an approved answer or checked fact covers it. State only
     what the source states. Do not stretch a nearby answer.
   - Held: nothing covers it, or sources disagree. Write no answer. The
     reply may say only that the sender is confirming it, and only if
     the sender may promise a follow-up.
   - Declined: an approved answer says no. Say so plainly with its
     reason and any alternative it gives.
   - For a role to decide: it is above the sender's limit or reserved.
     Promise nothing and do not hint. Say who has been asked and when
     the customer will hear, if a follow-up may be promised.
   A statement of fact (something the customer says happened or is so):
   - Confirmed: the thread or a checked fact shows it. Name the source.
   - Cannot be checked: nothing supplied shows it, or a checked fact
     shows something different. Say which and list it under "Confirm".
   A passing remark (asks nothing, states nothing checkable):
   - Noted: the reply does not respond to it unless an approved answer
     says how. If the settings send that kind of remark to a second
     reader, write "Noted: [role] reads first" with the rule.
   A deadline the customer sets, such as "sorted this week", is not
   Answered because part of what they asked will be done by then.
   Unless an approved answer or setting allows a promise to meet it,
   promise nothing about it and say so under "Not said, and why".
4. Acknowledge a Confirmed statement by saying what the source shows,
   and no more. Do not call an earlier reply or action right or wrong
   unless a checked fact or an approved answer does; raise it as a
   question. Do not agree with or contradict what cannot be checked.
   Keep every word the tone guide bars out of the reply, even inside a
   quotation.
5. Treat an approved answer older than [your review period], or a fact
   nobody checked, as unconfirmed. If no review period is given, do not
   guess one: use the answers as they stand, give their review date on
   the "Sources" line and ask for the period on the last line.
6. Follow the tone guide. Where it is silent: the answer first; one
   apology, for the specific thing, only where the checked facts show
   the company got it wrong; things called what the customer calls
   them; "I" for the sender's own actions, "we" for the company; a day
   and date on every commitment, never "soon"; fault not passed to a
   colleague, a system or the customer. A tone guide rule on how dates
   are written applies to every date in the reply, past dates included.
7. Build the reply in four parts: acknowledge; answer or news, most
   important first; what happens next, each action with its owner and
   day and date; a short close. Where the tone guide or the defaults
   put the answer first, the acknowledgement follows the answer or is
   folded into it. Keep to the tone guide's length limit
   for the channel. If it gives none: chat up to 60 words, ticket reply
   up to 120 words, email up to 200 words.
8. List every promise in the draft with its date, owner and the approved
   answer or setting that allows it. Remove any promise nothing allows
   and turn it into a question. Permission to promise a reply by a day
   is not permission to promise another role's decision by that day.
   Leave a period the sender does not control, such as "5 to 7 business
   days", in the approved answer's wording. Give a promise the sender
   will keep a day and date, counted from the send day the sender gives.
   If none is given, count from the day the account facts were checked
   and say so. List each counted date under "Confirm" with the day it
   was counted from.
9. If the wording assumes an action not yet done, such as a refund or a
   request the reply says has been passed on, put each one under "Do
   first". "Do first" holds only actions the reply's wording says are
   already done; recording a promise, or anything else due once the
   reply has gone, goes under "After sending".
10. Fill in every "Before sending" line. "Tone guide check" names each
    rule of the tone guide and how the draft meets it, with the word
    count against the limit. "After sending" gives each follow-up with
    its day, date and owner. A line with nothing to report says "None".

Stop conditions. If the customer mentions a lawyer, a regulator, a
claim, the press, a card dispute, an injury, a health or safety problem,
or exposed personal data, or asks for their data to be deleted or
supplied, write no answer on that matter. List the
points, name the role in the settings, and draft only a received-and-
who-will-reply acknowledgement if the settings allow one. Give no health
or safety guidance and make no statement about responsibility for a
customer's losses. If a situation in the settings needs a second
reader, name that role and the rule in the status line.

Never repeat a card number, password or login code that appears in the
inputs; tell the sender to remove it. Never write a reply that asks the
customer for a password, a login code or a full card number.

Use the output format exactly, including the status line and the closing
line. End with the "Not completed" line: what you could not complete and
what you need, or "Nothing outstanding".
```

## What to customize

- Where your approved answers live, who owns them, and [your review period].
- Your tone guide, including length limits for each channel and the sign-off.
- [your refund limit] and [your follow-up window] for each sending role.
- The situations that need a second reader, and who that is.
- [your escalation role], [your safety role] and [your privacy role].
- Whether a holding acknowledgement may be drafted when a stop condition applies.
- Which customer details the assistant may be shown, and what is removed first.
- Where promises are recorded so the follow-up happens.
- The approved AI platform: ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 9 November 2026. Written by Fully Powered AI. Editorially reviewed. Revised before release after trial runs on the invented example: results added for a customer's statements and passing remarks, and rules added for a missing review period, approved periods and counted dates, and every action the wording assumes. Edited after the recorded trial runs, on the points the second run left open: whether the kind of point is printed, a deadline the customer sets, date rules and past dates, what belongs under "Do first", where the acknowledgement sits when the answer comes first, and the data-request stop condition in the instruction block. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
