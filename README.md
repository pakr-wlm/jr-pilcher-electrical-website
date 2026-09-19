# J.R. Pilcher Electrical Contractor, Inc.

Homepage-only teaser. Two outputs: `python build.py` makes the single self-contained `index.html`; `python build.py --hosted` makes `hosted/` (72 KB HTML + real image files) where `loading="lazy"` really defers downloads. Use `hosted/` when it goes on a server. Edit `index.src.html` + `styles.css`, run `python build.py`, output is the self-contained `index.html` (~0.8 MB, images embedded as WebP).
Verifier: `0 FAIL, 2 WARN` (empty TO_EMAIL; 15 inert nav links because there is no Reviews link, both intentional).

## Audit of their current site (jrpilcherelectrical.com, GoDaddy, 4 pages)
Home is a stock-photo hero with the company name and "Industrial Electrical Work" run together, an About story and a phone number.
Services page is a bare 12-item list. Our Work is a real 18-photo gallery of industrial jobs, but it sits on its own page. Contact is
a form with reCAPTCHA, no email shown. No reviews, no logo, no hours, no license number. Copyright 2024.

## Real data used (source)
- Name, phone (770) 474-5339, "Industrial Electrical Work": their site + Google listing
- About story (52 yrs, Air Force, 17 yrs plastics, Master Electrician, own business 1993, licensed GA + AL): their homepage
- 12 services: their Services page
- Guarantee "We will not leave the job until you are satisfied": their homepage
- Photos (WebP, hero 1600w ~185 KB, tiles 720w ~30-40 KB each, hero eager + high priority, rest lazy + async decode): hero + 9 gallery tiles + About are from the Photo Gallery on /our-work (18 uploaded phone photos of industrial jobs)

## Placeholders
- Logo: none exists. Bolt badge + text wordmark is a stand-in. Primary color #59798e is the button color sampled from their own site (computed style); yellow #f2c200 is a chosen accent for the hero Call button only.
- `TO_EMAIL` is empty. No email is published anywhere (contact page is a form only; directory listings hide it). Until set, the form says to call.
- Service card one-liners are paraphrases of the service names; no extra claims.

## Conflicts / caveats
- **Address does not agree, so no town appears on the page.** His own Contact page: 2107 County Road 682, Coffee Springs, Alabama 36318.
  Google Maps (unclaimed listing): 38 Copeland Ln, Stockbridge, GA 30281 (hours 7-7 Mon-Sat). Yelp/YP listings: 260 Pinehurst Dr,
  Stockbridge, GA. Ask J.R. where he is based, then add the town, a map and LocalBusiness address.
- The man in the About photo (standing at a disconnect cabinet) is not named on their site, so the page does not call him J.R.
  Confirm before captioning.
- The 9 remaining gallery photos (18 total) were left out: 3 near-duplicates of the same wall, an empty wall, a wastewater tank
  and a shrink-wrap machine. Easy to add.
- Google shows no rating and no reviews. No reviews section, no aggregateRating.

## Not used and why
Street address/town/hours (conflicting), reviews (none), emergency/24-7 (never claimed), free estimates (never claimed), license number
(not published), GoDaddy stock hero and tools photos (replaced by real job photos).

## Next steps for the owner (local SEO angle)
1. Confirm the business address; claim and verify the Google Business Profile so the address, hours and services are correct.
2. Ask industrial customers for Google reviews (currently zero).
3. Publish a customer-facing email address and license number.
4. Move the Our Work photos onto the homepage and label them with what and where (plant, machine, control panel).
5. List the towns/counties served in Georgia and Alabama.

## After launch
Set canonical + og:image, add the domain, then run seo-page / seo-technical / seo-google against the live URL.

## UX/UI pass (ui-ux-pro-max skill, installed in `.claude/skills/ui-ux-pro-max`)
16-17px body text, 96px section rhythm, 44px+ tap targets, visible focus rings, pointer/hover/active feedback, "call or request a quote"
rows after Services and Our Work, stats-bar watermark numerals removed, mobile hero trimmed to 2 bullets so the Call button is above the fold.
Its suggested navy/blue palette was not used (slate #59798e + orange were chosen).
