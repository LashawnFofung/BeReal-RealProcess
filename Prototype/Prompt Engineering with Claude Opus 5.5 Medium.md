
## Prompt Engineering

### The prompt

> As a developer and product manager, I would like to create a prototype for my proposed BeReal enhancement, **BeReal Passport & Community Boards**. I have a presentation showing how the user flow and enhancements should look.

I started from a detailed slide deck I designed in Canva, covering the full user flow, UI states, and UI/UX design for the feature.

- **View:** [Slide Deck](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Prototype/BeReal%20Prototype%20-%20Real%20Passport%20And%20Community%20Boards.pptx)
- **View:** [PDF version](https://github.com/LashawnFofung/BeReal-RealProcess/blob/main/Prototype/BeReal%20Prototype%20-%20Real%20Passport%20And%20Community%20Boards.pdf)

<br>

### The prototype

Using the deck as the spec, I used Claude.ai to build a clickable prototype of the seven-screen flow: Today screen, capture toggle, board select, post confirmation, capsule, Passport and leaderboard, and settings/opt-out. It includes the empty, loading, success and error states from the deck, and a demo panel for switching between first-time and returning users.

- **Try it:** [Live Prototype with Claude.AI](https://claude.ai/artifact/QouixAtcmRQXoxXEiUsXgm)

<br>

### Hosting the prototype with GitHub Pages

To make the prototype viewable in any browser, with no login or sharing settings needed, I hosted it on GitHub Pages.

**Steps**
1. **Uploaded the prototype:** added `BeReal_Passport_Prototype.html` to the `Prototype` folder. It's a single self-contained file: all screens, images and interactions are built in, so it needs no build step or server.
2. **Turned on GitHub Pages:** in **Settings → Pages**, set the source to **Deploy from a branch** and chose **main / (root)**.
3. **Made the prototype the homepage:** added an `index.html` file at the repo root that redirects visitors straight to the prototype, so the site's main URL opens it.
4. **Confirmed the deploy:** checked the **Actions** tab for a green "pages build and deployment" run, then tested the live link.

**Troubleshooting**
- **The site showed only the README.** With no `index.html` in the repo root, GitHub Pages uses `README.md` as the homepage. Adding the redirect file fixed this.
- **The homepage returned a 404.** The redirect file was named `Index.html`. GitHub Pages is case-sensitive and only recognizes lowercase `index.html`, so renaming the file fixed it.
- **The Save button was greyed out.** GitHub only enables Save when a setting changes. Switching the branch to **None**, saving, then switching back to **main** started a fresh deploy.

- **View:** [lashawnfofung.github.io/BeReal-RealProcess](https://lashawnfofung.github.io/BeReal-RealProcess/)

<br>

### The promo reel

I then had Claude turn the prototype screens into a vertical promo reel and wrote a voiceover script timed to each scene. I recorded the voiceover myself, uploaded it to the chat, and Claude synced my voice to the video.

- **Watch:** [Promo Reel](https://youtube.com/shorts/exXoJ6NqmbI)
