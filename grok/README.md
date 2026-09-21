# Φ-Lite: The Shielded Attractor (Grok Edition)

**Version:** 0.5.3 · **Honesty:** Stage 4 *candidate* research console, not AGI. Honest stage floor **S2.9**.

Interactive development suite for a thermodynamically bounded scalar core: live camera/mic I/O, safety shield, 144-point audit, 48 enhancements.

## Requirements

- **Node.js 20.19+ or 22.12+** (Vite 8). Node 12/14/16/18 will fail the version gate.
- npm 10+ (comes with those Node releases)

```bash
# from the folder that contains package.json
nvm install 22 && nvm use 22   # if you use nvm
node -v                        # must print v20.19+ or v22.12+
npm install
npm run dev
```

`./startup.sh` does the same from any checkout: it `cd`s to its own directory, checks Node, then starts `npm run dev`. Do not expect a path named `/workspace`.

## Scripts

| Command | Purpose |
|---|---|
| `npm run dev` | Dev server (all interfaces, port 8080) |
| `npm run build` | Production build |
| `npm run typecheck` | `tsc --noEmit` |
| `npm test` | Platform + scalar-core unit tests |
| `npm run lint` | ESLint |

## Layout

- `src/lib/phi/` — scalar core (energy, agency, perception, memory, policy, safety, loop)
- `src/components/console/` — command, sensors, layers, audit, eval
- `src/lib/phi/audit.ts` — 144 shortcomings + 48 enhancements
- `attachments/` — source audits and the Stage 4 snapshot dump
- `public/` — favicon and share card

## Stage policy

Do not claim a stage upgrade without a new metrics window. Kill criteria live in the Eval view. Tensor RSSM training, MAML transfer, and 10⁶-cycle formal V&V remain open in v0.5.

License: Apache-2.0 (see `package.json`).
