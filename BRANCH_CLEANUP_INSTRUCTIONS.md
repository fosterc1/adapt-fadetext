# Branch Cleanup Instructions

## Current Status

✅ **Local branch deleted**: genspark_ai_developer has been removed locally  
⚠️ **Remote branch remains**: genspark_ai_developer is still on GitHub (it's the default branch)

## Why Can't We Delete It Automatically?

The `genspark_ai_developer` branch is currently set as the **default branch** on GitHub, and GitHub prevents deletion of the default branch for safety. We need to change the default branch to `main` first.

## Manual Steps to Complete Cleanup

### Option 1: Via GitHub Website (Easiest)

1. **Go to your repository settings**:
   - Visit: https://github.com/fosterc1/adapt-quote/settings

2. **Change the default branch**:
   - In the left sidebar, you should be on "General" (default)
   - Scroll down to "Default branch" section
   - Click the swap icon (⇄) or "Switch to another branch" button
   - Select **main** from the dropdown
   - Click "Update" or "I understand, update the default branch"
   - Confirm the change

3. **Delete the old branch**:
   - Go to: https://github.com/fosterc1/adapt-quote/branches
   - Find `genspark_ai_developer` in the branch list
   - Click the trash icon (🗑️) next to it
   - Confirm deletion

### Option 2: Using GitHub CLI (After Manual Default Change)

If you've manually changed the default branch to `main` on GitHub:

```bash
cd /home/user/webapp
gh api -X PATCH repos/fosterc1/adapt-quote -f default_branch=main
git push origin --delete genspark_ai_developer
```

### Option 3: Ask Me to Do It (After You Change Default)

After you manually change the default branch to `main` on GitHub:

1. Let me know it's done
2. I'll delete the remote branch with: `git push origin --delete genspark_ai_developer`

## What Will Remain After Cleanup

```
✅ Local branches:
  * main

✅ Remote branches:
  * origin/main

✅ Tags:
  * v1.0.0

✅ GitHub default branch: main
```

## Current Repository State

```
Repository: https://github.com/fosterc1/adapt-quote

Branches:
  - main (all content is here) ✅
  - genspark_ai_developer (to be deleted) ⚠️

Default Branch: genspark_ai_developer (needs to be changed to main) ⚠️

Tag: v1.0.0 (points to main) ✅
```

## Why This Is Safe

- ✅ Both branches have identical content (we merged everything)
- ✅ The v1.0.0 tag is on main
- ✅ All work is preserved in main
- ✅ No data will be lost

## Verification After Cleanup

After the branch is deleted, verify:

```bash
# Check branches
git branch -a
# Should show only: * main and remotes/origin/main

# Check on GitHub
https://github.com/fosterc1/adapt-quote/branches
# Should show only: main

# Verify default branch
https://github.com/fosterc1/adapt-quote
# Should show "main" as the default branch
```

## Quick Links

- **Repository Settings**: https://github.com/fosterc1/adapt-quote/settings
- **Branches Page**: https://github.com/fosterc1/adapt-quote/branches
- **Repository Home**: https://github.com/fosterc1/adapt-quote

---

**Note**: Once you change the default branch to `main` on GitHub, let me know and I'll complete the deletion of `genspark_ai_developer` remotely.
