# Samridh Deshwar — personal portfolio

A simple, responsive data analytics portfolio inspired by the paper textures and forest-green accents in `reference/`. Built with HTML and CSS; no dependencies, installation, JavaScript, or build step.

## Run locally

From the repository folder, run:

```sh
python3 -m http.server 8000
```

Open **http://localhost:8000** in your browser. Press **Ctrl+C** to stop the server. Refresh your browser after editing files.

## Publish with GitHub Pages

1. Commit and push the website files to GitHub.
2. In this repository, open **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Select the branch containing the website (usually `main`) and **/ (root)**, then click **Save**.

After GitHub finishes deployment, the website will be available at **https://samridhdeshwar01-hue.github.io/**. The `.nojekyll` file allows GitHub Pages to serve the static files directly. All local asset paths are relative, so the site also works under a repository subpath.

## Make it yours

- **`index.html`** — name, introduction, project cards, detail-page links, and about section. To add a project, copy an existing `<article class="project-card">` and update its content and links. Projects are curated manually; the page does not call the GitHub API.
- **`projects/<slug>/index.html`** — static detail pages containing the project README content, dashboard previews, and source repository links. Each full homepage card links to its detail page. Update these pages manually when a project README changes.
- **`styles.css`** — colors, typography, layout, and responsive styles.
- **`assets/`** — locally saved GitHub avatar, dashboard screenshots, and favicon. Replace `profile.jpg` with a personal photo if desired, then update its alternative text in `index.html`.
- **`reference/`** — original design references, preserved unchanged.

Project descriptions and dashboard images come from [Samridh's public GitHub repositories](https://github.com/samridhdeshwar01-hue?tab=repositories). The avatar is the account's public GitHub identicon. The movie preview is a styled code excerpt rather than a dashboard screenshot. Fonts are loaded from Google Fonts, with system fallbacks when offline. All other website assets are local.

## Project detail pages

Each page is a directory with an `index.html`, so GitHub Pages and the local Python server support direct navigation and refreshes without routing configuration:

- `/projects/ecommerce-sales-analysis/`
- `/projects/decathlon-retail-dashboard/`
- `/projects/red-bull-sales-dashboard/`
- `/projects/tmdb-movie-analysis/`

Page content is taken from the respective repository README, with headings and lists formatted for reading. Each page links to its original README and GitHub repository. Dashboard screenshots are stored locally, including additional views from the READMEs. The outdated ecommerce image URL in its README is replaced with the screenshot from its current repository. Visitors do not need a GitHub API request or JavaScript to read any project.
