# Institute of Thought Leaders website

The website for the Institute of Thought Leaders (ITL), built with Jekyll and published by GitHub Pages.
GitHub rebuilds the site automatically, about a minute after any file changes.

**Test address:** https://zarahussain-itl.github.io/instituteofthoughtleaders/

## Where things live

| What | Where |
|---|---|
| Pages (Home, Certifications, Fees, policies and so on) | the `.html` files in the top folder |
| Articles that are live | `_posts/` |
| Articles being written | `_drafts/` (never shown on the site) |
| "Coming soon" cards on Insights | `_data/upcoming.yml` |
| Main menu | `_data/nav.yml` |
| End-of-article buttons | `_data/related.yml` |
| Header and footer | `_includes/header.html`, `_includes/footer.html` |
| Images | `assets/images/` |
| Site settings (address, form service, search engines) | `_config.yml` |

To publish an article, see [PUBLISHING.md](PUBLISHING.md).

## Switching on the forms

GitHub Pages can't receive form submissions, so the forms send to Formspree (free for 50 submissions a month).

1. Sign up at formspree.io with info@instituteofthoughtleaders.com and create a form called "ITL website".
2. Copy its address, which looks like `https://formspree.io/f/abcdwxyz`.
3. In `_config.yml`, paste it between the quotes on the `form_endpoint:` line and save.

Every form on the site (contact, program preview, employer enquiries, newsletter) then sends to your inbox, with the page it came from in the subject line.
Until then, forms show "This form is not connected yet" with your email address.

## Using instituteofthoughtleaders.com

1. In this repository, go to **Settings → Pages → Custom domain**, enter `instituteofthoughtleaders.com` and save. GitHub adds a `CNAME` file.
2. At your domain registrar, set these DNS records (remove any other A records for the bare domain):
   - Four **A** records for `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One **CNAME** record for `www` pointing to `zarahussain-itl.github.io`
3. In `_config.yml`, change `url` to `"https://instituteofthoughtleaders.com"` and `baseurl` to `""`.
4. Once GitHub shows the domain as verified (can take up to 24 hours), tick **Enforce HTTPS**.

## Going live

When prices, dates and other `[PLACEHOLDERS]` are filled in, change `noindex: true` to `noindex: false` in `_config.yml` so Google can list the site. The sitemap is at `/sitemap.xml` for Google Search Console.

## Copyright

All rights reserved. See [LICENSE](LICENSE). This repository is public only so GitHub Pages can host it for free; that does not give anyone permission to reuse its contents.
