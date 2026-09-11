# Gem Catch website

The public marketing and privacy website for the Gem Catch mobile game. This
project is intentionally independent from the Unity game repository and uses
plain HTML, CSS, and JavaScript with no build step or runtime dependencies.

**Production:** <https://gemcatch.app/>

## Local preview

From this folder, run:

```bash
python3 -m http.server 8080
```

Open:

- Landing page: <http://localhost:8080/>
- Privacy policy: <http://localhost:8080/privacy-policy/>

Opening the HTML files directly is not recommended because a local server more
closely matches GitHub Pages path handling.

## Project structure

```text
.
|-- index.html
|-- privacy-policy/
|   `-- index.html
|-- assets/
|   |-- css/styles.css
|   |-- js/site.js
|   `-- images/
|-- robots.txt
`-- .nojekyll
```

## Content that must be supplied before launch

Search the project for `OWNER_TODO` and replace the related placeholder values:

1. Verified Google Play and App Store URLs. Replace each disabled store button
   with an anchor using the real URL; do not use a placeholder `href`.
2. A final Crystal Cave or Jungle Falls gameplay screenshot for the remaining
   preview placeholder.

The privacy policy should also be reviewed against the SDKs and settings in the
exact mobile build submitted to each store.

## GitHub Pages deployment

1. Create a GitHub repository for this folder and push the site to its default
   branch.
2. In the repository, open **Settings > Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the default branch and the `/ (root)` folder, then save.
5. Confirm the production URL above loads both the landing page and privacy
   policy.

The site uses relative paths and includes `.nojekyll`, so no GitHub Actions
workflow or static-site generator is required.

## Media provenance

The app icon, Gem Catch title art, and environment backgrounds are optimized
copies from the separate Gem Catch Unity project. Clearly named third-party
asset-pack content was not copied. Confirm that the selected source media is
cleared for public website use before deployment.
