# Known-issues list update: an invented example

*Illustrative example with invented data.* The company, its customers, the cases, the engineering note, the list, the release notes and every version number below are invented. Company K is an invented maker of a scheduling and work-order app for small trades businesses, on Android, iOS and the web. Its support team keeps an internal known-issues list that support engineers match new cases against. On Thursday 12 November 2026 the senior support engineer had two things to bring to the list: engineering had confirmed a fault behind a run of cases about lost photos, and release 5.3.3 had shipped on the Monday. First come the inputs the senior support engineer supplied, in full, then the update the workflow template returned for the support lead.

## The inputs

### 1. Settings

```
product: Company K field service app
today: 2026-11-12
run_by: senior support engineer
list_owner: support lead
quote_limit: 5
search_word_limit: 8
```

### 2. Engineering note

```
engineering_ref: ENG-2291
status: confirmed
confirmed_on: 2026-11-10
confirmed_by: mobile engineering lead
component: Photos
affected_versions: Android app 5.3.0 to 5.3.3
not_affected: iOS app; Web app
happens_when: Photos are added to a work order while the phone has no connection, and the app is closed before the phone reconnects.
workaround_steps:
1. After adding photos with no connection, keep the app open until the phone reconnects and the sync mark at the top of the work order turns into a tick.
2. If photos are already missing from a work order, open the phone's gallery, find the album named Company K, and attach the photos again from the work order with Add photo, then From gallery.
workaround_limits: Step 2 does not bring back photos on phones where the app's camera is set not to keep a copy in the gallery.
workaround_tested_on: Android app 5.3.2; Android app 5.3.3
workaround_tested_by: QA engineer
workaround_tested_date: 2026-11-10
fix_status: planned for Android app 5.3.4; no release date set
cause: The upload queue is emptied when the app closes before sync finishes.
```

### 3. Linked cases

```
case_id,opened,account,platform,product_version,customer_words,status,engineering_ref
C-4410,2026-11-03,A-118,Android,5.3.1,"Took 4 photos at a basement site with no signal, now the work order shows no photos at all.",open,ENG-2291
C-4417,2026-11-04,A-203,Android,5.3.2,"Pictures vanish after I get back to the van. My tech says he definitely attached them.",open,ENG-2291
C-4425,2026-11-05,A-118,Android,5.3.2,"Photos gone again from today's work orders. Call me on 555-0142.",open,
C-4431,2026-11-06,A-077,Android,5.2.4,"Some photos missing from the work order after it synced.",open,ENG-2291
C-4436,2026-11-07,A-310,iOS,5.3.3,"Photos not showing on the work order on my iPhone.",open,ENG-2291
C-4440,2026-11-09,A-290,Android,5.3.0,"Photos taken in airplane mode are gone after reconnecting. For now I take them with the normal camera app and add them later from the gallery.",open,ENG-2291
C-4442,2026-11-09,A-152,Android,5.3.3,"Notes on the work order show up twice after sync.",open,ENG-2304
```

### 4. Current known-issues list

```
entry_id,title,component,status,affected_versions,fixed_in,engineering_ref,linked_cases
KI-029,Exported timesheets show breaks twice,Timesheets,fixed,Web app 5.2.0 to 5.2.6,5.3.0,ENG-2190,C-4231; C-4240
KI-031,Calendar shows visits an hour late after the clock change,Calendar,open,iOS app 5.2.0 to 5.3.2,,ENG-2210,C-4302; C-4307; C-4311
KI-033,Invoice PDF cuts off the last line item,Invoices,open,Web app 5.3.1 and later,,ENG-2262,C-4350
KI-034,Customer signature box does not appear on small phones,Signature,open,Android app 5.3.0 to 5.3.2,,ENG-2275,C-4388; C-4401
KI-035,Photo thumbnails load slowly on large work orders,Photos,open,Android app 5.3.0 and later; iOS app 5.3.0 and later,,ENG-2280,C-4395
```

### 5. Release notes

```
version: 5.3.3
release_date: 2026-11-09
Fixed:
Calendar times are correct again after the clock change (ENG-2210).
The signature box now appears on most small Android phones (ENG-2275).
Faster loading of photo thumbnails.
Notes on a work order no longer appear twice after sync (ENG-2304).
```

## The output

