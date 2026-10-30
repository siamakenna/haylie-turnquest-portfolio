# Haylie Turnquest — Portfolio Draft

A fashion, beauty, lifestyle, and creative collaboration portfolio for Haylie Turnquest.

## Preview features

- Dedicated golf section with on-course and outfit videos.
- Nine supplied videos with native playback controls and video references in briefs.
- Filterable photography gallery and full-image viewer.
- Saved-look moodboard, kept in the visitor’s browser.
- Modeling, UGC/social, golf/sport, and brand collaboration brief builder.
- Copy and download a brief with saved visual references.
- Direct links to Instagram and official agency portfolios.
- Responsive layouts, keyboard navigation, native dialogs, and reduced-motion support.

## Run locally

Open `index.html`, or serve this directory with any static web server. No installation or build step is required. Clipboard features work best over HTTPS or localhost.

## GitHub Pages

In the repository’s **Settings → Pages**, choose **Deploy from a branch**, then **main** and **/ (root)**. Save and wait for the deployment to complete.

## Editing

- `index.html`: page content and external links.
- `styles.css`: colors, typography, and responsive layouts.
- `script.js`: gallery data, saved looks, and brief behavior.
- `assets/credits.json`: per-image sources and rights notes.

This is a draft for review. Creator service categories are collaboration inquiry options. Availability, rates, and usage rights are confirmed directly with Haylie or her agency. Briefs are generated locally; the website does not send inquiries automatically.

## Photography

Images are sourced from Haylie Turnquest’s public JAG Models and Wilhelmina Miami portfolios. All image rights remain with their respective rights holders. Individual photographer names were not provided in the source listings. See `assets/credits.json` for exact sources.

## Checks

Desktop checks passed for gallery filtering, photo navigation, saved looks after reload, project selection, brief generation, clipboard copy, text download, and image loading. Responsive CSS is included; mobile browser interaction testing is pending.

## Video assets

The nine unique supplied videos are converted to 720p H.264/AAC MP4 with fast-start playback, 30 fps, and poster frames. The HDR beauty routine is tone-mapped to SDR for consistent browser display. Full clips are retained; files are capped for static hosting. Original filenames and durations are recorded in `assets/video/sources.json`. Videos never autoplay and pause when another clip starts. Original uploads are preserved separately.

The nine video players and golf brief flow passed desktop browser QA, including paused previous playback and persistence of saved video references. See `qa-results.json`.

The repeated golf outfit upload is byte-identical to the existing clip and is represented once. Golf includes three clips; the motion section contains six.
