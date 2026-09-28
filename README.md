<div align="center">

# Hi, I'm MMK 👋

**Full-stack Developer** — building clean, fast and reliable web applications with modern JavaScript, from REST APIs to polished user interfaces.

[![Portfolio](https://img.shields.io/badge/Portfolio-6c5ce7?style=for-the-badge&logo=googlechrome&logoColor=white)](https://portfolio-xnfb.onrender.com)
[![Email](https://img.shields.io/badge/Email-00cec9?style=for-the-badge&logo=gmail&logoColor=white)](mailto:tetraoscloud931@gmail.com)
[![npm](https://img.shields.io/badge/npm-Packages-0ae448?style=for-the-badge&logo=npm&logoColor=white)](#-open-source)

</div>

---

## About

I'm **MMK** — a full-stack developer focused on the JavaScript/TypeScript ecosystem. I like taking an idea from an empty folder to something live on the internet: a REST API with real validation, a responsive interface, and a deployment that actually stays up.

Most of my work is **Arabic-first and RTL by design** — not an English layout flipped at the end, but interfaces that were built right-to-left from the first line of CSS.

I care about the details that are easy to skip: loading and empty states, error handling that says something useful, `prefers-reduced-motion`, keeping a demo link alive after 15 idle minutes.

## 🔭 Currently

Building Arabic/RTL product surfaces in React, and pulling the parts I keep rewriting into reusable packages.

## 📦 Open source

### [`@tetraoscloud931-creator/react-rtl`](https://github.com/tetraoscloud931-creator/react-rtl)

RTL primitives for React. Published to GitHub Packages.

Most RTL libraries stop at `dir="rtl"`. This one treats the locale as **state** — a single provider owns it, direction derives from it, and every consumer reads from the same source instead of re-deriving `ar` → `rtl` in a dozen files.

```bash
npm install @tetraoscloud931-creator/react-rtl --registry=https://npm.pkg.github.com
```

```tsx
import { LocaleProvider, useIsRTL, useNumberFormat } from '@tetraoscloud931-creator/react-rtl';

function Price({ amount }: { amount: number }) {
  const money = useNumberFormat({ style: 'currency', currency: 'SAR' });
  return <span dir="auto">{money.format(amount)}</span>;
}

export function App() {
  return (
    <LocaleProvider locale="ar">
      <Price amount={1250} />
    </LocaleProvider>
  );
}
```

- `useDirection()` / `useIsRTL()` — from the provider, or live off `<html>` via `MutationObserver`
- `useNumberFormat()` / `useDateTimeFormat()` — memoized per locale instead of rebuilt every render
- `detectDirection()` — via `Intl.Locale#maximize`, so `az-Arab` is RTL and `ar-Latn` is LTR
- Zero runtime dependencies, ESM + CJS + types, SSR-safe, 55 tests

## 🛠 Tech Stack

<div align="center">

**Frontend**

![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white) ![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white) ![React Three Fiber](https://img.shields.io/badge/React_Three_Fiber-000000?style=for-the-badge&logo=react-three-fiber&logoColor=white) ![Framer Motion](https://img.shields.io/badge/Framer_Motion-0055FF?style=for-the-badge&logo=framer&logoColor=white) ![GSAP](https://img.shields.io/badge/GSAP-0AE448?style=for-the-badge&logo=gsap&logoColor=black) ![Lenis](https://img.shields.io/badge/Lenis-111111?style=for-the-badge&logo=lenis&logoColor=white)

**Backend**

![Node.js](https://img.shields.io/badge/Node.js-5FA04E?style=for-the-badge&logo=nodedotjs&logoColor=white) ![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white) ![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white) ![REST API](https://img.shields.io/badge/REST_API-00cec9?style=for-the-badge)

**Tooling**

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white) ![Render](https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=white) ![npm](https://img.shields.io/badge/npm-CB3837?style=for-the-badge&logo=npm&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

</div>

## 💼 Selected work

> Client and product repositories are private. Live deployments are linked.

**TaskFlow** — full-stack task manager, React (Vite) frontend on a Node + Express API.
Priorities, smart due-date labels, debounced search, a stats dashboard, optimistic UI and skeleton
loading. The API returns one `{ success, data, error }` envelope shape, with centralized validation,
`helmet` / `cors` / `morgan`, and a persistence layer you can swap for any database.
**[App](https://taskflow-client-p5r3.onrender.com)** · **[API](https://taskflow-api-l3o2.onrender.com)**

**Ez Café** — Arabic RTL café concept for Riyadh, written in TypeScript. Responsive menu, café
information, location and contact, in a premium coffee-inspired design — laid out right-to-left from
the start, not mirrored at the end.

**هضاب الخليج** — Node + Express API with SQLite and authentication, powering a separate frontend.
Arabic product, Arabic-first data model.

**3D Portfolio** — React 19, Vite, Tailwind CSS and React Three Fiber, with GSAP and Framer Motion
animation, glassmorphism, smooth scrolling via Lenis, and full dark/light support.
**[Live](https://portfolio-xnfb.onrender.com)**

## 💡 What I care about

- **Arabic and RTL done properly** — not mirrored as an afterthought
- **Clear contracts** — one response shape, one error shape, one validator
- **Interfaces that explain themselves** — empty states, loading states, and errors that say what went wrong
- **Code that outlives the demo** — a store you can swap, config you can move to env vars
- **No long-lived secrets** — packages ship from CI using the built-in token, not a PAT on someone's laptop

## 📫 Get in touch

- **Portfolio** — [portfolio-xnfb.onrender.com](https://portfolio-xnfb.onrender.com)
- **Email** — [tetraoscloud931@gmail.com](mailto:tetraoscloud931@gmail.com)

---

<div align="center">
  <sub>Built with care by <a href="https://github.com/tetraoscloud931-creator">MMK</a> — MIT Licensed</sub>
</div>
