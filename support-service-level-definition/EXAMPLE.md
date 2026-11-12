# Support service level definition: an invented example

*Illustrative example with invented data.* The company, its team, its tickets, its rules and every figure below are invented. An invented 25-person company sells stock-control software to independent bike shops. Its support team is a support lead and one support specialist, and it has never had written targets. On Monday 9 November 2026 the support lead exports the four full weeks from 5 October to 1 November and runs the workflow template.

The inputs come first, in full, so the template can be run on them. The proposal follows.

## The inputs

### The priority definitions

```
SUPPORT PRIORITIES, version 3 (owner: support lead)

Urgent: a shop cannot sell at the till or cannot see its stock at all,
or one shop's information is shown to another.
High: a main function (the till, stock counts, supplier orders) is
wrong or failing for a shop and the workaround is slow; or a billing
error on a shop's account.
Normal: questions, set-up help, requests, and small faults with an
easy workaround.
```

### The coverage note

```
COVERAGE NOTE, 2 November 2026

Working days: Monday to Friday. Working hours: 09:00 to 17:00.
Closed days between 5 October and 1 November 2026: none.
Urgent is also watched by the support lead on rota from 08:00 to 09:00
and 17:00 to 18:00 on working days, and on Saturday from 09:00 to 13:00.
Nobody watches the queue on Sunday.
High and Normal: working hours only.
```

### The roster

```
ROSTER, 9 November 2026 (owner: support lead)

Queue hours in an ordinary week, after meetings, onboarding calls and
other duties:
- Support lead: 10
- Support specialist: 20

Queue hours lost in the weeks ahead:
- Week of 9 November: none.
- Week of 16 November: none.
- Week of 23 November: support specialist on leave Wednesday 25 to
  Friday 27 November, 12 hours lost. Office closed Thursday 26 November:
  support lead, 2 hours lost.
- Week of 30 November: none.
```

### Minutes per ticket, targets wanted and settings

```
Minutes per ticket (support lead's estimate, from first read to
resolution): Urgent 120, High 90, Normal 50.

Targets wanted:
- Urgent: first response within 1 hour.
- High: first response within 2 hours.
- Normal: first response within 8 working hours (one working day).
- No resolution targets in mind yet.

Settings: use the defaults. No busy-period rule. No week is one-off.
```

### The ticket export

