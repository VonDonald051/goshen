# 🛡️ Cyber Academy — Learn Ethical Hacking

A complete, self-contained, interactive web application that teaches cybersecurity and ethical hacking from absolute beginner to job-ready professional. No backend, no database, no build step — just open `index.html` (or serve the folder) and start learning.

![Module count: 10](https://img.shields.io/badge/modules-10-00e676) ![Lessons: 25](https://img.shields.io/badge/lessons-25-4fc3f7)

---

## 🚀 Quick Start

You can run the academy two ways:

### Option 1 — Open directly
Double-click `index.html`. It runs entirely in your browser.

### Option 2 — Serve locally (recommended)
```bash
cd cyber-academy
python3 -m http.server 8080
```
Then visit **http://localhost:8080** in your browser.

Your progress is saved automatically in your browser's `localStorage`.

---

## 📚 The Curriculum

The course is organized into **10 modules / 25 lessons** with over **75 quiz questions**, code examples, command references, and hands-on labs.

| # | Module | Lessons |
|---|--------|---------|
| 0 | **Cybersecurity Foundations** — CIA triad, threats, ethics, law, Cyber Kill Chain, MITRE ATT&CK | 3 |
| 1 | **Networking Fundamentals** — OSI model, TCP/UDP, IP/subnetting, DNS, DHCP, ARP, devices | 4 |
| 2 | **Linux & the Command Line** — filesystem, permissions, Bash, SSH, process management | 3 |
| 3 | **Cryptography** — symmetric/asymmetric, hashing, PKI, certificates, TLS, Heartbleed | 2 |
| 4 | **Reconnaissance & OSINT** — Google dorks, Shodan, subdomain enum, Nmap, active scanning | 2 |
| 5 | **Vulnerabilities & Exploitation** — CVE/CVSS, scanners, Metasploit, msfvenom | 2 |
| 6 | **Web Application Hacking** — OWASP Top 10, SQLi, XSS, IDOR, JWT, SSRF, Burp Suite | 3 |
| 7 | **Wireless, Sniffing & Social Engineering** — Wi-Fi cracking, ARP spoofing, Wireshark, phishing, malware | 2 |
| 8 | **Cloud, Post-Exploitation & IR** — AWS/Azure IAM, password cracking, Mimikatz, pivoting, forensics | 3 |
| 9 | **Career, Certs & Your Lab** — Kali setup, VirtualBox, cert roadmap (Security+ → OSCP), 12-month plan | 2 |

---

## ✨ Features

- **Interactive quizzes** at the end of every lesson with instant feedback and explanations.
- **Progress tracking** — checkmarks, per-module bars, and an overall completion percentage.
- **Automatic advance** — complete a lesson and you're taken to the next one.
- **Keyboard navigation** — `←` / `→` arrows move between lessons.
- **Responsive dark hacker theme** that works on mobile, tablet, and desktop.
- **Offline-friendly** — no external dependencies, CDNs, or tracking.
- **Callouts** — tips, warnings, info boxes, and legal/ethical reminders throughout.
- **Copy-ready command snippets** in terminal-styled blocks for every major tool.
- **Dashboard** with module cards showing your per-module progress.

---

## 🛠️ Tech Stack

- **Vanilla HTML5, CSS3, and JavaScript (ES6+)** — zero dependencies.
- Hash-based routing (`#/module/lesson`).
- `localStorage` for persistence.
- All content lives in `js/curriculum.js` — easy to extend.

## 📂 File Structure

```
cyber-academy/
├── index.html          # App shell, sidebar, topbar
├── styles.css          # Dark theme (all styling)
├── js/
│   ├── curriculum.js   # All lesson content & quizzes (the "database")
│   └── app.js          # Routing, rendering, quizzes, progress
└── README.md
```

---

## ➕ Adding Your Own Lessons

Open `js/curriculum.js`. Each module has the shape:

```js
{
  id: "module-id",
  title: "Module Title",
  icon: "🔐",
  description: "Short description shown on dashboard cards.",
  lessons: [
    {
      id: "lesson-id",
      title: "Lesson Title",
      tag: "Module X · Lesson Y",
      intro: "One-sentence intro shown under the title.",
      content: ` <p>Arbitrary HTML is supported here.</p> `,
      quiz: [
        {
          q: "Question text?",
          options: ["A", "B", "C", "D"],
          answer: 1,          // index of correct option
          explain: "Why that answer is correct."
        }
      ]
    }
  ]
}
```

Add a new object to the `CURRICULUM` array (or add a lesson to an existing module) and reload — the app picks it up automatically.

---

## ⚠️ Important: Use This Knowledge Ethically

This academy is for **educational purposes only**. Every technique is taught so you can *defend* systems and perform *authorized* penetration tests.

- Only test systems you **own** or have **written permission** to test.
- Use isolated labs (VMs on Host-Only networks) for hands-on practice.
- A signed Rules of Engagement / Statement of Work is required before any real engagement.
- Unauthorized access is a crime in nearly every country (CFAA in the US, Computer Misuse Act in the UK, Kenya Data Protection Act / Computer Misuse and Cybercrimes Act in Kenya, Budapest Convention internationally).

With great power comes great responsibility. Use these skills to make the digital world safer. 🛡️

---

## 🌐 Recommended Next Steps After the Course

1. Build a home lab (Kali + Metasploitable + Juice Shop) — see Module 9.
2. Sign up for **TryHackMe** and **Hack The Box** for guided, live practice.
3. Complete **PortSwigger Web Security Academy** (free) for deep web skills.
4. Earn **CompTIA Security+** as your first certification.
5. Start a blog / GitHub to publish writeups — build a portfolio.

Happy (legal) hacking!
