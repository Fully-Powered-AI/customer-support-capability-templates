# Known-issues list update: tried once on its example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-12

The inputs were the invented example in [example.md](example.md): the settings, the engineering note, the seven linked cases, the five-entry known-issues list and the release notes for the invented Company K. No client data was used. The fenced instruction block from the template, followed by the output format, was applied to the example's five inputs.

How this run differs from the two before it. The earlier runs were single calls to an assistant that had only the block, the format and the inputs. This run was made by the session that had just edited the template: the same model, but with the whole template, the example and the earlier record in view, so it is not a blind test and cannot show that the new wording alone produces the same output from a fresh assistant. The output below was written by following the block and the format line by line, then checked against the counts. Earlier runs of this template on the same example were recorded on this page before; this record replaces them. The earlier record's findings that led to this edit were: dates without a layout, a title with a version range and a repeated word, eight single search words, no release-platform caveat on proposed-as-fixed lines, and "See question" pointers on held-out lines that the format did not carry.

## What came out

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
Title: Photos gone from the work order when added with no connection and the app is closed before the phone reconnects (Android app)
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

## What was observed

Every part of the output format was produced. The counts add up: 4 linked and 3 held out make the 7 case rows, and the 4 fixed lines were each placed once. No workaround step was written or changed, and all six questions came from rules in the template.

What this run does and does not show:

1. **Close to the example.** The output matches the published example almost line for line. That is weak evidence: the run was made by a session that knew the example, so agreement does not show a fresh assistant would produce it. The example's text was updated in the same edit, so the two were also kept in step by hand.
2. **Dates.** Written as "Thursday 12 November 2026" under the layout the block now states. The earlier run wrote "Thursday 2026-11-12" under a format that gave no layout.
3. **Title.** Platform names only ("Android app"), and "photos" is used once. The earlier run added the version range and repeated the word. A fresh assistant could still do either; this run cannot show that the new rule prevents it.
4. **Search words.** Three phrases, chosen with the rule that prefers phrases a support engineer would type. The earlier run returned eight single words, three of which described nothing. The same caution as for the title applies.
5. **Questions.** Questions 2 and 4 are phrased as either/or ("the same fault on iOS, or a different one?"), which the block now allows as long as no answer is chosen for the list owner. None recommends an answer.
6. **Held-out lines.** "See question 1." and "See question 2." appear on the two held-out lines that raise a question, as the format now carries them.
7. **Release platform.** The proposed-as-fixed line for KI-031 now carries "Engineering to confirm release 5.3.3 reached the iOS app." The release notes do not say whether 5.3.3 shipped on iOS, so the caveat is the point of the line; the draft no longer hides the gap.
8. **Held-out reference.** C-4442 carries ENG-2304, which the release notes say was fixed, and no entry carries it. The draft files the case as held out with no question and the release line as "No entry on the list", and nothing connects the two. The reviewer checklist asks the support lead to compare them.
9. **Possible match.** "Photos" matches the component of KI-035 as a word, as the rule intends. A common component name will also match unrelated lines that use the word loosely; this only raises a question, and the template's customization list says so.

Facts not in the inputs: none were found in this run's output.

Shortcomings of this trial: it is one run by one model on one set of invented inputs, by a session that knew the example. It did not test any of the stop conditions, the unconfirmed-note path, the personal-details rule beyond the phone number in C-4425, the "reference already open" path, the new rule for a release earlier than an entry's range, or the "Not checked" lines for release notes. The acceptance tests in the template are still unrun, apart from the parts this example happens to cover.