```
Ticket,Created,Priority,First human reply,Resolved
S-1201,2026-10-05 13:55,High,2026-10-05 14:20,2026-10-06 13:55
S-1202,2026-10-05 14:30,Normal,2026-10-05 16:10,2026-10-06 13:30
S-1203,2026-10-05 16:45,High,2026-10-06 10:15,2026-10-06 14:15
S-1204,2026-10-06 18:30,High,2026-10-07 10:55,2026-10-07 16:00
S-1205,2026-10-06 21:10,Normal,2026-10-07 15:30,2026-10-08 16:40
S-1206,2026-10-07 09:50,Normal,2026-10-07 11:40,2026-10-09 14:30
S-1207,2026-10-07 16:45,Normal,2026-10-08 13:25,2026-10-12 16:25
S-1208,2026-10-07 18:30,Urgent,2026-10-08 08:35,2026-10-08 10:30
S-1209,2026-10-08 07:35,Normal,2026-10-08 09:45,2026-10-08 16:30
S-1210,2026-10-08 16:45,Normal,2026-10-09 13:35,2026-10-09 16:45
S-1211,2026-10-09 07:35,Normal,2026-10-09 11:00,2026-10-12 15:40
S-1212,2026-10-09 09:05,High,2026-10-09 10:45,2026-10-12 11:45
S-1213,2026-10-09 15:15,High,2026-10-12 11:35,2026-10-12 12:15
S-1214,2026-10-10 10:15,Normal,2026-10-12 16:50,2026-10-14 10:20
S-1215,2026-10-10 11:40,Normal,2026-10-12 13:30,2026-10-14 14:30
S-1216,2026-10-11 10:15,Normal,2026-10-12 10:15,2026-10-14 11:00
S-1217,2026-10-11 11:40,Normal,2026-10-12 14:00,2026-10-13 09:40
S-1218,2026-10-12 09:05,High,2026-10-12 09:45,2026-10-13 12:45
S-1219,2026-10-12 13:55,Normal,2026-10-13 11:55,2026-10-13 16:15
S-1220,2026-10-12 15:15,High,2026-10-12 16:30,2026-10-13 15:35
S-1221,2026-10-13 11:10,Normal,2026-10-14 09:50,2026-10-15 16:10
S-1222,2026-10-13 21:10,Normal,2026-10-14 13:00,2026-10-19 10:00
S-1223,2026-10-14 10:25,Urgent,2026-10-14 12:45,2026-10-15 10:25
S-1224,2026-10-14 12:40,,2026-10-14 14:15,2026-10-15 14:50
S-1225,2026-10-15 07:35,Normal,2026-10-15 10:00,2026-10-20 12:00
S-1226,2026-10-15 11:10,High,2026-10-15 12:45,2026-10-16 10:40
S-1227,2026-10-15 15:15,Normal,2026-10-16 09:35,2026-10-19 09:55
S-1228,2026-10-16 09:05,Normal,2026-10-16 11:15,2026-10-19 12:05
S-1229,2026-10-16 16:45,High,2026-10-19 09:45,2026-10-20 16:15
S-1230,2026-10-17 10:15,Normal,2026-10-19 12:40,2026-10-20 11:00
S-1231,2026-10-17 19:20,Normal,2026-10-19 12:50,2026-10-21 14:40
S-1232,2026-10-18 10:15,Normal,2026-10-19 09:30,2026-10-20 10:00
S-1233,2026-10-18 16:05,Normal,2026-10-19 12:30,2026-10-20 09:20
S-1234,2026-10-19 09:05,High,2026-10-19 12:10,2026-10-20 10:05
S-1235,2026-10-19 09:50,Normal,2026-10-20 11:10,2026-10-20 11:30
S-1236,2026-10-19 10:25,High,2026-10-19 12:25,2026-10-21 09:05
S-1237,2026-10-19 21:10,Normal,2026-10-20 10:35,2026-10-23 16:40
S-1238,2026-10-20 07:35,Normal,2026-10-21 09:30,2026-10-21 09:50
S-1239,2026-10-20 07:35,Normal,2026-10-20 15:50,2026-10-21 13:40
S-1240,2026-10-20 09:05,Normal,2026-10-20 12:15,2026-10-22 14:25
S-1241,2026-10-21 09:50,Normal,2026-10-21 13:10,2026-10-23 10:30
S-1242,2026-10-21 14:30,High,2026-10-21 16:20,2026-10-22 12:30
S-1243,2026-10-21 14:30,High,2026-10-21 15:15,2026-10-22 16:30
S-1244,2026-10-22 10:25,Normal,2026-10-22 13:15,2026-10-22 15:55
S-1245,2026-10-22 15:15,Normal,2026-10-23 14:15,2026-10-26 11:15
S-1246,2026-10-22 18:30,Normal,2026-10-23 10:30,2026-10-27 13:00
S-1247,2026-10-23 10:25,Urgent,2026-10-23 10:45,2026-10-23 17:25
S-1248,2026-10-23 14:30,Normal,2026-10-26 12:50,2026-10-27 10:10
S-1249,2026-10-23 15:15,High,2026-10-23 16:35,2026-10-26 13:55
S-1250,2026-10-24 11:40,Normal,2026-10-26 10:00,2026-10-28 12:40
S-1251,2026-10-24 19:20,High,2026-10-26 11:00,2026-10-27 13:40
S-1252,2026-10-24 19:20,Normal,2026-10-26 11:00,2026-10-27 16:00
S-1253,2026-10-25 10:15,Urgent,2026-10-26 08:10,2026-10-26 12:00
S-1254,2026-10-25 19:20,High,2026-10-26 12:20,2026-10-27 14:40
S-1255,2026-10-25 19:20,Normal,2026-10-26 14:40,2026-10-26 15:00
S-1256,2026-10-26 10:25,Urgent,2026-10-26 11:40,2026-10-26 15:25
S-1257,2026-10-26 11:10,Normal,2026-10-26 14:10,2026-10-28 14:10
S-1258,2026-10-26 14:30,Normal,2026-10-27 11:40,2026-10-27 12:00
S-1259,2026-10-27 07:35,Normal,2026-10-27 13:20,2026-10-28 17:00
S-1260,2026-10-27 16:45,High,2026-10-28 11:35,2026-10-28 11:45
S-1261,2026-10-28 11:10,Normal,2026-10-29 10:20,2026-10-29 10:40
S-1262,2026-10-28 12:40,Normal,2026-10-28 16:50,2026-10-30 15:00
S-1263,2026-10-28 13:55,High,2026-10-28 15:05,2026-10-29 09:55
S-1264,2026-10-29 09:05,High,2026-10-29 11:35,2026-11-02 14:45
S-1265,2026-10-29 09:05,Normal,2026-10-29 11:35,2026-10-29 15:45
S-1266,2026-10-30 09:05,Normal,2026-10-30 11:45,2026-11-02 15:05
S-1267,2026-10-30 10:25,Normal,2026-10-30 15:45,2026-11-02 15:45
S-1268,2026-10-30 16:45,Normal,2026-11-02 09:35,2026-11-02 16:45
S-1269,2026-10-31 10:15,High,2026-11-02 14:10,
S-1270,2026-10-31 11:40,Normal,2026-11-03 11:40,
S-1271,2026-11-01 16:05,Urgent,2026-11-02 08:50,2026-11-02 09:30
S-1272,2026-11-01 16:05,Normal,2026-11-02 10:20,
```

