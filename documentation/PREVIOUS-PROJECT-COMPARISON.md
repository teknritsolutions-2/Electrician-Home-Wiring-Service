# Previous-project comparison

Reviewed the user's actual Physiotherapy & Rehabilitation Clinic follow-up requests alongside that project's verification notes and implementation history. Relevant commits included `5c411b5`, `1b1cd1f`, `d3754f4`, `b754635` and `6b0b3f9`. Only applicable design and interaction fixes were carried into this electrical-service site.

| Previous request or issue | Result here |
| --- | --- |
| Remove the descriptor beneath the brand | Removed from all 28 header/footer lockups. Cirqavo stands alone beside the shared favicon mark. |
| Use background hero photography on mobile/tablet | Home 1 now uses its retained photograph as a full background below 1100px, with readable overlays in both directions. Home 2 already uses background photography. |
| Keep tablet footer brand above three navigation columns, including 600px | Full-width identity row above three equal columns from 600–1099px; smaller phones stack the lists. |
| Align logos and copy with exact page gutters | Verified shared logical gutters in LTR/RTL without compensating offsets. |
| Avoid tablet gaps and incomplete card rows | Audited card grids, paired compositions and full-row visit content; retained fitting pairs and complete rows rather than adding empty height. |
| Align tablet actions and provide usable touch controls | Existing CTA pairs remain side by side where space allows; header utility controls now have 44px targets. |
| Keep compact drawer utilities accessible and background content stable | Fixed a real background-scroll bug. Root scrolling is locked while open, opening/closing preserves position, closed navigation is inert, and desktop resize clears the lock. |
| Avoid decorative overlap and preserve dark-mode contrast | Narrow-tablet hero paragraph width now clears the component illustration. Phone illustrations are hidden; directional photo overlays keep hero copy readable. Existing circuit artwork remains appropriate to this site. |
| Avoid repeated prominent photography | Added two distinct, locally stored socket photographs for the Home 1 mosaic and Home 2 comparison. Interactive thumbnails may intentionally match their selected preview. |
| Keep back-to-top at the actual viewport edge | Retained the fixed arrow and tested click-to-top behavior in both directions and reduced motion. |
| Dashboard/auth and clinic-specific wave changes | Not applicable to this site's scope or visual system. |

Validation includes 616 route/width/theme/direction layout combinations, 57 interaction assertions, 48 accessibility audits, plus 72 focused breakpoint compositions and eight real-input drawer cases. These are browser-emulated viewport checks, not claims of testing physical mobile devices. Current screenshots cover desktop, tablet, mobile, dark mode and RTL.
