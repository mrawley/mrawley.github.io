# mrawley.github.io &mdash; Living Plan

## Where we are

- Scaffolded from Aminu Abdusalam's `personal-website-builder-aminu.md`
  playbook.
- Adapted for **Astro 6.4.8** because the corporate npm registry
  on this machine has a `before` date policy blocking Astro 7.x.
  All the playbook's Content Collections patterns (content.config.ts
  location, glob loader, render(entry) API) work on 6.4.8 too.
- Deployed to GitHub Pages at https://mrawley.github.io via
  GitHub Actions.

## Stack decisions

- **Framework:** Astro 6.4.8 (see note above about the 7.x block)
- **Styling:** vanilla CSS with design tokens in
  `src/styles/tokens.css` and `src/styles/global.css`. No
  Tailwind.
- **Content:** Astro Content Collections with Zod schemas at
  `src/content.config.ts`. Two collections: `projects` and
  `writing`.
- **Fonts:** Inter (body) + JetBrains Mono (accents), loaded from
  Google Fonts.
- **Theme:** dark mode default, no toggle for v1.
- **Accent color:** #40826D (viridian, playbook default).
- **Blog section name:** "Writing".
- **Hero tone:** hybrid (terminal aesthetic + conversational).

## Site structure

- `/` &mdash; Home. Terminal-aesthetic hero, brief intro, links
  to other sections.
- `/about/` &mdash; Bio, career timeline, honors, interests.
  Placeholder content pending achievements inventory.
- `/projects/` &mdash; Selected work (border-left accent) +
  Personal projects grid. Empty by default; add markdown files
  to `src/content/projects/`.
- `/writing/` &mdash; Blog. Empty by default; add markdown files
  to `src/content/writing/`.
- `/404` &mdash; terminal-style not-found page.

## Remaining todos

- [ ] **Populate About page** with real bio, timeline, honors,
  interests. Blocked on Todo #2 (achievements inventory) in the
  layoff transition plan.
- [ ] **Add real projects** to `src/content/projects/*.md` from
  Megan's approved career highlights.
- [ ] **Optionally add one blog post** if there's a real Connect
  reflection worth publishing. Ask before publishing.
- [ ] **Add favicon.svg** to `public/`.
- [ ] **Add resume.pdf** to `public/` for the downloadable resume
  link once the resume exists.
- [ ] **Verify LinkedIn URL** in `src/components/Footer.astro`
  (currently placeholder `/in/meganrawley/`). Correct if
  different.

## Personal GitHub setup notes

- **Personal account:** mrawley (github.com/mrawley)
- **Personal email for commits:** meganmrawley@gmail.com. Already
  set as per-repo git config in this repo.
- **Corporate global git config** (Megan Lange /
  megan.rawley@microsoft.com) is **NOT** touched by anything in
  this repo.
- **Auth for first push:**
  1. Create the `mrawley.github.io` repo on github.com:
     - Public (required for free GH Pages on personal accounts)
     - No README, no .gitignore, no license (repo must be empty)
     - You may need an incognito browser if your default GitHub
       login is a work account
  2. Generate a **fine-grained personal access token** scoped
     ONLY to `mrawley/mrawley.github.io`:
     - github.com &rarr; Settings &rarr; Developer settings
       &rarr; Personal access tokens &rarr; Fine-grained
     - Expiration: 90 days or shorter
     - Repository access: Only select `mrawley/mrawley.github.io`
     - Permissions &rarr; Repository: Contents: Read and write,
       Metadata: Read-only
     - Generate and COPY the token immediately (only shown once)
  3. Add the remote:
     `git remote add origin https://github.com/mrawley/mrawley.github.io.git`
  4. First push: `git push -u origin main`. When prompted for
     password, paste the PAT. Windows Credential Manager caches
     it after.
- **Enable Pages:** repo Settings &rarr; Pages &rarr; Source =
  "GitHub Actions"

## Post-Microsoft migration notes

**IMPORTANT: this repo lives on a Microsoft-owned laptop that will
be reclaimed by 6 PM PT on Tuesday, July 8, 2026.**

- As soon as the first push to `mrawley/mrawley.github.io`
  succeeds, the code is durably on GitHub under Megan's personal
  account. Losing the laptop no longer loses the site.
- To resume development on a personal machine post-Microsoft:
  1. `git clone https://github.com/mrawley/mrawley.github.io.git`
  2. `npm install`
  3. `npm run dev`
- No corporate identity is embedded anywhere in this repo. The
  per-repo git config is used everywhere and does not touch the
  global config.

## Corporate compliance notes

- `misc/` folder is gitignored (Aminu playbook gotcha). For
  personal reference files that shouldn't be committed.
- All content on the public site is Megan's own bio, work, and
  reflections. No proprietary Microsoft content.
- No Microsoft internal financial figures, product plans, or
  confidential material published on the public site.

## Writing style rules (per Aminu playbook)

- No em dashes. Use regular dashes or rewrite.
- Personal, honest tone. No corporate speak.
- No listicle energy. Prose over bullets when the point is a
  thought, not a spec.
- Never fabricate. If a fact isn't in Megan's materials, ask.
- Age-agnostic reflective phrasing in reflective writing (say
  "younger me" / "now me" instead of specific ages) so posts
  age well.
