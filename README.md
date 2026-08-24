# Muralikrishna A V — Personal CV Site

A single-file, no-build website (`index.html`) styled like an engineering drawing sheet —
fitting, since it's a PLM/CAD career. All HTML, CSS, and JavaScript live in one file, so there's
nothing to install or compile.

## 1. Put it on GitHub Pages (free hosting)

1. Go to [github.com](https://github.com) and create a **new repository**.
   - If you want it at `https://<your-username>.github.io`, name the repo exactly
     `<your-username>.github.io`.
   - Otherwise any repo name works — e.g. `cv-site` — and your site will live at
     `https://<your-username>.github.io/cv-site`.
2. Upload `index.html` to the repo (Add file → Upload files on github.com is the easiest way,
   no command line needed).
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`. Save.
5. Wait about a minute, then refresh — GitHub will show you the live URL at the top of the Pages settings page.

That's it — the site is live and free. Every time you edit `index.html` and push/upload the change, the live site updates automatically within a minute or two.

## 2. Editing your content later

Everything is plain text inside `index.html` — no build step, no dependencies. Open the file in
any text editor (or edit directly on github.com by clicking the pencil icon on the file) and look
for these landmarks:

| Want to change... | Find this in the file |
|---|---|
| Name, title, contact info | `<header class="titleblock">` near the top |
| Summary paragraph & stats | `<section id="summary">` |
| Current role bullets | `<section id="experience">` → first `.role` block |
| Earlier roles table | `<section id="experience">` → `.earlier-table` |
| Skills / technologies | `<section id="expertise">` — grouped in `.cat` blocks, each skill is a `<span class="chip">` |
| Client engagements table | `<section id="engagements">` → each `<tr>` is one client. The `data-industry="..."` attribute drives the filter buttons automatically — add a new industry value and a new filter button appears on its own |
| Education / publications | `<section id="education">` |

No JavaScript knowledge is needed to update content — just edit the text between HTML tags and
keep the tags themselves intact.

## 3. Optional: custom domain

If you buy a domain (e.g. `muralikrishna.com`) from any registrar:
1. In the repo, add a file named `CNAME` containing just your domain name.
2. At your domain registrar, add a CNAME record pointing to `<your-username>.github.io`.
3. In Settings → Pages, enter the custom domain and enable "Enforce HTTPS".

## 4. Exporting a PDF

The footer has a **Save as PDF** button — it opens the browser's print dialog with a clean,
navigation-free layout you can save as a PDF for emailing to recruiters.
