# The Runner number 1 — Support & Privacy Site

Static (HTML/CSS) version of the `sites.google.com/view/therunnernumber1` pages, ready to publish on GitHub Pages.

## Files

- `index.html` — Home / Support (hero, contact, FAQ, app information)
- `privacy-policy.html` — Privacy Policy
- `styles.css` — Shared stylesheet
- `images/` — Put your screenshots and logo here
- `.nojekyll` — Makes GitHub Pages serve the files as they are
- `.github/workflows/deploy.yml` — Optional GitHub Actions deploy workflow

## Publishing on GitHub Pages

1. Create a new **public** repo on GitHub named `therunnernumber1_page`.
2. Upload everything in this folder to the repo root, or from the command line:

   ```
   git init
   git add .
   git commit -m "Initial release"
   git branch -M main
   git remote add origin https://github.com/ucesur/therunnernumber1_page.git
   git push -u origin main
   ```

3. Go to **Settings → Pages**.
4. Under **Source**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then **Save**.
5. After a few minutes the site will be live at:
   `https://ucesur.github.io/therunnernumber1_page/`

> Note: On every push to `main`, the included GitHub Actions workflow
> (`.github/workflows/deploy.yml`) can deploy the site automatically. To use it,
> choose **Settings → Pages → Source = GitHub Actions**.

## Adding your own screenshots

The phone frames on the home page currently show placeholders. To add your own images:

1. Put the images in the `images/` folder (e.g. `images/screen-1.png`).
2. In `index.html`, replace each `.phone .screen` block with:

   ```html
   <div class="screen"><img src="images/screen-1.png" alt="Gameplay"></div>
   ```

## Email / store links

- The contact email is set to `randommobileapp@gmail.com` everywhere.
- In `index.html`, replace the App Store badge's `href="#"` with the real App Store link.
