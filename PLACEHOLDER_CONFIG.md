# 📋 Placeholder Configuration Template

Use this file to organize all your placeholder values before replacing them in the project.

---

## 👤 Personal Information

| Key | Placeholder | Your Value | Status |
|-----|-------------|-----------|--------|
| Full Name | `{{NAME}}` | Mayur Shetty | ⏳ Need Value |
| GitHub Username | `{{GITHUB-USERNAME}}` | mayurshetty100 | ⏳ Need Value |
| Email | `{{EMAIL}}` | your.email@example.com | ⏳ Need Value |

---

## 📸 Profile Photo

| Key | Placeholder | Your Value | Notes |
|-----|-------------|-----------|-------|
| Photo URL | `{{PHOTO-URL}}` | `https://avatars.githubusercontent.com/u/YOUR_ID?v=4` | Use GitHub avatar or Gravatar |

**How to find your GitHub Avatar URL:**
1. Go to `https://github.com/YOUR_USERNAME`
2. Right-click profile photo
3. Select "Copy image address"
4. Or use: `https://avatars.githubusercontent.com/u/YOUR_GITHUB_ID?v=4`

---

## 🔗 Social & Professional Links

| Service | Placeholder | Your URL | Example |
|---------|-------------|----------|---------|
| CodeChef | `{{CODECHEF-URL}}` | | `https://www.codechef.com/users/mayurshetty100` |
| LeetCode | `{{LEETCODE-URL}}` | | `https://leetcode.com/u/mayurshetty` |
| LinkedIn | `{{LINKEDIN-URL}}` | | `https://linkedin.com/in/mayurshetty` |
| Twitter | `{{TWITTER-URL}}` | | `https://twitter.com/mayurshetty100` |
| Instagram | `{{INSTAGRAM-URL}}` | | `https://instagram.com/mayurshetty` |

**How to get these URLs:**
1. Visit your profile on each platform
2. Copy the URL from address bar
3. Verify the URL is public (not private profile)

---

## 🚀 Featured Projects

### Project 1: Alpha

| Field | Placeholder | Your Value |
|-------|-------------|-----------|
| Repository Link | `{{PROJECT1-REPO}}` | `https://github.com/mayurshetty100/project-name` |
| Name (in carousel) | -- | Project Name |
| Description | -- | Brief one-line description |
| Tech Stack | -- | React, Node, MongoDB |

### Project 2: Beta

| Field | Placeholder | Your Value |
|-------|-------------|-----------|
| Repository Link | `{{PROJECT2-REPO}}` | `https://github.com/mayurshetty100/project-name` |
| Name (in carousel) | -- | Project Name |
| Description | -- | Brief one-line description |
| Tech Stack | -- | Python, TensorFlow, React |

### Project 3: Gamma

| Field | Placeholder | Your Value |
|-------|-------------|-----------|
| Repository Link | `{{PROJECT3-REPO}}` | `https://github.com/mayurshetty100/project-name` |
| Name (in carousel) | -- | Project Name |
| Description | -- | Brief one-line description |
| Tech Stack | -- | React, Node, Stripe |

---

## 📄 Additional Resources

| Resource | Placeholder | Your Value |
|----------|-------------|-----------|
| CV/Resume PDF | `{{CV-URL}}` | `https://github.com/mayurshetty100/cv/resume.pdf` |
| Portfolio Website | -- | `https://yourportfolio.com` |
| Blog | -- | `https://yourblog.com` |

**How to host your CV:**
1. Create `/cv` folder in your repo
2. Upload `resume.pdf`
3. Use: `https://github.com/USERNAME/REPO/raw/main/cv/resume.pdf`

---

## 🎨 Optional: Customization Values

### If Changing Color Scheme

Current colors (you can keep these or change them):
```
Primary Cyan:        #00d4ff
Secondary Magenta:   #ff00ff
Accent Green:        #00ff88
Dark Background:     #0a0e27
Lighter Background:  #1a1a3e
```

Want to change colors? Pick your hex codes:
- Favorite Color 1: `#______`
- Favorite Color 2: `#______`
- Favorite Color 3: `#______`

### If Updating Tech Icons

Current tech stack in SVG:
```
⬢ Node.js      | ⚛ React       | 📦 Express
🍃 MongoDB     | 📘 JavaScript | 🐳 Docker
🌐 HTML/CSS    | ⎇ Git         | 🔥 Firebase
🐍 Python
```

Want to add more? List them:
- [ ] Technology: ______ | Icon: ______
- [ ] Technology: ______ | Icon: ______
- [ ] Technology: ______ | Icon: ______

---

## 📋 Pre-Deployment Checklist

Before you start replacing, gather all information:

**Personal:**
- [ ] Full name ready
- [ ] GitHub username confirmed
- [ ] Email address finalized
- [ ] Photo URL working

**Social Links:**
- [ ] CodeChef URL copied
- [ ] LeetCode URL copied
- [ ] LinkedIn URL copied
- [ ] Twitter URL copied
- [ ] Instagram URL copied

**Projects:**
- [ ] Project 1 name finalized
- [ ] Project 1 repository link ready
- [ ] Project 2 name finalized
- [ ] Project 2 repository link ready
- [ ] Project 3 name finalized
- [ ] Project 3 repository link ready

