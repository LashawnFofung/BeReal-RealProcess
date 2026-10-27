# BeReal Passport & Community Boards — Product Requirements (PRD)

**Current (v2.0):** [1-pager](PRD_v2/BeReal_Passport_Community_Boards_-_PRD-lite_1-pager_v2.0.pdf) · [Full PRD](PRD_v2/BeReal_Passport_Community_Boards_-_Full_Requirements_Document_v2.0.pdf)  
**Original (v1.0):** [1-pager](PRD_v1/Real%20Passport%20%26%20Community%20Boards_-_PRD-lite_1-pager_v1.0.pdf) · [Full PRD](PRD_v1/Real%20Passport%20%26%20Community%20Boards%20-_Full_Requirements_Document_v1.0.pdf)  
[Live prototype](https://lashawnfofung.github.io/BeReal-RealProcess/) · [Back to README](https://github.com/LashawnFofung/BeReal-RealProcess#readme)

> *Independent concept created for a UI/UX program. Not affiliated with or endorsed by BeReal.*

---

## Purpose

A product requirements document (PRD) turns research and design into a clear, shared definition of what to build, for whom, and how success is measured. I wrote two versions for two kinds of readers:

| Document | Reader | What it covers |
| --- | --- | --- |
| **PRD-lite 1-pager** | Busy reviewers who need the decision in two minutes | Problem, target user, metrics, test results, assumptions and non-goals, user stories, acceptance criteria and brand guardrails |
| **Full Requirements Document** | Product, design and engineering teams | Everything in the 1-pager, plus detailed requirements, RICE prioritization, risks, test results, rollout plan, design assets and the ask |

<br>

## Where the PRD fits in the product development life cycle

The PRD is a living document. It isn't written once and filed away. It gets a new version whenever new evidence changes what we would build.

| PDLC stage | What happens | PRD version |
| --- | --- | --- |
| **1. Discover** | UI/UX teardown, company snapshot, problem framing | Not started; findings captured |
| **2. Define** | Persona ("Denise") and journey map | **v1.0 draft** for leadership review |
| **3. Design & prototype** | Seven-screen user flow and clickable prototype | Aligned to the design |
| **4. Test & validate** | 5-person focus group and survey | **v2.0** — results added, requirements revised *(current)* |
| **5. Build (MVP)** | Engineering builds from the approved PRD | v3.0 — final specs and edge cases |
| **6. Launch** | Release to a test cohort, then everyone | Status updated to shipped |
| **7. Measure & iterate** | Track metrics; plan the next version | New version or a follow-up PRD |

Each version carries a version number, date, status and revision history, so reviewers can see what changed and why.

<br>

## Version history

| Version | Date | Status | Summary | Documents |
| --- | --- | --- | --- | --- |
| **1.0** | September 2026 | Draft for discussion | Written before user testing, from research and early design | [1-pager](PRD_v1/Real%20Passport%20%26%20Community%20Boards_-_PRD-lite_1-pager_v1.0.pdf) · [Full PRD](PRD_v1/Real%20Passport%20%26%20Community%20Boards%20-_Full_Requirements_Document_v1.0.pdf) |
| **2.0** | October 27, 2026 | Revised after user testing; recommendation: refine, then retest | Aligned to the tested prototype; test results, new requirements and a re-phased rollout added | [1-pager](PRD_v2/BeReal_Passport_Community_Boards_-_PRD-lite_1-pager_v2.0.pdf) · [Full PRD](PRD_v2/BeReal_Passport_Community_Boards_-_Full_Requirements_Document_v2.0.pdf) |

<br>

## What testing showed

A 40-minute, in-person focus group with five participants (one daily, two occasional and two rare BeReal users) completed three tasks in the clickable prototype, then took an eight-question survey.

| Signal | Result |
| --- | --- |
| Would open BeReal more often | **4 of 5** |
| Reminders, streak and leaderboard feel low-pressure | **4.2 / 5**, the highest score |
| Would launch it | **3 yes · 1 maybe · 1 no** |
| Main friction | Too many taps from capture to stamp |
| Biggest risk | Complexity, not pressure. The non-user called it "less authentic and overly complex." |

These results drove most of the v2.0 changes.

<br>

## What changed from v1.0 to v2.0

### Titles and names

| Item | v1.0 | v2.0 |
| --- | --- | --- |
| Feature title | Real Passport & Community Boards | **BeReal Passport & Community Boards** (matching the prototype, decks, videos and job aid) |
| Document title (full) | Product Requirements Document (PRD-lite) | **Product Requirements Document** |
| Author | Product Design Team | **Lashawn Fofung, MBA, PMP, CSM, CSPO** |
| Friend group | Friends, friend group | **Squad** |
| Leaderboard | Leaderboard (+10 points per post) | **Squad Stamp Tally**, ranked by stamps collected |

### Product decisions aligned to the tested prototype

| Area | v1.0 | v2.0 |
| --- | --- | --- |
| Post types | "Theme Post / Random Post" toggle at capture | **SEND** (regular post, no stamp) or **COMMUNITY BOARD** (themed post + stamp), chosen *after* the photo so capture stays fast |
| October boards | College Campus, Brunch & Tea Time, Coffee Shop, Best Book/Music and more | **HIKE, CRAMMING, COFFEE, HAUNTED**, plus sponsored **LITTLE WINS** and **GAME TIME** |
| Social interaction | Hearts, votes and comments | **Squad-only emoji reactions**, no public like counts; comments moved to an open question |
| Settings | Turn off theme notifications | **Opt-in / Opt-out - Community Board** with a per-board ON/OFF switch (new section 7.6) |
| Re-engagement copy | "12 friends posted to Coffee Shop today" | Reminder bubble ("3 friends already posted to CRAMMING today"), soft streak cue and come-back banner |
| Screens | Today, Boards, Board Detail, Capture, Passport, Leaderboard | Seven-screen habit loop: Today, Capture toggle, Board select, Post confirm, Capsule / Board details, Passport & Leaderboard, Settings / Opt-out |

### Users and evidence

| Area | v1.0 | v2.0 |
| --- | --- | --- |
| Target user | Socially active users; three personas (Priya, Carter, Maya) | **Denise**, an introverted first-time user, plus casual and drifting users |
| Problem evidence | Benchmarking and user feedback | Adds the decline in daily users from about 15M to about 6M |
| Test results | None | New **User Testing Results** section (full) and summary (1-pager) |
| Metrics | DAU/MAU, daily opens, retention, board adoption | Adds **taps and time from capture to stamped post** and a **2.5x daily-opens target** |
| RICE confidence | Medium, "not yet validated with real users" | Medium, a **directional signal from a 5-person focus group** |
| Risks | Four risks | Adds **complexity** (too many taps), with mitigations from testing |

### Plan and ask

| Area | v1.0 | v2.0 |
| --- | --- | --- |
| Rollout | Phase 0 prototype → Phase 1 MVP → Phase 2 expand → Phase 3 sponsors | **Phase 0** prototype & test (complete) → **Phase 1** refine & retest (7–10 people) → **Phase 2** MVP with one friend group → **Phase 3** full rollout → **Phase 4** sponsored-board pilot |
| The ask | Approve a Phase 1 MVP test | Approve the **refine-and-retest round** before committing to the MVP |

<br>

## Open questions for v2.1

- **Comments:** the prototype has squad-only reactions and no comments. Should comments join the MVP, and if so, with the existing moderation stack?
- **Tap target:** what is the right number of taps from capture to stamped post? This gets set during the Phase 1 retest.
- **Shorter-run boards:** day- and week-long observance boards are planned after full rollout and aren't in the prototype yet.

<br>

## What I learned

- **Test before you commit.** v1.0 asked for an MVP; testing showed the flow needed fewer taps first, so v2.0 asks for a retest instead.
- **Keep every artifact in sync.** The prototype, case study, job aid and PRD drifted apart on names and labels. A versioned PRD is the place to bring them back together.
- **Write for two readers.** The 1-pager earns attention; the full PRD answers the follow-up questions.

<br>

## Files

| Folder | File | Description |
| --- | --- | --- |
| `PRD_v2` | [PRD-lite 1-pager v2.0 (PDF)](PRD_v2/BeReal_Passport_Community_Boards_-_PRD-lite_1-pager_v2.0.pdf) | Current 1-pager, revised after user testing |
| `PRD_v2` | [Full Requirements Document v2.0 (PDF)](PRD_v2/BeReal_Passport_Community_Boards_-_Full_Requirements_Document_v2.0.pdf) | Current full PRD, with revision history |
| `PRD_v1` | [PRD-lite 1-pager v1.0 (PDF)](PRD_v1/Real%20Passport%20%26%20Community%20Boards_-_PRD-lite_1-pager_v1.0.pdf) | Original 1-pager, before user testing |
| `PRD_v1` | [Full Requirements Document v1.0 (PDF)](PRD_v1/Real%20Passport%20%26%20Community%20Boards%20-_Full_Requirements_Document_v1.0.pdf) | Original full PRD, before user testing |


---

Built by **Lashawn Fofung**, MBA, PMP, CSM, CSPO.
