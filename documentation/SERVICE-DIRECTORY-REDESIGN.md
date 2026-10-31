# Photographic service board

The five residential services now form one joined photographic composition. Service titles, concise descriptions and visible links are integrated into the images, with numbered tabs and Volt Citron arrow controls. The frame, narrow seams and consistent controls tie the panels together. Cirqavo's palette, typography and original logo remain intact.

Desktop uses two wide panels above three smaller panels. Tablets use a two-column arrangement with a full-width panel-upgrade composition that pairs copy with a contained equipment photograph. Below 680px, all five services stack vertically. Panel heights grow with their text; the photography supplies the visual area rather than empty filler. Photos are not mirrored in RTL. Directional arrows and the tablet gradient follow the reading direction.

All five panels are full links to the existing dynamic service pages. The connection map, supporting services, workflow, FAQ, theme/direction preferences and booking routes remain available. The preceding ledger and its breakpoint rules were removed; the current components are `.service-board`, `.service-tile` and `.service-tile-copy`. The main stylesheet and direction stylesheet use version 8.

## Browser verification

- 76 layout combinations: 19 widths × light/dark × LTR/RTL.
- Widths: 320, 360, 390, 430, 600, 640, 679, 680, 700, 768, 820, 899, 900, 1024, 1099, 1100, 1280, 1440 and 1920px.
- Checked text bounds, clipping, tag/copy separation, image loading, readable descriptions, oversized panels and complete grid rows. No issues found.
- All five panel links reach the matching service and service-specific enquiry route.
- The 202 functional assertions and eight Services accessibility audits passed.
- Actual screenshots were reviewed at desktop, tablet, narrow tablet, phone and narrow phone sizes, including dark RTL.

These are browser-emulated viewport checks, not physical-device testing or an accessibility certification.

## Current evidence

| View | Capture |
| --- | --- |
| Desktop, 1440px | [Section](screenshots/service-board-1440-light-ltr.png) |
| Tablet, 820px | [Section](screenshots/service-board-820-light-ltr.png) |
| Narrow tablet, 640px | [Section](screenshots/service-board-640-light-ltr.png) |
| Phone, 390px | [Section](screenshots/service-board-390-light-ltr.png) |
| Narrow phone, 320px | [Section](screenshots/service-board-320-light-ltr.png) |
| Dark RTL tablet | [Section](screenshots/service-board-820-dark-rtl.png) |

The full Services desktop/tablet/mobile captures and representative dark/RTL views also show this composition. The earlier `service-directory-*` images record the preceding row layout. The existing viewport-fixed back-to-top control retains its scroll behavior.
