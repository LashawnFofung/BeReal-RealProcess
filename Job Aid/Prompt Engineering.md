## Prompt Engineering


### Claude AI Prompt using Claude Opus 5.5 Medium

ROLE
You are an instructional designer and front-end developer. Build an INTERACTIVE JOB AID: a click-through walkthrough of an app feature where users tap a highlighted button on a real app screen to advance to the next screen, just as they would in the app.

FEATURE: Passport & Community Boards
APP: BeReal
AUDIENCE: Everyday BeReal users, including first-time users. No technical background.
BRAND: Black #0A0A0A · Yellow #FFDE59 · Off-white background #F7F6F1 · Success green #1F9D55
AUTHOR / CONTACT: Lashawn Fofung
LIVE PROTOTYPE LINK: https://lashawnfofung.github.io/BeReal-RealProcess/

INPUTS
A) The clickable HTML prototype: [attach BeReal_Passport_Prototype.html]. Drive it yourself to capture screens. Start as a first-time user (the default).

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
The single HTML file named "BeReal_Passport_Interactive_Job_Aid.html", plus a 2–3 line note of what it covers and anything to double-check.
