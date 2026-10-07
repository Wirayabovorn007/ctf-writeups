# 🚩 CTF Writeups

![Status](https://img.shields.io/badge/Status-Active-brightgreen)
![Last Commit](https://img.shields.io/github/last-commit/Wirayabovorn007/ctf-writeups)
![Writeups](https://img.shields.io/badge/Writeups-1-blue)
![License](https://img.shields.io/badge/License-MIT-green)

Writeups, notes, and lessons learned from the Capture The Flag challenges I play.
Each writeup covers how I found the path, the dead ends along the way, and what I'd do differently next time.

## 🗂️ Writeups

| Date    | Name | Type | Writeup      |
|---------|--------------------------------|--------------|--------------|
| 2026-09 | CPTS - Hack the Box            | Cetification | [Link](./cpts) |


## 🧩 Categories

| Category | What it covers |
|----------|----------------|
| 🌐 Web | SQLi, XSS, SSRF, auth bypass, deserialization |
| 🔐 Crypto | Classical ciphers, RSA, padding oracles, custom schemes |
| 💥 Pwn | Buffer overflows, ROP, format strings, heap |
| 🔎 Forensics | Disk and memory analysis, pcaps, file carving |
| 🔄 Reverse | Static and dynamic analysis, unpacking, decompiling |
| 🕵️ OSINT | Public-source investigation and geolocation |
| 🧠 Misc | Scripting, stego, jail escapes, everything else |

## 📁 Repository Structure

```
ctf-writeups/
├── <ctf-or-platform>/
│   └── <challenge-name>/
│       ├── README.md      # the writeup
│       ├── solve.py       # exploit / solver (if any)
│       └── files/         # supporting material (no flags)
├── templates/
│   └── writeup-template.md
└── README.md
```

## 📝 Writeup Format

Every writeup follows the same structure so they're easy to skim:

1. **Overview**: category, points, difficulty, short description
2. **Recon**: what I looked at first and why
3. **Approach**: the thinking, including failed attempts
4. **Solution**: step-by-step with commands and code
5. **Takeaways**: what I learned and how to spot it next time

A reusable template lives in [`templates/writeup-template.md`](./templates/writeup-template.md).

## ⚠️ Spoiler & Ethics Policy

- Writeups for **active competitions** are only published after the event ends.
- Flags are redacted (`flag{REDACTED}`) where a platform's rules require it.
- Everything here is for **educational purposes**. Only test systems you own or have explicit permission to test.

## 🤝 Connect

[Instagram](https://www.instagram.com/wiraya.sh/) · [LinkedIn](https://www.linkedin.com/in/wiraya/)

If you spot a mistake or know a cleaner solution, feel free to open an issue :)
