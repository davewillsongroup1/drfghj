## Cursor Cloud specific instructions

This is a Next.js 13 app that generates AI images via the Replicate API (Stable Diffusion XL).

### Quick reference

- **Lint:** `npm run lint` (runs `next lint`)
- **Build:** `npm run build` (runs `next build`)
- **Test:** `npm test` (runs lint + build; no unit/integration tests exist)
- **Dev server:** `npm run dev` (starts on port 3000)
- See `README.md` for full usage instructions.

### Non-obvious notes

- **Node 18 is required.** The CI pins Node 18 and the project uses Next.js 13 / `@next/font` 13. Use `source ~/.nvm/nvm.sh && nvm use 18` before running any commands.
- **`REPLICATE_API_TOKEN` env var** is required for the image-generation API routes to work. Without it the app loads fine but API calls return 500. Set it in `.env.local` or export it in the shell.
- The repo has both `package-lock.json` and `yarn.lock`; CI uses `npm ci`, so prefer `npm` as the package manager.
- There are no databases, Docker services, or background workers — only the Next.js dev server and the external Replicate API.
