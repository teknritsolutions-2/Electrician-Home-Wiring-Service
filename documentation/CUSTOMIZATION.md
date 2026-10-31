# Setup, customization and integrations

## Source structure

Only `index.html` is a root HTML page. All 13 secondary pages are in `pages/`. Styles are split into `style.css`, `dark-mode.css`, `rtl.css`, with local `fonts.css`. The main stylesheet has eight ordered groups: tokens, typography, layout, navigation, controls, shared components, page components and responsive rules. Breakpoint groups are consolidated; component replacements do not accumulate patches at the end. Behavior is in `assets/js/main.js`; editable rates are in `assets/js/config.js`. `assets/js/plugins/` is reserved and intentionally empty; no third-party runtime plugins are needed. `assets/fonts/` includes font license files.

## Branding

The public brand is **Cirqavo**, displayed without a subtitle. See `BRANDING.md` for the dated naming search and its limits. Headers, footers and the favicon reference the same `circuit-socket-v2.svg?v=2` artwork. `logo-light.svg` and `logo-dark.svg` export that identical two-color symbol. The mark stays unflipped in RTL. The name for generated content is in `ELECTRICAL_CONFIG.brand`; static HTML titles and brand lockups also contain the name for immediate, accessible rendering.

The existing favicon SVG and 16px/32px PNGs retain their approved artwork. The main and direction stylesheets use `?v=8`; the dark stylesheet, configuration and behavior URLs use `?v=6`; no hosting path or repository rename is required.

The two brand colors are Carbon Slate `#26343B` and Volt Citron `#D2ED68`. Semantic neutral and surface variables live at the top of `style.css`; dark overrides are in `dark-mode.css`. Headings use Sora; body copy uses DM Sans. Fonts and images do not request a third-party service at runtime.

## Content editing

Each HTML page contains its complete layout, including a generated common header and footer. To change shared navigation, update all 14 files consistently. Keep the relative `../` prefix for secondary pages. Service detail fields, explorer descriptions and service query keys are in `serviceData` in `main.js`. The default detail route displays wiring. Unknown service/article query values safely fall back to a known entry.

Prices appear through `data-rate` attributes and use `ELECTRICAL_CONFIG.prices`, including the service detail sidebar. No other source contains hard-coded numeric prices. The empty provider fields reserve space for verified details; entering a value there alone does not render it or activate a sending integration. Add a real contact block only after those details have been verified.

The five Home Journal articles are written as general service-planning information. They do not include hazardous repair instructions, fake author profiles or invented publishing history.

## Booking handoff

Booking links accept `?service=wiring`, `fan`, `lighting`, `switchboard`, `panel` or `inspection`, followed by `#booking`. Required fields are validated in the browser. The date minimum is recalculated on submission using the visitor's local date. Preferred times are requests, never real-time availability.

The urgency selector displays general keep-away guidance for a potential electrical hazard. It does not trigger dispatch. The summary uses DOM text nodes, so entered markup is displayed as text. Form contents are never written to local storage or sent over the network. Theme and direction are the only local-storage values.

Copy uses the browser Clipboard API, which usually requires HTTPS or localhost. If denied, an honest fallback offers the text download or manual copying. Download creates a temporary Blob URL and revokes it after use. Editing preserves the current page's form state. Reloading does not persist personal details.

## Adding a real enquiry service

There is no email address or submission destination configured. To add sending later, connect an approved backend, validate on the server, update the privacy/terms notices, define retention and access controls, and handle real success/error responses. Confirm receiving the request before displaying any sent state; appointment confirmation requires a separate provider action. Do not put API secrets in client-side JavaScript.

## Section composition and alignment

Major headings, copy and actions share a start-aligned block. Narrow FAQ and legal containers follow the same logical page gutter, rather than centering the whole block. Home 1 retains the full request route; About uses a working-standards ledger; Services has a joined photographic service board, an infrastructure connection map and a compact workflow. Home 2 has a photographic architectural-lighting banner, a wiring/accessory comparison, panel callouts and separate estimate guidance. Closing content is specific to each page.

Meaningful eyebrows and metadata use at least 14px, service descriptions and controls use 16px, and primary desktop paragraphs use 17–18px. Substantive modules stack below 680px. Below 680px the header uses a single row with the full brand, a short “Book” label and a 44px menu control. The booking link retains its full accessible name.

## Accessibility and responsive behavior

Navigation collapses below 1100px. Utilities move inside the drawer, and the booking action remains in the header. The closed compact drawer is inert. Opening it locks root scrolling and preserves the current page position; it traps keyboard focus and closes by Escape or the scrim. Resizing to desktop clears the lock. The desktop Home menu supports pointer hover, click, keyboard activation, Escape and outside clicks. The service tabs use arrow keys, Home and End. FAQ sections use native `details`/`summary`.

Use the visible RTL/LTR control to change reading direction; photographs and the logo stay unflipped. Mobile pricing is arranged as readable rows rather than an overflowing table. SVG circuit traces are decorative. Reduced motion disables tracing and object movement.

## Deployment

This is a static website. No build artifacts or dependencies need to be uploaded. All assets are local and every internal URL is relative. Any host must serve the correct MIME types for HTML, CSS, JS, JPEG, SVG and TTF. Preserve the folder tree when publishing to a GitHub Pages project subdirectory.

The back-to-top arrow is a fixed 46px viewport control at the logical end/bottom, visible after 300px of scrolling. Its click returns to the actual page top; reduced-motion mode uses an immediate scroll. It is no longer positioned by the footer layout.

Below 1100px, Home 1 uses the retained hero photograph as a full background with a direction-aware contrast overlay. Its decorative component clears the copy and actions on narrow tablets and is hidden below 680px. From 600–1099px the footer brand occupies a full row above three equal navigation columns; narrower phones stack those groups. Icon controls use 44px touch targets.

## Service architecture and specification sheets

`serviceData` remains the source for six service IDs. Service Details uses `[data-detail-image]` as its full-width photographic banner. The `contexts` map supplies a different photograph and caption for `[data-detail-context-image]` and `[data-detail-context-caption]`. Shared dynamic fields update via the original `data-detail-*` attributes; every `[data-detail-book]` link is updated, including the closing action. Related links omit the current service. No sticky booking sidebar remains.

Services' five `[data-connection]` buttons describe an infrastructure connection rather than the Home 2 room view. `connectionDescriptions` controls their title, explanation and service link; the outlets node routes to the supported switchboard/socket service. Buttons support pointer/touch, Enter/Space and arrow/Home/End navigation, with an announced result. Keep the map explanatory rather than adding installation instructions.

The Home 2 banner photograph is `architectural-lighting.jpg`. Its full-background image stays unmirrored; gradients reverse in RTL. The banner has no fixed minimum height. Its installation note and circuit path remain in document flow to prevent text overlap. The main and direction stylesheets use version 8; the dark stylesheet and JavaScript use version 6.

The Services board uses five `.service-tile` links in a 12-column desktop grid. Tablets use two columns with a full-width protection panel; phones stack below 680px. `.service-tile-copy` keeps text in normal flow, and the image/gradient layers stay behind it. Keep panel minimums content-aware and preserve the contained tablet equipment photograph.
