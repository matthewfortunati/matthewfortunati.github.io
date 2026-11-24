# Links page

A free, self-hosted replacement for Linktree. Minimal, on black, with the portfolio's fonts and motion: letters
that thin under your finger or cursor, a wave across each title as it lands, and mono labels that shuffle into place.

It's a single file, `index.html`. There's no build step, no account and no monthly fee.

## Editing your links

Open `index.html` in any text editor and look for the block marked `YOUR LINKS`. Each link is one line:

```html
<li><a class="link" href="https://…"><span class="t">Title</span><span class="m">small grey line</span></a></li>
```

- **Add:** copy a line, then change the address (`href`), the title (`class="t"`) and the grey line (`class="m"`).
- **Remove:** delete the line. **Reorder:** move the line up or down.
- **New section:** copy a whole `<section class="group"> … </section>` block and rename its label, e.g. `03 · Watch`.
- **Top link:** Portfolio sits on its own above the sections. Put any link there that should come first.

New links get the animation automatically.

### The Linktree Pro features, free

- **Highlight a link:** use `class="link is-new"` and a pulsing dot appears in front of its grey line.
- **Schedule a link:** put dates on its `<li>`, e.g. `<li data-from="2026-12-05" data-until="2027-01-31">`.
  The link shows only between those dates, and you can use just one of the two. Handy for a release-day link.
- **Click analytics:** see below.
- **Your own design, and no Linktree logo.**

### Click analytics (optional, free)

1. Sign up at [goatcounter.com](https://www.goatcounter.com) and pick a code, e.g. `matthewfortunati`.
2. In `index.html`, find the GoatCounter line near the top of `<head>`, put your code in place of `YOURCODE`
   and remove the `<!--` and `-->` around that line.
3. Your dashboard then shows visits, plus every tap on a link (`click/stones`, `click/bandcamp`, …).
   GoatCounter doesn't use cookies.

## Putting it online for free (GitHub Pages)

You already host the portfolio there, so it's the same routine:

1. On GitHub, create a new **public** repository named exactly `matthewfortunati.github.io`.
2. Upload `index.html` (**Add file → Upload files**), then commit.
3. After a minute or so it's live at **https://matthewfortunati.github.io/**. That short address goes in your
   Instagram bio. (If it doesn't appear: **Settings → Pages → Deploy from a branch → main / root**.)

To change a link later, open `index.html` on GitHub, click the pencil icon, edit and commit. The site updates
in about a minute.

Other free options: Netlify Drop (drag the folder onto app.netlify.com/drop) or Cloudflare Pages. A custom
domain (about €10 a year) works with any of them, GitHub Pages included.

## Previewing on your computer

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Notes

- Stones and Il Granchio open their videos on your YouTube channel. The other releases open Spotify, with type
  and year taken from Spotify and links stored without the `?si=` tracking tag.
- On the old Linktree, Il Granchio's spotify.link short link was dead (it only opened Spotify's home page).
- The portfolio's About section still links to linktr.ee. Once this page is live you may want to point it here.
