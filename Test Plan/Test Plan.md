# BeReal Passport & Community Boards — Test Plan

**[PRD v2.0](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/PRD/PRD.md)** · **[Competitive Analysis](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Competitive%20Analysis/Competitive%20Analysis.md)** · **[Live prototype](https://lashawnfofung.github.io/BeReal-RealProcess/)** · **[Back to README](https://github.com/LashawnFofung/BeReal-RealProcess#readme)**

> *Independent concept created for a UI/UX Design & Product Management Externship. Not affiliated with or endorsed by BeReal.*

---

## Summary

The 5-person focus group gave a directional signal: **4 of 5** would open BeReal more often, and the main friction was **too many taps from capture to stamp**. Five people can find usability problems, but they can't prove that a feature changes behavior.

This plan tests the feature in two stages before any wide rollout:

| Stage | PRD phase | Question it answers | Method |
| --- | --- | --- | --- |
| **1. Usability retest** | Phase 1: refine & retest | Did the redesign fix the friction? | Moderated usability test, 7–10 people |
| **2. A/B experiment** | Phase 2: MVP | Does the feature make casual users come back more, without hurting regular posting? | Randomized controlled experiment |

The decision this plan supports: **ship to full rollout (Phase 3), iterate, or kill.**

<br>

## Stage 1: Usability retest

**Goal:** confirm the refined flow is simple enough before spending engineering time on an MVP.

**Participants:** 7–10 people, including **at least 3 lapsed or non-users**. The first round had only one non-user, and that person raised the "overly complex" concern.

**Tasks:** the same three tasks as the [interactive job aid](https://lashawnfofung.github.io/BeReal-RealProcess/Job%20Aid/BeReal_BeReal%20Passport%20and%20Community%20Boards_Interactive_Job_Aid.html), unaided:
1. Post a stamped BeReal to a board
2. Find your stamp in your Passport and open the capsule
3. Opt out of one board in Settings

**Measures and pass criteria:**

| Measure | Baseline (round 1) | Pass criteria |
| --- | --- | --- |
| Task 1 completed without help | Not measured | **≥ 80%** of participants |
| Taps from shutter to stamped post | **4** (shutter → COMMUNITY BOARD → pick board → Stamp & post) | **≤ 3** |
| Time from capture to stamped post | Not measured | Median **≤ 15 seconds** |
| Ease of Task 1 (1–7 single-ease question) | Not measured | Median **≥ 6** |
| "Reminders and streak feel low-pressure" (1–5) | **4.2** | **≥ 4.0** (hold the gain) |
| "I'd open BeReal more often" | **4 of 5** | **≥ 70%** |
| "Overly complex" raised unprompted | 1 of 5 | **≤ 1** participant |

**If it fails:** iterate on the design and retest before moving to Stage 2.

<br>

## Stage 2: A/B experiment

### Hypothesis

> **If** casual BeReal users can post their daily photo to a themed squad board and earn a collectible Real Passport stamp, **then** they will be active on more days, **because** boards give them a reason to return that adds no time pressure.

- **Null hypothesis (H₀):** active days per user are the same in treatment and control.
- **Secondary hypotheses:**
  - Better day-7 and day-30 retention.
  - No drop in regular posting (the feature adds to the core habit rather than replacing it).

### Who is in the test

- **Eligible:** users with at least one squad of 3+ friends, on an app version that supports boards.
- **Primary segment:** **casual users**, active on 1–12 of the last 28 days. They're the users the feature is designed to win back.
- **Also reported:** all users and daily users, as a check that the feature doesn't hurt the most engaged users.

### How users are randomized

| Decision | Choice | Why |
| --- | --- | --- |
| **Unit of randomization** | The **squad (friend cluster)**, not the individual user | Boards are social. If one friend has boards and another doesn't, they influence each other and contaminate the results. |
| **How clusters are formed** | Friend-graph communities, frozen at the start of the test | Keeps each squad entirely in one group |
| **Split** | **50 / 50**, stratified by squad size and baseline activity | Balances the groups on the factors most likely to affect results |
| **Treatment** | Community Boards, stamps, Passport, Squad Stamp Tally and opt-in prompts | The full MVP loop |
| **Control** | Standard BeReal, with the same number of notifications | Rules out "more notifications" as the cause |
| **Analysis** | **Intent-to-treat**: compare everyone *assigned*, not only users who opted in | Opt-in users are self-selected and would overstate the effect. Opt-in rate is reported separately. |

### Metrics

**Primary metric (one, decided in advance):**

| Metric | Definition | Why this one |
| --- | --- | --- |
| **Active days per casual user** | Days with at least one app open in a 28-day window | Measures directly whether the feature brings people back. It is the building block of DAU/MAU, the North Star. |

**Secondary metrics:**

| Metric | What it tells us |
| --- | --- |
| Day-7 and day-30 retention | Whether the effect lasts beyond the novelty |
| Sessions per user per day | Progress toward the PRD's 2.5x daily-opens goal |
| Board opt-in rate | Adoption; an effect needs enough people to join |
| Share of posts sent to a board | Feature usage |
| Passport and Squad Stamp Tally visits | Whether the collection loop is pulling people back |
| Taps and time from capture to stamped post | Usability at scale |

**Guardrail metrics (these must not get worse):**

| Guardrail | Threshold to stop or kill |
| --- | --- |
| **Regular (SEND) posts per user** | Drop of **more than 2%** |
| **Total BeReals posted per user** | Any significant drop |
| Notification disable rate | Increase of **more than 10%** |
| Uninstall rate | Any significant increase |
| Board opt-out rate | Above **20%** of joiners within 14 days |
| Report and block rate on board posts | Any significant increase |
| Post failures (error state) and crashes | Above the current app baseline |
| "Still feels like BeReal" (in-app survey, 1–5) | Below **3.5** |

### Sample size and duration

The numbers below are **planning assumptions**. They should be replaced with BeReal's real baselines before launch.

| Input | Assumption |
| --- | --- |
| Baseline active days per casual user (28 days) | Mean **6**, standard deviation **5** |
| Minimum detectable effect (MDE) | **+5% relative** (+0.3 active days) |
| Significance and power | α = 0.05 (two-sided), power = 80% |
| Average squad size | 8 users |
| Correlation within squads (ICC) | 0.05–0.10 |

| Result | Per arm | Total |
| --- | --- | --- |
| Users needed if individually randomized | ~4,360 | ~8,700 |
| Adjusted for squad randomization (×1.35–1.70) | **~5,900–7,400 users** (~740–930 squads) | **~12,000–15,000 users** |

**Duration: 8 weeks**, with a 4-week minimum. Eight weeks covers **two full monthly board cycles**, shows whether interest fades after the novelty, and gives a clean day-30 retention read. The test runs its full length even if early results look good, so there's no stopping early.

**Before launch:**
- Run a 1-week **A/A test**, with both groups getting standard BeReal, to confirm the split and the tracking are sound.
- Check that the 50/50 split holds, with no sample-ratio mismatch, throughout the test.

### Decision criteria

| Outcome | Rule | Next step |
| --- | --- | --- |
| ✅ **Ship** | Primary metric lifts **≥ +5%** for casual users (statistically significant) **and** no guardrail is breached | Phase 3 full rollout |
| 🔁 **Iterate** | Primary metric is positive but not significant, **or** board opt-in is below 15%, **or** a guardrail is close to its threshold | Fix onboarding or the flow, then rerun |
| ❌ **Kill** | Primary metric's upper confidence bound is **below +2%**, **or** any guardrail is breached (e.g., regular posts drop more than 2%) | Stop; write up the learnings |

<br>

## Instrumentation

These events need to be tracked before Stage 2 can run:

| Event | Fires when |
| --- | --- |
| `app_open` | The app opens; feeds the primary metric |
| `board_optin` / `board_optout` | A user joins or leaves a board, with the board ID |
| `post_type_selected` | The user picks `send` or `community_board` |
| `board_selected` | A board is chosen, with the board ID |
| `stamp_post_success` / `stamp_post_error` | Posting finishes, with taps and seconds since capture |
| `passport_view` / `stamp_tally_view` / `capsule_view` | Collection screens are opened |
| `reaction_sent` | A squad reaction is sent |
| `notification_disabled` | A notification setting is turned off |

<br>

## Threats to validity

| Threat | Mitigation |
| --- | --- |
| **Novelty effect:** people try anything new | 8-week run; compare week 1–2 with week 7–8 |
| **Spillover between friends** | Randomize by squad, not by individual |
| **Self-selection:** opt-in users differ | Intent-to-treat analysis |
| **Seasonality:** some board themes are more appealing | Two full monthly cycles; the same calendar period for both groups |
| **More notifications in the treatment group** | Match notification volume in the control group |
| **Peeking at results early** | One primary metric chosen in advance; fixed duration |

<br>

## Timeline

| Week | Activity |
| --- | --- |
| 0 | Stage 1 usability retest and design fixes |
| 1–2 | Build the MVP; add instrumentation; run the A/A test |
| 3–10 | A/B experiment (8 weeks) |
| 11 | Analysis and readout; ship, iterate or kill decision |

<br>

## Readout template

1. **Decision:** ship, iterate or kill, in one line.
2. **Primary metric:** lift, confidence interval, p-value.
3. **Guardrails:** each one with its value, marked pass or fail.
4. **Secondary metrics and segments:** casual, daily and all users.
5. **What we learned** and **what we'd test next**.

---

Built by **Lashawn Fofung**, MBA, PMP, CSM, CSPO.
