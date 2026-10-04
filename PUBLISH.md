# Publish to GitHub

Suggested name: **windows-365-link-unbrick**

Suggested description: **Documentation-based Windows 365 Link recovery guide with USB BMR instructions and troubleshooting.**

## Browser upload

1. Extract the repository ZIP.
2. On GitHub, create a new repository with the name above and choose its visibility.
3. Leave automatic README, license, and gitignore initialization unchecked.
4. Upload the contents inside the extracted folder, so README.md is at the repository root.
5. Commit the files. Verify that docs/ and the optional hidden .github/ issue-template folder were uploaded.

## Git alternative

Create an empty GitHub repository first. Replace YOUR-USERNAME below with its owner.

```bash
cd windows-365-link-unbrick
git init -b main
git add .
git commit -m "Add Windows 365 Link recovery guide"
git remote add origin https://github.com/YOUR-USERNAME/windows-365-link-unbrick.git
git push -u origin main
```

No license has been selected on your behalf. Add your preferred documentation license before inviting reuse under specific license terms.
