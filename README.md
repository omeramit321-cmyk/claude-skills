# claude-skills

Claude Code skills, stored in `.claude/skills/` so every session opened on this repository loads them automatically.

| Skill | Source |
|---|---|
| shadcn | shadcn/ui |
| emil-design-eng | emilkowalski/skills |
| grill-me, to-spec, handoff, tdd, improve-codebase-architecture, code-review | mattpocock/skills |
| brainstorming, writing-plans, systematic-debugging | obra/superpowers |
| vercel-react-best-practices, web-design-guidelines | vercel-labs/agent-skills |
| hyperframes | heygen-com/hyperframes |
| ui-ux-pro-max, banner-design, brand, design, design-system, slides, ui-styling | nextlevelbuilder/ui-ux-pro-max-skill (MIT) |

`ui-ux-pro-max` runs its search script from the repository root: `python3 .claude/skills/ui-ux-pro-max/scripts/search.py "<query>" --design-system`. The `design` skill's logo, CIP and icon generators need `GEMINI_API_KEY` (and `pip install google-genai pillow`); everything else works without API keys.

Update a skill: `npx skills add https://github.com/<owner>/<repo> --skill <name>`, then copy it into `.claude/skills/`.
