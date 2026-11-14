# Popsicle Apps website

The public developer site for Popsicle Apps, served by GitHub Pages.

- Plain HTML and CSS only: no build step, JavaScript, cookies, analytics or backend.
- App source code is **not** here. Each app's repository is private.

## Structure

```
/                                   Popsicle Apps homepage (list of apps)
/support/                           General developer support (contact email)
/apps/<app-slug>/                   App overview
/apps/<app-slug>/privacy/           App-specific privacy policy
/apps/<app-slug>/support/           App-specific support
/assets/css/site.css                Shared styles (light and dark)
/assets/apps/<app-slug>/icon.png    App icon (256 × 256)
/404.html                           Not-found page
/.nojekyll                          Serve files as-is (no Jekyll processing)
```

URLs never change once an app is published: App Store Connect and the app itself link to them.

## Adding a new app

1. Copy `apps/mild-medium-hot/` to `apps/<new-app-slug>/`. Slugs are lowercase with hyphens.
2. Edit the three pages in the new folder: name, description, features, and an accurate privacy
   policy for **that** app. Never copy privacy statements without checking them against the app.
3. Add the icon: `assets/apps/<new-app-slug>/icon.png`.
4. Add one `.app-card` block on `/index.html`, and one link in each list on `/support/index.html`.
5. Check every link, then commit. Pages updates within a few minutes.

## Changing a privacy policy

Update the policy **before** releasing an app version that changes how information is handled, and
change its effective date.
