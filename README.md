# PIChE Singapore Chapter — Website

The premier community of Filipino Chemical Engineers in Singapore.
Next.js 15 (App Router) · React 19 · TypeScript · Tailwind CSS v4 · Framer Motion · Lucide Icons.

## Quick start

```bash
npm install
npm run dev      # http://localhost:3000
npm run build    # production build
```

## Structure

```
app/            Pages (App Router): / about membership events news resources contact join
components/     Navbar, Footer, HeroArt, EventList, JoinFlow, ContactForm, Reveal, Counter…
lib/data.ts     All content (events, tiers, board, news…) — CMS-ready: swap this file for a headless CMS later
public/logo.png Official chapter seal
```

## Notes

- **Design tokens** live in `app/globals.css` (`@theme`): orange `#F57C00`, blue `#14508C`, ink `#1F242B`.
- **Dark mode**: class-based toggle in the navbar, persisted to localStorage.
- **Fonts**: system stacks for zero-latency loads. To use a Google font, add `next/font/google` in `app/layout.tsx` and map it to `--font-display` / `--font-body`.
- **Forms** are front-end only (contact, newsletter, join flow). Wire them to Netlify Forms, Supabase, or an API route when ready.
- **Accessibility**: skip link, focus-visible styles, aria labels, reduced-motion support.
