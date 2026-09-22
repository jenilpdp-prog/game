# Contributing to Emberfall

Thanks for helping improve Emberfall.

## Development

1. Fork or branch from `main`.
2. Install dependencies with `npm install`.
3. Run the game with `npm run dev`.
4. Keep changes focused and test the gameplay path you changed.
5. Before opening a pull request, run:

```bash
npm run check
```

## Pull Requests

A good pull request should explain:

- What changed
- Why the change is useful
- How it was tested
- Any gameplay or balance side effects

For gameplay changes, include the affected wave, enemy, upgrade, control, or setting when possible.

## Code Guidelines

- Keep the core loop responsive.
- Avoid unnecessary dependencies.
- Preserve keyboard remapping.
- Keep local co-op working.
- Prefer readable game-state changes over clever abstractions.
- Do not commit secrets, API keys, or generated build folders.

## Bug Reports

Useful bug reports include:

- Browser and device
- Solo or 2-player mode
- Wave number
- Exact steps to reproduce
- Expected result
- Actual result
