# Skill routing

This repository holds many skills, and some overlap. When more than one could apply, prefer:

- **Tests:** `tdd` for the test-first loop; `test-driven-development` only when following the superpowers workflow (`writing-plans` → `executing-plans`).
- **UI components:** `shadcn` in any project with a `components.json`; `ui-styling` for Tailwind without shadcn, and for posters/canvas compositions.
- **Design direction:** `ui-ux-pro-max` for style, palette and font choices; `emil-design-eng` for motion and polish; `web-design-guidelines` for reviewing finished UI.
- **Design tokens:** `shadcn` (its design-system flow) in shadcn projects; `design-system` otherwise.
- **Accessibility:** `israeli-accessibility-compliance` for anything legal or the accessibility statement; `accessibility` for technical WCAG fixes.
- **Code review:** `code-review` for reviewing a diff against standards and spec; `requesting-code-review` inside the superpowers execution workflow.
- **Security:** `owasp-security-review` for reviewing code; `israeli-appsec-scanner` when Israeli privacy-law obligations are in scope.
- **Performance:** `vercel-react-best-practices` while writing React/Next.js code; `performance` / `core-web-vitals` / `web-quality-audit` for measuring and auditing a running site.
- **Payments:** an Israel-based business can't open a Stripe account — use `israeli-payment-orchestrator` and the Grow/Cardcom/Tranzila skills; use `stripe-best-practices` only for a business registered in a Stripe-supported country.

Compliance skills (`israeli-*-compliance`, `israeli-privacy-shield`) give guidance, not legal advice; say so when relying on them for a launch decision.
