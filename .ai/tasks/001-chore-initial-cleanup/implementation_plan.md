# Repository Cleanup Implementation Plan

We are cleaning up a forked Next.js personal website template to remove the original author's specific content and prepare it for customization.

## Proposed Changes

### Version Control
- Create a new branch `chore/initial-cleanup`

---

### Blog Articles
- #### [DELETE] `app/thoughts/_articles/*.mdx`
  Delete all existing blog posts written by the original author.
- #### [NEW] `app/thoughts/_articles/hello-world.mdx`
  Create a simple placeholder article to serve as a reference template.

---

### Personal Assets
- #### [DELETE] `assets/images/*`
  Remove old post banners and photos.
- #### [DELETE] `public/og/*`
  Remove the author's Open Graph images.

---

### Core Pages
- #### [MODIFY] [page.mdx](file:///Users/admin/Downloads/hello/app/page.mdx)
  Strip the author's bio and personalized introduction from the home page, leaving only structural markup.
- #### [MODIFY] [projects/page.mdx](file:///Users/admin/Downloads/hello/app/projects/page.mdx)
  Remove the author's specific projects list and replace it with a generic placeholder structure.
- #### [MODIFY] [guestbook/page.mdx](file:///Users/admin/Downloads/hello/app/guestbook/page.mdx)
  Remove any author-specific context from the guestbook page.

---

### Site Metadata
- #### [MODIFY] [layout.tsx](file:///Users/admin/Downloads/hello/app/layout.tsx)
  Replace the hardcoded name, SEO configuration, and social media links with empty or generic placeholder strings.
- #### [MODIFY] [package.json](file:///Users/admin/Downloads/hello/package.json)
  Change the package name from `"shud.in"` to something generic, e.g., `"my-portfolio"`.
