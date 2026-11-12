# Help article from a resolved issue: an invented example

*Illustrative example with invented data.* The company, the customer, the staff, the tickets, the articles and every document below are invented. Company H is an invented 20-person company that sells time-tracking and invoicing software to small agencies; Client W is an invented customer. First come the inputs the support agent supplied, in full, then the draft the workflow template returned.

## The inputs

### 1. The resolution record

```
TICKET 2318
Opened: Wednesday 4 November 2026, 10:14. Resolved: Thursday 5 November
2026, 15:40.
Customer: Ana, office manager, Client W. Account AW-4471.

Message 1. Customer, Wednesday 4 November, 10:14
Hi, I changed our logo under Settings > Company yesterday, but every
invoice I make still has our old logo on it. I sent INV-0932 to
Client P this morning and it went out with the old one. Screenshot
attached. Can you help?
Ana, Client W
ana@clientw.example, 555-0142
Attachment: clientw-inv-0932.png

Message 2. Support (Sam), Wednesday 4 November, 11:02
Hi Ana, thanks for the screenshot. Each invoice template keeps its own
copy of the logo, so changing it under Settings > Company does not
change your templates. Go to Settings > Invoice templates, open the
template you use, and under Logo choose Use company logo, then Save.
Do this for each template you use. Invoices made before the change keep
the old logo; to update one, open it and choose More > Regenerate PDF.
Sam

Message 3. Customer, Wednesday 4 November, 14:30
Done for both of our templates, and a new invoice shows the new logo.
But I regenerated INV-0932 and it still shows the old one.

Internal note. Support (Sam), Wednesday 4 November, 14:52
Cleared the PDF cache for AW-4471 from the admin console. Only staff
can do this. Not sure whether Regenerate PDF should have worked on its
own. Asked Kai.

Message 4. Support (Sam), Wednesday 4 November, 14:55
I've made a change on our side. Could you regenerate INV-0932 once
more?

Message 5. Customer, Thursday 5 November, 09:20
Regenerated again and the new logo is there now. Thanks.

Internal note. Support (Sam), Thursday 5 November, 15:38
Kai says engineering plans to make templates follow the company logo
automatically in a later release. No date. Do not tell customers.
Kai has not answered on the cache yet. Only account admins can see
Settings > Invoice templates.

Resolution. Thursday 5 November, 15:40
Fix: Use company logo on each invoice template; regenerate older
invoices. PDF cache cleared by support for this account.
```

### 2. The note from the person running it

```
From Sam, support agent, Monday 9 November 2026:
Third ticket on this in two weeks (2290, 2297, 2318). Worth an article.
Maybe it belongs in KB-104?
```

### 3. The list of existing articles (exported)

```
article_id,title,category,tags,last_updated,owner
KB-104,Add or change your company logo,Account settings,logo; branding; company details,2026-03-12,Support lead
KB-131,Create and edit invoice templates,Invoicing,invoice template; layout; invoice PDF,2026-06-02,Support lead
KB-150,Resend an invoice to a client,Invoicing,resend; email invoice,2026-08-19,Support lead
```

### 4. The help-centre style guide

```
HC-2, dated 1 September 2026
1. Address the reader as "you". Sentence-case headings.
2. Menu paths in bold, with ">" between levels: **Settings > Company**.
3. Never "simply", "just" or "easy".
4. Body under 300 words.
5. End every article, above Related articles, with: "Need more help?
   Contact support from **Help > Contact us**."
6. Refer to other articles by their title, with the article ID in
   brackets.
```

### 5. Settings

```
Knowledge-base owner: Ren, support lead.
Subject expert, invoicing: Kai, product specialist. Reviews any article
  that explains why something happens, or that relies on a step the
  customer did not confirm.
Audiences: All users; Account admins.
Categories: Account settings; Invoicing; Time tracking; Billing and
  plans.
Review interval: six months from today, moved to the next working day
  if it falls on a weekend.
Today: Monday 9 November 2026.
Extra customer details: none.
Security role: Ren, support lead. Escalation role: operations director.
Approved product facts: none supplied.
```

## The output

