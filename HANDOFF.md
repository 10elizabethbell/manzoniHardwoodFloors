# Manzoni Hardwood Floors — handoff at ~60%

**Live:** https://10elizabethbell.github.io/manzoniHardwoodFloors/ · **Repo:** https://github.com/10elizabethbell/manzoniHardwoodFloors · **Built:** 2026-10-18 from Muse brief (run 2026-10-18, FB group sweep, "New Jersey Small Business Network")

## What's built
- **World:** a racked-out oak strip floor seen from above (random lengths, staggered joints, plain-sawn cathedral grain), Special Walnut wiped into raw sanded oak. The ground is trim white (`#f4f2ec`, neutral like the walls in Kevin's photos), with walnut ink and walnut buttons. Painter's-tape blue (`#2a67a8`) appears only on hover, focus and form outlines.
- **Hero (signature):** under "Start to finish.", a floor canvas that starts half-stained with a ragged edge. A finger or the mouse wipes stain on in any direction: `touch-action:none`, rect read every frame, rebuilds only on a real size change, pull-to-refresh off. Wet stain runs fast along the grain, slowly across it, and barely over seams. It looks darker while wet, then soaks in unevenly along the open grain. When idle, a rag works along the least-stained course. At 90% coverage it holds the finished floor for 3.2s, then a sanding pass (with dust) lifts it back to raw. One cycle is about 24s.
- **Same engine everywhere:** three course-strip dividers between sections (they stain themselves and take a finger, with `pan-y` so the page still scrolls), and a static walnut board field the two work photos are set into like inlays. One shared rAF loop, paused off screen; Reduce Motion stops the auto rag, but wiping still works.
- **Sections:** header (wordmark + `tel:` number top right), hero (two buttons: **Text Kevin a photo** opens a pre-filled SMS, **Free estimate** scrolls to the form), What I do (3 rows, each a pre-filled text; only the arrow reacts on hover; "Fully insured · Free estimates"), Big repairs are part of the job (walnut band, Kevin's voice, plus the ad's line "Special Walnut stain, 3 coats of polyurethane"), My work (2 photos + "See more of my work on Facebook"), How it works (3 steps), Free estimate form (name, town, job chips, notes; composes a text, then shows the message with Copy and Call fallbacks), close (name, "Northern New Jersey", Text Kevin), footer (name, services, phone, Facebook, insured line).
- **Tunables** at the top of the floor IIFE: `CELL ALONG ACROSS SEAM SOAK DRY BRUSH RAG AUTO_SPEED SAND_SPEED SAND_AT HOLD IDLE`.
- **Files:** `index.html` (all CSS/JS inline), `img/` (2 WebP photos ~83KB total, og.jpg 1200x630, apple-touch-icon.png).

## Assumptions I made
- **"I" voice:** the only named contact is Kevin ("Call/text Kevin"), so I treated it as a one-person business. If he runs a crew, switch to "we".
- **Copy I wrote for him (needs his OK):** the hero promise ("I handle your floor myself, from the first board pulled to the last coat of poly, and I treat your home like it's my own."), the care paragraph ("I'd rather fix a bad spot right than sand around it…"), and the step lines.
- **Colors:** there's no logo or brand color, so walnut and oak come from his finished Special Walnut floor and the white from the walls in his photos.
- **Favicon / home-screen icon:** a cream "M" on walnut, set in the site's own lettering (there's no logo).
- **Area:** "Northern New Jersey" only, as the brief says. No towns. The form asks for their town instead.
- **Texts:** the brief says he takes texts, so texting is the main action; calling is the top-right number and the footer. Pre-filled texts say "I'll send a photo of my floor" rather than claiming one is attached.
- **Photos:** the repair shot came from the ad (a phone screenshot; black bars cropped, 936x700). The finished floor is his Facebook profile picture (720px; top cropped to remove feet in the doorway). They're shown without captions and not labeled as a before/after pair.
- **Not an older-audience build:** the brief doesn't say his customers are 40+, so it has full motion. Homeowners refinishing floors may skew older; if you think so, `older-audience.md` says to make the floor a still picture.

## Placeholders and gaps
- **Email:** none found, so there's no footer email. Add it to the footer only if he gives one.
- **Photos:** only two. More finished jobs (and real before/after pairs) would strengthen My work and could feed a before/after slider.
- **Logo:** none. The header is a type wordmark.
- No hours, prices, reviews, years in business, or towns on the page, because none were found.
- **410 (Maryland) area code:** printed exactly as given.

## Questions for the owner
- Is it just you, or a crew? (This decides "I" vs "we".)
- Do you come out to look before quoting? (I removed "I come look" because the brief doesn't say so.)
- Which towns do you cover? Hours? An email for the footer?
- Any more job photos, especially before and after the same room?
- Do you have a logo, or a truck or shirt with your name on it?
- Are there other stains or finishes you're known for besides Special Walnut?

## Ideas not built (yours to pick)
- **Runner-up world:** the stain chip card, a strip of oak with named stain swatches (Special Walnut, Jacobean, Provincial…). Tapping one would recolor the hero floor and pre-fill "the color you want" in the form.
- **A finish stage in the loop:** stain → poly cure (a real wet-to-cured change inside the engine, never an overlay film) → sand. That would complete "the last coat of poly".
- Before/after slider once he sends real pairs.
- Hero hint wording per input ("Drag" on touch, "Move across" on mouse); it's "Wipe on the stain" for both right now.
- The concept roll's other grounded candidates: sanding pass, lumber bundle grade stamps, window light and dust over a fresh finish, chalk line and carpenter's pencil.

## Not verified
- Real-device touch on iPhone and Android, inside Facebook's in-app browser (tested in Playwright Chromium and WebKit with touch emulation: vertical drags stain and don't scroll).
- Real SMS handoff: that the `sms:…?&body=` pre-fill lands in Messages and Android's default SMS app.
- Frame rate on old phones (at 4x CPU throttle, frames averaged 10.6ms with an 18.6ms worst case).
- Canvas `filter: blur()` on older Safari (pre-18). Without it, the stain edge is a little blockier but still works.

## Process notes
- Unattended build: Impeccable's interactive question and decision steps were skipped (nobody was there). The direction came from concept roll `fd77705c`, assigned candidate 3 (racked boards), fused with the stain-wipe act.
- Impeccable: an all-modes sweep (all except live, onboard, shape, init, document, extract) and the finish reviewer ran; their fixes are applied. Six detector findings were triaged as intentional and ignored in `.impeccable/config.json` (system font, trim-white ground, no-JS stripe fallback, seam-line list, body-only type ramp, the chip gradient's contrast).
