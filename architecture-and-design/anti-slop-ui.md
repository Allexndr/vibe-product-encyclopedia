# Anti-AI-Slop UI/UX & Mobile Adaptive (MurdaSoft Block 02)

## Prohibited AI-Slop Patterns
- No generic purple-indigo gradients on dark backgrounds.
- No 3-column "feature icon cards" with identical blur/glow borders.
- No duplicate navigation bars or horizontal scrollbars inside floating docks.

## Required Production Rules
1. **Color Discipline:** 1 clean base surface (`#FFFFFF` or `#0B101C`), 1 primary accent (`#10B981`), WCAG AA contrast (`>= 4.5:1`).
2. **Spacing & Shadows:** Strictly follow the 4px/8px spacing scale; avoid shadows larger than `shadow-md` on cards.
3. **Mobile First (`375px`):** Zero horizontal overflow; all interactive tap targets >= `44x44px`.
4. **4 UI States:** Always implement Loading (skeleton), Empty (with CTA), Error (with retry), and Success states.
