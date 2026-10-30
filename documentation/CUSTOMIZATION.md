# Setup, customization and integrations

## Source structure

Only `index.html` is a root HTML page. All 13 secondary pages are in `pages/`. Styles are split into `style.css`, `dark-mode.css`, `rtl.css`, with local `fonts.css`. The main stylesheet has eight ordered groups: tokens, typography, layout, navigation, controls, shared components, page components and responsive rules. Breakpoint groups are consolidated; component replacements do not accumulate patches at the end. Behavior is in `assets/js/main.js`; editable rates are in `assets/js/config.js`. `assets/js/plugins/` is reserved and intentionally empty; no third-party runtime plugins are needed. `assets/fonts/` includes font license files.

## Branding

The project title is used as a descriptive identity, not an invented company name. The logo combines two conductive paths and junction nodes. Light/dark SVG exports and the favicon are in `assets/images/`. The new favicon is a compact socket/junction drawing in a Carbon Slate enclosure with Volt Citron contacts. All pages request `circuit-socket-v2.svg?v=2` and include `favicon-32-v2.png?v=2` as a fallback. `favicon.svg` also contains the replacement artwork; the previous icon is gone. Native 16px and 32px PNG exports are included. Style and behavior URLs use `?v=2` to prevent old assets from surviving an HTML refresh. Live header/footer SVGs use theme-aware color without mirroring in RTL.

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

Major headings, copy and actions share a start-aligned block. Narrow FAQ and legal containers follow the same logical page gutter, rather than centering the whole block. Home 1 retains the full request route; About uses a working-standards ledger; Services has its own compact visit summary and no copied homepage explorer. Home 2 has architectural lighting, a wiring/accessory comparison, panel callouts and separate estimate guidance. Closing content is specific to each page.

Meaningful eyebrows and metadata use at least 14px, service descriptions and controls use 16px, and primary desktop paragraphs use 17–18px. The logo subtitle is a compact 13px brand lockup, not an instruction or form label. Substantive modules stack below 680px. Under 480px, the header places booking on a second row to retain a readable 15px label rather than shrinking the controls.

## Accessibility and responsive behavior

Navigation collapses below 1100px. Utilities move inside the drawer, and the booking action remains in the header. The drawer traps keyboard focus and closes by Escape or the scrim. The desktop Home menu supports pointer hover, click, keyboard activation, Escape and outside clicks. The service tabs use arrow keys, Home and End. FAQ sections use native `details`/`summary`.

Use the visible RTL/LTR control to change reading direction; photographs and the logo stay unflipped. Mobile pricing is arranged as readable rows rather than an overflowing table. SVG circuit traces are decorative. Reduced motion disables tracing and object movement.

## Deployment

This is a static website. No build artifacts or dependencies need to be uploaded. All assets are local and every internal URL is relative. Any host must serve the correct MIME types for HTML, CSS, JS, JPEG, SVG and TTF. Preserve the folder tree when publishing to a GitHub Pages project subdirectory.
