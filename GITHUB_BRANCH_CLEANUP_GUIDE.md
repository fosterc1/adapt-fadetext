# 🔧 GitHub Branch Cleanup - Step-by-Step Guide

## Overview

This guide will help you:
1. ✅ Change the default branch from `genspark_ai_developer` to `main`
2. ✅ Delete the `genspark_ai_developer` branch
3. ✅ Verify everything is correct

**Time needed**: 2-3 minutes

---

## 📋 Prerequisites

- You need **admin access** to the repository
- Repository: https://github.com/fosterc1/adapt-quote

---

## Step 1: Change Default Branch to `main`

### 1.1 Navigate to Branch Settings

**Click this link**: https://github.com/fosterc1/adapt-quote/settings/branches

Or manually:
1. Go to https://github.com/fosterc1/adapt-quote
2. Click on **Settings** tab (top right)
3. Click on **Branches** in the left sidebar

### 1.2 Change the Default Branch

You should see a section called **"Default branch"** at the top.

**Current state**: Shows `genspark_ai_developer`

**What to do**:
1. Look for the **switch/swap icon** (⇄) or button that says **"Switch to another branch"**
2. Click on it
3. A dropdown menu will appear
4. Select **`main`** from the dropdown
5. Click the **"Update"** button
6. A confirmation dialog will appear with a warning
7. Click **"I understand, update the default branch"** to confirm

### 1.3 What You'll See

After updating:
- ✅ Default branch section now shows: `main`
- ✅ A success message: "Default branch changed to main"

---

## Step 2: Delete `genspark_ai_developer` Branch

### 2.1 Navigate to Branches Page

**Click this link**: https://github.com/fosterc1/adapt-quote/branches

Or manually:
1. Go to https://github.com/fosterc1/adapt-quote
2. Click on the **branch dropdown** (shows "main" with branch icon)
3. Click **"View all branches"** at the bottom

### 2.2 Delete the Branch

On the branches page:

1. Look for the **"Your branches"** or **"Active branches"** section
2. Find the row with **`genspark_ai_developer`**
3. On the right side of that row, click the **trash/delete icon** (🗑️)
4. A confirmation dialog will appear
5. Click **"Delete branch"** to confirm

### 2.3 What You'll See

After deletion:
- ✅ `genspark_ai_developer` is removed from the list
- ✅ Only `main` branch remains (and possibly the tag `v1.0.0`)
- ✅ Success message: "Branch genspark_ai_developer deleted"

---

## Step 3: Verify Everything is Correct

### 3.1 Check Repository Home

**Go to**: https://github.com/fosterc1/adapt-quote

**Verify**:
- ✅ Repository shows **"main"** as the default branch (near the top left)
- ✅ File structure shows files at root level (bower.json, js/, less/, etc.)
- ✅ Branch dropdown shows only **"main"** and tag **"v1.0.0"**

### 3.2 Check Branches Page

**Go to**: https://github.com/fosterc1/adapt-quote/branches

**Verify**:
- ✅ Only **1 branch** listed: `main`
- ✅ `genspark_ai_developer` is NOT in the list
- ✅ Shows: "main" with green checkmark (default)

### 3.3 Check Settings

**Go to**: https://github.com/fosterc1/adapt-quote/settings/branches

**Verify**:
- ✅ Default branch shows: **`main`**
- ✅ No longer shows `genspark_ai_developer`

---

## 📸 Visual Reference

### Before (Current State - Incorrect ❌)

```
Repository: fosterc1/adapt-quote
Default Branch: genspark_ai_developer ❌
Branches:
  - genspark_ai_developer (default) ❌
  - main
```

### After (Target State - Correct ✅)

```
Repository: fosterc1/adapt-quote
Default Branch: main ✅
Branches:
  - main (default) ✅
Tags:
  - v1.0.0
```

---

## 🔗 Quick Links

| Action | Direct Link |
|--------|-------------|
| 🔧 Change Default Branch | https://github.com/fosterc1/adapt-quote/settings/branches |
| 🗑️ Delete Branch | https://github.com/fosterc1/adapt-quote/branches |
| ✅ Verify Repository | https://github.com/fosterc1/adapt-quote |
| 📋 View Settings | https://github.com/fosterc1/adapt-quote/settings |

---

## ⚠️ Troubleshooting

### Problem: "Can't change default branch"

**Cause**: You might not have admin permissions

**Solution**: 
- Check if you're logged in as the repository owner
- Or ask the repository owner to make the change
- Ensure you have "Admin" role on the repository

### Problem: "Can't delete the branch"

**Cause**: The branch is still set as default

**Solution**:
- Make sure you completed Step 1 first (change default to `main`)
- Refresh the branches page
- Try deleting again

### Problem: "Branch is protected"

**Cause**: Branch protection rules are enabled

**Solution**:
1. Go to https://github.com/fosterc1/adapt-quote/settings/branches
2. Find branch protection rules for `genspark_ai_developer`
3. Delete the protection rule
4. Then delete the branch

---

## ✅ Success Checklist

After completing all steps, verify:

- [ ] Repository home shows `main` as default branch
- [ ] Only `main` branch exists (check branches page)
- [ ] `genspark_ai_developer` is completely deleted
- [ ] Files are at repository root (bower.json, js/, less/, etc.)
- [ ] v1.0.0 tag is still present and working
- [ ] No errors or warnings on the repository

---

## 🎉 You're Done!

Once complete, your repository will be:
- ✅ Clean and organized with only `main` branch
- ✅ Properly structured with files at root
- ✅ Tagged with v1.0.0 release
- ✅ Ready for production use

---

## 📞 Need Help?

If you encounter any issues:

1. **Check your permissions**: Ensure you have admin access
2. **Refresh the page**: Sometimes GitHub UI needs a refresh
3. **Try incognito mode**: Clear cache issues
4. **Contact me**: Let me know what error you're seeing

---

## 🚀 After Cleanup

Once the cleanup is complete, you can verify locally:

```bash
# Fetch the latest from GitHub
cd /home/user/webapp
git fetch --prune origin

# Check remote branches
git branch -r
# Should show only: origin/main

# Verify your local setup
git branch -a
# Should show only: * main and remotes/origin/main
```

---

**Repository**: https://github.com/fosterc1/adapt-quote  
**Status**: Waiting for manual cleanup  
**Target**: main branch only with v1.0.0 tag
