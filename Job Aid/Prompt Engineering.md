# BeReal Passport & Community Boards — Interactive Job Aid

**[▶ Try the interactive job aid](https://lashawnfofung.github.io/BeReal-RealProcess/Job%20Aid/BeReal_BeReal%20Passport%20and%20Community%20Boards_Interactive_Job_Aid.html)** · **[Live prototype](https://lashawnfofung.github.io/BeReal-RealProcess/)** · **[Back to README](https://github.com/LashawnFofung/BeReal-RealProcess#readme)**

> *Independent concept created for a UI/UX & Product Management Externship. Not affiliated with or endorsed by BeReal.*

---

## Purpose

A new feature only works if people can use it on their first try. I built this job aid so that someone who has never seen Passport & Community Boards can join a board, post a stamped BeReal, and manage their boards without training or help.

User testing showed why this matters. Four of five testers said they'd open BeReal more often, but the biggest risk wasn't pressure; it was complexity. Testers noticed the extra taps between capture and stamp, and the one non-user called the flow "less authentic and overly complex." A job aid lowers that first-use barrier while the design is refined.

**Who it's for**

- **App users:** first-time and returning users learning the new feature.
- **Testers:** participants in the next round of usability testing (7–10 people), so everyone starts from the same baseline.
- **Stakeholders:** reviewers who want to see the full flow without installing anything.

<br>

## Prompt Engineering

### The prompts

I built the job aid with Claude.ai in three rounds, each prompt building on the last.

> **1.** Create a job aid for the application.

This produced a quick-reference guide: key terms, step tables for each task, on-screen messages and troubleshooting, written from the prototype's actual screens and messages.

> **2.** I want the job aid to be HTML.

Claude turned the guide into a single, self-contained HTML page in BeReal's black and yellow palette.

> **3.** Can you make the job aid similar to the app workflow, as the user clicks on buttons and pages?

This turned the job aid into an interactive walkthrough built from real prototype screens, where users tap the highlighted button on each screen to move to the next one.

> **4.** Final prompt

After the job aid was done, I had Claude write one detailed prompt that recreates it in a single pass. This is the final prompt:

```text
ROLE
You are an instructional designer and front-end developer. Build an INTERACTIVE JOB AID: a click-through walkthrough of an app feature where users tap a highlighted button on a real app screen to advance to the next screen, just as they would in the app.

FEATURE: Passport & Community Boards
APP: BeReal
AUDIENCE: Everyday BeReal users, including first-time users. No technical background.
BRAND: Black #0A0A0A · Yellow #FFDE59 · Off-white background #F7F6F1 · Success green #1F9D55
AUTHOR / CONTACT: Lashawn Fofung
LIVE PROTOTYPE LINK: https://lashawnfofung.github.io/BeReal-RealProcess/

INPUTS
A) The clickable HTML prototype: [attach Prototype/BeReal_Passport_Prototype.html]. Drive it yourself to capture screens. Start as a first-time user (the default).

TASKS AND STEPS

Task 1: Post a stamped BeReal
  1. Lock screen → tap the "12:00 AM Community Board open!!" notification
  2. Today screen with intro pop-up → tap "Got it"
  3. Today screen → tap "Opt-in to join Community Boards" (wait for the "You're in!" toast to clear)
  4. Today screen showing the six October boards → tap the capture (camera) button in the bottom nav
  5. Camera → tap the shutter
  6. Caption and post type → tap "COMMUNITY BOARD" (Tip: SEND posts a regular BeReal to My Friends, with no stamp)
  7. Board select → tap the CRAMMING board
  8. CRAMMING selected (card turns white, lock opens) → tap "Stamp & post to CRAMMING"
  9. AUTO: "Stamping your passport.." loading screen
  10. Success pop-up "Stamp earned! Added to CRAMMING board 🎉" → tap "See it on the board" (Tip: "Open my Passport" goes straight to the collection)
  END: Post in the CRAMMING board feed with its passport stamp, next to the squad's posts

Task 2: Check your Passport (continue from Task 1's end screen)
  1. Board feed → tap the "Passport" tab
  2. Passport (squad leaderboard + October stamp gallery with CRAMMING unlocked) → scroll down and tap "View October Capsule Carousel"
  3. October capsule in Memories → tap any photo (Tip: "Board details" shows who took part)
  4. Photo open full size → tap the right arrow for the next photo
  5. Next photo → tap X to close
  END: Back on the capsule. When a month ends, its boards stay in Memories as capsules

Task 3: Opt in or out of boards (continue from Task 2's end screen)
  1. Capsule screen → tap "Profile" in the bottom nav
  2. Settings → under Features, tap "Opt-in - Community Board" (Tip: "Opt-out - Community Board" opens the same list)
  3. Community Board list → tap the COFFEE row to switch it off
  END: COFFEE is off and the app confirms "Left COFFEE." Turning every board off returns to the opt-in screen. Regular BeReal works the same either way

HOW TO BUILD IT

1. Capture screens
- Use a headless browser (Playwright) at device scale 2. Walk through all three tasks in ONE continuous session, so the CRAMMING stamp shows as unlocked in Task 2.
- For each step: scroll the target into view, screenshot ONLY the phone frame (#phone), record the target's bounding box as FRACTIONS of the frame (x, y, w, h from 0 to 1), then click it. Wait for toasts and animations to finish before the next capture.
- If a modal or overlay blocks the next tap (the intro pop-up, the photo viewer), add a step to close it. Never skip it.
- Before building, make a contact sheet of all screens with the target boxes drawn in red. Confirm every box sits on the right button.

2. Write the copy (per step)
- "Do this": one action, starting with a verb, using the exact on-screen label ("Tap Stamp & post to CRAMMING.").
- "On this screen": 1–2 sentences describing what the user is looking at NOW, in plain words.
- "Tip" (optional): use the tips listed above.
- End step: a short "What happened" summary (use the END lines above).
- Plain language, 6th–8th grade reading level, sentences under 20 words, second person. Quote on-screen messages exactly. Don't invent buttons, screens or messages.

3. Build ONE self-contained HTML file
- No external CSS, JS, fonts or images. Embed screenshots as base64 JPEG (600px wide, quality about 80). Keep the file under about 3 MB.
- Keep the step data in a single JS array: {task, kind: "tap" | "auto" | "end", do, screen, tip, box, img}.

LAYOUT
- Header (black): title "BeReal Passport & Community Boards Job Aid", subtitle "Interactive walkthrough. Tap the highlighted button on each screen to move through the app, just as you would on your phone.", and task tabs: "1 Post a stamped BeReal", "2 Check your Passport", "3 Opt in or out of boards" (active = yellow pill; completed = green ✓).
- Desktop (two columns): the phone screen on the left (height about 76vh, rounded corners, soft shadow), and a white instruction panel on the right (sticky).
- Panel contents, in order:
  - "Task N · Step X of Y" label and a black progress bar.
  - The "Do this" text as the heading.
  - The "On this screen" text.
  - A tip box (pale yellow #FFF6CC, left border #E9C935).
  - Buttons: ← Back, Next → (black; turns yellow on hover), ↺ Restart.
  - A small hint below the buttons: "use ← → keys".
- Phone (under 820px wide): the instruction panel ABOVE the screen in a compact form, with smaller text, no "On this screen" label, and all buttons on one row. Task tabs scroll sideways. The screen is about 86vw wide. No sideways page scroll.

BEHAVIOR
- Hotspot: a transparent button placed over the target box (slightly padded), with a 3px yellow border, a pulsing yellow glow and a small yellow "TAP" badge on its top-right corner. The badge must never cover text on the screen.
- Tapping the hotspot goes to the next step. Tapping anywhere else on the screen shakes the hotspot and shows "Tap the highlighted button to continue."
- The "Stamping your passport.." step shows a spinner in the panel and advances after about 1.6 seconds.
- End steps show a green "✓ Task complete" badge, mark the tab done, and turn Next into "Next task: [name] →". The last task's button becomes "Start over ↺".
- Tabs jump to the first step of that task. Restart returns to the current task's first step. Back is disabled on step 1.
- Arrow keys go back and forward. Screens crossfade quickly. Respect prefers-reduced-motion.
- Changing tabs must never jump the page vertically. Scroll the tab row sideways only.

ACCESSIBILITY AND PRINT
- The hotspot button's aria-label is the step's "Do this" text. Each screen image gets alt text from "On this screen". The panel is aria-live="polite". Focus states must be visible.
- Below the walkthrough, add a collapsible "Text version of all steps (for printing or screen readers)": each task as a numbered list (bold action, description, tip) plus its "Done" line.
- Print styles: hide the interactive part, open and print the text version, use white background and black text, and avoid splitting a task across pages.
- Footer: "BeReal Passport & Community Boards · Concept prototype by Lashawn Fofung · Try the live prototype at lashawnfofung.github.io/BeReal-RealProcess" (the link must be clickable).

QUALITY CHECKS (do these before handing it over)
1. Click through all 21 screens (18 steps + 3 end screens) by tapping only the hotspots. Every step must advance, with no console errors.
2. Screenshot at 1280px and at 390px wide. Confirm the phone is fully visible on desktop, there's no sideways scroll on mobile, and no "TAP" badge covers text (check the "Stamp earned!" pop-up especially).
3. Confirm the step counts read Task 1: 10 steps, Task 2: 5 steps, Task 3: 3 steps, and each task ends on a "Task complete" screen.
4. List anything you were unsure of for me to confirm.

DELIVERABLE
The single HTML file named "BeReal_BeReal Passport and Community Boards_Interactive_Job_Aid.html", plus a 2–3 line note of what it covers and anything to double-check.
```

<br>

### The job aid

The interactive job aid covers three tasks:

1. **Post a stamped BeReal** (10 steps): alert → opt in → capture → COMMUNITY BOARD → pick a board → stamp earned
2. **Check your Passport** (5 steps): Passport tab → leaderboard and stamp gallery → capsule carousel
3. **Opt in or out of boards** (3 steps): Profile → Settings → switch a board on or off

**How it works**

- Each step shows a **real screen from the prototype**, with the button to tap outlined in yellow and a **TAP** badge.
- Tapping the highlighted button advances to the next screen. Tapping anywhere else gives a gentle nudge.
- The panel beside the screen says **what to do**, **what you're looking at**, and a **tip** where one helps (for example, "SEND posts a regular BeReal with no stamp").
- Loading screens advance on their own, just as they do in the app.
- Each task ends with a **Task complete** check and a button to start the next task.
- Back, Next and Restart are always available, and the arrow keys work on desktop.

- **Try it:** [Interactive Job Aid](https://lashawnfofung.github.io/BeReal-RealProcess/Job%20Aid/BeReal_BeReal%20Passport%20and%20Community%20Boards_Interactive_Job_Aid.html)

<br>

### How it was built

**1. Defined the tasks from the user flow.** I started from the seven-screen habit loop in the case study and the tasks from the focus group. I kept only what a user needs on day one: post, check progress, and control participation.

**2. Captured the real screens.** Instead of redrawing screens, Claude scripted the [clickable prototype](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Prototype/BeReal_Passport_Prototype.html) with Playwright, a browser automation tool. The script walks through all three tasks in one session, so later tasks show earlier results (such as the CRAMMING stamp appearing as unlocked). At each step it:

- screenshots the phone screen
- records the exact position of the button to tap
- clicks it to reach the next screen

Where a pop-up blocked the next tap, such as the photo viewer, a step was added to close it rather than skip it. A contact sheet of all 21 screens, with the tap targets outlined, confirmed every highlight landed on the right button.

**3. Wrote the copy.** Each step has three parts:

- **Do this:** one action that starts with a verb and uses the exact on-screen label.
- **On this screen:** a sentence or two about what the user is looking at now.
- **Tip:** an alternative or warning, only where it helps.

On-screen messages are quoted word for word from the prototype ("Stamping your passport..", "Stamp earned! Added to CRAMMING board 🎉"), at a 6th–8th grade reading level.

**4. Built one self-contained HTML file.** Screenshots, styles and logic all live in a single file. It works offline, needs no install, and runs on GitHub Pages.

- **Desktop:** the phone screen sits beside the instructions.
- **Phone:** the instructions sit above the screen, with compact controls.

**5. Tested and refined.** Every step was clicked through at desktop (1280px) and phone (390px) widths. Fixes from testing:

- Moved the **TAP** badge to the corner of the highlight so it never covers text on the screen (it was hiding the "Stamp earned!" message).
- Placed the instructions above the screen on phones so the step and the button to tap are visible together.
- Made task tabs scroll sideways so switching tasks never jumps the page.

<br>

### Accessibility

- Every tap target is a real button labeled with its instruction, so it works with a keyboard and screen readers.
- Each screen image has alt text describing what's shown.
- A **text version of all steps** sits below the walkthrough, for screen readers and printing.
- Printing hides the interactive part and prints the text version in black and white.
- Motion is reduced for users who turn on "reduce motion" in their system settings.

<br>

### Reusable prompt for future enhancements

The [final prompt](#the-prompts) above is reusable. For a new feature, I copy it with the copy button in the top-right corner of the prompt box, then swap in the feature name, tasks, steps, tips and step counts. The rest stays the same.

<br>

### Starting from scratch: the step list spreadsheet

The job aid is only as good as its step list. To make the process repeatable, I turned the steps into a spreadsheet that gets uploaded with the final prompt. The AI follows it row by row instead of guessing the flow from the prototype.

**What's in the spreadsheet**

- **One row = one screen** the user sees, in the order they see it.
- **Three step types:** **Tap** (the user taps something), **Auto** (the screen moves on by itself, like a loading screen) and **End** (the task is finished).
- **Columns:**

| Column | What it holds | BeReal example |
| --- | --- | --- |
| Task # / Task Name | Which task the step belongs to | 1 · Post a stamped BeReal |
| Step # / Step Type | Order within the task, and Tap, Auto or End | 3 · Tap |
| Starting Screen | Where the user is before the step | Today screen |
| Action (Do this) | One action, starting with a verb | Tap Opt-in to join Community Boards. |
| Tap Target | The exact on-screen label to highlight | "Opt-in to join Community Boards" |
| On This Screen | What the user is looking at, in plain words | Boards stay off until you join. |
| Result / Next Screen | What happens after the tap, with messages quoted exactly | "You're in! Joined all 6 October boards." |
| Tip | An alternative or warning, only where it helps | You only opt in once. |
| Builder Notes | Instructions for whoever builds it; not shown to users | Wait for the toast to clear. |

- **A Task Summary** counts each task's steps and flags any task missing its END row, so gaps show up before upload. For BeReal it reads 10, 5 and 3 steps (18 in total), each with an END row.

**How I use it**

1. **Walk through the prototype** start to finish and add one row for every screen, in order.
2. **Copy button labels exactly** as they appear on screen, including capitals and punctuation.
3. **End every task with an END row** that says what the user accomplished.
4. **Check the Task Summary** for step counts and "Yes" on every END row.
5. **Upload three things together:** the step list spreadsheet, the prototype HTML and the final prompt.
6. **Add one line to the prompt** so the AI uses the spreadsheet as its source:

```text
Use the attached steps spreadsheet (BeReal Steps tab) as the TASKS AND STEPS list. Follow it row by row: one screen per row, in order. Use the Tap Target column for the hotspot, Action for "Do this", On This Screen for the description and Tip for the tip box. Don't add, skip or reword steps; if a row is unclear, list it under open questions.
```

**Why a spreadsheet**

- **It separates content from build.** I can review and edit the steps without touching code or the prompt.
- **It's the single source of truth.** The prompt, the job aid and its printable text version all come from the same rows.
- **It scales to any feature.** For a new enhancement, I clear the rows, walk through the new prototype and fill them in. The prompt stays the same.

- **View:** [Step list spreadsheet](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Job%20Aid/Job_Aid_Steps_BeReal_Passport.xlsx) — one file with three tabs: **How to Use**, **BeReal Steps** (filled in) and a blank **Template** for future features. For a new feature, fill in the Template tab and change "BeReal Steps tab" to "Template tab" in the prompt line.

<br>

## What I learned

- **Real screens beat redrawn ones.** Capturing from the prototype kept the job aid accurate to the design, and it can be recaptured whenever the prototype changes.
- **Show, then tell.** Users follow a highlighted button faster than a written description of where it is.
- **Test the job aid like a product.** The overlapping badge and mobile spacing only showed up when every step was clicked through.
- **Iterate the prompt, then save it.** Three short prompts got to the final design; one detailed prompt now reproduces it for the next feature.
- **Write the steps down first.** A step list spreadsheet keeps the AI on the exact flow and makes the next job aid a fill-in-the-rows task.

<br>

## Files

| File | Description |
| --- | --- |
| [`Job Aid/BeReal_BeReal Passport and Community Boards_Interactive_Job_Aid.html`](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Job%20Aid/BeReal_BeReal%20Passport%20and%20Community%20Boards_Interactive_Job_Aid.html) | Interactive click-through job aid (self-contained, about 2 MB) |
| [`Job Aid/Prompt Engineering.md`](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Job%20Aid/Prompt%20Engineering.md) | This page: purpose, process, reusable prompt and step list |
| [`Job Aid/Job_Aid_Steps_BeReal_Passport.xlsx`](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Job%20Aid/Job_Aid_Steps_BeReal_Passport.xlsx) | Step list spreadsheet: BeReal Steps tab (filled in, upload with the prompt) and a blank Template tab for future features |
| [`Prototype/BeReal_Passport_Prototype.html`](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Prototype/BeReal_Passport_Prototype.html) | Clickable prototype the screens were captured from |

---

Built by **Lashawn Fofung**, MBA, PMP, CSM, CSPO.