The export was taken on Monday 9 November 2026 at 08:30.

## The output

The proposal is plain text. It is set here with bold headings so it reads well on a page; the words and their order are the template's.

**SUPPORT SERVICE LEVELS: Support team, proposed Monday 9 November 2026**

For: Support lead. Internal targets for running the team. Not a promise to customers.
From: ticket export 5 October to 1 November 2026 (4 full weeks, 72 tickets), taken Monday 9 November 2026, 08:30. Priority definitions version 3. Coverage note 2 November 2026. Roster 9 November 2026. Minutes per ticket Urgent 120, High 90, Normal 50. Targets wanted: Urgent, first response, 1 h; High, first response, 2 h; Normal, first response, 8 h.
Settings: target share 90%, minimum count 10, steps 30 min, 1 h, 2 h, 4 h, 8 h, 16 h, 24 h and 40 h, load ceiling 80%, top-level share 10%, warning point half of each target, planning horizon the weeks of 9, 16, 23 and 30 November. Defaults used: all of these.

**LEVELS AND CLOCKS**

Urgent: a shop cannot sell at the till or cannot see its stock at all, or one shop's information is shown to another. Clock: Monday to Friday 08:00 to 18:00, Saturday 09:00 to 13:00; 10 covered hours on a weekday, 4 on Saturday. Tickets: 6.
High: a main function (the till, stock counts, supplier orders) is wrong or failing for a shop and the workaround is slow; or a billing error on a shop's account. Clock: Monday to Friday 09:00 to 17:00; 8 covered hours make one working day. Tickets: 20.
Normal: questions, set-up help, requests, and small faults with an easy workaround. Clock: Monday to Friday 09:00 to 17:00; 8 covered hours make one working day. Tickets: 45.
Top level: 6 of 71 counted tickets (8%), within the top-level share of 10%.

**NOT COUNTED**

No priority, or a priority not in the definitions: S-1224. Left out of every figure and of the estimated work.
No first reply at the export: none.
Not resolved at the export: S-1269 (High); S-1270 and S-1272 (Normal).
Times that run backwards: none.

**WHAT THE TEAM ACHIEVES TODAY (covered time)**

