# Contributing

## Where code lives

The Baas.lk platform is developed in the [service-hub](https://github.com/luminary-dev/service-hub) monorepo. The `service-hub-*` repositories are **read-only mirrors** created with `git subtree` — never push to them directly; open PRs against the monorepo and changes sync out automatically.

## Workflow

1. Branch from `main` (`<your-name>/<topic>`).
2. Make the change where it is owned: web app and infra at the repo root, service code under `services/<service>/`.
3. Verify locally — each package must pass `npm run typecheck && npm test && npm run build`; for behavior changes run the stack (`npm run dev:all`) and the smoke suite (`npm run e2e`).
4. Open a PR. All 22 CI checks (`<package> / <check>`) must pass; branch protection enforces them.
5. Every PR gets a review before merge.

## Issues

New issues land on the [Service Hub board](https://github.com/orgs/luminary-dev/projects/1) automatically. File work in the repo that owns the code; cross-cutting work goes on the monorepo. The `v0.1` milestone marks the launch set.

## Style

Match the surrounding code — its naming, comment density and idiom. No attribution trailers in commits.
