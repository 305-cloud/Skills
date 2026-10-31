# Prompt for another Claude

Use this if a skill or repo goes missing (new computer, reinstall, a folder got deleted). Paste everything below the line into a new Claude Code chat opened on this library folder.

---

You are restoring the owner's Claude setup from the "Skills and Repos Library" folder you are in. Read `README.md`, `SKILLS-INDEX.md` and `REPOS.md` first.

1. **Check what is missing.** For every folder in `skills/`, read its `ABOUT.md` and check whether the "Installed at" path still exists. List the missing ones before changing anything.
2. **Restore standalone skills** (folder names with no `__`, for example `skills/seo-audit`): copy that folder's `files/` contents to `C:\Users\HomePC\.claude\skills\<skill-name>\`.
3. **Restore plugin skills** (folder names like `superpowers__…`, `marketing__…`, `searchfit-seo__…`, `canva__…`): don't copy files in by hand. Ask the owner to reinstall that plugin from the Claude app's plugin settings, then check the skill shows up again.
4. **Skip `claude-code-builtin__…` folders.** They come with Claude Code; updating Claude Code restores them.
5. **Restore agents:** if `C:\Users\HomePC\.claude\agents\` is missing any of the 11 personas in `REPOS.md`, clone `https://github.com/msitarzewski/agency-agents` into `%TEMP%\agency-agents` and copy only those 11 `.md` files into that folder. Don't install the rest.
6. **Restore repos:** for each repo in `REPOS.md` whose local copy is missing, `git clone --depth 1` it into `C:\Users\HomePC\Documents\Codex\2026-10-13\lo\outputs\github-toolkit\<owner>--<repo>`. Don't re-download `last30days-skill` if that copy exists. Install Scrapling with `pip install scrapling`.
7. **Report** what you restored, what you skipped and why, and anything the owner has to do (plugin reinstalls, sign-ins). Don't enter passwords, change accounts or delete anything.
