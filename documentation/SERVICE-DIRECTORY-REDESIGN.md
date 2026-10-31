# Expandable service installation sheets

The residential service index now uses five numbered installation sheets. Opening a service reveals its scope, a photograph framed with drawing marks, three assessment priorities and a details link. One sheet opens at a time, with Wiring shown initially. The remaining service names stay available as full-width controls.

The open sheet uses a shared assessment footer across the desktop/tablet preview. This balances the explanation and photograph without leaving a long empty column. On phones, the explanation, photograph and assessment points follow the selected heading in one column. Heights follow the content; photos and text do not depend on absolute positioning. Cirqavo's branding, palette and existing home-page interactions remain intact.

## Interaction and implementation

Native `details`/`summary` provide expansion by pointer, touch, Enter and Space. Up/Down and Home/End move keyboard focus between service headings. The native named group and a small JavaScript fallback preserve exclusive opening. A selected heading is brought clear of the sticky header after the previous sheet closes. The page does not scroll itself on initial load.

Each service has its own description, image, assessment priorities and matching details/enquiry route. The connection map, supporting services, workflow and FAQ remain available. The former photographic panel styles were removed. Current components are `.service-plan`, `.service-case`, `.case-summary`, `.case-content` and `.case-checkpoints`. Main/direction stylesheets and main behavior use version 9; configuration and the dark stylesheet remain version 6.

## Browser verification

- 380 rendered states: five services × 19 widths × light/dark × LTR/RTL.
- Widths: 320, 360, 390, 430, 600, 640, 679, 680, 700, 768, 820, 899, 900, 1024, 1099, 1100, 1280, 1440 and 1920px.
- Checked exclusive opening, text bounds, clipping, preview overlap, image loading, readable descriptions and stable initial scroll position.
- 90 touch, keyboard and selected-heading visibility checks across phone/tablet widths in both directions.
- All five details links reach their matching service and service-specific enquiry route.
- The 202 existing functional assertions and eight Services accessibility audits passed.
- Actual desktop, tablet, phone and dark RTL screenshots were reviewed. A narrow-phone number-width issue was corrected during the pass.

These are browser-emulated checks, not physical-device testing or an accessibility certification.

## Current evidence

| View | Capture |
| --- | --- |
| Desktop, 1440px | [Section](screenshots/service-plan-1440-light-ltr.png) |
| Tablet, 820px | [Section](screenshots/service-plan-820-light-ltr.png) |
| Narrow tablet, 640px | [Section](screenshots/service-plan-640-light-ltr.png) |
| Phone, 390px | [Section](screenshots/service-plan-390-light-ltr.png) |
| Narrow phone, 320px | [Section](screenshots/service-plan-320-light-ltr.png) |
| Dark RTL tablet | [Section](screenshots/service-plan-820-dark-rtl.png) |

Full Services page captures also show the installation sheets. The earlier `service-board-*` and `service-directory-*` images record preceding designs. The viewport-fixed back-to-top control retains its existing scroll behavior.