**Resources:**
- [ ] CV URL ready (or upload to repo first)
- [ ] All external links tested

---

## 🔄 Quick Copy-Paste Template

Once you've gathered all values, use this template for bulk replacement:

```
NAME: Mayur Shetty
GITHUB-USERNAME: mayurshetty100
EMAIL: mayur@example.com
PHOTO-URL: https://avatars.githubusercontent.com/u/YOUR_ID?v=4

CODECHEF-URL: https://www.codechef.com/users/mayurshetty100
LEETCODE-URL: https://leetcode.com/u/mayurshetty
LINKEDIN-URL: https://linkedin.com/in/mayurshetty
TWITTER-URL: https://twitter.com/mayurshetty100
INSTAGRAM-URL: https://instagram.com/mayurshetty

PROJECT1-REPO: https://github.com/mayurshetty100/project-alpha
PROJECT2-REPO: https://github.com/mayurshetty100/project-beta
PROJECT3-REPO: https://github.com/mayurshetty100/project-gamma

CV-URL: https://github.com/mayurshetty100/cv/resume.pdf
```

---

## 🚀 Using This Template

### Method 1: Manual Find & Replace (IDE)

1. Open `README.md` in your editor
2. Press `Ctrl+H` (or `Cmd+H` on Mac)
3. For each placeholder:
   - Find: `{{PLACEHOLDER}}`
   - Replace: `YOUR_VALUE`
   - Click "Replace All"

### Method 2: Command Line (Bash Script)

Create a file `replace.sh`:

```bash
#!/bin/bash

# Replace personal info
sed -i 's/{{NAME}}/Mayur Shetty/g' README.md
sed -i 's/{{GITHUB-USERNAME}}/mayurshetty100/g' README.md
sed -i 's/{{EMAIL}}/mayur@example.com/g' README.md

# Replace social links
sed -i 's|{{CODECHEF-URL}}|https://www.codechef.com/users/mayurshetty100|g' README.md
sed -i 's|{{LEETCODE-URL}}|https://leetcode.com/u/mayurshetty|g' README.md
sed -i 's|{{LINKEDIN-URL}}|https://linkedin.com/in/mayurshetty|g' README.md
sed -i 's|{{TWITTER-URL}}|https://twitter.com/mayurshetty100|g' README.md
sed -i 's|{{INSTAGRAM-URL}}|https://instagram.com/mayurshetty|g' README.md

# Replace project links
sed -i 's|{{PROJECT1-REPO}}|https://github.com/mayurshetty100/project-alpha|g' README.md
sed -i 's|{{PROJECT2-REPO}}|https://github.com/mayurshetty100/project-beta|g' README.md
sed -i 's|{{PROJECT3-REPO}}|https://github.com/mayurshetty100/project-gamma|g' README.md

# Replace CV link
sed -i 's|{{CV-URL}}|https://github.com/mayurshetty100/cv/resume.pdf|g' README.md

# Replace in header.svg
sed -i 's|{{PHOTO-URL}}|https://avatars.githubusercontent.com/u/YOUR_ID?v=4|g' assets/header.svg

echo "✅ All replacements complete!"
```

Run it:
```bash
chmod +x replace.sh
./replace.sh
```

### Method 3: VS Code Find & Replace with Regex

1. Press `Ctrl+H` to open Find & Replace
2. Enable Regex with `.*` button
3. Use pattern:
   ```
   Find: \{\{([A-Z-]+)\}\}
   Replace: YOUR_VALUE_HERE
   ```

---

## ✅ Validation Checklist

After replacing, verify:

- [ ] `README.md` has no `{{}}` placeholders
- [ ] `assets/header.svg` has valid photo URL
- [ ] All social links start with `https://`
- [ ] GitHub username appears correctly
- [ ] Email is clickable (has `mailto:`)
- [ ] Project links are valid GitHub repos
- [ ] CV link is accessible
- [ ] No typos in URLs

---

## 🐛 Troubleshooting Replacements

**Issue:** Find & Replace not working
**Solution:** 
- Check exact spelling of placeholder (case-sensitive)
- Ensure you're searching in the right file
- Try exact match instead of regex

**Issue:** Special characters causing issues
**Solution:**
- Escape forward slashes in URLs: `https:\/\/...`
- Use single quotes in bash: `'...'`
- Use double quotes only if no spaces

**Issue:** Replacements didn't take effect
**Solution:**
- Close and reopen the file
- Run command again
- Check git diff: `git diff README.md`

---

## 📝 Notes & Tips

- **Keep this file for reference** - You'll need it for updates
- **Save your values somewhere** - For future reference
- **Test URLs before replacing** - Verify they're publicly accessible
- **Take a backup** - Before replacing, commit to git
- **Double-check email** - Most important for contact
- **Use raw GitHub URLs** - If having SVG issues

---

## 🎯 Final Steps

1. **Fill out this template completely**
2. **Review all values for accuracy**
3. **Run replacement using your preferred method**
4. **Verify no placeholders remain**
5. **Commit to git**
6. **Push to GitHub**
7. **Check your profile**

---

<div align="center">

**Template Version:** 1.0  
**Last Updated:** 2024

Once you've completed this template, you're ready to deploy! 🚀

</div>
