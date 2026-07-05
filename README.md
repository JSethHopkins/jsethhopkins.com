# jsethhopkins.com

Personal site for J. Seth Hopkins. Plain HTML — no build step, no dependencies.
Hosted on GitHub Pages.

## What's in here

| File | What it is |
|---|---|
| `index.html` | The main site |
| `resume.html` | The digital résumé (has a Print / Save PDF button) |
| `writing/` | Personal essays live here |
| `writing/sample-essay.html` | Essay template — duplicate this to publish |
| `og-image.png` | The image shown when the site is shared on LinkedIn etc. |
| `seth-hopkins.jpg` | Headshot used in the hero |
| `CNAME` | Tells GitHub Pages the custom domain — don't delete |

## How to edit (no software needed)

Open any file on github.com → click the **pencil icon** (top right of the
file view) → make your change → **Commit changes**. The live site updates
in about a minute.

### Add a LinkedIn post or Forvis Mazars article

1. Open `index.html`, click the pencil.
2. Scroll to the bottom — find `const posts = [`.
3. Add a new entry at the TOP of the list (copy an existing one):

```js
{
  date: "Jul 2026",
  source: "LinkedIn",            // or "Forvis Mazars" or "Essay"
  title: "The headline shown on the site",
  excerpt: "One line so visitors know whether to click.",
  url: "https://www.linkedin.com/posts/..."
},
```

LinkedIn post links: on the post, `⋯` menu → **Copy link to post**.

4. Commit changes. Done.

### Publish a personal essay

1. Open `writing/sample-essay.html` → pencil → select all → copy.
2. Go to the `writing/` folder → **Add file → Create new file**.
3. Name it something like `why-i-build.html` (lowercase, hyphens, no spaces).
4. Paste, then edit the title, date, headline, and article paragraphs
   (instructions are in a comment at the top of the file).
5. Commit, then add a `posts` entry in `index.html` with
   `source: "Essay"` and `url: "writing/why-i-build.html"`.

### Change site text

Everything is plain text inside `index.html` and `resume.html` —
find the sentence, edit it, commit. If you want a structural or design
change, that's a job for a bigger edit session.

## Domain

`CNAME` points GitHub Pages at jsethhopkins.com. DNS is configured at the
domain registrar (A records → GitHub Pages IPs, www CNAME → the
github.io address). If the site ever shows a certificate warning, check
Settings → Pages → "Enforce HTTPS" is on.
