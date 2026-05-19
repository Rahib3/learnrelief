# Learnrelief Landing

This repository contains a Vite + React + TypeScript landing site for Learnrelief.

## Local development

```bash
npm install
npm run dev
```

Open the local dev server at `http://localhost:5173`.

## Build for production

```bash
npm run build
```

The static production output is written to `dist/`.

## Preview the production build locally

```bash
npm run preview -- --host 127.0.0.1 --port 4173
```

Then open `http://127.0.0.1:4173/`.

## Recommended deployment platforms

### Netlify

1. Create a free Netlify account.
2. Connect your Git repository.
3. Set the build command to:

```bash
npm run build
```

4. Set the publish directory to:

```text
dist
```

5. Deploy.

Netlify will automatically use `netlify.toml` for the redirect rule needed by single-page routing.

### Vercel

1. Create a Vercel account.
2. Import the repository.
3. Use the build command:

```bash
npm run build
```

4. Set the output directory to:

```text
dist
```

5. Deploy.

### Static hosting

Any static host can serve the files in `dist/`.

If you use a custom domain, make sure:

- the site is served over HTTPS
- `index.html` is the canonical homepage URL
- the `og:image` entry in `index.html` points to the correct final image URL

## Audit commands

```bash
npm run serve:dist
```

In another terminal:

```bash
npm run audit:accessibility
npm run audit:lighthouse
```

The Lighthouse report is written to `lighthouse-report.html`.

## Pre-launch checklist

- Replace placeholder site URL in `index.html` with your real production domain.
- Confirm `public/og-image.png` works on social previews.
- Verify the Instagram contact link remains the primary contact channel.
- Make sure the build passes with `npm run build`.
- Run a final browser test on the deployed URL.

## GitHub Actions CI

This repository includes a GitHub Actions workflow at `.github/workflows/ci.yml`.

The workflow:

- installs dependencies
- builds production assets
- runs `npm run lint`
- runs `npm run test`
- starts a local static server
- runs accessibility and Lighthouse audits

## Files of interest

- `.github/workflows/ci.yml` - CI build and audit workflow.
- `netlify.toml` - Netlify build and redirect config.
- `public/mentor-terms.html` - downloadable mentor terms.
- `public/mentor-terms.pdf` - generated mentor PDF.
- `public/og-image.png` - optimized Open Graph image.
