# Design refinement: QA evidence

Latest section update: [Photographic service board](SERVICE-DIRECTORY-REDESIGN.md), with 76 focused layout combinations, eight accessibility audits and 202 functional assertions.

Current pass: **31 October 2026**. See [the current refinement report](REFINEMENT-2026-10-31.md) for the Home 2, Services and Service Details redesign, computed typography, 616 layout combinations, 202 functional assertions, 48 accessibility audits and current screenshots.

## Earlier refinement record — 30 October 2026

Reviewed baseline: `45d072e88043e1698bb466cf1f896e81520e70c1`.

Verification date: 30 October 2026. Browser automation used Playwright with the locally installed Brave/Chromium browser. Temporary testing tools stayed outside the repository; there are no application build or testing dependencies.

## Checks

| Scope | Executed verification |
| --- | --- |
| Layout matrix | 14 HTML pages × 11 widths × 2 themes × 2 directions = 616 combinations |
| Widths | 320, 360, 390, 430, 640, 768, 820, 1024, 1280, 1440 and 1920 pixels |
| Layout checks | Document and body bounds, displayed image loading and runtime errors |
| Functional regression | 57 assertions covering navigation, theme/direction persistence, explorers, pricing and enquiry handoff |
| Accessibility | 48 axe-core audits: six key routes × desktop/mobile × light/dark × LTR/RTL |
| Refinement-specific checks | 84 route/width/direction combinations covering meaningful font sizes, heading/copy/action gutters and menu visibility |
| Source audit | Local link and anchor targets, unique IDs, relative asset paths, versioned favicon references and standalone SVG validity |
| Fonts and subdirectory hosting | All eight font weights loaded; GitHub Pages-style relative navigation, booking prefill and reduced-motion behavior checked |

The layout pass reported no horizontal overflow, missing displayed images or runtime errors. All 57 functional assertions passed. The 48 accessibility audits reported no WCAG A/AA findings. This is automated evidence, not a claim of full accessibility certification. All 84 refinement-specific combinations passed.

## Preserved functionality

- Home dropdown by hover, click and keyboard, with Escape and outside-click dismissal.
- Sticky navigation after scrolling and the back-to-top action.
- Mobile drawer on the appropriate LTR/RTL side, controls inside it, and scrim dismissal.
- Persistent light/dark and direction settings.
- All four switchboard modules, selected states, updated detail links and arrow/Home/End keyboard navigation.
- All four Home 2 room-selector buttons.
- Six meaningful query-selected service details with matching booking links.
- Pricing category filters and correct service prefill.
- Required-field and past-date validation; preferred time and urgency selection.
- Hazard guidance, request review, safely rendered entered text, copy, download and editing with retained details.
- Keyboard-operable FAQ accordions.

## Composition changes verified

Only Home 1 contains the complete service-request route. About uses a professional-standards ledger and communication questions. Services uses a compact visit summary, with neither homepage explorer repeated. Home 2 has separate lighting, wiring/accessory, panel, safety-consideration and estimate compositions. Closing headings and copy are page-specific. Contact has no duplicate booking CTA section below its form.

The CSS is organized into eight source groups and consolidated breakpoint rules. Meaningful labels use at least 14px; body and service descriptions remain readable as modules stack on small screens. Narrow FAQ/legal content starts at the shared logical gutter. There are no centered public text sections.

## Visual evidence

Full-page captures were inspected for all eight requested routes at **1440px desktop, 820px tablet and 390px mobile**. The files are in `screenshots/`:

