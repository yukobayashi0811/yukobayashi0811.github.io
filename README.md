# Personal portfolio

A static Jekyll portfolio for **https://yukobayashi0811.github.io**. GitHub Pages builds the site from Markdown and templates; there is no React app, database, or separate deployment step.

## Before publishing

1. Review the supplied name, Home introduction, and biography in `index.md` and `about.md` before publishing.
2. Review the verified professional roles and responsibilities in `work-experience.md` and the approved public LinkedIn profile link in `contact.md` before publishing.
3. Optionally update `title` and `description` in `_config.yml` if the public copy changes.

Do not leave placeholder text on a public portfolio unless you want visitors to see it.

## Publish on GitHub Pages

1. Create the public GitHub repository **`yukobayashi0811.github.io`** under the `yukobayashi0811` account.
2. Commit the **contents of this project root** to its `main` branch; `index.md`, `_config.yml`, `_layouts/`, `_includes/`, and `assets/` must stay at the top level.
3. In repository **Settings → Pages**, choose **Deploy from a branch**, branch **`main`**, folder **`/ (root)`**, and save.
4. Wait for GitHub Pages to build, then visit **https://yukobayashi0811.github.io/**. The configured `url` matches the user site and `baseurl` is empty. Internal links and assets use Jekyll’s `relative_url` filter.

GitHub Pages uses the supported `jekyll-seo-tag` and `jekyll-sitemap` plugins declared in `_config.yml`. The sitemap is generated at `/sitemap.xml`. `Gemfile` is for matching GitHub Pages locally, not a required GitHub Pages build step. Do not enable GitHub Actions for this site unless you deliberately change the publishing approach.

## Update content

Edit the Markdown files in the project root. The YAML block between `---` lines at the top of each page sets its layout, title, description, and URL. Shared page structure is in `_layouts/default.html`; navigation and footer are in `_includes/`. CSS is in `assets/css/style.css`; the favicon is in `assets/favicon.svg`. Add navigation items in `_includes/header.html` only when you add a corresponding page.

## Preview locally

Install Ruby and Bundler, then from this project root run:

```sh
bundle install
bundle exec jekyll serve
```

Open `http://127.0.0.1:4000/`. Local preview is optional; GitHub Pages builds directly from the repository root. `_site/` is generated output and is ignored by Git.

## Check quality

After publishing or while serving locally, open Chrome DevTools → **Lighthouse**. Run the **Navigation** audit for both mobile and desktop, and check Performance, Accessibility, Best Practices, and SEO; the target is **90 or above in each category**. Also inspect the pages at **375px** and **1280px** viewport widths, follow each navigation link, and inspect `/sitemap.xml` and the favicon. Lighthouse results vary with device and network conditions; rerun after changes.

## Assumptions

- The name and biography on Home and About reflect the supplied content; employer and sponsor names are intentionally omitted.
- `work-experience.md` contains verified professional roles and responsibilities.
- `contact.md` contains the approved public LinkedIn profile link. No email address or `mailto:` link is published.
- The reference photography site informs the classic feel only; no text, images, or personal details are copied from it.