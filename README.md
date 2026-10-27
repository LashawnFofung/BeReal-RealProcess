<div align="center">

# 📸 BeReal Passport & Community Boards
### A re-engagement feature concept for casual BeReal users

**UI/UX Design + Product Management Case Study** · UI/UX Design & Product Management Externship · Aug 2026 – Oct 2026

[![Prototype](https://img.shields.io/badge/Try_the_Prototype-Live-2EA44F?style=flat&logo=githubpages&logoColor=white)](https://lashawnfofung.github.io/BeReal-RealProcess/)
[![Case Study](https://img.shields.io/badge/Case_Study-16_min-FF0000?style=flat&logo=youtube&logoColor=white)](https://youtu.be/yxYclJn8ZGc)
[![Pitch](https://img.shields.io/badge/Pitch-5_min-FF0000?style=flat&logo=youtube&logoColor=white)](https://youtu.be/Or5O1wUj_Ow)
[![Job Aid](https://img.shields.io/badge/Job_Aid-Interactive-FFDE59?style=flat&logo=githubpages&logoColor=black)](https://lashawnfofung.github.io/BeReal-RealProcess/Job%20Aid/BeReal_BeReal%20Passport%20and%20Community%20Boards_Interactive_Job_Aid.html)
[![PRD](https://img.shields.io/badge/PRD-v2.0-0A0A0A?style=flat&logo=readthedocs&logoColor=white)](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/PRD/PRD.md)
[![MBA Portfolio](https://img.shields.io/badge/Portfolio-View-6E40C9?style=flat&logo=github&logoColor=white)](https://github.com/LashawnFofung/MBA-IT-Management-Portfolio)


<br>

<a href="https://lashawnfofung.github.io/BeReal-RealProcess/"><img src="Project%20Marketing%20Images/Images/BeReal%20Passport%20Hero.png" alt="BeReal Passport &amp; Community Boards: three phone screens showing squad board posts with passport stamps, and the tagline Your daily real, now stamped." width="100%"></a>

</div>

> *Independent concept created for a UI/UX Design & Product Management Externship. Not affiliated with or endorsed by BeReal.*

---

## Contents
[TL;DR](#tldr) · [Start Here](#-start-here) · [The Problem](#the-problem) · [The User](#the-user) · [The Solution](#the-solution) · [Testing & Results](#testing--results) · [Next Steps](#next-steps) · [Process & Artifacts](#process--artifacts) · [My Role](#my-role) · [📅 Project Timeline](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Project%20Timeline.md)

---

## TL;DR

| | |
|---|---|
| **Problem** | BeReal's daily users fell from about 15M to about 6M in a matter of months. Casual users drift away when nothing pulls them back. |
| **User** | "Denise," an introverted first-time user who values privacy and feels stressed by forced, real-time posting |
| **Solution** | Small squads share monthly themed boards. Each post earns a collectible *Real Passport* stamp, and each month is saved as a capsule. Opt-in, same real photo, no public likes. |
| **Result** | In a 5-person focus group, **4 of 5** testers said they'd open BeReal more often. Reminders and streaks scored **4.2/5** for feeling low-pressure. |
| **Recommendation** | Cut taps from capture to stamp, then retest with 7–10 people before an MVP ([PRD v2.0](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/PRD/PRD.md)) |

---

## 🎬 Start Here

| Deliverable | Watch / Try | Files |
|---|---|---|
| **Interactive prototype** | [GitHub Pages](https://lashawnfofung.github.io/BeReal-RealProcess/) · [Claude](https://claude.ai/artifact/QouixAtcmRQXoxXEiUsXgm) | [HTML](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Prototype/BeReal_Passport_Prototype.html) |
| **Case study** (16 min) | [▶️ YouTube](https://youtu.be/yxYclJn8ZGc) | [PPTX](https://github.com/LashawnFofung/BeReal-RealProcess/raw/main/Case%20Study/BeReal%20Passport%20And%20Community%20Boards%20Case%20Study.pptx) · [PDF](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Case%20Study/BeReal%20Passport%20And%20Community%20Boards%20Case%20Study.pdf) |
| **Pitch** (5 min) | [▶️ YouTube](https://youtu.be/Or5O1wUj_Ow) | [PPTX](https://github.com/LashawnFofung/BeReal-RealProcess/raw/main/Pitch/BeReal%20Passport%20And%20Community%20Boards%20Pitch.pptx) · [PDF](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Pitch/BeReal%20Passport%20And%20Community%20Boards%20Pitch.pdf) |
| **Promo reel** (45 sec) | [▶️ YouTube Short](https://youtube.com/shorts/exXoJ6NqmbI) | |
| **Interactive job aid** | [Try it](https://lashawnfofung.github.io/BeReal-RealProcess/Job%20Aid/BeReal_BeReal%20Passport%20and%20Community%20Boards_Interactive_Job_Aid.html) | [HTML](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Job%20Aid/BeReal_BeReal%20Passport%20and%20Community%20Boards_Interactive_Job_Aid.html) · [Process & prompt](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Job%20Aid/Prompt%20Engineering.md) |
| **Product requirements** (v2.0) | [1-pager (PDF)](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/PRD/PRD_v2/BeReal_Passport_Community_Boards_-_PRD-lite_1-pager_v2.0.pdf) · [Full PRD (PDF)](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/PRD/PRD_v2/BeReal_Passport_Community_Boards_-_Full_Requirements_Document_v2.0.pdf) | [Process & changes](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/PRD/PRD.md) |

---

## The Problem

BeReal's core idea, one unfiltered photo a day at a random time, made it stand out. But daily users fell from about 15M to about 6M in a matter of months. For casual users, the app asks for effort every day and offers little reason to come back once the novelty fades.

**The question:** How might we give casual users a reason to return, without breaking what makes BeReal *real*?

---

## The User

**Persona: "Denise"** — an introverted first-time user who prefers low-pressure interactions, values privacy, and feels friction with forced real-time sharing.

I mapped her journey through five stages of the current app:

| Stage | What Denise feels | Friction |
|---|---|---|
| **1. Onboard** | Curious but cautious | Required phone number and notifications feel like a lot up front |
| **2. Connect** | Selective, protective of privacy | Contact-sync prompts push for a wider circle than she wants |
| **3. Prompt** | Stressed, put on the spot | The 2-minute timer adds performance anxiety |
| **4. Capture** | Self-conscious, exposed | No control over the photo; the "Late" label feels like public judgment |
| **5. Consume** | Relieved, a passive observer | The feed is locked until she posts, a barrier for someone who mostly wants to watch |

📄 [Full persona & journey map](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/User%20Journey/Users.md)

---

## The Solution

**BeReal Passport & Community Boards** adds a slower, friendlier reason to open the app.

- **Squads** — small, chosen groups instead of a wide friend list
- **Monthly themed boards** — a shared prompt the squad posts to on their own time
- **Real Passport stamps** — each post earns a collectible stamp
- **Monthly capsules** — each month is saved as a keepsake

**How it works:** take your BeReal as usual → choose **SEND** (regular post) or **COMMUNITY BOARD** (themed post + stamp) → pick a board → collect your stamp. Reactions stay inside the squad, and you can opt in or out of any board in Settings.

### How the design answers Denise's pain points

| Pain point | Design response |
|---|---|
| Pressure from a wide audience | Small squads she picks herself |
| Anxiety from the 2-minute timer | Monthly boards with no countdown |
| Fear of public judgment | No public likes |
| Feeling forced to participate | Fully opt-in |
| Little reason to come back | Collectible stamps, streaks, and capsules |
| Risk of drifting from BeReal's identity | Uses the same real, unfiltered photo |

**Prototype:** a seven-screen user flow covering UI states and re-engagement hooks. [Try it live →](https://lashawnfofung.github.io/BeReal-RealProcess/)

---

## Testing & Results

**Method:** Clickable prototype tested with a 5-person focus group, followed by a survey.

| Signal | Result |
|---|---|
| Would open BeReal more often | **4 of 5** testers |
| Reminders & streak feel low-pressure | **4.2 / 5** |
| Would launch it | **3 yes · 1 maybe · 1 no** |
| Main friction found | Too many taps from capture to stamp |
| Biggest risk | Complexity, not pressure |

📄 [Survey results](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Survey)

> **Caveat:** Five testers is enough to find usability issues and gauge direction, but not enough to predict behavior at scale. These results are an early signal, not proof.

---

## Next Steps

The [PRD v2.0](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/PRD/PRD.md) re-phased the rollout based on testing:

| Phase | Plan |
|---|---|
| **0. Prototype & test** | ✅ Complete: clickable prototype and 5-person focus group |
| **1. Refine & retest** | Cut taps from capture to stamp, make SEND vs. COMMUNITY BOARD clear, add a first-use explainer; retest with 7–10 people, including users who have stopped using BeReal |
| **2. MVP** | One board with the full loop, shipped to one friend group |
| **3. Full rollout** | Four themed boards per month, plus shorter observance boards |
| **4. Sponsored pilot** | Sponsor-branded boards as a monetization test |

**Proposed success metrics for a real pilot:**
- DAU/MAU ratio for opted-in users vs. a control group
- Board participation rate per squad per month
- 30- and 60-day return rate for casual users
- Taps and time from capture to stamped post

---

## Process & Artifacts

| Phase | What I did | Artifact |
|---|---|---|
| **1. Discover** | UI/UX teardown, company snapshot and competitor benchmarking | [Teardown (PDF)](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/BeReal_UIUX_Teardown.pdf) · [Corporate Snapshot](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/BeReal%20Corporate%20Snapshot.png) · [Competitive Analysis](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Competitive%20Analysis/Competitive%20Analysis.md) · [Feature Working Session](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Competitive%20Analysis/Feature%20Working%20Session.md) |
| **2. Define** | Introvert persona, 5-stage journey map and PRD v1.0 draft | [Persona & Journey](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/User%20Journey/Users.md) · [PRD v1.0](https://github.com/LashawnFofung/BeReal-RealProcess/tree/main/PRD/PRD_v1) |
| **3. Design** | Seven-screen user flow, UI states, re-engagement hooks | [Spec Deck](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Prototype) |
| **4. Prototype & Test** | Clickable prototype, 5-person focus group, survey | [Prototype](https://lashawnfofung.github.io/BeReal-RealProcess/) · [Survey](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Survey) |
| **5. Pitch** | Test summary, recommendation, pitch and case study videos | [Pitch](https://youtu.be/Or5O1wUj_Ow) · [Case Study](https://youtu.be/yxYclJn8ZGc) |
| **6. Revise requirements** | Updated the PRD from v1.0 (pre-test draft) to v2.0 with test results and a re-phased rollout | [PRD process & changes](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/PRD/PRD.md) · [1-pager](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/PRD/PRD_v2/BeReal_Passport_Community_Boards_-_PRD-lite_1-pager_v2.0.pdf) · [Full PRD](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/PRD/PRD_v2/BeReal_Passport_Community_Boards_-_Full_Requirements_Document_v2.0.pdf) |
| **7. Enable users** | Interactive job aid built from real prototype screens, a step-list spreadsheet and a reusable prompt | [Job aid](https://lashawnfofung.github.io/BeReal-RealProcess/Job%20Aid/BeReal_BeReal%20Passport%20and%20Community%20Boards_Interactive_Job_Aid.html) · [Process & prompt](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Job%20Aid/Prompt%20Engineering.md) · [Step list template](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Job%20Aid/Job_Aid_Steps_BeReal_Passport.xlsx) |
| **8. Plan validation** | Two-stage test plan: usability retest, then a squad-randomized A/B experiment with guardrails and ship/kill criteria | [Test Plan](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Test%20Plan/Test%20Plan.md) |


📅 See the full [Project Timeline](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Project%20Timeline.md) for dates, milestones and how the plan changed along the way.

---

## My Role

<img src="Project%20Marketing%20Images/Images/BeReal%20Passport%20Project%20Cover.png" alt="Project cover: Lashawn Fofung, UI/UX Design and Product Management, BeReal Passport and Community Boards enhancement proposal, 2026." width="600">

**UI/UX Designer and Product Manager** (solo project)

- **Research:** teardown, persona, journey mapping
- **Design:** user flow, UI states, accessibility (WCAG color contrast, keyboard navigation, screen reader support)
- **Requirements:** PRD-lite 1-pager and full PRD, versioned from draft (v1.0) to post-test (v2.0)
- **Validation:** usability testing, focus group, survey
- **Enablement:** interactive job aid and a reusable prompt for future features
- **Storytelling:** recommendation, pitch, and case study

**Tools:** Canva · Claude · Google Forms · Microsoft Word · GitHub Pages

**Why a TPM did a design program:** A strong grasp of technical delivery and business strategy is a real advantage in product design. UI/UX training closes the loop, so I can balance what's viable for the business, feasible to build, and right for the user.

---

<div align="center">

**Lashawn Fofung** · Technical Product Manager · [LinkedIn](https://www.linkedin.com/in/lashawnfofung/) · [MBA Portfolio](https://github.com/LashawnFofung/MBA-IT-Management-Portfolio) · [AI Portfolio](https://github.com/LashawnFofung/AI-Portfolio)

*Independent concept created for a UI/UX Design & Product Management Externship. Not affiliated with or endorsed by BeReal.*

</div>
