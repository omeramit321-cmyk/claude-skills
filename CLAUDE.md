# Building a website: which skill, when

The user does not remember the skill names and should not have to. When they ask to build, change or launch a site, run the matching skills yourself at each stage below, without being asked. Before each one, say in a short line which skill you're using and why, in the user's language (often Hebrew).

1. **Before any code — understand it.** `brainstorming` (what to build and why, approaches, short design doc). If the user wants their idea stress-tested, `grilling`. To write it up as a spec, `to-spec`.
2. **Plan.** `writing-plans` once the design is approved; then `executing-plans` (or `subagent-driven-development` for larger plans).
3. **Design direction.** `ui-ux-pro-max` for style, palette, fonts and layout; `brand` if there is a brand to define or follow; `banner-design` / `design` for hero images, logos and social images.
4. **Build.** `shadcn` (with a `components.json`) or `ui-styling`; `vercel-react-best-practices` while writing React/Next.js; for Hebrew sites always `hebrew-rtl-best-practices` and `hebrew-i18n` (plus `hebrew-tailwind-preset` on Tailwind v4); `hebrew-content-writer` for site copy.
5. **Backend, payments, messaging — when the site needs them.** Data/auth: `supabase`, `supabase-postgres-best-practices`. Payments: `israeli-payment-orchestrator` → the chosen gateway skill. Email: `resend`, `react-email`, `email-best-practices`. SMS/WhatsApp: `israeli-sms-gateway`, `israeli-whatsapp-business`.
6. **While coding.** `test-driven-development` for features with logic; `systematic-debugging` on any bug; `verification-before-completion` before saying something works; `emil-design-eng` for animations and polish.
7. **Before showing the user a finished piece.** `code-review`, then `web-design-guidelines` on the UI.
8. **Before launch — every time, even if not asked.** `web-quality-audit` (performance, SEO, accessibility), `webapp-testing` for the main user flows, `owasp-security-review`, and for a site serving Israeli users `israeli-accessibility-compliance` (accessibility statement) and `israeli-privacy-shield` (privacy policy, consent) — `israeli-ecommerce-compliance` too if it sells anything. Report what needs a lawyer or certified accessibility expert.
9. **Launch and after.** `deploy-to-vercel`; `posthog-instrument-integration` + `posthog-instrument-error-tracking`; later `vercel-optimize`.

Skip stages that don't apply (a static one-page site needs no backend or payments) and say you're skipping them.

# Skill routing

This repository holds many skills, and some overlap. When more than one could apply, prefer:

- **Stress-testing a decision:** `llm-council` when the user faces a real decision with options and stakes and wants several perspectives (it runs 11 sub-agents, so not for small questions); `grilling` when they want their own plan interrogated question by question (`/grill-me` is the user's shortcut to it).
- **UI components:** `shadcn` in any project with a `components.json`; `ui-styling` for Tailwind without shadcn, and for posters/canvas compositions.
- **Design direction:** `ui-ux-pro-max` for style, palette and font choices; `emil-design-eng` for motion and polish; `web-design-guidelines` for reviewing finished UI.
- **Design tokens:** `shadcn` (its design-system flow) in shadcn projects; `design-system` otherwise.
- **Accessibility:** `israeli-accessibility-compliance` for anything legal or the accessibility statement; `accessibility` for technical WCAG fixes.
- **Code review:** `code-review` for reviewing a diff against standards and spec; `requesting-code-review` inside the superpowers execution workflow.
- **Security:** `owasp-security-review` for reviewing code; `israeli-appsec-scanner` when Israeli privacy-law obligations are in scope.
- **Performance:** `vercel-react-best-practices` while writing React/Next.js code; `performance` / `core-web-vitals` / `web-quality-audit` for measuring and auditing a running site.
- **Payments:** an Israel-based business can't open a Stripe account — use `israeli-payment-orchestrator` and the Grow/Cardcom/Tranzila skills; use `stripe-best-practices` only for a business registered in a Stripe-supported country.

Compliance skills (`israeli-*-compliance`, `israeli-privacy-shield`) give guidance, not legal advice; say so when relying on them for a launch decision.
