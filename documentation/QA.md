# Quality assurance

Verification performed on 30 October 2026 using Playwright with the locally installed Brave/Chromium browser. Browser tooling and temporary test scripts were kept outside the deliverable. The site itself has no test or build dependency.

## Executed checks

| Check | Result |
| --- | --- |
| Responsive layout matrix | 616 combinations passed: 14 HTML pages × 11 widths × 2 themes × 2 directions |
| Widths | 320, 360, 390, 430, 640, 768, 820, 1024, 1280, 1440, 1920 pixels |
| Overflow and images | No document/body horizontal overflow and no missing displayed images in the matrix |
| Font, asset and hosting smoke checks | All eight local font weights loaded; no external requests or HTTP failures; relative subdirectory navigation and booking passed; reduced-motion mode disabled travelling lights |
| JavaScript | Both scripts passed `node --check`; no runtime errors in the layout pass |
| Links and assets | 620 local references checked, including target files, fragment anchors and duplicate IDs; no failures |
| Functional assertions | 57 passed |
| Accessibility | 48 axe-core audits of six key routes × desktop/mobile × light/dark × LTR/RTL; no WCAG A/AA findings reported |
| Visual review | Actual browser captures of all 14 public pages reviewed, plus desktop/tablet/mobile and dark RTL delivery screenshots |

The six accessibility routes were Home 1, Home 2, Services, Pricing Guide, Contact and FAQ. Axe checks are automated evidence, not a claim of full WCAG certification. Layout checks cover all 14 pages; service and article variants were also checked through their actual query-driven interactions.

## Functional coverage

- Home menu: click, hover, keyboard activation, Escape and outside click.
- Sticky header after scrolling; working back-to-top.
- Mobile drawer opening from the correct side in LTR and RTL, controls inside the drawer and closing on the scrim.
- Light/dark and reading-direction changes persisted across reloads.
- All four switchboard modules updated their selected states and detail links; arrow-key and End navigation worked.
- All four home diagram selections updated the associated service link.
- Six service detail variants displayed substantial scope information and correct booking-prefill links.
- Pricing filters restored the appropriate two fitting rows, three quote rows or all seven rows.
- Pricing enquiry links preselected the intended booking service.
- Empty form blocked review; a past date failed validation.
- Hazard urgency showed the keep-away message.
- Valid details produced an unsent request summary; user-entered markup remained literal text.
- Copy handoff placed the expected request on the clipboard; download contained the expected request text.
- Editing returned to the form with details retained.
- FAQ accordion activated from the keyboard.

## Corrections during QA

- Replaced an unrelated stock-image download after direct asset inspection.
- Changed mobile rates from a wide table into readable stacked rows.
- Corrected interaction between hover opening and the first dropdown click.
- Removed service-card background-color interpolation during theme changes so text and surface colors update together.
- Removed an aspect-ratio/min-height conflict that extended a safety photograph beyond the mobile body width.
- Used natural bidirectional paragraph handling to keep English punctuation readable in the RTL layout.

## Screenshots

- [Home 1 — desktop](screenshots/home-desktop.png)
- [Home 1 — tablet](screenshots/home-tablet.png)
- [Home 1 — mobile](screenshots/home-mobile.png)
- [Home 2 — desktop](screenshots/home2-desktop.png)
- [Pricing — mobile](screenshots/pricing-mobile.png)
- [Booking — dark RTL on tablet](screenshots/booking-dark-rtl.png)

## Deployment boundaries

The source is static and uses relative links for GitHub Pages project hosting. No repository or GitHub Pages target was supplied, so an actual GitHub Pages production deployment was not performed or claimed. See README for setup. The exact requested source structure places the custom 404 at `pages/404.html`; GitHub does not automatically select it for unknown routes without an additional root 404 page.

The form has no sending integration. End-to-end delivery to a service provider, real coverage, actual rates, credentials and appointment availability cannot be verified from a frontend-only template.

## Optional hosted preview

A private Sites destination was registered, but source upload was blocked by automatic approval review because the user had not explicitly authorized that external publication destination. No source upload or deployment succeeded. The local deliverable is complete and unaffected. Publication requires explicit approval.
