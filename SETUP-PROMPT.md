# Prompt: set up another Claude with all of this

Paste everything below the line into a new Claude Code chat opened on this library folder. It installs every skill, agent and repo, then sets that Claude up to use them on every job.

---

You are setting up the owner's Claude with the skills, agents and repos in this "Skills and Repos Library" folder. The owner runs **Web Alpha** (websites, Google SEO, AI search visibility, lead research and outreach, social content, motion design and animated ads, AI automation, all for business clients). Read `README.md`, `SKILLS-INDEX.md` and `REPOS.md` first.

## Part 1: Install

1. **Standalone skills** (folders in `skills/` with no `__` in the name): copy each folder's `files/` contents to `C:\Users\HomePC\.claude\skills\<skill-name>\`. Skip any that are already there and match.
2. **Plugin skills** (folder names starting `superpowers__`, `marketing__`, `design__`, `finance__`, `productivity__`, `searchfit-seo__`, `canva__`, `postiz__`, `modern-web-guidance__`, `frontend-design__`, `cowork-plugin-management__`, `anthropic-skills__`): these come from plugins. List which plugins are missing and ask the owner to install them from the Claude app's plugin settings. Don't copy plugin files in by hand.
3. **Built-in skills** (`claude-code-builtin__…`): nothing to install; they ship with Claude Code.
4. **Agents:** clone `https://github.com/msitarzewski/agency-agents` into `%TEMP%\agency-agents` and copy only these 11 files into `C:\Users\HomePC\.claude\agents\`: `marketing-seo-specialist`, `marketing-aeo-foundations`, `marketing-ai-citation-strategist`, `marketing-social-media-strategist`, `marketing-content-creator`, `marketing-video-optimization-specialist`, `sales-offer-lead-gen-strategist`, `sales-outbound-strategist`, `paid-media-creative-strategist`, `engineering-frontend-developer`, `engineering-ai-engineer` (all `.md`). Don't install the other ~220.
5. **Repos:** for every repo in `REPOS.md` without a local copy, `git clone --depth 1` it into `C:\Users\HomePC\Documents\Codex\2026-10-13\lo\outputs\github-toolkit\<owner>--<repo>`. Never re-download `last30days-skill` if that copy exists. Install Scrapling with `pip install scrapling`.
6. **Save the rules:** append the "How to work" section below to `C:\Users\HomePC\.claude\CLAUDE.md` under a heading `# Skills and agents (Web Alpha)`, so every future chat follows it. Show the owner the text before saving.
7. **Report** what you installed, what was already there, and what the owner must do (plugin installs, sign-ins). Never enter passwords, change accounts, post publicly or delete anything.

## Part 2: How to work (save this to CLAUDE.md)

**The rule.** Before starting any task, check the list below. If a skill or agent fits, use it without being asked, and say in one line which one you're using. Web Alpha's own skills (`webalpha`, `web-alpha-service-delivery`, `ai-visibility-playbook`, `motion-design-taste`, `video-hooks`, `animation-scriptwriting`) win over generic ones when they disagree.

**How to use.** Skills: call them through the Skill tool, or type `/skill-name` (plugin skills are `/plugin:skill`, for example `/superpowers:brainstorming`). Agents: read the persona file in `~/.claude/agents/` and follow it inside the current chat. Don't spawn subagents for personas, because that multiplies token cost. Load one skill at a time, only when the task needs it.

**When to use what:**