Urgent, first response: 6 measured. Too few to set a mark: 10 min, 20 min, 35 min, 50 min, 1 h 15 min, 2 h 20 min.
Urgent, resolution: 6 measured. Too few to set a mark: 1 h 30 min, 2 h 30 min, 4 h, 5 h, 7 h, 10 h.
High, first response: 20 measured. At least 90% within 3 h 20 min; slowest 5 h 10 min.
High, resolution: 19 measured. At least 90% within 15 h 30 min; slowest 21 h 40 min. Left out: 1 not resolved (5% of the level).
Normal, first response: 45 measured. At least 90% within 7 h 10 min; slowest 10 h 40 min.
Normal, resolution: 43 measured. At least 90% within 21 h 40 min; slowest 31 h 40 min. Left out: 2 not resolved (4% of the level).

**PROPOSED TARGETS**

A warning point is when an open ticket is raised to the Support lead.
Urgent | First response lead to set | Resolution lead to set | For 90% of tickets | Warning points not set
- Basis: first response, too few tickets, see decision 2; 4 of 6 met the wanted 1 h. Resolution, too few tickets, see decision 2.

High | First response 4 h | Resolution 16 h | For 90% of tickets | Warning points 2 h and 8 h
- Basis: first response, history: at least 90% within 3 h 20 min; wanted 2 h not met, see decision 3. Resolution, history: at least 90% within 15 h 30 min.

Normal | First response 8 h | Resolution 24 h | For 90% of tickets | Warning points 4 h and 12 h
- Basis: first response, wanted target, met for 42 of 45 (93%); history gives the same step. Resolution, history: at least 90% within 21 h 40 min.

**TARGETS WANTED THAT HISTORY DOES NOT MEET**

High, first response: wanted 2 h; met for 14 of 20 (70%) in the period. Proposed instead: 4 h. See decision 3.

**CAPACITY CHECK**

Queue hours in an ordinary week: Support lead 10, Support specialist 20. Total 30.
Estimated work, average week: 19.9 hours. Load 66%.
Estimated work, busy week (19 to 25 October, 22 tickets): 25.3 hours. Load 84%.
Estimated from the Support lead's minutes per ticket and the tickets created each week, not measured. 1 not-counted ticket left out.
Week of 9 November: 30 queue hours; load 66% in an average week, 84% in a busy week.
Week of 16 November: 30 queue hours; load 66% in an average week, 84% in a busy week.
Week of 23 November: 16 queue hours; load 124% in an average week, 158% in a busy week.
Week of 30 November: 30 queue hours; load 66% in an average week, 84% in a busy week.
Above the load ceiling of 80%: the busy week of 19 to 25 October (84%); the weeks of 9, 16 and 30 November in a busy week (84%); the week of 23 November in an average week (124%) and in a busy week (158%).

**BUSY-PERIOD RULE**

Not set: see decision 4.

**DECISIONS FOR THE SUPPORT LEAD: 4**

1. S-1224, created on 14 October, has no priority. It is left out of every figure and of the estimated work. Which level should it count as, or should it stay out?
2. Urgent had 6 tickets in the period, below the minimum count of 10, so no target is proposed. First response times: 10 min, 20 min, 35 min, 50 min, 1 h 15 min, 2 h 20 min; 4 of 6 were within the wanted 1 h. Resolution times: 1 h 30 min, 2 h 30 min, 4 h, 5 h, 7 h, 10 h. What first-response and resolution targets should Urgent have?
3. High first response: the wanted 2 h was met for 14 of 20 tickets (70%). Ninety per cent were answered within 3 h 20 min, which gives 4 h. Should the target be 4 h, or should 2 h stand, and if so, what changes?
4. The estimated work passes the 80% ceiling in a busy week (84%), and in the week of 23 November, with 16 queue hours, it reaches 124% in an average week and 158% in a busy one. The team has no busy-period rule. What rule applies in weeks above the ceiling, starting with the week of 23 November?

**NEXT CHECK**

Run again on an export of 4 full weeks after the approved targets take effect, and compare each target with the share of tickets that met it.

Prepared for the Support lead. Every figure comes from the ticket export, the coverage note and the roster named above; the estimated work uses the Support lead's minutes per ticket. Nothing has been changed in the support system, and nothing has been sent or published.
