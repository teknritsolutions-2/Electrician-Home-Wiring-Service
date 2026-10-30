# Electrician & Home Wiring Service

A complete, buildless HTML5, CSS3 and vanilla JavaScript website using the Circuit Grid design system. The workspace is the website root: `index.html` is the actual homepage.

## Preview

Open `index.html`, or serve this directory:

```sh
python3 -m http.server 4173
```

Visit `http://localhost:4173`. A local HTTP server supports the clipboard handoff more reliably than opening files directly. No npm dependencies or build step are required.

## Included

- Two distinct homepages, About, Services, service details, Pricing Guide, Contact, FAQ, Home Journal and article details, Privacy, Terms, 404 and Coming Soon: 14 HTML pages.
- Four keyboard-operable switchboard service modules and a separate interactive home diagram.
- Six service detail variants using `pages/service-details.html?service=wiring|lighting|fan|switchboard|panel|inspection`.
- Five complete informational articles using `pages/blog-details.html?article=inspection|switchboards|lighting|panels|fixtures`.
- Pricing filters and service-aware enquiry links.
- Client-side validation, hazard guidance, enquiry review, safe text rendering, copy and text download.
- Persistent light/dark and LTR/RTL preferences, mobile drawer, keyboard navigation, FAQ accordions, sticky navigation and reduced-motion support.
- Local photographs, local fonts, SVG logo variants and favicon.

## Important operational details

The enquiry form is frontend-only. It does **not** send, store or confirm requests. Visitors review and copy/download their details to share directly with a provider. No provider phone number, address, service coverage, credentials or availability was supplied; none is invented.

Rates are illustrative design defaults, clearly disclosed on the site. Edit all displayed amounts in **`assets/js/config.js`**. Replace them with approved provider prices before commercial launch. Service copy and detail content are in `assets/js/main.js`; page structure and long-form content live in the HTML files.

## GitHub Pages

1. Put the contents of this directory in the root of the intended repository.
2. In repository Settings → Pages, select deployment from the intended branch and `/ (root)`.
3. Keep `index.html`, `pages/` and `assets/` together. Every site link uses relative paths, including project-subdirectory hosting.
4. Verify the published URL after GitHub finishes deployment.

No GitHub repository or GitHub Pages deployment target was supplied. Compatibility is checked locally; a GitHub Pages production deployment cannot be verified without that destination. `pages/404.html` is an intentional utility page; the exact requested structure does not include a root `404.html`, so GitHub's default unknown-route response will not automatically use it.

Read [customization and integration notes](documentation/CUSTOMIZATION.md), [asset credits](documentation/CREDITS.md) and [QA evidence](documentation/QA.md).
