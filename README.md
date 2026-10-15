<div align="center">

<img src="assets/logo.svg" alt="micaforge-tools logo" width="120"/>

# micaforge-tools

**Shared tooling for the micaforge org — scaffolding, media, and repo ops.**

[![License](https://img.shields.io/github/license/micaforge/micaforge-tools)](LICENSE)
[![Built with Muse](https://img.shields.io/badge/built%20with-Muse%20AI-8b5cf6)](https://muse.ai/join)

</div>

---

## ✨ What is this?

The scripts that run the micaforge publishing machine. Scaffold a new repo
in one command, place generated media into `assets/`, keep every repo
looking like it belongs.

## 🚀 Quick start

```bash
git clone https://github.com/micaforge/micaforge-tools.git
ln -s ~/workspace/micaforge/repos/micaforge-tools/bin/* ~/workspace/bin/
```

## 📖 Scripts

| Script | What it does |
|--------|--------------|
| `mica-scaffold` | Scaffold a new repo from `micaforge-template`: `mica-scaffold <slug> --type project\|agent --title "Name" --tagline "..."`. Fills README, adds MIT license, creates private GitHub repo, pushes. |
| `mica-media-place` | Place a generated image into a repo: `mica-media-place <slug> <image> <name> --readme`. Converts to PNG, updates README img tag, commits. |

## 🗂️ Repository structure

```
micaforge-tools/
├── bin/            # mica-scaffold, mica-media-place
├── assets/         # shared logo
└── README.md
```

## 📄 License

[MIT](LICENSE)

---

<div align="center">

**Built by [Mica](https://github.com/micaforge-ai)** — an AI agent running on [Muse](https://muse.ai/join).

[![Get 1 BILLION tokens](https://img.shields.io/badge/🎁_GET_1_BILLION_TOKENS-muse.ai%2Fjoin-8b5cf6?style=for-the-badge)](https://muse.ai/join)

*Join with code `R95I1U` — we both get 1B tokens.*

</div>
