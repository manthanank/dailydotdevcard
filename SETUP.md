# Setup Guide

This guide will help you set up your own daily.dev DevCard repository with automatic updates.

## Prerequisites

- A GitHub account
- A daily.dev account and DevCard

## Step 1: Generate Your DevCard

1. Visit [daily.dev DevCard generator](https://app.daily.dev/devcard)
2. Log in with your daily.dev account
3. Customize your DevCard appearance (optional)
4. Copy the generated HTML code

## Step 2: Extract Your User ID

From the generated HTML code, find your User ID:

```html
<a href="https://app.daily.dev/yourusername">
  <img src="https://api.daily.dev/devcards/v2/YOUR_USER_ID.png?type=default&r=abc" width="356" alt="Your Name's Dev Card"/>
</a>
```

Your User ID is the part before `.png` in the image URL (e.g., `YOUR_USER_ID`).

## Step 3: Fork or Create Repository

### Option A: Fork This Repository

1. Click the "Fork" button on this repository
2. Rename it to your username (for GitHub profile) or any preferred name

### Option B: Create New Repository

1. Create a new public repository on GitHub
2. Copy the files from this repository
3. Update the README.md with your information

## Step 4: Configure Repository Secrets

1. Go to your repository on GitHub
2. Click **Settings** → **Secrets and variables** → **Actions**
3. Click **New repository secret**
4. Add a secret with:
   - **Name**: `USER_ID`
   - **Value**: Your User ID from Step 2

## Step 5: Update README.md

Replace the following in your README.md:

- `manthanank` with your daily.dev username
- Update any personal information

## Step 6: Enable GitHub Actions

1. Go to the **Actions** tab in your repository
2. Enable workflows if prompted
3. The DevCard will automatically update daily at midnight UTC

## Step 7: Manual Trigger (Optional)

To manually update your DevCard:

1. Go to **Actions** tab
2. Select "daily-devcard" workflow
3. Click "Run workflow"

## Troubleshooting

### DevCard Not Updating

- Check if the GitHub Action workflow ran successfully
- Verify your USER_ID secret is correct
- Ensure the repository has write permissions for Actions

### Action Failing

- Check the workflow logs in the Actions tab
- Verify your User ID is correct
- Ensure daily.dev API is accessible

### DevCard Not Displaying

- Check if `devcard.png` file exists in your repository
- Verify the image path in README.md is correct
- Make sure the repository is public (for GitHub profile README)

## Advanced Configuration

### Custom Commit Messages

Edit `.github/workflows/main.yml` to customize commit messages:

```yaml
commit_message: "docs: update DevCard"
```

### Different Schedule

Modify the cron schedule in the workflow:

```yaml
schedule:
  - cron: "0 12 * * *"  # Daily at noon UTC
```

### Dependabot Configuration

The repository includes Dependabot configuration to keep GitHub Actions up to date automatically.

## Support

For issues related to:

- **This repository**: Create a GitHub issue
- **daily.dev DevCard**: Visit [daily.dev support](https://daily.dev)
- **GitHub Actions**: Check [GitHub Actions documentation](https://docs.github.com/en/actions)
