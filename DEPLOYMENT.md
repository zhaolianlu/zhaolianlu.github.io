# Deployment

## Repository

- Authorized repository: `https://github.com/zhaolianlu/zhaolianlu.github.io`
- Default branch: `main`
- Inspected baseline commit: `a21009030e3ff59f21018dbc942dd6b87c63cb47`
- Framework: HugoBlox Academic CV template

## Preserved deployment workflow

The repository already contains `.github/workflows/deploy.yml` and `.github/workflows/build.yml`. They are preserved without modification. A push to `main` runs the reusable Hugo build and deploys the generated artifact with `actions/deploy-pages`.

## Local production build

Install the tool versions expected by the repository, then run:

```bash
pnpm install --frozen-lockfile
pnpm run build
```

The build generates `public/` and the Pagefind search index. The GitHub Actions workflow is the authoritative deployment environment.

## Safety checks before push

1. Confirm `git remote get-url origin` is exactly `https://github.com/zhaolianlu/zhaolianlu.github.io.git`.
2. Confirm `git diff --diff-filter=D --name-only HEAD` returns no paths.
3. Confirm `git diff --name-only HEAD` contains no baseline tracked files.
4. Stage only the reviewed new paths with explicit `git add <path>` commands.
5. Review `git diff --cached --stat` and `git diff --cached --name-status`.
6. Push normally to `main`; never force-push.

## Verification after deployment

Confirm the workflow is successful and test:

- `/` and `/zh/`
- `/research/` and `/zh/research/`
- `/people/` and both PI profile variants
- `/publications/`
- `/news/`
- `/join/`
- `/contact/`
- Both email links and the language switcher

