# Dr. Ma Jie's Academic Homepage

## Local workflow

This repository is configured with a local Git hook in `.githooks/post-commit`.

- After you run `git commit`, the hook automatically runs `git push` for the current branch.
- If the remote branch has moved ahead, the push can fail with a `fetch first` error.
- In that case, run `git pull --rebase origin main`, resolve any conflicts if needed, then run `git push origin main`.
- The hook is enabled by `git config core.hooksPath .githooks`.

## Notes

- The GitHub Actions workflow in `.github/workflows/google_scholar_crawler.yaml` only updates citation data on the `google-scholar-stats` branch.
- It does not replace normal pushes to `main`.
