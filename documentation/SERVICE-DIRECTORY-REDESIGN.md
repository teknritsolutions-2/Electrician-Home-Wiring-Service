# Service directory follow-up

The requested five-service section now uses one consistent service ledger instead of an oversized Wiring feature beside a separate list. All five services have the same visual weight, a practical description, relevant photograph and working details link.

Desktop uses aligned columns for the number, service name, explanation, photograph and action. Tablets combine the title and explanation into one column beside the photograph. Below 680px, the title and image share the opening area, with the description and visible action flowing across the row below. Heights follow the content; there are no fixed card heights, image stretch fillers or spanning feature panels. The introduction stays at the shared logical gutter.

The former `service-architecture`, `wiring-module` and `service-index-row` rules were removed from every breakpoint. Only the main stylesheet URL advances to version 7. The existing map, supporting service matrix, workflow, FAQ, themes, RTL and booking routes remain available.

## Verification

- 76 rendered combinations: 19 widths × light/dark × LTR/RTL.
- Widths: 320, 360, 390, 430, 600, 640, 679, 680, 700, 768, 820, 899, 900, 1024, 1099, 1100, 1280, 1440 and 1920px.
- Checked every row for internal overlap, clipped text, missing images, unwanted gaps, content exceeding its bounds, and description sizes below 16px. No issues found.
- All five directory links reached their matching dynamic service and service-specific enquiry route.
- The existing 202 functional assertions passed again.
- Eight Services accessibility audits passed across desktop/mobile, themes and directions, with no WCAG A/AA findings.
- Browser screenshots were visually reviewed at desktop, tablet, narrow tablet and narrow phone sizes, including dark RTL.

These are browser-emulated viewport checks, not physical-device testing or an accessibility certification.

## Evidence

| View | Capture |
| --- | --- |
| Desktop, 1440px | [Section](screenshots/service-directory-1440-light-ltr.png) |
| Tablet, 820px | [Section](screenshots/service-directory-820-light-ltr.png) |
| Narrow tablet, 640px | [Section](screenshots/service-directory-640-light-ltr.png) |
| Phone, 390px | [Section](screenshots/service-directory-390-light-ltr.png) |
| Narrow phone, 320px | [Section](screenshots/service-directory-320-light-ltr.png) |
| Dark RTL tablet | [Section](screenshots/service-directory-820-dark-rtl.png) |

Full Services page captures were refreshed for desktop, tablet, phone, dark tablet and dark RTL phone. The viewport-fixed back-to-top control retains its existing scroll behavior.