| Page | Desktop | Tablet | Mobile |
| --- | --- | --- | --- |
| Home 1 | [View](screenshots/home-desktop.png) | [View](screenshots/home-tablet.png) | [View](screenshots/home-mobile.png) |
| Home 2 | [View](screenshots/home2-desktop.png) | [View](screenshots/home2-tablet.png) | [View](screenshots/home2-mobile.png) |
| About | [View](screenshots/about-desktop.png) | [View](screenshots/about-tablet.png) | [View](screenshots/about-mobile.png) |
| Services | [View](screenshots/services-desktop.png) | [View](screenshots/services-tablet.png) | [View](screenshots/services-mobile.png) |
| Service Details | [View](screenshots/service-details-desktop.png) | [View](screenshots/service-details-tablet.png) | [View](screenshots/service-details-mobile.png) |
| Pricing Guide | [View](screenshots/pricing-desktop.png) | [View](screenshots/pricing-tablet.png) | [View](screenshots/pricing-mobile.png) |
| FAQ | [View](screenshots/faq-desktop.png) | [View](screenshots/faq-tablet.png) | [View](screenshots/faq-mobile.png) |
| Contact | [View](screenshots/contact-desktop.png) | [View](screenshots/contact-tablet.png) | [View](screenshots/contact-mobile.png) |

Additional captures cover [dark Home 1](screenshots/home-dark-desktop.png), [light RTL Home 2](screenshots/home2-light-rtl-tablet.png), [dark RTL booking](screenshots/booking-dark-rtl.png), [dark RTL mobile Services](screenshots/services-dark-rtl-mobile.png), and the [favicon at native sizes on light/dark surfaces](screenshots/favicon-v2-review.png).

Visual QA caught and corrected a desktop menu-button cascade conflict, a narrow-content gutter mismatch and a tightly cropped directory image. The pricing project-enquiry copy/action now follows a single editorial alignment rather than a remote second column.

## Favicon verification

Every HTML page references the newly named `circuit-socket-v2.svg?v=2`, with a versioned 32px PNG fallback. The conventional `favicon.svg` was also replaced. The SVG is standalone, namespaced and has a `0 0 32 32` viewBox. Native 16px/32px PNGs were rendered from the artwork and visually reviewed against white and near-black surfaces.

A cache-disabled browser navigation followed by `Page.reload(ignoreCache: true)` requested the new SVG twice, returning HTTP 200 and `image/svg+xml`, with `fromDiskCache: false`. Browser tab chrome itself is outside the headless screenshot surface; it was not captured or claimed as a screenshot. Both the browser-fetched asset and its rendered artwork were checked.

## Deployment and operational boundaries

Production target: <https://teknritsolutions-2.github.io/Electrician-Home-Wiring-Service/>. Pages is configured to publish `main` from the repository root. The final handoff reports the pushed commit and production verification result.

The enquiry form remains frontend-only. It does not send requests, confirm appointments or arrange emergency dispatch. Indicative rates and provider credentials still require client verification. The specified source structure keeps the 404 page at `pages/404.html`; GitHub's unknown-route response does not automatically select it without an additional root 404 file.

## Back-to-top position correction

The arrow is now fixed to the viewport, 20px from its logical end and bottom edge (with safe-area allowance). It appears after 300px of scrolling and hides on returning to the top. Footer spacing reserves room for it. Its click retains smooth scrolling and respects reduced-motion preferences.

Sixteen browser cases covered Home 1 and Contact, 1440px/390px, LTR/RTL, and normal/reduced motion. Checks exercised real clicks from the footer, verified `scrollY === 0`, stable viewport placement across scroll positions, hidden-at-top behavior and the sticky header. See [desktop](screenshots/back-top-fixed-desktop.png) and [mobile](screenshots/back-top-fixed-mobile.png) captures.

## Cirqavo identity and previous-project comparison

All 14 pages now display **Cirqavo**, without a brand subtitle. Header/footer marks use the favicon SVG, logo exports match its bytes, and dynamic titles use the new name. See [BRANDING.md](BRANDING.md) for the dated naming screen and its limits.

The current update passed 616 layout combinations, 57 functional assertions and 48 accessibility audits. An additional 72 compositions covered 18 breakpoint widths from 320–1440px in light/dark and LTR/RTL, checking background heroes, gutters, decorative overlap, footer columns and touch targets. Eight real-input drawer cases covered scroll locking, position preservation, closed-menu inertness and desktop resize. Full-page screenshots were refreshed for the current brand and layouts. Dedicated brand captures use `screenshots/cirqavo-header-*` and `screenshots/cirqavo-footer-*`.

The comparison and resulting fixes are recorded in [PREVIOUS-PROJECT-COMPARISON.md](PREVIOUS-PROJECT-COMPARISON.md).
