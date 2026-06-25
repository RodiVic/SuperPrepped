# SuperPrepped.com

Static promotional site for *Code of Deception* by Robert Frank (MVRO Publishing LLC).

---

## What This Is

A single-page static site that presents SuperPrepped as a real AI travel platform — the fictional company at the center of *Code of Deception*. The site is designed to feel legitimate on first look and unsettling on closer reading. It functions as immersive book marketing and hosts the buy links for the novel.

---

## Files

```
index.html        — the entire site (one file)
cover.jpg         — book cover image (add this before deploying)
README.md         — this file
```

The itinerary document image lives separately — it's used inside the book as a front matter artifact and links to this site via QR code.

---

## Deploy to Netlify

1. Push this folder to your GitHub repo (account: RodiVic)
2. In Netlify, connect the repo and set publish directory to `/` (root)
3. Point `superprepped.com` at the Netlify site via DNS
4. Done — no build step, no dependencies, no framework

---

## Before You Go Live — Checklist

- [ ] Add `cover.jpg` to the root folder (same folder as `index.html`)
- [ ] Replace all `YOUR_AMAZON_LINK` placeholders with real URLs
- [ ] Replace `YOUR_BARNES_NOBLE_LINK` with real URL
- [ ] Replace `YOUR_BOOKSHOP_LINK` with real URL
- [ ] Replace `YOUR_AUDIBLE_LINK` with real URL (or remove that button if no audiobook yet)
- [ ] Update the QR code in the itinerary image to point to `https://superprepped.com`
- [ ] Test the modal on mobile — tap "Plan My Journey" and confirm it opens correctly
- [ ] Read the fine print section one more time to make sure nothing needs updating

---

## Updating Buy Links

All four buy links are in the HTML inside the `<!-- BOOK SECTION -->` div. Search for `YOUR_AMAZON_LINK` and replace each placeholder. They look like this:

```html
<a href="YOUR_AMAZON_LINK" class="buy-btn" target="_blank" rel="noopener">
```

The footer also contains duplicate buy links — update those too. Search for all instances of `YOUR_AMAZON_LINK` to catch them all.

---

## Adding the Real Cover Image

Name your cover file `cover.jpg` and drop it in the root folder. The HTML already points to it:

```html
<img src="cover.jpg" alt="Code of Deception by Robert Frank" class="book-cover-img" />
```

If you use a different filename or format (`.png`, `.webp`), update the `src` attribute to match.

---

## The Hidden Easter Eggs (don't change these)

These details are intentional — readers who look closely get rewarded:

- **Itinerary ID: SP-HVN-30-7X9Q2** — appears in the footer and in the modal. Matches Margaret's itinerary number in the front matter document.
- **Profiling bar** — a thin progress bar appears at the top of the page 1.5 seconds after load, fills over 3.5 seconds, then fades. Label reads *Profiling in progress...* then *Profile compiled.*
- **Modal close button** — reads *Cancellation Unavailable — Close* instead of a normal close label.
- **Fine print section** — contains the full SuperPrepped terms of service including *Silence preference noted* and *family involvement protocols.*
- **Testimonial ID** — third testimonial lists traveler ID as `SP-HVN-30`, the same itinerary prefix as Margaret's.
- **Footer sign-off** — *Safe travels, The SuperPrepped Team* mirrors the itinerary document exactly.

---

## For Book 2

When Book 2 launches, consider updating the site to show SuperPrepped as suspended:

- Replace the hero with a notice: *SuperPrepped services are currently suspended pending regulatory review.*
- Add a "Read what happened" link pointing to Book 1's buy page
- Add Book 2 buy links in a new section below

This makes the site a living artifact of the series rather than a static marketing page.

---

## Contact / Ownership

Domain: superprepped.com  
Publisher: MVRO Publishing LLC  
Pen name: Robert Frank  
GitHub: RodiVic  
Deploy: Netlify# SuperPrepped
Book advertising site
