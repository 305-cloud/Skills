# Skills and Repos Library

Everything Claude currently uses for Web Alpha work, in one place. Made 28 October 2026.

- **`skills/`**: one folder per skill Claude has active right now (160). Each has:
  - `ABOUT.md`: what the skill does, how to call it, and where it is installed.
  - `files/`: a backup copy of the skill itself. The 17 built into Claude Code have no `files/`, because they ship inside Claude Code.
- **`SKILLS-INDEX.md`**: all 160 skills in one table.
- **`REPOS.md`**: the 14 GitHub repos in current use, with links and local copies.
- **`SETUP-PROMPT.md`**: paste into another Claude to install everything and make it use the right skill on every job (with when and how for each).
- **`HANDOFF-PROMPT.md`**: a shorter prompt to restore anything that goes missing.

## How to use a skill

Type `/skill-name` in Claude Code (for example `/seo-audit` or `/superpowers:brainstorming`), or just describe the task: Claude picks the matching skill by itself.

Folder names use `__` where the skill name has `:`, because Windows can't use `:` in names. So `skills/marketing__seo-audit` is the skill `/marketing:seo-audit`.

The backups are copies. Editing them changes nothing; the live skills are at the paths shown in each `ABOUT.md`.
