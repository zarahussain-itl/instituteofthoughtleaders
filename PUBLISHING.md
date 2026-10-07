# Publishing an article

Articles are Markdown files: plain text with `##` for headings and `**bold**`.
When a file is in `_posts/`, it appears automatically on the Insights page, on the Home page (latest three), in the RSS feed and in the sitemap.

## The workflow

1. **Draft.** Ask Claude to write the article and save it to `_drafts/` in this repository, or copy `_templates/new-article.md` into `_drafts/` and write it yourself. Drafts are never shown on the site.
2. **Review.** Read the draft on GitHub (open the file; GitHub shows it formatted). Edit with the pencil icon.
3. **Publish.** Move the file from `_drafts/` to `_posts/` and add the date to the front of the file name:
   `_drafts/coaching-is-not-counselling.md` → `_posts/2026-11-03-coaching-is-not-counselling.md`
   On GitHub: open the file, click the pencil icon, and change the name box at the top to `_posts/2026-11-03-coaching-is-not-counselling.md`, then **Commit changes**. (Or just ask Claude to publish it.)
4. **Tidy up.** If the article was listed in `_data/upcoming.yml`, delete its entry.
5. **Check.** About a minute later it's live at `/insights/coaching-is-not-counselling/`.

A post dated in the future won't appear until you next change the site on or after that date.

## Article settings

The top of each file, between the `---` lines:

| Setting | What it does |
|---|---|
| `title` | Headline |
| `summary` | Shown under the headline and on cards |
| `description` | What Google shows in search results (about 150 characters) |
| `category` | One of: For employers, Coaching practice, Wellbeing at work, Careers in coaching |
| `related` | Which button appears at the end: `employers`, `corporate-performance-coach`, `executive-team-coach`, `workplace-wellbeing-coach` or `certifications` |
| `featured: true` | Pins it as the large card at the top of Insights (only one article should have this) |
| `image` / `image_alt` | Optional picture under the headline; put the file in `assets/images/` |

Author defaults to Zara Hussain, and reading time is calculated automatically.

## Sharing it

After it's live, paste the article link into LinkedIn and your newsletter. If you set up beehiiv, its RSS-to-email feature can read `/insights/feed.xml` and draft the newsletter for you.
