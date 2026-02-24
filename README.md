<div align="center">

# 🖥️ Terminal GIF for GitHub Profile

**An animated terminal GIF showcasing your GitHub stats — auto-generated daily.**

![Terminal GIF](./output.gif)

[![Stars](https://img.shields.io/github/stars/dbuzatto/gif-terminal?style=flat-square&color=yellow)](https://github.com/dbuzatto/gif-terminal/stargazers)
[![Forks](https://img.shields.io/github/forks/dbuzatto/gif-terminal?style=flat-square&color=blue)](https://github.com/dbuzatto/gif-terminal/network/members)
[![License](https://img.shields.io/github/license/dbuzatto/gif-terminal?style=flat-square)](LICENSE)

</div>

---

## ✨ Features

- 📊 Fetches **real-time GitHub stats** (commits, stars, PRs, followers, rank, and more)
- 🎨 Fully **customizable** — colors, layout, skills, and commands
- ⚙️ **Auto-regenerated daily** via GitHub Actions
- 🚀 Easy to set up — fork, configure, and you're done

---

## 🚀 Quick Start

### 1. Fork this repository

Click the **Fork** button at the top right of this page.

### 2. Add your GitHub Token

Go to **Settings → Secrets and variables → Actions** and create a new secret:

| Name | Value |
|------|-------|
| `GH_TOKEN` | Your GitHub Personal Access Token (`read:user` scope) |

> 💡 Generate a token at [github.com/settings/tokens](https://github.com/settings/tokens) — only `read:user` permission is needed.

### 3. Set your username

Edit `generate_with_stats.py` and update:

```python
USERNAME = "your-username-here"
```

### 4. Add to your profile README

```markdown
![Terminal GIF](https://raw.githubusercontent.com/YOUR_USER/YOUR_REPO/main/output.gif)
```

The GIF will be automatically regenerated every day at **6:00 AM UTC**.

---

## 💻 Running Locally

### Install dependencies

```bash
pip install github-readme-terminal requests python-dotenv

# Install ffmpeg (macOS)
brew install ffmpeg

# Install ffmpeg (Ubuntu/Debian)
sudo apt install ffmpeg
```

### Configure your GitHub Token

Create a `.env` file in the project root:

```bash
cp .env.example .env
```

Then edit `.env` and add:

```env
GITHUB_TOKEN=your_github_token_here
```

### Generate the GIF

```bash
python generate_with_stats.py
```

The output will be saved as `output.gif`.

---

## 🎨 Customization

Edit `generate_with_stats.py` to make it your own:

- **Skills section** — update the `skills` list with your own tech stack
- **Colors** — use ANSI escape codes to change text colors
- **Commands** — add or remove terminal commands and sections
- **Layout** — adjust width, height, padding, and typing speed

---

## 🗂️ Project Structure

```
.
├── generate_with_stats.py   # Main script
├── output.gif               # Generated GIF (auto-updated)
├── .env.example             # Environment variable template
├── .github/
│   └── workflows/           # GitHub Actions workflow
└── README.md
```

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!  
Feel free to open an [issue](../../issues) or submit a pull request.

---

<div align="center">

If this project helped you, consider leaving a ⭐ — it means a lot!

</div>