```
HELP ARTICLE DRAFT: Invoices still show the old logo after you change it
Status: Draft for Ren, support lead. Not published. Ready for review
Source: Ticket 2318, resolved Thursday 5 November 2026. Fix confirmed by
the customer, Thursday 5 November 2026.
How often: third ticket in two weeks (Sam's note: 2290, 2297, 2318).
Style: HC-2, 1 September 2026. Body: 179 words against a limit of 300.
Recommendation: New article

ARTICLE
Title: Invoices still show the old logo after you change it
Type: Troubleshooting
Category: Invoicing
Audience: Account admins
Tags: logo; invoice template; invoice PDF; branding
Search terms: invoice still has old logo; changed logo; old logo on
invoice; logo not updating on invoices. Exact error text: none in the
record

# Invoices still show the old logo after you change it

Changed your company logo, but your invoices still carry the old one?
The fix is in your invoice templates, and you need to be an account
admin to make it.

## What you see

- You changed your logo under **Settings > Company**.
- New invoices still show your old logo.

## Why it happens

Each invoice template keeps its own copy of your logo. Changing the
logo under **Settings > Company** does not change your templates.

## How to fix it

1. Go to **Settings > Invoice templates**. Only account admins see
   this page.
2. Open the template you use.
3. Under **Logo**, choose **Use company logo**.
4. Select **Save**.
5. Repeat for each template you use.

New invoices made from that template now show your new logo.

## Invoices made before the change

Invoices made before you changed the template keep the old logo. To
update one, open it and choose **More > Regenerate PDF**. To send it
again, see Resend an invoice to a client (KB-150).

## If that does not work

If a regenerated invoice still shows the old logo, contact support.

Need more help? Contact support from **Help > Contact us**.

## Related articles

- Add or change your company logo (KB-104)
- Create and edit invoice templates (KB-131)
- Resend an invoice to a client (KB-150)

TRACE
1. Title and opening: the old logo stays after a change — message 1,
   Wednesday 4 November, customer.
2. The fix is in the invoice templates — message 2, Wednesday
   4 November, support. Account admins only, in the opening and step 1
   — internal note, Thursday 5 November, support.
3. What you see: logo changed under Settings > Company, new invoices
   still show the old one — message 1, Wednesday 4 November, customer.
4. Why it happens: each template keeps its own copy — message 2,
   Wednesday 4 November, support.
5. Steps 1 to 4: Settings > Invoice templates, open the template, Use
   company logo, Save — message 2, Wednesday 4 November, support.
6. Step 5: repeat for each template — message 2, Wednesday 4 November,
   support; done for two templates in message 3, Wednesday 4 November,
   customer.
7. New invoices show the new logo — message 3, Wednesday 4 November,
   customer.
8. Older invoices keep the old logo; More > Regenerate PDF — message 2,
   Wednesday 4 November, support. Not confirmed on its own: see Check
   the steps.
9. Resend an invoice to a client (KB-150) — article list.
10. If that does not work: contact support — message 3, Wednesday
    4 November, customer (regenerated invoice still showed the old
    logo); internal note, Wednesday 4 November, support (only staff can
    clear the cache); message 5, Thursday 5 November, customer (new
    logo after that).
11. Closing line — style guide HC-2, rule 5.
12. Related articles: KB-104, KB-131, KB-150 — article list.

CUSTOMER DETAILS REMOVED
- Customer's name and job title: ticket header, messages 1 and 2. Not
  carried into the article.
- Customer's company name: ticket header and message 1. Not carried
  into the article.
- Email address and phone number: message 1. Not carried into the
  article.
- Account number: ticket header and internal note, Wednesday
  4 November. Not carried into the article.
- The customer's own client: message 1. Not carried into the article.
- Invoice number: messages 1, 3 and 4. Not carried into the article.
- Screenshot and its file name: message 1. Not carried into the
  article.
- Ticket numbers: ticket header and Sam's note. Not carried into the
  article.
- Dates of the case: every message. Not carried into the article.

KEPT OUT OF THE ARTICLE
- Clearing the PDF cache from the admin console (internal note,
  Wednesday 4 November: only staff can do it). The article says to
  contact support instead.
- Engineering's plan to make templates follow the company logo (internal
  note, Thursday 5 November: no date, and not to be told to customers).
- Support staff names (messages 2 and 4, both internal notes).

BEFORE PUBLISHING
Check the steps: a colleague who did not work on ticket 2318 follows
the steps once on a test account, from changing the logo under
Settings > Company to regenerating an invoice made before the change.
Not confirmed: More > Regenerate PDF on its own. In ticket 2318 the
regenerated invoice still showed the old logo (message 3) until support
cleared the cache (internal note, Wednesday 4 November), and showed the
new logo after that (message 5).
Expert review: Kai, product specialist (invoicing). The article
explains why the old logo stays, and the regenerate step was not
confirmed by the customer on its own; the settings call for review in
both cases.
Overlapping articles:
- KB-104, "Add or change your company logo": covers changing the logo,
  not why invoices keep the old one. Sam's note asks whether this
  belongs in KB-104; it is a different problem from KB-104's task, so a
  separate troubleshooting article is recommended, with one line added
  to KB-104 linking here. Ren decides.
- KB-131, "Create and edit invoice templates": templates are where the
  fix is made; linked under Related articles. Its text was not
  supplied, so whether it mentions Use company logo is not known.
- KB-150, "Resend an invoice to a client": linked for sending a
  regenerated invoice again.
Screenshots: None required by HC-2. If one is added: the Logo option on
Settings > Invoice templates, taken from a test account, never from the
customer's attachment.
Sections left out: None
Questions for Kai, product specialist: Should More > Regenerate PDF
show the new logo without support clearing the cache? If it should,
is the "If that does not work" section still needed? If it should not,
the steps change before publishing.
Questions for Ren, support lead: Add the line to KB-104 linking to this
article? Does KB-131 need a mention of Use company logo?
Review date: Monday 10 May 2027, six months from Monday 9 November 2026
(Sunday 9 May 2027 moved to the next working day).
Approval: Ren, support lead, approves before the article is published.

Prepared for Sam, support agent. Nothing has been published, edited or
sent by the assistant, and the ticket is unchanged.
Not completed, and what is needed: whether More > Regenerate PDF works
without support clearing the cache (Kai's answer).
```
