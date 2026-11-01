# claude-skills

Claude Code skills, stored in `.claude/skills/` so every session opened on this repository loads them automatically. Default web stack these skills assume: **Next.js + shadcn/ui + Tailwind, Supabase, Vercel**, built for the Israeli market (Hebrew/RTL).

When several skills overlap, `CLAUDE.md` tells Claude which one to prefer.

## Skills by stage of building a site

| Stage | Skills | Source |
|---|---|---|
| Understand what to build | brainstorming, grill-me, grilling, to-spec | obra/superpowers, mattpocock/skills |
| Plan | writing-plans, executing-plans, subagent-driven-development, using-git-worktrees | obra/superpowers |
| Design direction | ui-ux-pro-max, design-system, brand, design, banner-design, slides | nextlevelbuilder/ui-ux-pro-max-skill |
| UI polish | emil-design-eng, web-design-guidelines | emilkowalski/skills, vercel-labs/agent-skills |
| Build the UI | shadcn, ui-styling, vercel-react-best-practices | shadcn/ui, ui-ux-pro-max-skill, vercel-labs/agent-skills |
| Hebrew / RTL | hebrew-rtl-best-practices, hebrew-i18n, hebrew-tailwind-preset, hebrew-content-writer | skills-il/localization |
| Backend & data | supabase, supabase-postgres-best-practices, israeli-postgres-toolkit | supabase/agent-skills, skills-il/developer-tools |
| Payments (Israel) | grow-payment-gateway, cardcom-payment-gateway, tranzila-payment-gateway, israeli-payment-orchestrator | skills-il/tax-and-finance |
| Payments (global) | stripe-best-practices | stripe/ai |
| Email, SMS, WhatsApp | resend, react-email, email-best-practices, israeli-sms-gateway, israeli-whatsapp-business, israeli-phone-formatter | resend/resend-skills, skills-il |
| Code quality | tdd, test-driven-development, code-review, requesting-code-review, systematic-debugging, find-bugs, verification-before-completion, codebase-design, domain-modeling, improve-codebase-architecture | mattpocock/skills, obra/superpowers, getsentry/skills |
| End-to-end tests | webapp-testing, playwright-cli | anthropics/skills, microsoft/playwright-cli |
| Performance, SEO, accessibility | web-quality-audit, performance, core-web-vitals, seo, accessibility, best-practices | addyosmani/web-quality-skills |
| Security | owasp-security-review, israeli-appsec-scanner | getsentry/skills, skills-il/security-compliance |
| Israeli compliance | israeli-accessibility-compliance, israeli-privacy-shield, israeli-ecommerce-compliance | skills-il |
| Analytics & errors | posthog-instrument-integration, posthog-instrument-product-analytics, posthog-instrument-error-tracking | PostHog/ai-plugin |
| Deploy & operate | deploy-to-vercel, vercel-cli-with-tokens, vercel-optimize | vercel-labs/agent-skills |
| Session handoff | handoff, finishing-a-development-branch | mattpocock/skills, obra/superpowers |
| Other | hyperframes (HTML→video), setup-matt-pocock-skills | heygen-com/hyperframes, mattpocock/skills |

Renamed on import to avoid clashes: getsentry's `security-review` → `owasp-security-review` (Claude Code has a built-in `/security-review`), PostHog's `instrument-*` → `posthog-instrument-*`.

## Things to know

- **Stripe does not open accounts for Israel-based businesses.** For an Israeli business use Grow, Cardcom or Tranzila (see `israeli-payment-orchestrator`); `stripe-best-practices` is only for a business registered in a Stripe-supported country.
- **Compliance skills are guidance, not legal advice.** Israeli accessibility (regulations 35–35ו, IS 5568 at level AA, accessibility statement), the Privacy Protection Law after Amendment 13 (in force 14 Aug 2025) and the anti-spam law (Communications Law s.30A) all have real penalties — have a lawyer or a certified accessibility expert review before launch.
- **API keys these skills expect** (set as environment variables, never commit them): `VERCEL_TOKEN`, Supabase project URL and keys, `RESEND_API_KEY`, the PostHog project token, the payment gateway's terminal/API credentials, and `GEMINI_API_KEY` for the `design` skill's logo/CIP/icon generators. `.env*` files stay out of git.
- `ui-ux-pro-max` runs its search script from the repository root: `python3 .claude/skills/ui-ux-pro-max/scripts/search.py "<query>" --design-system`.

## Updating a skill

`npx skills add https://github.com/<owner>/<repo> --skill <name>`, then copy it into `.claude/skills/` (re-apply the renames above).
