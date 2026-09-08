# Daily Green

Daily Green is a small GitHub Actions automation and learning experiment. It demonstrates scheduled workflows, automated commits, Git configuration inside Actions, and workflow permissions.

## What it does

The `Daily Repository Maintenance` workflow runs once every day on a GitHub-hosted Ubuntu runner. It appends the current UTC date and `Daily repository maintenance completed.` to `activity.txt`, then automatically commits and pushes the update to the repository.

No external server, deployment platform, database, API, Docker container, or paid service is required. GitHub-hosted runners execute the workflow.

This project is intended to teach GitHub Actions automation. It is not intended as a way to artificially inflate contribution activity.

## Manual trigger

1. Open the repository on GitHub and select the **Actions** tab.
2. Select **Daily Repository Maintenance**.
3. Select **Run workflow**, choose the branch, and confirm with **Run workflow**.

The workflow also runs automatically according to its daily cron schedule.

## Required GitHub setting

The workflow needs permission to write repository contents. In the repository, open **Settings > Actions > General**, find **Workflow permissions**, select **Read and write permissions**, and save the setting.

The workflow file also declares `contents: write`. If branch protection rules prevent direct pushes to the default branch, the workflow will need an allowed target branch or an adjusted branch protection policy.

## Push this project to a new repository

From the directory containing `daily-green/`:

```bash
cd daily-green
git init
git add .
git commit -m "chore: add daily maintenance workflow"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/daily-green.git
git push -u origin main
```

Create the empty GitHub repository named `daily-green` before running the final command. Replace `YOUR-USERNAME` with your GitHub username or organization name. Do not initialize the GitHub repository with an additional README, license, or `.gitignore` when creating it.

## What to expect after a successful run

The workflow run will show green in the Actions tab. A new commit named `chore: daily repository maintenance` will appear in the repository, and `activity.txt` will contain one additional dated line, for example:

```text
2026-09-08 Daily repository maintenance completed.
```# Github_streak_automation
# Github_streak_automation
