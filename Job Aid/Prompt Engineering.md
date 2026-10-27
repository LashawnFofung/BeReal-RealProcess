# BeReal Passport & Community Boards — Job Aid

**[▶ Try the interactive job aid](https://lashawnfofung.github.io/BeReal-RealProcess/BeReal_Passport_Interactive_Job_Aid.html)** · **[Quick-reference version](https://lashawnfofung.github.io/BeReal-RealProcess/BeReal_Passport_Job_Aid.html)** · **[Live prototype](https://lashawnfofung.github.io/BeReal-RealProcess/)**

## Purpose

A new feature only works if people can use it on their first try. I built this job aid so that someone who has never seen Passport & Community Boards can join a board, post a stamped BeReal, and manage their boards without training or help.

User testing showed why this matters. Four of five testers said they'd open BeReal more often, but the biggest risk wasn't pressure; it was complexity. Testers noticed the extra taps between capture and stamp, and the one non-user called the flow "less authentic and overly complex." A job aid lowers that first-use barrier while the design is refined.

**Who it's for**

- **App users:** first-time and returning users learning the new feature.
- **Testers:** participants in the next round of usability testing (7–10 people), so everyone starts from the same baseline.
- **Stakeholders:** reviewers who want to see the full flow without installing anything.

## What's included

| Version | Best for | What it does |
| --- | --- | --- |
| **Interactive job aid** | Learning by doing | A click-through walkthrough of real prototype screens. Users tap the highlighted button on each screen to move to the next one, just like in the app. |
| **Quick-reference job aid** | Scanning, printing, sharing | A one-page reference with step tables, key terms, on-screen messages and troubleshooting. |

Both versions cover the same three tasks:

1. **Post a stamped BeReal** (10 steps): alert → opt in → capture → COMMUNITY BOARD → pick a board → stamp earned
2. **Check your Passport** (5 steps): Passport tab → leaderboard and stamp gallery → capsule carousel
3. **Opt in or out of boards** (3 steps): Profile → Settings → switch a board on or off

## How the interactive job aid works

- Each step shows a **real screen from the prototype**, with the button to tap outlined in yellow and a **TAP** badge.
- Tapping the highlighted button advances to the next screen. Tapping anywhere else gives a gentle nudge.
- The panel beside the screen says **what to do**, **what you're looking at**, and a **tip** where one helps (for example, "SEND posts a regular BeReal with no stamp").
- Loading screens advance on their own, just as they do in the app.
- Each task ends with a **Task complete** check and a button to start the next task.
- Back, Next and Restart are always available, and the arrow keys work on desktop.

## Process

### 1. Defined the tasks from the user flow

I started from the seven-screen habit loop in the case study and the three tasks from the focus group. I kept only the tasks a user needs on day one: post, check progress, and control participation.

### 2. Captured the real screens

Instead of redrawing screens, I scripted the clickable prototype with Playwright, a browser automation tool. The script walks through all three tasks in one session, so later tasks show earlier results (such as the CRAMMING stamp appearing as unlocked). At each step it:

- screenshots the phone screen
- records the exact position of the button to tap
- clicks it to reach the next screen

Where a pop-up blocked the next tap, such as the photo viewer, I added a step to close it rather than skip it. Before building, I reviewed a contact sheet of all 21 screens with the tap targets outlined, to confirm every highlight landed on the right button.

### 3. Wrote the copy

Each step has three parts:

- **Do this:** one action that starts with a verb and uses the exact on-screen label.
- **On this screen:** a sentence or two about what the user is looking at now.
- **Tip:** an alternative or warning, only where it helps.

I quoted on-screen messages word for word from the prototype ("Stamping your passport..", "Stamp earned! Added to CRAMMING board 🎉") and wrote at a 6th–8th grade reading level.

### 4. Built a single self-contained HTML file

Everything, including screenshots, styles and logic, lives in one HTML file. It works offline, needs no install, and runs on GitHub Pages. The layout uses BeReal's black and yellow palette:

- **Desktop:** the phone screen sits beside the instructions.
- **Phone:** the instructions sit above the screen, with compact controls.

### 5. Tested and refined

I clicked through every step on desktop (1280px) and phone (390px) widths and checked for errors and layout problems. Refinements from testing:

- Moved the **TAP** badge to the corner of the highlight so it never covers text on the screen (it was hiding the "Stamp earned!" message).
- Placed the instructions above the screen on phones so the step and the button to tap are visible together.
- Made task tabs scroll sideways so switching tasks never jumps the page.

## Accessibility

- Every tap target is a real button labeled with its instruction, so it works with a keyboard and screen readers.
- Each screen image has alt text describing what's shown.
- A **text version of all steps** sits below the walkthrough, for screen readers and printing.
- Printing hides the interactive part and prints the text version in black and white.
- Motion is reduced for users who turn on "reduce motion" in their system settings.

## What I learned

- **Real screens beat redrawn ones.** Capturing from the prototype kept the job aid accurate to the design, and it can be recaptured whenever the prototype changes.
- **Show, then tell.** Users follow a highlighted button faster than a written description of where it is.
- **Test the job aid like a product.** The overlapping badge and mobile spacing only showed up when I clicked through it myself.

## Reuse for future enhancements

The process is repeatable. I wrote a reusable prompt that captures the screens, writes the copy, builds the HTML and runs the same quality checks. For a new feature, I swap in the feature name, tasks, steps and tips, and the rest of the prompt stays the same.

## Files

| File | Description |
| --- | --- |
| `BeReal_Passport_Interactive_Job_Aid.html` | Interactive click-through job aid (self-contained, about 2 MB) |
| `BeReal_Passport_Job_Aid.html` | Quick-reference job aid (print-friendly) |
| `index.html` | Clickable prototype the screens were captured from |

---

*Concept prototype for a proposed enhancement. Not an official BeReal product.* Built by **Lashawn Fofung**, MBA, PMP, CSM, CSPO.
