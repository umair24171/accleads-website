# AccLEADS Website

Redesigned single-file website for **AccLEADS (Accounting Leaders)**: Canadian
bookkeeping, catch-up and clean-up, year-end files, T1, T2, T4 and T5 returns,
and compilation engagement support (CSRS 4200) for business owners and CPA firms.

## Files

- `index.html` — the whole site in one self-contained file (all CSS and JS inline,
  no build step, no external images). Navigation is hash-routed, so every page is
  a view inside this file.

## View locally

Open `index.html` directly in a browser, or serve it from this folder:

```bash
cd accleads-website
python3 -m http.server 8000
```

Then visit http://localhost:8000

## Deploy to GitHub Pages

1. Create a repository (for example `accleads-website`) on GitHub.
2. Push this folder's contents to the `main` branch.
3. In the repository, go to **Settings > Pages**, set the source to
   **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
4. The site will be live at `https://<your-username>.github.io/accleads-website/`

## Before launch (owner to supply)

- **Real contact details**: the phone number, email address, and office address
  are still shown as placeholders (`[+1 (000) 000-0000]`, `[hello@accleads.ca]`,
  `[Office address]`) in the contact page sidebar and the footer. Replace them
  in `index.html` before publishing.
- **Prices**: plan prices are shown as "Quoted after your free review" because
  no prices were provided. Replace with real figures when ready.
- **Team section**: the About page has a clearly marked placeholder. Add real
  team members (name, designation, experience, bio) or remove the section.
- **Compilation-report licensing**: the FAQ answer "Can AccLEADS issue a
  compilation engagement report?" starts with "[Edit to match your licensing.]".
  Confirm the wording matches the firm's licensing.
- **Contact form**: the form currently shows a preview confirmation message
  only. Connect it to an inbox (for example Formspree, a Google Form, or a
  small backend) so requests are actually delivered.

## Design notes

- Pine green (`#1F5C4A` / deep `#163F33`) and brass accent on a paper
  background, Newsreader display type with Public Sans body and IBM Plex Mono
  for form codes, matching the original ledger identity.
- The hero uses a CSS-built filing dashboard (real CRA due dates only, no
  invented data). Service cards use inline SVG icons, no emoji.
- Responsive (mobile, tablet, desktop), keyboard accessible, and
  `prefers-reduced-motion` is respected. A light/dark toggle is in the header.
