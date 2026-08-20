# Xcel Cleaning Inc. — Website

A static one-page site for Xcel Cleaning Inc., built from the Figma design. Plain HTML/CSS/JS — no build step, no framework.

## Structure

```
index.html          Page markup (nav, hero, about, services, process, faq, contact, footer)
styles.css           All styling
script.js             Mobile nav, FAQ accordion, form submission
assets/images/        Photos exported from the Figma design
```

## Running it locally

No build step needed — just open `index.html` in a browser, or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## The contact form (Formspree)

The quote-request form posts to Formspree using the no-signup email endpoint:

```
https://formspree.io/f/wunistudios@gmail.com
```

**One-time setup:** submit the form once from the live site (or locally). Formspree will send a confirmation email to `wunistudios@gmail.com` — click the link in it to activate the endpoint. After that, every submission gets emailed there automatically. Until it's confirmed, submissions are held/rejected.

If you'd rather manage the form from a Formspree dashboard (spam filtering, submission history, custom "thank you" behavior), create a free account at formspree.io, create a form, and swap the `action` URL in `index.html` (search for `quoteForm`) for your form's `https://formspree.io/f/xxxxxxxx` ID.

## Placeholders to fill in

The Figma design left these as placeholders — search for them in `index.html` and replace with real values:

- `(Your Phone Number)` — appears in the Contact section and the footer
- `(Your Email Address)` / `(Your Email)` — appears in the Contact section and the footer

## Deploying to GitHub Pages

1. Create a GitHub repo (e.g. `xcel-cleaning`) and push this project to it.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. Save — the site will be published at `https://<your-username>.github.io/<repo-name>/`.

To use a custom domain instead, add a `CNAME` file at the repo root containing your domain, and point your domain's DNS at GitHub Pages per [GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).
