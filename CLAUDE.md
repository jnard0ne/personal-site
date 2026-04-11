# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm run dev       # start dev server at localhost:4321
npm run build     # production build to dist/
npm run preview   # preview the production build
```

## Stack

- **Astro 6** — static site generator, zero JS shipped by default
- **Tailwind CSS v4** — integrated via `@tailwindcss/vite` Vite plugin (no `tailwind.config.js`; Tailwind config lives in `src/styles/global.css` using `@plugin` directives)
- **TypeScript** (strict mode)

## Architecture

### Content collections

Content is managed through Astro's Content Layer API. Schemas are defined in `src/content.config.ts`.

- **Blog posts** — Markdown files in `src/content/blog/`. Required frontmatter: `title`, `description`, `date`. Optional: `draft: true` to hide from listings.
- **Projects** — Markdown files in `src/content/projects/`. Required frontmatter: `title`, `description`. Optional: `url`, `repo`, `tags[]`, `status` (`active` | `completed` | `paused`).

### Pages

- `/` — home page with about section + previews of active projects and recent posts
- `/projects` — full project list grouped by status
- `/blog` — post listing grouped by year
- `/blog/[slug]` — individual post rendered via `render()` from `astro:content`

The slug for blog posts matches the filename (without `.md`).

### Layout

`src/layouts/BaseLayout.astro` wraps every page. It imports `src/styles/global.css`, renders the nav, and uses a `max-w-3xl` centered column.

Typography for blog post body copy uses the `prose` classes from `@tailwindcss/typography`.

## Customization checklist

When setting up the site for real, replace these placeholders:
- "Your Name" in `BaseLayout.astro` (nav, footer) and page `<title>` tags
- GitHub and LinkedIn URLs in `BaseLayout.astro` footer
- Bio copy in `src/pages/index.astro`
- Favicon letter in `public/favicon.svg`
- `repo` URL in `src/content/projects/personal-site.md`
