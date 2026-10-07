# wcd-bank-github-actions

[![learn-github-actions](https://github.com/gkoufie1/wcd-bank-github-actions/actions/workflows/learn-github-actions.yml/badge.svg)](https://github.com/gkoufie1/wcd-bank-github-actions/actions/workflows/learn-github-actions.yml)

Day 2 of the WCD Bank cloud enablement project: a first GitHub Actions workflow.

The workflow in [.github/workflows/learn-github-actions.yml](.github/workflows/learn-github-actions.yml) runs on every push to `main`, on pull requests, and on demand (**Actions → learn-github-actions → Run workflow**). It shows the different kinds of variables:

| Kind | Where it's defined | Example |
|---|---|---|
| Workflow `env` | Top of the workflow, visible to all jobs | `CLIENT`, `PROJECT` |
| Job `env` | Under the job, visible to its steps | `ENVIRONMENT` |
| Step `env` | Under a single step | `GREETING` |
| Configuration variable | Repo **Settings → Secrets and variables → Actions → Variables**, read with `vars.` | `DEPLOY_REGION` |
| Default variables | Set by GitHub on every run | `GITHUB_REPOSITORY`, `GITHUB_SHA`, `RUNNER_OS` |
| Variable for later steps | Written to `$GITHUB_ENV` | `BUILD_TAG` |

Each run also writes a summary table to the run page.
