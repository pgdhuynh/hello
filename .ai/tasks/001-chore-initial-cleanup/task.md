# Repository Cleanup Task

- [x] Create `chore/initial-cleanup` branch
- [x] Clean up blog articles
  - [x] Delete all `.mdx` files in `app/thoughts/_articles/`
  - [x] Create a placeholder "Hello World" article
- [x] Remove personal assets
  - [x] Delete images in `assets/images/`
  - [x] Delete files in `public/og/`
- [x] Reset core pages content
  - [x] Strip personal content from `app/page.mdx` (Home)
  - [x] Strip personal content from `app/projects/page.mdx`
  - [x] Strip personal content from `app/guestbook/page.mdx`
- [x] Update site metadata
  - [x] Update `app/layout.tsx` (names, SEO titles, social links)
  - [x] Update `package.json` package name

## Follow-up Fixes
- [x] Fix Vercel build errors in `mdx-components.tsx` caused by missing images and deleted articles
- [x] Fix Vercel build errors caused by missing exported `metadata` in `hello-world.mdx`
