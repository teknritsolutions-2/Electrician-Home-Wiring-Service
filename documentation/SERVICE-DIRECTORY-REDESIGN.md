# Cirqavo service panels

The expandable service index now shares the existing site's visual language. Carbon Slate headers, Volt Citron controls, recognizable electrical icons, 8px corners, soft surfaces and restrained photograph depth follow the treatments already used by the Home 1 service modules and dimensional component details. The drawing grid, crop marks and large reference numbers were removed. The introductory copy also follows the site's home-care tone.

The working expandable structure is preserved. Only one service opens at a time, and the current service's scope, photograph, assessment priorities and details link appear beneath its heading. The assessment footer spans the preview on larger screens; phone content stacks in reading order. All service information and enquiry links remain available.

## Implementation

- Shared semantic surface variables preserve light/dark behavior; the open carbon header uses explicit readable foreground colors.
- Electrical icons use the same thin SVG stroke as existing controls: plug, fan, light, switch and panel.
- Service numbers are compact metadata, leaving titles as the main navigation cues.
- Photo frames use the existing restrained offset-shadow treatment instead of the technical drawing treatment.
- Native summaries retain touch, Enter/Space and arrow/Home/End support. Selected headings remain clear of the sticky header.

## Verification

380 service/width/theme/direction states passed across five services, 19 widths, both themes and both directions. The widths are 320, 360, 390, 430, 600, 640, 679, 680, 700, 768, 820, 899, 900, 1024, 1099, 1100, 1280, 1440 and 1920px. Checks cover icon/text bounds, clipping, preview overlap, image loading, readable descriptions and stable initial scroll position.

The 90 touch/keyboard/heading-visibility checks, all five matching service links, 202 site interaction assertions and eight Services accessibility audits also passed. Actual screenshots were reviewed in desktop, tablet, phone and dark RTL views. These are browser-emulated checks, not physical-device testing or an accessibility certification.

## Current evidence

| View | Capture |
| --- | --- |
| Desktop | [1440px](screenshots/service-panels-1440-light-ltr.png) |
| Tablet | [820px](screenshots/service-panels-820-light-ltr.png) |
| Narrow tablet | [640px](screenshots/service-panels-640-light-ltr.png) |
| Phone | [390px](screenshots/service-panels-390-light-ltr.png) |
| Narrow phone | [320px](screenshots/service-panels-320-light-ltr.png) |
| Dark RTL | [820px](screenshots/service-panels-820-dark-rtl.png) |

The complete Services page captures were also refreshed. Earlier service-plan, service-board and service-directory captures remain records of the preceding designs.
