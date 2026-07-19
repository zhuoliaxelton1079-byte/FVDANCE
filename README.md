# Fox Valley Chinese Dance Group — Website

A small site (7 pages + shared nav/footer) deployed on **GitHub Pages**.
`index.html` redirects to `Home.html`. Pages need an internet connection
for fonts and the React runtime.

## ✏️ Editing text — the copy files

**All words on the website live in the `*-copy.js` files.** You never need
to touch HTML to change text: open the matching copy file, edit the words
between the quotes, and save.

| Copy file | Controls |
|---|---|
| `home-copy.js` | Home page (hero, teaser cards) |
| `about-copy.js` | About page story, missions, events |
| `team-copy.js` | Team page members |
| `performances-copy.js` | Performances page intro + photo/video captions |
| `culture-copy.js` | Culture page repertoire cards, "why it matters", dance history |
| `testimonials-copy.js` | Testimonials page quotes |
| `contact-copy.js` | Contact page, incl. form labels + contact details |
| `site-nav-copy.js` | Top navigation labels + brand name |
| `site-footer-copy.js` | Footer brand line + copyright |

Rules of thumb:

- Keep the quote marks around text. Need a quote inside your text? Type `\"`.
- Don't change the words to the **left** of the colons — those are field
  names the pages look up.
- In lists (team members, gallery photos, testimonials), copy an existing
  `{ ... },` block to add an entry. Photo entries have an `id` that links
  the caption to its dropped photo — don't change ids once a photo is in
  place.
- Every page also has a built-in fallback copy of its text, so a typo in a
  copy file won't blank the page — but the page will show the old fallback
  text until the file is fixed.

**Publishing:** the live site updates when changes are committed and pushed
to GitHub (GitHub Pages). If an edit doesn't show up, do a hard refresh
(Ctrl+F5) — and note `About.html` loads its copy file with a `?v=...`
version tag to defeat caching; bump that tag if About text seems stuck.

## Other files

| File | What it is |
|---|---|
| `Home / About / Team / Performances / Culture / Testimonials / Contact .html` | Page structure and styling — text comes from the copy files |
| `SiteNav.html`, `SiteFooter.html` | Shared header and footer components |
| `index.html` | Redirects to `Home.html` (GitHub Pages entry point) |
| `assets/` | Logo and decorative art extracted from the group's PowerPoint |
| `support.js`, `image-slot.js` | Runtime files — **do not edit** |

## Photos

Every photo box is a drag-and-drop slot: drop an image file onto it (or
click to browse) while viewing the page in the design tool. Dropped images
persist via the `.image-slots.state.json` sidecar (uploads are author-only).

## Placeholders still to replace

- Phone number `(920) 555-1234` and email in `contact-copy.js`.
- Testimonials in `testimonials-copy.js` are sample text.
- The second team member in `team-copy.js` has an empty `name`.
- The contact form shows a thank-you message but doesn't send email yet —
  connect it to a form service (e.g. Formspree) to make it real.