```
KNOWN-ISSUES LIST UPDATE: Company K field service app, Thursday 12 November 2026

For: support lead. Prepared for senior support engineer.
Engineering note: ENG-2291, status confirmed, dated Tuesday 10 November 2026 by mobile engineering lead.
Cases: 7 rows: linked 4, held out 3.
Known-issues list: 5 entries: open 4, fixed 1, retired 0. Next number: KI-036.
Release notes: 5.3.3, released Monday 9 November 2026, 4 fixed lines.
Questions: 6.

PART 1. NEW ENTRY (DRAFT)
Entry: KI-036 (proposed). Status: open, once approved.
Title: Photos gone from the work order when added with no connection and the app is closed before reconnecting (Android app)
Component: Photos
Affected versions: Android app 5.3.0 to 5.3.3
Not affected: iOS app; Web app
Happens when: Photos are added to a work order while the phone has no connection, and the app is closed before the phone reconnects.
What customers see, in their words:
- "Took 4 photos at a basement site with no signal, now the work order shows no photos at all." (C-4410, Android 5.3.1)
- "Pictures vanish after I get back to the van. …" (C-4417, Android 5.3.2)
- "Photos gone again from today's work orders. …" (C-4425, Android 5.3.2)
- "Photos taken in airplane mode are gone after reconnecting. …" (C-4440, Android 5.3.0)
Search words: no signal, pictures vanish, airplane mode
Workaround, as tested by QA engineer on Android app 5.3.2; Android app 5.3.3, Tuesday 10 November 2026:
1. After adding photos with no connection, keep the app open until the phone reconnects and the sync mark at the top of the work order turns into a tick.
2. If photos are already missing from a work order, open the phone's gallery, find the album named Company K, and attach the photos again from the work order with Add photo, then From gallery.
Limits: Step 2 does not bring back photos on phones where the app's camera is set not to keep a copy in the gallery.
Not tested on: every affected version except Android app 5.3.2; Android app 5.3.3. Linked cases on untested versions: C-4410 (5.3.1), C-4440 (5.3.0).
Fix: planned for Android app 5.3.4; no release date set. Internal: give customers no date.
Engineering reference: ENG-2291
Linked cases: 4 cases from 3 accounts: C-4410, C-4417, C-4425 (reference not on the case), C-4440.

Held out:
C-4431, Android 5.2.4: version 5.2.4 is outside the affected versions engineering stated. See question 1.
C-4436, iOS 5.3.3: iOS 5.3.3 is not affected, per engineering. See question 2.
C-4442, Android 5.3.3: carries ENG-2304, not ENG-2291.

Reported in cases, not tested (internal; never give to customers):
C-4440: "For now I take them with the normal camera app and add them later from the gallery."

PART 2. POSSIBLE OVERLAP WITH OPEN ENTRIES
KI-035, "Photo thumbnails load slowly on large work orders": same component (Photos); affected Android app 5.3.0 and later; iOS app 5.3.0 and later. See question 4.

PART 3. RELEASE NOTES CHECK
Proposed as fixed:
KI-031, "Calendar shows visits an hour late after the clock change". Line: "Calendar times are correct again after the clock change (ENG-2210)." Affected iOS app 5.2.0 to 5.3.2; release 5.3.3 is later. Proposed: status open to fixed; fixed_in 5.3.3. Linked cases on the list: C-4302; C-4307; C-4311. Engineering to confirm release 5.3.3 reached the iOS app. Who tells customers: for support lead to decide.
Named, not proposed:
KI-034, "Customer signature box does not appear on small phones". Line: "The signature box now appears on most small Android phones (ENG-2275)." Why: the fix is limited ("most"). Stays open. See question 5.
Already closed:
None.
Possible match:
"Faster loading of photo thumbnails.": no reference on the list; mentions Photos, the component of open entry KI-035, "Photo thumbnails load slowly on large work orders". See question 6.
No entry on the list:
"Notes on a work order no longer appear twice after sync (ENG-2304).": names ENG-2304, which no entry carries.

QUESTIONS
1. For engineering. C-4431 is on Android 5.2.4, outside the affected versions you stated (Android app 5.3.0 to 5.3.3). The customer wrote: "Some photos missing from the work order after it synced." Does the fault reach 5.2.4, or is this a different fault? The case is held out until you answer.
2. For engineering. C-4436 is on iOS 5.3.3, and the note says the iOS app is not affected. The customer wrote: "Photos not showing on the work order on my iPhone." Is this the same fault on iOS, or a different one? The case is held out until you answer.
3. For engineering. The workaround was tested on Android app 5.3.2 and 5.3.3 only. Two linked cases are on untested versions: C-4410 (5.3.1) and C-4440 (5.3.0). Will the workaround be tested on the earlier affected versions? Until then the entry says where it was not tested.
4. For the support lead. KI-035, "Photo thumbnails load slowly on large work orders", is open on the same component (Photos) and its affected versions include Android app 5.3.0 to 5.3.3. Should KI-036 stand as a separate entry?
5. For engineering. The 5.3.3 notes say the signature box now appears "on most small Android phones" (ENG-2275). On which phones does KI-034 still happen? It stays open until you answer.
6. For engineering. The 5.3.3 notes list "Faster loading of photo thumbnails." with no reference. Does 5.3.3 fix ENG-2280, behind KI-035? Nothing is proposed for KI-035 until you answer.

AFTER APPROVAL, BY A PERSON
- Add KI-036 to the known-issues list.
- Add ENG-2291 to case C-4425.
- KI-031: status open to fixed; fixed_in 5.3.3.

DATA NOTES
C-4425: personal details in the case's words not repeated.

Draft for support lead's approval. Nothing has been added to the list, no status has changed, no case has been edited, and nothing has been published or sent to a customer.
```

The support lead reads the draft, sends questions 1, 2, 3, 5 and 6 to engineering, decides question 4, and approves the three changes under After approval. A support engineer then makes them in the list and the case. Who tells the customers on KI-031's three cases that the calendar fault is fixed is the support lead's decision; the workflow template contacts no one.
