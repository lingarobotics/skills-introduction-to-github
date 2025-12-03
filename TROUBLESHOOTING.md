# Troubleshooting Guide

Having trouble with the GitHub Skills tutorial? This guide covers common issues and their solutions.

## 🔍 Common Issues

### The README Didn't Update After Completing a Step

**Symptoms**: You completed an activity but the README still shows the same step.

**Solutions**:
1. **Wait longer**: GitHub Actions can take 20-30 seconds to run. Wait a full 30 seconds before worrying.
2. **Refresh the page**: Make sure you're actually refreshing (Ctrl+R or Cmd+R), not just clicking the README link.
3. **Check GitHub Actions**:
   - Go to the "Actions" tab in your repository
   - Look for a workflow run that should have been triggered
   - If it's still running, wait for it to complete
   - If it failed, click on it to see the error message

4. **Verify you followed instructions exactly**:
   - Branch names are case-sensitive and must match exactly (e.g., `my-first-branch`)
   - File names must match exactly (e.g., `PROFILE.md`, not `profile.md`)
   - Check that you're on the correct branch when creating files

### I Created the Wrong Branch Name

**Problem**: You created a branch with a different name than `my-first-branch`.

**Solution**:
1. Create a new branch with the correct name: `my-first-branch`
2. If you already made changes on the wrong branch, you can copy those changes to the new branch
3. Alternatively, delete your repository and start fresh

### GitHub Actions Are Not Running

**Symptoms**: Nothing happens after you complete a step, even after waiting.

**Checks**:
1. **Repository must be public** OR you must have GitHub Actions minutes available for private repos
2. **Actions must be enabled**:
   - Go to Settings → Actions → General
   - Make sure "Allow all actions and reusable workflows" is selected
3. **Check if workflows exist**:
   - Look in `.github/workflows/` directory
   - All workflow files (0-welcome.yml through 4-merge-your-pull-request.yml) should be present

### I'm on the Wrong Step

**Problem**: The `.github/steps/-step.txt` file shows the wrong step number.

**Solution**: You can manually edit this file to go back to a previous step:
1. Click on `.github/steps/-step.txt` in your repository
2. Click the pencil icon (Edit this file)
3. Change the number to the step you want:
   - `0` for Welcome
   - `1` for Create a branch
   - `2` for Commit a file
   - `3` for Open a pull request
   - `4` for Merge your pull request
4. Commit the change

### The "Compare & Pull Request" Button Doesn't Appear

**Problem**: After making a commit, you don't see the "Compare & pull request" button.

**Solution**: This is optional! You can manually create a pull request:
1. Go to the "Pull requests" tab
2. Click "New pull request"
3. Select `main` as the base branch
4. Select `my-first-branch` as the compare branch
5. Click "Create pull request"

### I Accidentally Closed/Merged Something Wrong

**Problem**: You closed a pull request instead of merging it, or merged the wrong thing.

**Solutions**:
1. **Closed PR by accident**: You can reopen it from the PR page by clicking "Reopen pull request"
2. **Merged the wrong thing**: This is trickier. You might need to:
   - Revert the merge (advanced)
   - Or start fresh with a new repository

### Files Are Not Showing Up

**Problem**: You created a file but it's not visible in your repository.

**Checks**:
1. **Make sure you committed the file**: Creating a file and committing it are two separate actions
2. **Check the correct branch**: Switch to `my-first-branch` using the branch dropdown to see your file
3. **Wait for the page to load**: Sometimes GitHub takes a moment to update the view

### The Merge Button Is Not Green

**Problem**: The "Merge pull request" button is greyed out or shows a warning.

**Common causes**:
1. **GitHub Actions are still running**: Wait for the workflows to complete (you'll see a yellow circle that turns into a green checkmark)
2. **Merge conflicts**: This shouldn't happen in this tutorial, but if it does, you may need to resolve the conflict
3. **Protected branch rules**: Check if the repository has branch protection enabled (Settings → Branches)

## 🆘 Still Stuck?

If none of these solutions work:

1. **Check the Actions tab** for error messages in the workflow runs
2. **Review your work** step-by-step against the instructions
3. **Start fresh**: Delete your repository and create a new one from the template
4. **Ask for help**:
   - [GitHub Skills Discussion Board](https://github.com/orgs/skills/discussions/categories/introduction-to-github)
   - [GitHub Community Forum](https://github.community/)
   - [GitHub Support](https://support.github.com/)

## 💡 Pro Tips

- **Read carefully**: Most issues come from not following instructions exactly
- **Check case sensitivity**: Branch and file names are case-sensitive
- **Be patient**: Automation takes time - wait a full 30 seconds before investigating
- **Use GitHub Actions tab**: This shows you exactly what's happening behind the scenes
- **It's okay to restart**: Don't be afraid to delete your repo and try again

## 📚 Understanding GitHub Actions

This tutorial uses GitHub Actions to automatically update your instructions. Here's how it works:

1. You complete an activity (create a branch, make a commit, etc.)
2. This triggers a GitHub Actions workflow
3. The workflow checks which step you're on
4. If conditions are met, it updates the README with the next step's instructions
5. It also updates `.github/steps/-step.txt` to track your progress

You can see all this happening in the **Actions** tab of your repository!

---

**Remember**: Learning is a process, and mistakes are part of that process. Don't get discouraged! 🌟
