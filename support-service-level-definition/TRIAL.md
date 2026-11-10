# Support service level definition: tried on its invented example

- **Product:** Claude, run in Claude Code

Model: Claude Sonnet 5.5 (model ID claude-sonnet-5-5). Date: 2026-11-09.

The inputs are the invented example in `public/example.md`: the priority definitions, the coverage note, the roster, the minutes per ticket, the targets wanted, the settings and the 72-row ticket export, all invented. No client data was used. The run was done by a model that did not write the template. It followed the fenced instruction block and the output format in `member/template.md`, and read the example's own output only after producing its own. The ticket times were worked out with a small script written for the run, because counting covered time by hand across 72 tickets is error-prone; the script followed the template's clocks and position rule.

## What came out

```
SUPPORT SERVICE LEVELS: support team (all tickets), proposed Monday 9 November 2026

For: support lead. Internal targets for running the team. Not a promise to customers.
From: ticket export Monday 5 October 2026 to Sunday 1 November 2026 (4 full weeks, 72 tickets), taken Monday 9 November 2026, 08:30. Priority definitions version 3. Coverage note 2 November 2026. Roster 9 November 2026. Minutes per ticket Urgent 120, High 90, Normal 50. Targets wanted: Urgent, first response, 1 h; High, first response, 2 h; Normal, first response, 8 h (one working day).
Settings: target share 90%, minimum count 10, steps 30 min, 1 h, 2 h, 4 h, 8 h, 16 h, 24 h, 40 h, load ceiling 80%, top-level share 10%, warning point half of each target, planning horizon 4 weeks from Monday 9 November 2026. Defaults used: all of these.

LEVELS AND CLOCKS
Urgent: a shop cannot sell at the till or cannot see its stock at all, or one shop's information is shown to another. Clock: Monday to Friday 08:00 to 18:00 and Saturday 09:00 to 13:00 (10 covered hours on a weekday, 4 on Saturday; no Sunday). Tickets: 6.
High: a main function (the till, stock counts, supplier orders) is wrong or failing for a shop and the workaround is slow; or a billing error on a shop's account. Clock: Monday to Friday 09:00 to 17:00; 8 covered hours make one working day. Tickets: 20.
Normal: questions, set-up help, requests, and small faults with an easy workaround. Clock: Monday to Friday 09:00 to 17:00; 8 covered hours make one working day. Tickets: 45.
Top level: 6 of 71 counted tickets (8%), within the top-level share of 10%.

NOT COUNTED
No priority, or a priority not in the definitions: S-1224. Left out of every figure and of the estimated work.
No first reply at the export: None.
Not resolved at the export: S-1269 (High), S-1270 (Normal), S-1272 (Normal).
Times that run backwards: None.

WHAT THE TEAM ACHIEVES TODAY (covered time)
Urgent, first response: 6 measured. Too few to set a mark: 0 h 10 min, 0 h 20 min, 0 h 35 min, 0 h 50 min, 1 h 15 min, 2 h 20 min.
Urgent, resolution: 6 measured. Too few to set a mark: 1 h 30 min, 2 h 30 min, 4 h 00 min, 5 h 00 min, 7 h 00 min, 10 h 00 min.
High, first response: 20 measured. 90% within 3 h 20 min; slowest 5 h 10 min.
High, resolution: 19 measured. 95% within 15 h 30 min; slowest 21 h 40 min. Left out: 1 not resolved (5% of the level).
Normal, first response: 45 measured. 91% within 7 h 10 min; slowest 10 h 40 min.
Normal, resolution: 43 measured. 91% within 21 h 40 min; slowest 31 h 40 min. Left out: 2 not resolved (4% of the level).

PROPOSED TARGETS
A warning point is when an open ticket is raised to the support lead.
Urgent | First response lead to set | Resolution lead to set | For 90% of tickets | Warning points not set
- Basis: first response, too few tickets, see decision 2; 4 of 6 met the wanted 1 h. Resolution, too few tickets, see decision 2.
High | First response 4 h | Resolution 16 h | For 90% of tickets | Warning points 2 h and 8 h
- Basis: first response, history: 90% within 3 h 20 min; wanted 2 h not met, see decision 3. Resolution, history: 95% within 15 h 30 min.
Normal | First response 8 h | Resolution 24 h | For 90% of tickets | Warning points 4 h and 12 h
- Basis: first response, wanted target, met for 42 of 45 (93%); history gives the same step. Resolution, history: 91% within 21 h 40 min.

TARGETS WANTED THAT HISTORY DOES NOT MEET
High, first response: wanted 2 h; met for 14 of 20 (70%) in the period. Proposed instead: 4 h. See decision 3.

CAPACITY CHECK
Queue hours in an ordinary week: support lead 10, support specialist 20. Total 30.
Estimated work, average week: 19.9 hours. Load 66%.
Estimated work, busy week (19 October to 25 October, 22 tickets): 25.3 hours. Load 84%.
Estimated from the support lead's minutes per ticket and the tickets created each week, not measured. 1 not-counted ticket left out.
Week of 9 November: 30.0 queue hours; load 66% in an average week, 84% in a busy week.
Week of 16 November: 30.0 queue hours; load 66% in an average week, 84% in a busy week.
Week of 23 November: 16.0 queue hours; load 124% in an average week, 158% in a busy week.
Week of 30 November: 30.0 queue hours; load 66% in an average week, 84% in a busy week.
Above the load ceiling of 80%: week of 9 November, busy week 84%; week of 16 November, busy week 84%; week of 23 November, average week 124% and busy week 158%; week of 30 November, busy week 84%.

BUSY-PERIOD RULE
Not set: see decision 5.

DECISIONS FOR THE SUPPORT LEAD: 5
1. Ticket S-1224 has no priority and is left out of every figure and of the estimated work. Which level does it belong to, and should the export be corrected?
2. Urgent has 6 tickets in the period, fewer than the minimum of 10, so no first-response or resolution target is proposed. For first response, 4 of the 6 met the wanted 1 h. What first-response and resolution targets does the support lead set for Urgent?
3. The wanted first-response target of 2 h for High was met for 14 of 20 tickets (70%); the history gives 4 h (90% within 3 h 20 min). Does the support lead keep the proposed 4 h, or set 2 h in their own name with this history beside it?
4. In the week of 23 November, 14 queue hours are lost (support specialist 12, support lead 2), leaving 16.0 queue hours. Estimated work of 19.9 hours in an average week is a load of 124%, and 25.3 hours in a busy week is 158%. In the other three weeks the busy-week load is 84%, above the ceiling of 80%. What does the support lead decide for these weeks?
5. The team has no busy-period rule, and loads are above the ceiling. Does the support lead set a busy-period rule, and which weeks does it cover?

NEXT CHECK
Run again on an export of 4 full weeks after the approved targets take effect, and compare each target with the share of tickets that met it.

Prepared for the support lead. Every figure comes from the ticket export, the coverage note and the roster named above; the estimated work uses the support lead's minutes per ticket. Nothing has been changed in the support system, and nothing has been sent or published.
```