- **Any Web Alpha client work or copy:** `web-alpha-service-delivery`, `webalpha` first, then the job-specific ones below.
- **Google SEO:** `seo-project-setup` (new client), `seo-audit`, `keyword-research`, `keyword-clustering`, `competitor-analysis`, `competitive-landscape`, `link-prospecting`, `local-seo` (Google Business Profile), `seo-report` (the write-up), `seo-coach` (explaining). Page-level fixes: `searchfit-seo:on-page-seo`, `technical-seo`, `schema-markup`, `internal-linking`, `broken-links`; quick checks `/searchfit-seo:seo-check`. Persona: `marketing-seo-specialist`.
- **AI search visibility (ChatGPT, Gemini, AI Overviews):** `ai-visibility-playbook`, `ai-visibility-audit`, `ai-prompt-research`, `searchfit-seo:ai-visibility`. Personas: `marketing-aeo-foundations`, `marketing-ai-citation-strategist`.
- **Content and blogs:** `searchfit-seo:content-strategy`, `content-brief`, `/searchfit-seo:create-topic`, `/searchfit-seo:create-content`, `content-translation`; `marketing:content-creation`, `draft-content`. Always finish prose with `humanizer`. Persona: `marketing-content-creator`.
- **Social posts and captions:** `video-hooks` (hooks, titles, captions), `webalpha` (hashtags, tone), `postiz` (scheduling via Postiz). Personas: `marketing-social-media-strategist`, `marketing-video-optimization-specialist`.
- **Lead research and outreach:** the lead engine in `Documents\lead-engine` (read its files first; it uses last30days and Scrapling), `marketing:email-sequence`. Personas: `sales-offer-lead-gen-strategist`, `sales-outbound-strategist`. Never send outreach without the owner's yes.
- **Motion design, animations, video ads:** `hyperframes` (read first), `hyperframes-cli`, `hyperframes-registry` (ready-made blocks, check before building any effect), `media-use` (music, voice, images), `motion-design-taste`, `animation-scriptwriting`, `video-hooks`, `short-form-stat-edit` (talking-head shorts), `remotion-to-hyperframes` (porting). Blocks: `canopy-part-title`, `code-slice-hero`, `cuboid-carousel`, `frost-sequence-camera-orbit`, `glass-shard-title`, `orbit-card`, `wireframe-portal-title`. Remotion projects: the `remotion-*` skills. Launch videos of a built site: `brag`, `brag-slim`. Figma input: `figma`. Persona: `paid-media-creative-strategist`.
- **Websites and front-end:** `frontend-design:frontend-design`, `modern-web-guidance`, `design:*` (critique, design-system, handoff, ux-copy, accessibility-review, user-research, research-synthesis), `canva:*` for Canva designs. Persona: `engineering-frontend-developer`.
- **AI automation:** n8n MCP for workflows, `claude-api` for Claude apps, `pinokio`/`gepeto` for local AI apps. Persona: `engineering-ai-engineer`.
- **Any coding:** `karpathy-guidelines`; `superpowers:brainstorming` before building, `writing-plans` → `executing-plans`, `systematic-debugging` for bugs, `test-driven-development`, `verification-before-completion` before saying done, `requesting-code-review`/`code-review` after.
- **Marketing plans and reports:** `marketing:campaign-plan`, `competitive-brief`, `brand-review`, `performance-report`.
- **Documents and files:** `anthropic-skills:docs` (default for documents), `docx`/`pdf`/`pptx`/`xlsx` only when that file type is asked for, `google-workspace` for Google files, `slideshow` for decks to present.
- **Research:** `anthropic-skills:deep-research` for multi-source reports; `graphify` for understanding a codebase or document set.
- **Browser and desktop:** `built-in-browser`, `chrome-browser`, `computer-use` skills before using those tools.
- **Charts, dashboards, pages:** `dataviz`, `artifact-design`, `artifact-diagramming`, `artifact-capabilities`.
- **Finance and bookkeeping:** `finance:*` (journal entries, reconciliation, statements, variance, close, audit, SOX).
- **Tasks and memory:** `productivity:*`, `anthropic-skills:consolidate-memory`, `explain-usage` for token questions.
- **Claude setup itself:** `update-config` (settings, hooks), `skill-creator`/`superpowers:writing-skills` (new skills), `plugin-authoring`, `loop`/`schedule` (repeating jobs), `fewer-permission-prompts`.

**Cost.** Keep it low: one skill or persona at a time, no background loops or watchers unless the owner asks, and no subagents unless a task truly needs parallel work.
