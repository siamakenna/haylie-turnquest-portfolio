# Portfolio update guide

Live site: https://siamakenna.github.io/haylie-turnquest-portfolio/

Repository: https://github.com/siamakenna/haylie-turnquest-portfolio

## Navigation and contact improvements included

The sticky header keeps Home, Portfolio, Golf, In motion, Meet Haylie, Collaborate, and Connections reachable. On narrower screens, Menu reveals every section instead of hiding links. Escape closes the menu and returns focus to its button. Choosing a destination closes it and moves keyboard focus into the section. The current section is marked while scrolling. A portal map offers four entry points and the footer includes Back to top.

Connections contains a direct email link to haylieturnquest2002@gmail.com, Instagram, agency links, and a shortcut to the brief builder. Generated briefs offer an email draft with the subject and body filled in, plus copy and download alternatives. No message is sent by the website. An email app must be configured; long mailto drafts can be truncated by some apps, so copy or attach the downloaded text when needed.

## Make a small edit in GitHub

1. Open the repository and the file you want to edit. Use the pencil button if you have write access.
2. Change only the intended text or value. Preserve quotes, HTML tags, and existing file paths.
3. For reviewable changes, commit to a new branch and open a pull request. Review the diff, then merge when ready. This site has no automatic pull-request preview.
4. After the change reaches `main`, wait for the Pages workflow in Actions to succeed. Reload the public site and check the edited section.

## Where to change things

| Adjustment | File and location |
| --- | --- |
| Intro, biography, campaign labels, section copy | `index.html`, in the corresponding section |
| Pink/lilac palette and dark canvas | `portal.css`, variables under `:root` and the section rules |
| Portal cards | `index.html`, `.portal-grid` |
| Navigation label/order | `index.html`, `#main-navigation`; keep each `href` matched to a unique section ID |
| Direct contact address | `index.html`, all `mailto:` links and visible email text; `script.js`, `CONTACT_EMAIL` |
| Agency and Instagram URLs | `index.html` links; also update `JAG` and the brief footer in `script.js` if these change |
| Photo gallery titles, categories, descriptions | `script.js`, `looks` array; retain stable, unique IDs so saved favorites continue to work |
| Video titles used in saved references | `script.js`, `videoRefs`; match each ID to its file basename |
| Photos and credit records | `assets/` and `assets/credits.json` |
| Video files, posters, source inventory | `assets/video/`, matching players in `index.html`, and `assets/video/sources.json` |

Keep relative paths such as `assets/photo-00.jpg`; a leading slash would point outside the project site. Match filename capitalization exactly. The site uses native HTML, CSS, and JavaScript, so every change remains portable without a build tool.

## Replace or add media

- Prefer replacing a file at the same path when it is the same look or clip. If it becomes a different look, give it a new stable ID and update the visible labels and source credits.
- For a new gallery photo, add the image and its source credit, then add its data to `looks`. Update the “All looks” count in the HTML to match.
- For a new clip, add an H.264/AAC MP4 and JPEG poster, a player and save button in the relevant section, and a matching `videoRefs` entry. Add the original filename, duration, and credit to `sources.json`. Update any counts in the portal copy and README.
- Keep clips compact and below GitHub’s per-file limit. Preserve fast-start MP4 encoding, native controls, `playsinline`, and `preload="none"`. Do not add autoplay.
- Preserve agency and supplied-video credits. Do not treat public portfolio images as openly licensed.

## Review an update

- Check narrow and wide browser windows: no sideways page scrolling; menu reveals all seven destinations; sections clear the sticky header.
- Use Tab and Escape, open/close a photo, and navigate between photos.
- Filter the gallery, save one photo and one video, and reload to confirm they remain selected.
- Play each changed clip. Starting a second should pause the first.
- Generate a brief containing saved photo and video URLs. Check its email recipient, subject, body, copy, and text download.
- Check Connections, footer email, Instagram, agencies, and Credits. The email recipient must be the same everywhere.
- Confirm `.nojekyll` remains in the root, the Pages workflow succeeded, and the public site shows the update.

## Future adjustments to discuss with Haylie

These are options for a later revision, not features currently promised or enabled.

1. **Her preferred edit:** choose the lead portrait, reorder gallery/campaigns, revise bio and category names, and remove any clip she does not want public.
2. **Booking details:** add approved availability/location, representation preferences, a media kit, and rates only if she wants them published.
3. **Accessibility:** add reviewed captions/transcripts for spoken video content and test with a screen reader and real mobile devices.
4. **Custom domain:** connect a domain she owns; decide ownership/renewal responsibilities first.
5. **Submission form:** if desired, replace mailto with an agreed form service, including spam protection, delivery checks, and a privacy notice. The current site has no inbox backend.
6. **Ownership and maintenance:** arrange repository access or a transfer if requested, and agree how new assets and edits will be supplied. No access or ownership changes have been made.

All existing content remains a draft for Haylie’s review. Favorites belong to each visitor’s browser, not a shared account.
