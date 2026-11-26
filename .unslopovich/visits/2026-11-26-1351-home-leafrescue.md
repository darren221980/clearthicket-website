Dr. Unslopovich's diagnosis
Verdict: Honest now and easy to use from a keyboard. It still downloads a 421 KB icon font to draw one hamburger, and the LeafRescue banner's alt text describes a picture that isn't there.
Stack: Static HTML, CSS and vanilla JS on GitHub Pages (per chart).
Reviewed: Home and LeafRescue on the live site (clearthicket.co.uk, deploy acda3f3 finished 13:32), the day's treatment. Headless Chrome: 1920, 1280, 640 (= 1280 at 200% zoom) and 375. Keyboard tab-through of both pages through the Chrome DevTools protocol. Contrast computed from the theme colours.
Score: 21/24 Discharged  Task path 4 · Truth 3 · Native fit 4 · States 4 · Access 3 · Specificity 3
(Same total as the treatment estimate. Native fit, States and Access are now measured, not estimated.)
Performance: Not profiled. Static lead: both pages load the Material Symbols Rounded font (421 KB) for a single "menu" icon; its stylesheet is render-blocking.

Noticeable
- leafrescue/index.html hero banner: the alt text written in the treatment, "LeafRescue: a plant photo with its diagnosis", is wrong. The image is the Play feature graphic: the app icon, the name and two lines of small text. Its baked-in text also says "100% private BYOK Gemini" and "AI BOTANICAL CARE", the wording removed from the page. -> Use a real screen in its place (images/screen-diagnose.png is already in the folder), with alt text that describes it. If the banner stays, give it alt="" because the heading already says what it says.
- index.html:39 and leafrescue/index.html:32: Material Symbols (421 KB font plus a render-blocking stylesheet) is loaded for one glyph, the menu button. -> Replace the icon with a 24 px inline SVG (three lines and a cross for the open state) and drop the font link. The same applies on every other page that uses only the menu icon.

Minor
- index.html hero: the headline runs to three lines at 1280 and 1920 because .hero-compact h1 caps it at 900 px. -> max-width about 1100px gives two lines at 1280 and up; text-wrap: balance stays.
- The hero glow (.hero::before) is cut off with a visible straight edge at the bottom of the shorter hero, at every width. -> Lower the glow or fade it out before the section edge.
- leafrescue/index.html nav says Features, Preview, Pricing, FAQ, but the sections are now titled "What it does", "How it works" and "Questions". -> Match the labels to the headings.
- --text-muted (#7C8F85) on --surface (#162B22) is 4.37:1, just under 4.5. Not used for body text on the two reviewed pages; check before using it inside cards.

Worth keeping
- Keyboard: every stop has a visible 3 px focus ring, in reading order, starting with Skip to content. On LeafRescue, "Get it on Google Play" is the first stop after the nav.
- 200% zoom: both pages reflow cleanly at 640 CSS px, with nothing clipped and no sideways scroll.
- Contrast: body text 7.98:1, green labels and links 6.28:1, amber badge 8.97:1, button text 4.53:1 and up.
- Live: social preview image (200) and 404 page (404 status) are deployed.

Not checked
- Performance profiling (no Lighthouse run).
- A screen reader pass (labels and order checked, nothing listened to).
- Hobnote, Mendwise, BreatheRun, About, Contact and the privacy pages (still carry the claims listed in the 13:50 treatment notes).

Treatment (2026-11-26, Darren: "fix all")
- LeafRescue hero: the Play feature graphic (baked-in "100% private BYOK Gemini") is replaced by the real plant screen (images/screen-diagnose.png) in a phone frame, alt text describing it.
- Menu icon: inline SVG (menu, and a cross when open via aria-expanded) on the 13 pages whose only icon was the menu. The Material Symbols stylesheet (421 KB font) is no longer loaded on those pages. Hobnote, Mendwise and BreatheRun pages still use other icons, so they keep the font.
- Home headline: two lines at 1280 and up (max-width 1100px).
- Hero glow: smaller and centred in the compact hero, so the hero no longer clips it into a straight edge.
- LeafRescue nav: What it does, How it works, Pricing, Questions, Privacy, Support (matches the section titles).
- --text-muted on --surface (4.37:1): not used on these pages; no change.
Checked over a local server with headless Chrome: home at 375, 1280, 1920; LeafRescue at 375 (menu opened: icon turns to a cross, aria-expanded true) and 1280; About at 375 with the menu open. Detector: 0 hits.
Not checked: performance profiling, screen reader, the live site after deploy.
