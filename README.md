# Rescue_Watch-DSE

DSE final project: **UMBRA — Protocolo de rescate**, an interactive rescue smart-watch simulator. The game is a static HTML page with built-in CSS and JavaScript; no build step, dependencies, or backend are required.

## Play on GitHub Pages

**Site:** <https://bmunozsd.github.io/Rescue_Watch-DSE/>

GitHub Pages is configured to publish the root of the `main` branch. To publish these changes:

1. Merge them into `main`.
2. In the repository, open **Settings → Pages** and verify:
   - **Source:** Deploy from a branch
   - **Branch:** `main`
   - **Folder:** `/ (root)`
3. Save if you changed the settings, then wait for the Pages deployment to finish in **Actions** before opening the site.

`index.html` is the homepage that GitHub Pages loads automatically. The old `JuegoRESWATCH.html` URL redirects to it so existing links still work. Asset paths are relative, so they work under the `/Rescue_Watch-DSE/` project path as well as locally. `.nojekyll` tells Pages to serve the files as a plain static site.

## Run locally

From the repository directory, run:

```sh
python3 -m http.server 8000 --bind 0.0.0.0
```

Open <http://localhost:8000/>. Edit `index.html` to change the game; `watch.svg` is the bundled watch illustration.

Use **WASD / arrow keys** to move, **Ctrl** to crouch, **Space** to breathe, and **E** to send SOS. Touch controls are available on small screens. WebGL is preferred, with a 2D fallback. VR requires a WebXR-compatible browser and headset, using HTTPS (provided by GitHub Pages) or localhost.
