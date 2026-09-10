# Paul Schelhaas

Personal website for Paul Schelhaas, multi-patent inventor and former CEO who
helps security, energy and industrial businesses commercialise new technology,
protect their intellectual property and win major customers.

Live site: https://www.paulschelhaas.com

## Overview

A single-page, self-contained static website. Everything the page needs (markup,
styles, fonts, the portrait, icons and the interactive runtime) is embedded
inside `index.html`, so the site has no build step and no external asset
requests. It is served as a static file through GitHub Pages with a custom
domain.

The page covers Paul's dossier, capabilities, track record, ways to engage and a
contact section.

Capabilities featured on the site:

- Fractional Chief Innovation Officer
- Innovation and Commercialisation Strategy
- IP Strategy and Patent Portfolio
- Technical Design and Systems Engineering
- Board Advisory and Non-Executive Director roles
- Diligence and Dispute Support

## Repository structure

```
index.html        The complete website (markup, CSS, fonts and assets embedded)
CNAME             Custom domain for GitHub Pages (www.paulschelhaas.com)
Attachment-1.jpg  Source copy of the portrait photo
brand/            Brand assets (logo and LinkedIn banners, see below)
README.md         This file
llms.txt          Machine-readable site summary for language models
```

## Brand

- Typeface: Archivo (headings at weight 800)
- Core colours:
  - Ink background `#06070f`
  - Off-white text `#eef0ff`, muted body `#9ba1c4`
  - Periwinkle accent `#7c8cff`, light periwinkle `#b4beff`
  - Coral `#ff563c`
- Signature motif: the spark gradient, periwinkle to coral,
  `linear-gradient(90deg, #7c8cff, #ff563c)`, defined once in the page as
  `--gx-spark` and used on calls to action, section labels, numbers and accent
  lines.
- Logo: the PS monogram, a rounded tile with a periwinkle-gradient "PS" and a
  coral spark underline. Master files are in `brand/`.

### Brand assets in `brand/`

| File | Use |
| --- | --- |
| `ps_monogram_logo.svg` | Monogram logo exactly as used on the site (scalable) |
| `ps_monogram_logo_256/512/1024.png` | Raster monogram at common sizes |
| `ps_linkedin_banner_1128x191.png` | LinkedIn company page cover |
| `ps_linkedin_banner_1584x396.png` | LinkedIn profile background banner |
| `ps_linkedin_banner_*.svg` | Editable vector masters for both banners |

All lettering in the SVG masters is converted to outlines, so they render
identically without Archivo installed.

## Updating the portrait or other embedded assets

Important: because the images are embedded inside `index.html` as base64 data,
replacing a loose file such as `Attachment-1.jpg` in the repository does not
change what the page shows. The page renders the embedded copy, not the file on
disk.

To change the portrait you must re-embed the new image into `index.html`,
replacing the base64 payload for the portrait asset. The same applies to the
favicons and any other embedded image. Keep the loose source file in the repo in
sync so it stays a faithful source copy.

## Deployment

The site is hosted with GitHub Pages. Pushing to the default branch publishes the
latest `index.html`. The `CNAME` file points the site at `www.paulschelhaas.com`;
the matching DNS records are configured with the domain registrar.

## Contact

- Email: paul@assistiv.co
- LinkedIn: https://linkedin.com/in/paul-schelhaas

## Credits

Design and build by Marketing for my Mates, https://www.marketingformymates.com
