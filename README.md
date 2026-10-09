# Mobile Notary Website

A static site (HTML, CSS, and JS only) that can be hosted for free on GitHub Pages.

## 1. Fill in the business details

Search `index.html` for these placeholders and replace them:

| Placeholder | Example |
|---|---|
| `TAGLINE` | Signed with care. Delivered to your door. |
| `REVIEW_n_TEXT` / `REVIEW_n_NAME` | Real client reviews only. The section is hidden for now: to show it, remove `hidden` from `<section id="reviews">` and uncomment the Reviews menu link |
| `FORMSPREE_ID` | From formspree.io (see below) |

**Images (optional):** add `images/hero.jpg` for the hero background.

## 2. Contact form

GitHub Pages can't process forms on its own, so the form uses Formspree, which has a free tier:
1. Sign up at https://formspree.io and create a form.
2. Copy the form ID (the part after `/f/`) into `FORMSPREE_ID` in `index.html`.

## 3. Publish on GitHub Pages

```bash
cd notary-site
git init
git add .
git commit -m "Initial site"
gh repo create notary-site --public --source=. --push
```

Then, on GitHub, go to the repo's **Settings → Pages**. Under **Source**, choose `main` and `/ (root)`.

## 4. Custom domain

1. In **Settings → Pages → Custom domain**, enter `yourdomain.com` and save. This creates a `CNAME` file.
2. At your domain registrar, add these DNS records:
   - `A` records for `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` record for `www` → `YOUR_GITHUB_USERNAME.github.io`
3. Once DNS finishes updating (minutes to a few hours), turn on **Enforce HTTPS**.
# Notary-Website