## What was observed

- **Every required part was produced.** All the format's headings and lines were filled, the counts add up (72 tickets: 71 counted and one, S-1224, with no priority), and no stop condition was triggered. The header, period, definitions and coverage note were all present.
- **The figures match the published example.** Every mark, slowest time, target, warning point, "met for" count and capacity figure is the same: marks 3 h 20 min, 15 h 30 min, 7 h 10 min and 21 h 40 min; targets 4 h and 16 h for High, 8 h and 24 h for Normal; 14 of 20 (70%) for the unmet High target; loads 66%, 84%, 124% and 158%.
- **No stop was needed.** Nothing in the inputs made the template stop or ask.
- **Differences from the published example, all in wording or choices the template leaves open:**
  - Share within the mark. The example prints 90% for every mark. This run printed the actual share (95% for High resolution, 91% for Normal first response and resolution). The format says "[share]% within [time]" and does not say whether that is the target share or the actual share. The example's 90% for High resolution is below the actual 95%, so the example is the looser reading.
  - Load ceiling list. The example names the busy week in the export (19 to 25 October, 84%) among the loads above the ceiling. This run left it out and listed only the weeks ahead. Step 8.6 says "name every load above the load ceiling", which includes it. This run's output was wrong on that point.
  - Decisions. The example has four. This run had five, splitting the loads above the ceiling from the busy-period rule. The template lists them in one position ("loads above the ceiling and the busy-period rule") without saying whether that is one decision or two.
  - Decision content. The example's decision 3 also carries the 84% busy-week load, which is a capacity fact in a first-response decision. This run's decisions kept each to its own subject. The example's decision 2 ends "or should it go without targets until 10 tickets have been measured?", which offers an option, close to a recommendation. This run did not.
  - Team name. The inputs name no team or queue. The example wrote "Support queue", this run "support team (all tickets)". Both are guesses.
  - Small wording and layout: time units ("4 h" against "4 h 00 min", "10 min" against "0 h 10 min"), queue hours as "30" against "30.0", "None" against "none", weekday names on the export dates, and the role written as "support lead" against "Support lead". This run added "(one working day)" to the Normal wanted target and a note on the Urgent clock's daily lengths. The format does not fix any of these.
