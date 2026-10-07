<LeftMouse># 🚩 Challenge Name

![Category](https://img.shields.io/badge/Category-Web-blue)
![Difficulty](https://img.shields.io/badge/Difficulty-Medium-orange)
![Points](https://img.shields.io/badge/Points-300-green)
![Status](https://img.shields.io/badge/Status-Solved-brightgreen)

> One-line summary of the challenge and the core idea behind the solution.

---

## 📋 Overview

| Field | Details |
|-------|---------|
| **CTF / Platform** | Name of the event or platform |
| **Challenge** | Challenge name |
| **Category** | Web / Crypto / Pwn / Forensics / Reverse / OSINT / Misc |
| **Difficulty** | Easy / Medium / Hard / Insane |
| **Points** | 000 |
| **Solves** | 000 (at time of solving) |
| **Author** | Challenge author (if known) |
| **Date** | YYYY-MM-DD |
| **Time Spent** | e.g. 2h 30m |
| **Solved During Event?** | Yes / No / Upsolved |

### Challenge Description

> Paste or paraphrase the original challenge description here.

### Provided Files / Targets

- `challenge.zip`: description of what's inside
- `http://target:port`: remote service

---

## 🔎 Recon

What did I look at first, and why?

- **First impressions:**
- **Tech stack / file types / protections identified:**
- **Interesting observations:**

```bash
# Initial commands run
file challenge
strings challenge | head
checksec --file=challenge
```

**Findings:**

-

---

## 🧠 Approach

My thinking process, including hypotheses, dead ends, and pivots. This is the most valuable section for future me.

### Hypotheses

1. **Hypothesis:** …
   **Result:** ✅ Worked / ❌ Dead end, because …
2. **Hypothesis:** …
   **Result:** …

### Dead Ends & Mistakes

- What I tried that didn't work, and why
- Time wasted on something avoidable

### The "Aha" Moment

What clue or observation unlocked the solution?

---

## 🛠️ Solution

### Step 1: Title

Explain what I did and *why it works*.

```bash
command --here
```

### Step 2: Title

```python
# Short snippets inline; full solver goes in solve.py
```

### Step 3: Title

Screenshots or output (redact anything sensitive):

![Description](./files/screenshot.png)

### Final Exploit / Solver

Full script: [`solve.py`](./solve.py)

```python
#!/usr/bin/env python3
from pwn import *

# Minimal, commented solver
```

### Flag

```
flag{REDACTED}
```

---

## 🧬 Root Cause / How It Works

A short technical explanation of the underlying vulnerability or trick.

- **Vulnerability class:** e.g. SQL injection, ret2libc, weak RSA exponent
- **Why it exists:** the flawed assumption or bug
- **Relevant references:** CWE, CVE, papers, docs

---

## 💡 Key Takeaways

- **New technique learned:**
- **How to spot this next time:** signs and patterns that point to this vulnerability
- **What I'd do differently:**
- **Tools or commands worth remembering:**

---

## 🛡️ Mitigation

How would a developer or defender prevent this?

-

---

## 🔗 References

- [Resource title](https://example.com)
- [Other writeups for comparison](https://example.com)
- [Tool documentation](https://example.com)

---

## 📎 Appendix (optional)

- Alternative solutions
- Extra notes, scratch work, or unfinished ideas
- Cleaner approaches I learned from other people's writeups

---

For educational purposes only. Flags are redacted where required by platform or event rules.

