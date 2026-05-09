# AGENTS.md

## Cursor Cloud specific instructions

This is a simple Next.js (Pages Router) app that generates images using the Replicate API (Stable Diffusion XL).

### Services

| Service | Command | Notes |
|---------|---------|-------|
| Next.js Dev Server | `npm run dev` | Serves on http://localhost:3000 |

### Key Commands

- **Lint:** `npm run lint`
- **Build:** `npm run build`
- **Test:** `npm test` (runs lint + build)
- **Dev server:** `npm run dev`

### Environment

- Requires Node.js 18 (matches CI). Use `source ~/.nvm/nvm.sh && nvm use 18` before running commands.
- Requires `REPLICATE_API_TOKEN` in `.env.local` for the image generation API to work. Without it, the frontend renders but API calls return 500.
- No database or Docker services needed.

### Gotchas

- The project has both `package-lock.json` and `yarn.lock`; CI uses `npm ci`, so prefer npm.
- `npm test` is lint + build (no unit test framework configured).