- **Facts not in the inputs.** None in either output that is invented. Every figure comes from the export, the coverage note, the roster or the minutes per ticket. The only unsupported text is the team label noted above. The example's "created on 14 October" is in the export.
- **Ambiguities in the template met during the run:**
  - Whether "[share]% within [time]" is the actual share or the target share.
  - Whether "every load above the ceiling" includes the busy week in the export or only the planning-horizon weeks.
  - Whether the loads above the ceiling and the busy-period rule are one decision or two.
  - How to state a clock where covered days differ in length (Urgent: 10 hours on a weekday, 4 on Saturday). The format's bracket is for a uniform day only.
  - Whether to print "Left out" for a level when the left-out share is 5% or less. Step 5 only requires the warning above 5%; the format shows "Left out" with no condition. This run printed it in both cases; so did the example. High resolution is exactly 5%, which is not "more than 5%", so no warning was given.
  - What "[team or queue]" is when the inputs give none.
  - A reply or resolution outside covered hours: the procedure counts only covered time, so the clock stops at the end of covered hours. It does not say so for the end of a ticket, only for the start.
  - Placeholders such as "[your target share]" appear in the procedure and inputs, while the instruction block states the defaults in plain words. The defaults were taken from both and agreed.
- **Limits of this trial.** One run, one product, one invented example, with a script doing the arithmetic. It shows the instructions can be followed to a complete output on this input. It does not test the stop conditions or the refusals (the acceptance tests), a real export, or any other product. The template's own version note still says it has not been tried; that line is the template owner's to update.

## Edits after the recorded run

9 November 2026. After an independent review, the template and the example were edited after the run recorded above, and the run was not repeated. The output and observations above are unchanged. Each edit settles one of the ambiguities listed above:

- **Share within the mark.** The format now prints the mark as "at least [target share]% within [time]", never the actual share. The example now reads "At least 90% within" for each mark. This run's actual shares (95%, 91%, 91%) would now be printed as "at least 90%".
- **Load ceiling list.** The step that names every load above the ceiling now says it includes the busy week in the export, as the example has it. This run's omission of that week would now be wrong against the wording as well as the intent.
- **Decisions.** The loads above the ceiling and the busy-period rule are now stated to be one decision, as in the example's four. This run's fifth decision would now be folded into its fourth.
- **Decision content.** The example's decision 2 no longer offers the option of going without targets, and its decision 3 no longer carries the busy-week load. Both now keep to their own subject, as this run's decisions did.
- **Team name.** Where the inputs name no team or queue, the heading now says "Support team". The example now uses it. This run's "support team (all tickets)" would now be "Support team".
- **Clocks.** Where a level's covered days differ in length, the clock now gives the covered hours for each kind of day, as this run did for Urgent; the example now does the same. A reply or resolution logged outside covered hours now stops the clock at the end of the covered hours before it. No reply or resolution in the example falls outside its level's covered hours, so no figure changes.
- **Left out note.** The "Left out" note is now printed whenever any ticket is left out of a measure, with the warning only above 5%, as both this run and the example did.
- **Instruction block.** It now also says that a level with no tickets counts as a level with too few, and that any assignee column is left out of every figure, as the procedure already said.

The template's version note and the public profile now say that it was tried once, in Claude, on 9 November 2026.
