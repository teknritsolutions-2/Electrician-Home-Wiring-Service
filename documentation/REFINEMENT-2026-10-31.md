# Cirqavo refinement — 31 October 2026

Baseline: `d488f0a68e364060e5e65cc60967a6e8ef4790c1`. This pass refines the existing HTML/CSS/vanilla JavaScript website. Cirqavo, the shared socket logo/favicon, Carbon Slate/Volt Citron palette, Sora/DM Sans and existing enquiry boundaries remain in place.

## Design changes

Home 2 now uses an authentic fitted-pendant-light photograph as the full banner background, with directional contrast, a content-sized layout, an architectural rule and a restrained circuit/installation note. Its typography, photograph and composition differ from Home 1. Image focal positions were adjusted after screenshot review; the photograph is never mirrored.

Services now has a five-category residential index: a primary Home Wiring module paired with four numbered photographic rows. A separate technical matrix covers Socket Installation, Electrical Inspection, Troubleshooting and Fixture Replacement. The new connection map describes infrastructure from the distribution panel to lighting, switches, outlets and wiring. Its buttons work by pointer, touch and keyboard, announce the selected explanation, and link to the supported service. It complements the existing Home 2 room explorer rather than repeating a room illustration. Connection traces follow variable-height button rows so wrapping does not break the bus. A short numbered workflow, safety note and FAQ finish the page.

Service Details is now a service specification sheet. Six query-selected services have distinct banner photographs, service-specific information and correct enquiry links. The former large-image/text/sticky-sidebar structure and its CSS were removed. Two scope columns, a compact numbered checklist, a different context photograph, preparation guidance, safety information and related links replace it. Every booking action is populated, including the closing CTA. The selected service is omitted from related links; an unknown ID safely falls back to Wiring.

## Typography measured in the browser

The initial computed-style audit found 14px mobile pricing/credential notes and component captions, a 14px hero note, and a 15px form introduction. Text was adjusted in the existing component and responsive rules.

| Content | Desktop | Phone |
| --- | --- | --- |
| Body | 17px | 16px |
| Section descriptions | 18px | 16px |
| Small/pricing/credential notes | 16px | 15px |
| Dimensional component caption | 15px | 15px |
| Home 2 installation caption | 15px | 15px |
| Form introduction | 16px | 16px |
| Room selector labels | 15px | 15px |
| Navigation / Home dropdown | 15px / 16px | 17px / 16px |
| Eyebrows | 14–15px | 14–15px |

Card descriptions remain 16–17px. Meaningful text was prioritized over decorative counters and circuit artwork. RTL currency strings now retain their intended reading order while remaining right-aligned. The journal inspection and panel-upgrade photographs were also corrected to match their subjects.

## Responsive corrections

The phone header is a compact 76px row with the full brand, a short Book action and a 44px menu control. The booking link retains its full accessible name. Tablet gutters stay at 40px from 600px upward; smaller phones use 20px. Substantial compositions stack below 680px, while compact service rows retain useful photography. The footer retains its identity row above three navigation columns on tablets and stacks naturally on phones.

Keyboard testing caught a visibility-transition bug that prevented focus entering the drawer immediately on opening. Visibility now switches immediately when opening and is delayed only when closing. Focus enters the Home control, wraps between drawer controls and the menu button, and returns on dismissal. Scroll locking and page-position preservation remain intact. Theme/direction controls stay inside the drawer, which opens from the logical start side.

Prior-project prevention references and applicability are recorded in [PREVIOUS-PROJECT-COMPARISON.md](PREVIOUS-PROJECT-COMPARISON.md). Sticky ancestors continue to use `overflow-x: clip`. No dashboard, authentication, sending integration or framework was introduced.

## Browser verification

Playwright used the installed Brave/Chromium browser. Temporary tooling and dependencies stayed outside the repository. Existing documented regression behavior was exercised with a fresh temporary runner because the earlier temporary scripts were no longer present.

| Check | Result |
| --- | --- |
| All 14 pages × 11 requested widths × light/dark × LTR/RTL | 616 combinations; no horizontal overflow, missing images or runtime errors |
| Focused typography/alignment/overlap checks | 170 combinations: five key routes × 17 widths × two directions |
| Functional regression | 202 assertions passed, including all six services, every enquiry link, both existing explorers, the new map, preferences, pricing, validation, safe review/copy/download/edit, FAQ and drawers |
| Accessibility | 48 axe-core audits; no WCAG A/AA findings |
| Back-to-top | 16 cases: Home/Contact × phone/desktop × LTR/RTL × normal/reduced motion |
| Touch and focus | Map nodes, Home dropdown navigation, room selector, drawer focus trapping and focus restoration passed |
| Source integrity | HTML local links/anchors, unique IDs, SVG parsing and JavaScript syntax passed |

Requested matrix widths: 320, 360, 390, 430, 640, 768, 820, 1024, 1280, 1440 and 1920px. Intermediate checks also cover 600, 679, 680, 700, 1099 and 1100px. The evidence describes browser-emulated viewports, not physical-device testing or a full accessibility certification.

## Rendered evidence

Screenshots were captured and reviewed for hierarchy, spacing, photography, readable controls, wrapping and directional composition. Review corrected banner cropping, drawer focus timing and RTL price ordering. The final pass includes 46 full-page/drawer captures plus three isolated Home 2 banners. Ten public routes are captured at 1440, 820 and 390px, alongside representative dark/RTL states and both drawer sides.

| Page | Desktop | Tablet | Phone |
| --- | --- | --- | --- |
| Home 2 banner | [View](screenshots/home2-banner-desktop.png) | [View](screenshots/home2-banner-tablet.png) | [View](screenshots/home2-banner-mobile.png) |
| Services | [View](screenshots/services-desktop.png) | [View](screenshots/services-tablet.png) | [View](screenshots/services-mobile.png) |
| Wiring specification | [View](screenshots/service-details-desktop.png) | [View](screenshots/service-details-tablet.png) | [View](screenshots/service-details-mobile.png) |
| Panel specification | [View](screenshots/panel-details-desktop.png) | [View](screenshots/panel-details-tablet.png) | [View](screenshots/panel-details-mobile.png) |
| Home 1 | [View](screenshots/home-desktop.png) | [View](screenshots/home-tablet.png) | [View](screenshots/home-mobile.png) |
| Contact | [View](screenshots/contact-desktop.png) | [View](screenshots/contact-tablet.png) | [View](screenshots/contact-mobile.png) |

Additional evidence: [tablet drawer](screenshots/drawer-tablet.png), [phone drawer](screenshots/drawer-mobile.png), [dark RTL drawer](screenshots/drawer-mobile-rtl.png), [dark Services](screenshots/services-dark-tablet.png), [dark RTL Services](screenshots/services-dark-rtl-mobile.png), [RTL Home 2](screenshots/home2-light-rtl-tablet.png), [dark RTL specification](screenshots/service-details-dark-rtl-tablet.png), and [dark phone Panel](screenshots/panel-details-dark-mobile.png). About, Pricing, FAQ and Home Journal also have refreshed desktop/tablet/phone captures.

Earlier dated comparison/brand screenshots remain evidence of their respective passes. Current page and drawer captures supersede their former responsive arrangements.
