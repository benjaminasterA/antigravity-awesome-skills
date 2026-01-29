# Getting Started with Antigravity Awesome Skills (V3)

**New here? This guide will help you supercharge your AI Agent in 5 minutes.**

---

## 🤔 What Are "Skills"?

AI Agents (like **Claude Code**, **Gemini**, **Cursor**) are smart, but they lack specific knowledge about your tools.
**Skills** are specialized instruction manuals (markdown files) that teach your AI how to perform specific tasks perfectly, every time.

**Analogy:** Your AI is a brilliant intern. **Skills** are the SOPs (Standard Operating Procedures) that make them a Senior Engineer.

---

## ⚡️ Quick Start: The "Starter Packs"

Don't panic about the 560+ skills. You don't need them all at once.
We have curated **Starter Packs** to get you running immediately.

### 1. Install the Repo

Copy the skills to your agent's folder:

```bash
# Universal Installation (works for most agents)
git clone https://github.com/sickn33/antigravity-awesome-skills.git .agent/skills
```

### 2. Pick Your Persona

Find the bundle that matches your role (see [BUNDLES.md](BUNDLES.md)):

| Persona               | Bundle Name    | What's Inside?                                    |
| :-------------------- | :------------- | :------------------------------------------------ |
| **Web Developer**     | `Web Wizard`   | React Patterns, Tailwind mastery, Frontend Design |
| **Security Engineer** | `Hacker Pack`  | OWASP, Metasploit, Pentest Methodology            |
| **Manager / PM**      | `Product Pack` | Brainstorming, Planning, SEO, Strategy            |
| **Everything**        | `Essentials`   | Clean Code, Planning, Validation (The Basics)     |

---

## 🚀 How to Use a Skill

Once installed, just talk to your AI naturally.

### Example 1: Planning a Feature (**Essentials**)

> "Use **@brainstorming** to help me design a new login flow."

**What happens:** The AI loads the brainstorming skill, asks you structured questions, and produces a professional spec.

### Example 2: Checking Your Code (**Web Wizard**)

> "Run **@lint-and-validate** on this file and fix errors."

**What happens:** The AI follows strict linting rules defined in the skill to clean your code.

### Example 3: Security Audit (**Hacker Pack**)

> "Use **@api-security-best-practices** to review my API endpoints."

**What happens:** The AI audits your code against OWASP standards.

---

## 🔌 Supported Tools

| Tool            | Status          | Path              |
| :-------------- | :-------------- | :---------------- |
| **Claude Code** | ✅ Full Support | `.claude/skills/` |
| **Gemini CLI**  | ✅ Full Support | `.gemini/skills/` |
| **Antigravity** | ✅ Native       | `.agent/skills/`  |
| **Cursor**      | ✅ Native       | `.cursor/skills/` |
| **Copilot**     | ⚠️ Text Only    | Manual copy-paste |

---

## 🛡️ Trust & Safety (New in V3)

We classify skills so you know what you're running:

- 🟣 **Official**: Maintained by Anthropic/Google/Vendors (High Trust).
- 🔵 **Safe**: Community skills that are non-destructive (Read-only/Planning).
- 🔴 **Risk**: Skills that modify systems or perform security tests (Authorized Use Only).

_Check the [Skill Catalog](../CATALOG.md) for the full list._

---

## ❓ FAQ

**Q: Do I need to install all 560 skills?**
A: You clone the whole repo, but your AI only _reads_ the ones you ask for (or that are relevant). It's lightweight!

**Q: Can I make my own skills?**
A: Yes! Use the **@skill-creator** skill to build your own.

**Q: Is this free?**
A: Yes, MIT License. Open Source forever.

---

## ⏭️ Next Steps

1. [Browse the Bundles](BUNDLES.md)
2. [See Real-World Examples](EXAMPLES.md)
3. [Contribute a Skill](../CONTRIBUTING.md)
