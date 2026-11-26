Dr. Unslopovich's diagnosis
Verdict: A tidy, well-built site that says your photos never leave your phone, right above three apps that send them to Google, and hides the one install button that matters below the pricing.
Stack: Static HTML, CSS and vanilla JS (GitHub Pages, clearthicket.co.uk). Dark-only theme ("forest"), Manrope + Material Symbols from Google Fonts.
Reviewed: Home (index.html) and LeafRescue (leafrescue/index.html), the live app's page. Visitor tasks: understand what the studio makes, then pick an app and install it. Screenshots from headless Chrome at 1280x800, 1920x1080, a full 1280 page, and 375 and 768 inside an iframe. No keyboard tab-through, no 200% zoom, no screen reader.
Score: 14/24 Admitted  Task path 2 · Truth 2 · Native fit ~3 · States ~3 · Access ~2 · Specificity 2
Performance: Not profiled. Static leads: two render-blocking Google Fonts stylesheets, one of them the Material Symbols font for about 10 icons; the 512 px app icons show at about 56 px (28 to 61 KB each, small).

Critical
- index.html:377-378 "Your photos, running logs, and garden databases stay on your device where they belong." LeafRescue, Mendwise and Hobnote send photos to Google Gemini with the user's key. A privacy claim that is untrue for three of the four apps, on the site the Play listings link to. -> Say what actually happens: "No accounts, no ads, no analytics. Your data is stored on your phone. Photos you choose to diagnose go straight from your phone to Google Gemini with your own key, never through our servers."
- leafrescue/index.html:117 "100% Client-Side Privacy" and index.html:105 "uncompromising client-side privacy architectures": same problem in short form. -> Same wording as above, or "No accounts. No servers of ours."

Noticeable
- leafrescue/index.html:120-127 The live app's page has no install button above the fold. The hero offers "See the App" and "How it Works"; the only Play link is in the pricing block (line 361), far down. -> Make the primary hero button "Get it on Google Play" (the Play link) and keep "How it works" as the secondary.
- leafrescue/index.html:116 "Available on Google Play" sits beside a clock ("schedule") icon, the icon the home page uses for "Coming soon". -> Use a check or the Play mark, or no icon.
- leafrescue/index.html:105-109 "clinical AI accuracy" and "Gemini 3.8 Flash": nobody measured the accuracy, and the app prefers gemini-2.0-flash then gemini-1.5-flash (GeminiLeafRescueClient.kt:154, :226, :279); 3.8 appears only in a comment. -> "Find out what's wrong with your houseplant from one photo." Name the model only if it is the one the app uses, or say "Google Gemini".
- index.html:155 and 24 other spots: Material Symbols spans (check_circle, schedule, shield_person, payments, bolt) have no aria-hidden, so a screen reader reads "check circle" before every bullet, and while the font loads, sighted visitors see the raw words. -> Add aria-hidden="true" to every decorative icon span (only 2 of 25 have it).
- index.html:22 og:image points to images/social-preview.png, which does not exist. Shared links to the home page get no preview image. -> Add a 1200x630 image or point at an existing one.
- index.html:92-119 At 1280x800 the hero fills the screen and shows no app, no icon and no screenshot; the first app appears after a scroll. The headline "Thoughtful apps crafted with purpose, precision & privacy." could belong to any studio. -> Shorten the hero and bring the four app icons, or the app row itself, into the first screen. Let the headline say what the apps are for.
- leafrescue/index.html:66-84 At 375 wide the header breaks onto two rows: the "Clear Thicket Studio" pill and the logo take the first row, and the menu button wraps underneath at the left. -> Below the nav breakpoint, hide the pill text (keep an arrow or move the link into the menu) so logo and menu fit on one row.
- Generated look, both pages: an emoji eyebrow pill over a gradient headline (style.css:486), small capitals above every heading ("Our Creations", "The Clear Thicket Ethos", "The Developer"), three icon-tile ethos cards, a check icon on every bullet, an initials "DB" avatar, and every section fading up on scroll. LeafRescue repeats the same hero. What is specific to Clear Thicket is the app icons, the LeafRescue feature graphic and the no-subscription stance; that is where the page should lead. -> See Ask first.

Minor
- index.html:240-354 At 1280 the app grid is 3 + 1: BreatheRun sits alone on a second row beside empty space, and the action rows differ per card ("Discover Hobnote" wraps to two lines beside a small "Privacy" link; LeafRescue and BreatheRun stack Google Play underneath). -> Two columns of two at desktop, and the same action row on every card (main link, then Play or Privacy as a text link).
- index.html:222, 226 Developer terms in user copy: "(WorkManager)", "Android Keystore", "BYOK", "Multimodal". -> "Daily watering reminders", "Your key is stored securely on your phone".
- index.html:399, 422 "fluid 120Hz transitions", "buttery-smooth", "zero dark patterns": claims nobody measured. -> Cut, or replace with something checkable ("Works offline", "No account needed").
- Voice switches between "We build" (hero, ethos) and "I am an independent software engineer" (bio). It is one person. -> Pick "I" throughout, or the studio name.
- leafrescue/index.html:366 "Google Play in-app product ID: leafrescue_pro_unlock" shown to visitors. -> Remove.
- No 404.html. GitHub Pages shows its own 404 for old links. -> Add a short one with links to the four apps.
- script.js:2 header says "BreatheRun Website"; leafrescue/ carries its own copies of style.css, themes.css and script.js, so fixes must be made twice.

Ask first
- Hobnote is marked "Coming Soon to Google Play" on the home page, but version 27 has Play release notes. If it is in closed testing, "coming soon" is right; if it is public, the badge and a Play link should change.
- The hero and section style (emoji pill, gradient headline, small-caps eyebrows, icon-tile cards) is the site's current visual identity. Replacing it with a quieter layout led by the app icons and screenshots is a redesign, so it is your call.

Waived
- Privacy pages for ForkTrace, Serum Sense and Clearspoken are in the sitemap but not linked from the home page: they exist for Play listings of unreleased apps. Record in the chart if that is right.

Worth keeping
- Real controls throughout: links are <a href>, the menu is a <button> with aria-expanded and Escape to close, there is a skip link, and focus-visible rings use the accent colour.
- Reduced motion is respected in both CSS and script.js, and the reveal states are scoped to .js, so the page still shows everything with JavaScript off.
- No horizontal scroll at 375 on the home page.
- Honest pricing: one price, the free allowance stated, no subscription.
- No analytics libraries in the LeafRescue, Hobnote or BreatheRun builds, so "no analytics" is true.

Not checked
- Performance (not profiled; no Lighthouse run).
- Keyboard tab order, 200% zoom, a screen reader pass, and measured contrast of the muted text on the dark green.
- The hobnote, mendwise, breatherun, about, contact and privacy pages.
- The live site (screenshots are of the local files at 145eb34).
