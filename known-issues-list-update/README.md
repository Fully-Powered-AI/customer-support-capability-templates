# Known-issues list update

When engineering confirms a fault, your support lead gets the known-issues entry drafted from the cases and the engineering note: affected versions, what customers see in their own words, the workaround exactly as tested, the linked cases. Entries a release says are fixed are flagged. A person approves every change.

*Workflow template · Customer support and service · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/known-issues-list-update/)*

## The outcome

Your support team matches every new case against one list, so the list has to be right. When engineering confirms a fault, the entry your people will lean on for weeks is ready the same day: the versions engineering says are affected, the conditions it happens under, what customers actually see, quoted from their own cases, and the workaround copied word for word from what engineering tested, with the versions it was tested on. Where the workaround was tested on only some of the affected versions, the entry says so and names the cases on the others.

Every case handed over is either linked to the entry or held out with its reason: another fault's reference, a platform engineering says is not affected, a version outside the range. A held-out case that might mean the range is wrong becomes a question for engineering, not a quiet edit to the versions. What customers say they did to get around the fault is kept to one side, marked as untested, and never offered as the workaround.

When a release ships, the fixed items in its notes are read against the open entries. An entry named by its reference, with a fix that is not limited to some users, is proposed as fixed, with its linked cases listed so the support lead can decide who is told. A fix "for most phones", or one that names no reference, stays a question for engineering. Nothing is added to the list, no status changes and no customer hears anything until a person approves it.

## Who starts the work, and when

The support lead or a senior support engineer starts it when engineering confirms a fault that support cases have reported, and again when a release ships. When both land in the same week, one run covers both.

The support lead, as owner of the list, reads the draft, sends the questions to engineering, and approves each change before a person on the support team makes it in the list and the cases.

## What they supply

- **The engineering note** that confirms the fault: its reference, the component, the affected and unaffected versions, when it happens, the workaround steps with who tested them, on which versions and when, and the fix status.
- **The linked cases,** exported with the case number, date opened, account, platform, version, the customer's own words, status and engineering reference. The template names the column headers it expects; when yours differ, it stops and asks which is which.
- **The current known-issues list,** exported with each entry's number, title, component, status, affected versions, fixed-in version, engineering reference and linked cases.
- **The release notes,** for a release check: the version, the release date and the lines of the fixed section, with the references your team keeps on them.
- **A few settings:** today's date, who owns the list, and how many quotes and search words an entry carries.

## What comes out

One draft update in a fixed order. The header counts the cases linked and held out, the list's entries by status, the release checked and the questions raised.

Then the new entry, numbered after the last one on the list: title in customers' words, affected and unaffected versions, when it happens, quotes from the cases, search words your team can match new cases on, the workaround as tested and where it was not tested, the fix status marked internal, and the linked cases. The held-out cases and the untested customer fixes follow. Open entries that may describe the same fault come next, then the release check: entries proposed as fixed, entries named but not proposed, possible matches, and fixes with no entry on the list. The draft ends with numbered questions, each addressed to the support lead or engineering, and the list of record changes a person makes once the support lead approves. When a section has nothing in it, it says so.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Customer support and service](https://fullypowered.ai/functions/customer-support-and-service/), where the support lead keeps the list every support engineer checks a new case against.
- [Software technology](https://fullypowered.ai/industries/software-technology/), where every release changes which faults are open and on which versions.
- [Hardware and physical technology](https://fullypowered.ai/industries/hardware-and-physical-technology/), where a fault can belong to one firmware version and the workaround has to say which.
- [Finance and investment](https://fullypowered.ai/industries/finance-and-investment/), where customers of a banking or payments app call about the same fault for days and need one tested answer.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when the support team grows past the senior engineer who used to hold every known fault in their head.
- [Startups & new ventures](https://fullypowered.ai/situations/startups-and-new-ventures/), where releases ship weekly and the list has to keep up.

## What has to change for your company

Tell it the column headers your support system and issue tracker export, or export with the ones it expects. Agree with engineering what a confirmation note carries, above all the versions a workaround was tested on, because the entry carries nothing engineering did not test. Set your entry numbering, your platform names and how your versions are written. Name the owner of the list and who answers questions for engineering. If your release notes mark a partial fix with words beyond the defaults, add them. Decide who tells customers when an entry is marked fixed. It runs in ChatGPT, Claude, Copilot or Gemini from files and text you supply; it needs no connection to your support system or issue tracker.

## What has been checked

Fully Powered AI wrote this workflow template as original work. It was editorially reviewed on 12 November 2026. It was tried on its invented example in Claude on 12 November 2026, and the record of that run is published with the template. After an independent review the same day, the instructions were corrected and the template was run again on the example. After a second review that day, small corrections were made and it was run once more on the example; the published record is of that third run, made by the session that edited the template, so it is not a blind test. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past confirmation and a past release your support lead already knows, with hard cases written in advance: a workaround tested on only some versions, a case on a version engineering did not list, a case on a platform engineering says is not affected, a fix the notes describe as working "for most", a fixed line with no reference, an export with different column headers. The support lead checks every copied version and workaround step against the engineering note before anyone relies on the entry. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 12 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 12 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the workflow template drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related workflow templates

- [Support ticket triage](../support-ticket-triage/)
- [Release notes draft](https://fullypowered.ai/workflows/release-notes-draft/)
- [Help article from a resolved issue](../help-article-from-a-resolved-issue/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
