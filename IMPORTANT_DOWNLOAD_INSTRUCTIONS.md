# ⚠️ IMPORTANT: How to Download This Plugin

## 🎯 Recommended Method: Use GitHub Releases

**DO NOT use the "Download ZIP" button on the main branch page!**

### ✅ CORRECT Way to Download

1. Go to the **Releases** page: https://github.com/fosterc1/adapt-fadetext/releases
2. Download the latest release ZIP (e.g., `adapt-fadetext-v1.0.13.zip`)
3. Upload directly to Adapt Authoring Tool
4. Works perfectly! ✅

### ❌ INCORRECT Way (Will Fail)

1. Click "Code" → "Download ZIP" on main branch page
2. This creates `adapt-fadetext-main.zip` with folder named `adapt-fadetext-main/`
3. Adapt expects folder named exactly `adapt-fadetext/` (no `-main` suffix)
4. Upload fails with "Package does not contain a schema" ❌

## Why This Happens

**GitHub's Behavior:**
- When downloading from main branch, GitHub **always** appends the branch name
- Creates: `adapt-fadetext-main/` instead of `adapt-fadetext/`
- This is GitHub's standard behavior for all repositories

**Adapt's Requirement:**
- Folder name MUST match the `name` field in `bower.json` exactly
- bower.json says: `"name": "adapt-fadetext"`
- Therefore, folder must be: `adapt-fadetext/` (not `adapt-fadetext-main/`)

## Manual Fix (If You Downloaded Wrong ZIP)

If you already downloaded `adapt-fadetext-main.zip`:

1. Extract the ZIP file
2. Rename the folder from `adapt-fadetext-main` to `adapt-fadetext`
3. Delete unnecessary files:
   - All `*.md` files (README.md, CHANGELOG.md, etc.)
   - `.gitignore` file
   - `docs/` folder
4. Re-zip the `adapt-fadetext/` folder
5. Upload the new ZIP to Adapt Authoring Tool

### Quick Command (Linux/Mac)
```bash
unzip adapt-fadetext-main.zip
mv adapt-fadetext-main adapt-fadetext
cd adapt-fadetext
rm -rf *.md .gitignore docs/
cd ..
zip -r adapt-fadetext.zip adapt-fadetext/
```

## Current Available Releases

Visit: https://github.com/fosterc1/adapt-fadetext/releases

Look for:
- **v1.0.13** - Latest production release
- **v1.0.12** - Previous stable release
- **v1.0.11** - Previous stable release

All release ZIPs have the correct folder structure and will work immediately!

## For Developers

If you're cloning the repository for development:

```bash
# Clone the repository
git clone https://github.com/fosterc1/adapt-fadetext.git
cd adapt-fadetext

# Create a production ZIP
mkdir ../adapt-fadetext-production
cp -r bower.json package.json properties.schema schemas/ js/ less/ templates/ example/ ../adapt-fadetext-production/
cd ..
mv adapt-fadetext-production adapt-fadetext
zip -r adapt-fadetext.zip adapt-fadetext/
```

## Summary

| Download Method | Folder Name | Works? | Recommended? |
|----------------|-------------|--------|--------------|
| Releases page | `adapt-fadetext/` | ✅ Yes | ✅ **Use This!** |
| Main branch ZIP | `adapt-fadetext-main/` | ❌ No | ❌ Don't use |
| Manual fix | `adapt-fadetext/` | ✅ Yes | ⚠️ Extra work |
| Git clone + package | `adapt-fadetext/` | ✅ Yes | 👨‍💻 Developers only |

## Why We Can't Fix This in the Repository

This is a limitation of how GitHub creates ZIP files:
- GitHub **always** appends the branch name when creating ZIPs from branches
- There's no way to configure this behavior
- The only solution is to use GitHub Releases, where we control the folder structure

## Bottom Line

**Always download from the Releases page, not the main branch!**

📦 Releases: https://github.com/fosterc1/adapt-fadetext/releases

---

**Last Updated**: 2025-11-13  
**Current Version**: 1.0.13  
**Status**: Working correctly via Releases page ✅
