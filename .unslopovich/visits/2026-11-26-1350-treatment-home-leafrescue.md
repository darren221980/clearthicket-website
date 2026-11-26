Dr. Unslopovich's treatment
Verdict: The site now tells the truth about where photos go, puts the apps on the first screen, and lets a LeafRescue visitor install it without scrolling past the price.
Case: Heavy (Task path 2, Truth 2). Darren: "fix all", 2026-11-26. Hobnote confirmed in closed testing, so "Coming soon" stays.
Scope: index.html, leafrescue/index.html, shared style.css and script.js, new 404.html and images/social-preview.png, one line in leafrescue/support.html.
Score: 14 -> 21/24 Discharged  Task path 2 -> 4 · Truth 2 -> 4 · Native fit ~3 -> ~3 · States ~3 -> ~4 · Access ~2 -> ~3 · Specificity 2 -> 3

Direction
- Product: one person's small Android apps for the kitchen, plants, home repair and running; no accounts, pay once.
- Use: a visitor on a phone, often arriving from a Play listing, deciding in under a minute.
- Character: plain-spoken, honest, outdoorsy.
- Bright spot: the four app icons.
- Signature: the logo's forest-green ring line, kept on the top edge of the app cards and the 1200x630 preview.

Changes
Home
- Hero: emoji pill, gradient headline and scroll arrow removed. New headline "Small Android apps for the kitchen, the garden, the toolbox and the run." First-person intro. The four app icons link to their pages from the first screen.
- Apps: 2 x 2 grid (was 3 + 1). Same action row on every card: "About <app>" button plus a text link (Google Play for live apps, Privacy for the rest). Icon-per-bullet removed (plain list, green markers). Jargon removed (WorkManager, Keystore, BYOK, Multimodal). LeafRescue no longer names "Gemini 3.8 Flash".
- "How the apps work": true privacy wording (stored on the phone; photos and recipes go from the phone to Google Gemini with your own key; no Clear Thicket server). Icon tiles and card boxes removed. "120Hz" removed.
- "Who makes them": "DB" initials avatar removed, first person, no "buttery-smooth".
- Small-caps eyebrows removed from section headings; scroll fade-ins removed.
- og:image now exists (images/social-preview.png, rendered from the logo and app icons). Meta descriptions match the new copy.
LeafRescue
- Hero: "Photograph a sick leaf. Find out what's wrong." Primary button "Get it on Google Play" (was "See the App"); secondary "See how it works". Availability line has no clock icon and states the price.
- "Clinical AI accuracy", "Gemini 3.8 Flash", "high confidence scores", "100% Client-Side Privacy" removed. FAQ no longer says the key never leaves the phone (it is sent to Google with each request).
- Icon tiles, check icons, eyebrows, product ID line and scroll fade-ins removed. WorkManager wording replaced.
- support.html: "Gemini 3.8 Flash model" -> "the Gemini model the app uses".
Shared
- style.css: hero headline solid colour site-wide (was gradient text), no hover lift on cards, sentence-case category labels, .text-link with 44 px target, phone header keeps logo and menu on one row (the studio link shrinks to an arrow under 520 px; affects every app page).
- 404.html added (GitHub Pages uses it), with root paths so it works at any depth.
- leafrescue/style.css, themes.css, script.js deleted: identical copies nobody loaded.

Self-check
1. Cover the logo: the app icons, the four named jobs and the forest palette carry it; not a template.
2. Neighbour test: another studio would not open with its four app icons under a line naming kitchen, garden, toolbox and run.
3. Containers: down (ethos cards, icon tiles, avatar ring, eyebrow pills gone).
4. Colours: green for actions and links, amber for "coming soon", green for "on Google Play"; status is also in words.
5. Dots and pills: only the two status pills remain, both labelled in text.
6. Task: the LeafRescue install button is now the first button on the page; app pages are one tap from the home hero.
7. Detector: 0 hits on the changed files (was 7).
8. Fresh look: not run (no sub-agent started).
9. Not checked below.

Screens checked (headless Chrome): home at 375, 768, 1280 (fold and full), 1920; LeafRescue at 375 and 1280; 404 over a local server; Hobnote and About at 1280 for shared-CSS side effects (headlines now solid, otherwise unchanged).

Not checked
- Performance (not profiled).
- Keyboard tab-through, 200% zoom, screen reader.
- The live site after deploy.

Next visit
- hobnote/index.html, about.html and the privacy pages still use "100% Local-First Privacy", "Zero Telemetry", "120Hz smooth scrolling", "My apps run locally" and the emoji-pill hero. The privacy pages say "operates entirely client-side"; the policies should say photos are sent to Google Gemini.
