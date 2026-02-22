# 🌌 Antigravity Awesome Skills: 889+ Agentic Skills for Claude Code, Gemini CLI, Cursor, Copilot & More

> **The Ultimate Collection of 889+ Universal Agentic Skills for AI Coding Assistants — Claude Code, Gemini CLI, Codex CLI, Antigravity IDE, GitHub Copilot, Cursor, OpenCode, AdaL**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Anthropic-purple)](https://claude.ai)
[![Gemini CLI](https://img.shields.io/badge/Gemini%20CLI-Google-blue)](https://github.com/google-gemini/gemini-cli)
[![Codex CLI](https://img.shields.io/badge/Codex%20CLI-OpenAI-green)](https://github.com/openai/codex)
[![Kiro CLI](https://img.shields.io/badge/Kiro%20CLI-AWS-orange)](https://kiro.dev)
[![Cursor](https://img.shields.io/badge/Cursor-AI%20IDE-orange)](https://cursor.sh)
[![Copilot](https://img.shields.io/badge/GitHub%20Copilot-VSCode-lightblue)](https://github.com/features/copilot)
[![OpenCode](https://img.shields.io/badge/OpenCode-CLI-gray)](https://github.com/opencode-ai/opencode)
[![Antigravity](https://img.shields.io/badge/Antigravity-DeepMind-red)](https://github.com/sickn33/antigravity-awesome-skills)
[![AdaL CLI](https://img.shields.io/badge/AdaL%20CLI-SylphAI-pink)](https://sylph.ai/)
[![ASK Supported](https://img.shields.io/badge/ASK-Supported-blue)](https://github.com/yeasy/ask)
[![Buy Me a Book](https://img.shields.io/badge/Buy%20me%20a-book-d13610?logo=buymeacoffee&logoColor=white)](https://buymeacoffee.com/sickn33)

If this project helps you, you can [support it here](https://buymeacoffee.com/sickn33) or simply ⭐ the repo.

**Antigravity Awesome Skills** is a curated, battle-tested library of **889 high-performance agentic skills** designed to work seamlessly across all major AI coding assistants:

- 🟣 **Claude Code** (Anthropic CLI)
- 🔵 **Gemini CLI** (Google DeepMind)
- 🟢 **Codex CLI** (OpenAI)
- 🟠 **Kiro CLI** (AWS)
- 🔴 **Antigravity IDE** (Google DeepMind)
- 🩵 **GitHub Copilot** (VSCode Extension)
- 🟠 **Cursor** (AI-native IDE)
- ⚪ **OpenCode** (Open-source CLI)
- 🌸 **AdaL CLI** (Self-evolving Coding Agent)

This repository provides essential skills to transform your AI assistant into a **full-stack digital agency**, including official capabilities from **Anthropic**, **OpenAI**, **Google**, **Microsoft**, **Supabase**, and **Vercel Labs**.

## Table of Contents

- [🚀 New Here? Start Here!](#new-here-start-here)
- [📖 Complete Usage Guide](docs/USAGE.md) - **Start here if confused after installation!**
- [🔌 Compatibility & Invocation](#compatibility--invocation)
- [🛠️ Installation](#installation)
- [🧯 Troubleshooting](#troubleshooting)
- [🎁 Curated Collections (Bundles)](#curated-collections)
- [🧭 Antigravity Workflows](#antigravity-workflows)
- [📦 Features & Categories](#features--categories)
- [📚 Browse 889+ Skills](#browse-889-skills)
- [🤝 How to Contribute](#how-to-contribute)
- [🤝 Community](#community)
- [☕ Support the Project](#support-the-project)
- [👥 Contributors & Credits](#credits--sources)
- [👥 Repo Contributors](#repo-contributors)
- [⚖️ License](#license)
- [🌟 Star History](#star-history)
- [🏷️ GitHub Topics](#github-topics)

---

## New Here? Start Here!

**Welcome to the V6.0.0 Workflows Edition.** This isn't just a list of scripts; it's a complete operating system for your AI Agent.

### 1. 🐣 Context: What is this?

**Antigravity Awesome Skills** (Release 6.0.0) is a massive upgrade to your AI's capabilities.

AI Agents (like Claude Code, Cursor, or Gemini) are smart, but they lack **specific tools**. They don't know your company's "Deployment Protocol" or the specific syntax for "AWS CloudFormation".
**Skills** are small markdown files that teach them how to do these specific tasks perfectly, every time.

### 2. ⚡️ Quick Start (1 minute)

Install once; then use Starter Packs in [docs/BUNDLES.md](docs/BUNDLES.md) to focus on your role.

1. **Install**:

   ```bash
   # Default: ~/.gemini/antigravity/skills (Antigravity global). Use --path for other locations.
   npx antigravity-awesome-skills
   ```

2. **Verify**:

   ```bash
   test -d ~/.gemini/antigravity/skills && echo "Skills installed in ~/.gemini/antigravity/skills"
   ```

3. **Run your first skill**:

   > "Use **@brainstorming** to plan a SaaS MVP."

4. **Pick a bundle**:
   - **Web Dev?** start with `Web Wizard`.
   - **Security?** start with `Security Engineer`.
   - **General use?** start with `Essentials`.

### 3. 🧠 How to use

Once installed, just ask your agent naturally:

> "Use the **@brainstorming** skill to help me plan a SaaS."
> "Run **@lint-and-validate** on this file."

👉 **NEW:** [**Complete Usage Guide - Read This First!**](docs/USAGE.md) (answers: "What do I do after installation?", "How do I execute skills?", "What should prompts look like?")

👉 **[Full Getting Started Guide](docs/GETTING_STARTED.md)**

---

## Compatibility & Invocation

These skills follow the universal **SKILL.md** format and work with any AI coding assistant that supports agentic skills.

| Tool            | Type | Invocation Example                | Path                                                                  |
| :-------------- | :--- | :-------------------------------- | :-------------------------------------------------------------------- |
| **Claude Code** | CLI  | `>> /skill-name help me...`       | `.claude/skills/`                                                     |
| **Gemini CLI**  | CLI  | `(User Prompt) Use skill-name...` | `.gemini/skills/`                                                     |
| **Codex CLI**   | CLI  | `(User Prompt) Use skill-name...` | `.codex/skills/`                                                      |
| **Kiro CLI**    | CLI  | `(User Prompt) Use skill-name...` | `.kiro/skills/`                                                       |
| **Antigravity** | IDE  | `(Agent Mode) Use skill...`       | Global: `~/.gemini/antigravity/skills/` · Workspace: `.agent/skills/` |
| **Cursor**      | IDE  | `@skill-name (in Chat)`           | `.cursor/skills/`                                                     |
| **Copilot**     | Ext  | `(Paste content manually)`        | N/A                                                                   |
| **OpenCode**    | CLI  | `opencode run @skill-name`        | `.agents/skills/`                                                     |
| **AdaL CLI**    | CLI  | `(Auto) Skills load on-demand`    | `.adal/skills/`                                                       |

> [!TIP]
> **Default installer path**: `~/.gemini/antigravity/skills` (Antigravity global). Use `--path ~/.agent/skills` for workspace-specific install. For manual clone, `.agent/skills/` works as workspace path for Antigravity.
> **OpenCode Path Update**: opencode path is changed to `.agents/skills` for global skills. See [Place Files](https://opencode.ai/docs/skills/#place-files) directive on OpenCode Docs.

> [!WARNING]
> **Windows Users**: this repository uses **symlinks** for official skills.
> See [Troubleshooting](#troubleshooting) for the exact fix.

---

## Installation

To use these skills with **Claude Code**, **Gemini CLI**, **Codex CLI**, **Cursor**, **Antigravity**, **OpenCode**, or **AdaL**:

### Option A: npx (recommended)

```bash
# Default: ~/.gemini/antigravity/skills (Antigravity global)
npx antigravity-awesome-skills

# Antigravity (explicit; same as default)
npx antigravity-awesome-skills --antigravity

# Cursor
npx antigravity-awesome-skills --cursor

# Claude Code
npx antigravity-awesome-skills --claude

# Gemini CLI
npx antigravity-awesome-skills --gemini

# Codex CLI
npx antigravity-awesome-skills --codex

# Kiro CLI
npx antigravity-awesome-skills --kiro

# OpenCode
npx antigravity-awesome-skills --path .agents/skills

# Workspace-specific (e.g. .agent/skills for Antigravity workspace)
npx antigravity-awesome-skills --path ~/.agent/skills

# Custom path
npx antigravity-awesome-skills --path ./my-skills
```

Run `npx antigravity-awesome-skills --help` for all options. If the directory already exists, the installer runs `git pull` to update.

### Option B: git clone

Without `--path`, the npx installer uses `~/.gemini/antigravity/skills`. For manual clone or a different path (e.g. workspace `.agent/skills`), use one of the following:

```bash
# Antigravity global (matches npx default)
git clone https://github.com/sickn33/antigravity-awesome-skills.git ~/.gemini/antigravity/skills

# Workspace-specific (e.g. .agent/skills in your project)
git clone https://github.com/sickn33/antigravity-awesome-skills.git .agent/skills

# Claude Code specific
git clone https://github.com/sickn33/antigravity-awesome-skills.git .claude/skills

# Gemini CLI specific
git clone https://github.com/sickn33/antigravity-awesome-skills.git .gemini/skills

# Codex CLI specific
git clone https://github.com/sickn33/antigravity-awesome-skills.git .codex/skills

# Kiro CLI specific
git clone https://github.com/sickn33/antigravity-awesome-skills.git .kiro/skills

# Cursor specific
git clone https://github.com/sickn33/antigravity-awesome-skills.git .cursor/skills

# OpenCode
git clone https://github.com/sickn33/antigravity-awesome-skills.git .agents/skills
```

---

## Troubleshooting

### `npx antigravity-awesome-skills` returns 404

Use the GitHub package fallback:

```bash
npx github:sickn33/antigravity-awesome-skills
```

### Windows clone issues (symlinks)

This repository uses symlinks for official skills. Enable Developer Mode or run Git as Administrator, then clone with:

```bash
git clone -c core.symlinks=true https://github.com/sickn33/antigravity-awesome-skills.git .agent/skills
```

### Skills installed but not detected by your tool

Install to the tool-specific path. Use installer flags: `--antigravity` (default), `--claude`, `--gemini`, `--codex`, `--cursor`, or `--path <dir>` for a custom location (e.g. `~/.agent/skills` for Antigravity workspace).

### Update an existing installation

```bash
# If you used the default installer (Antigravity global):
git -C ~/.gemini/antigravity/skills pull

# If you installed to a custom path (e.g. ~/.agent/skills):
git -C ~/.agent/skills pull
```

### Reinstall from scratch

```bash
rm -rf ~/.gemini/antigravity/skills
npx antigravity-awesome-skills
```

---

## Curated Collections

**Bundles** are curated groups of skills for a specific role or goal (for example: `Web Wizard`, `Security Engineer`, `OSS Maintainer`).

They help you avoid picking from 889+ skills one by one.

### ⚠️ Important: Bundles Are NOT Separate Installations!

**Common confusion:** "Do I need to install each bundle separately?"

**Answer: NO!** Here's what bundles actually are:

**What bundles ARE:**

- ✅ Recommended skill lists organized by role
- ✅ Curated starting points to help you decide what to use
- ✅ Time-saving shortcuts for discovering relevant skills

**What bundles are NOT:**

- ❌ Separate installations or downloads
- ❌ Different git commands
- ❌ Something you need to "activate"

### How to use bundles:

1. **Install the repository once** (you already have all skills)
2. **Browse bundles** in [docs/BUNDLES.md](docs/BUNDLES.md) to find your role
3. **Pick 3-5 skills** from that bundle to start using in your prompts
4. **Reference them in your conversations** with your AI (e.g., "Use @brainstorming...")

For detailed examples of how to actually use skills, see the [**Usage Guide**](docs/USAGE.md).

### Examples:

- Building a SaaS MVP: `Essentials` + `Full-Stack Developer` + `QA & Testing`.
- Hardening production: `Security Developer` + `DevOps & Cloud` + `Observability & Monitoring`.
- Shipping OSS changes: `Essentials` + `OSS Maintainer`.

## Antigravity Workflows

Bundles help you choose skills. Workflows help you execute them in order.

- Use bundles when you need curated recommendations by role.
- Use workflows when you need step-by-step execution for a concrete goal.

Start here:

- [docs/WORKFLOWS.md](docs/WORKFLOWS.md): human-readable playbooks.
- [data/workflows.json](data/workflows.json): machine-readable workflow metadata.

Initial workflows include:

- Ship a SaaS MVP
- Security Audit for a Web App
- Build an AI Agent System
- QA and Browser Automation (with optional `@go-playwright` support for Go stacks)

## Features & Categories

The repository is organized into specialized domains to transform your AI into an expert across the entire software development lifecycle:

| Category       | Focus                                              | Example skills                                                                  |
| :------------- | :------------------------------------------------- | :------------------------------------------------------------------------------ |
| Architecture   | System design, ADRs, C4, and scalable patterns     | `architecture`, `c4-context`, `senior-architect`                                |
| Business       | Growth, pricing, CRO, SEO, and go-to-market        | `copywriting`, `pricing-strategy`, `seo-audit`                                  |
| Data & AI      | LLM apps, RAG, agents, observability, analytics    | `rag-engineer`, `prompt-engineer`, `langgraph`                                  |
| Development    | Language mastery, framework patterns, code quality | `typescript-expert`, `python-patterns`, `react-patterns`                        |
| General        | Planning, docs, product ops, writing, guidelines   | `brainstorming`, `doc-coauthoring`, `writing-plans`                             |
| Infrastructure | DevOps, cloud, serverless, deployment, CI/CD       | `docker-expert`, `aws-serverless`, `vercel-deployment`                          |
| Security       | AppSec, pentesting, vuln analysis, compliance      | `api-security-best-practices`, `sql-injection-testing`, `vulnerability-scanner` |
| Testing        | TDD, test design, fixes, QA workflows              | `test-driven-development`, `testing-patterns`, `test-fixing`                    |
| Workflow       | Automation, orchestration, jobs, agents            | `workflow-automation`, `inngest`, `trigger-dev`                                 |

Counts change as new skills are added. For the current full registry, see [CATALOG.md](CATALOG.md).

## Browse 889+ Skills

We have moved the full skill registry to a dedicated catalog to keep this README clean.

👉 **[View the Complete Skill Catalog (CATALOG.md)](CATALOG.md)**

---

## How to Contribute

We welcome contributions from the community! To add a new skill:

1. **Fork** the repository.
2. **Create a new directory** inside `skills/` for your skill.
3. **Add a `SKILL.md`** with the required frontmatter (name, description, risk, source). See [docs/SKILL_ANATOMY.md](docs/SKILL_ANATOMY.md) and [docs/QUALITY_BAR.md](docs/QUALITY_BAR.md).
4. **Run validation**: `npm run validate` (or `npm run validate:strict` for CI). Optionally run `python3 scripts/validate_references.py` if you touch workflows or bundles.
5. **Submit a Pull Request**.

Please ensure your skill follows the Antigravity/Claude Code best practices. Maintainers: see [docs/AUDIT.md](docs/AUDIT.md) for coherence checks and [.github/MAINTENANCE.md](.github/MAINTENANCE.md) for the full validation chain.

---

## Community

- [Community Guidelines](docs/COMMUNITY_GUIDELINES.md)
- [Security Policy](docs/SECURITY_GUARDRAILS.md)

---

## Support the Project

Support is optional. This project stays free and open-source for everyone.

If this repository saves you time or helps you ship faster, you can support ongoing maintenance:

- [☕ Buy me a book on Buy Me a Coffee](https://buymeacoffee.com/sickn33)

Where support goes:

- Skill curation, testing, and quality validation.
- Documentation updates, examples, and onboarding improvements.
- Faster triage and review of community issues and PRs.

Prefer non-financial support:

- Star the repository.
- Open clear, reproducible issues.
- Submit PRs (skills, docs, fixes).
- Share the project with other builders.

---

## Credits & Sources

We stand on the shoulders of giants.

👉 **[View the Full Attribution Ledger](docs/SOURCES.md)**

Key contributors and sources include:

- **HackTricks**
- **OWASP**
- **Anthropic / OpenAI / Google**
- **The Open Source Community**

This collection would not be possible without the incredible work of the Claude Code community and official sources:

### Official Sources

- **[anthropics/skills](https://github.com/anthropics/skills)**: Official Anthropic skills repository - Document manipulation (DOCX, PDF, PPTX, XLSX), Brand Guidelines, Internal Communications.
- **[anthropics/claude-cookbooks](https://github.com/anthropics/claude-cookbooks)**: Official notebooks and recipes for building with Claude.
- **[remotion-dev/skills](https://github.com/remotion-dev/skills)**: Official Remotion skills - Video creation in React with 28 modular rules.
- **[vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills)**: Vercel Labs official skills - React Best Practices, Web Design Guidelines.
- **[openai/skills](https://github.com/openai/skills)**: OpenAI Codex skills catalog - Agent skills, Skill Creator, Concise Planning.
- **[supabase/agent-skills](https://github.com/supabase/agent-skills)**: Supabase official skills - Postgres Best Practices.
- **[microsoft/skills](https://github.com/microsoft/skills)**: Official Microsoft skills - Azure cloud services, Bot Framework, Cognitive Services, and enterprise development patterns across .NET, Python, TypeScript, Go, Rust, and Java.
- **[google-gemini/gemini-skills](https://github.com/google-gemini/gemini-skills)**: Official Gemini skills - Gemini API, SDK and model interactions.

### Community Contributors

- **[rmyndharis/antigravity-skills](https://github.com/rmyndharis/antigravity-skills)**: For the massive contribution of 300+ Enterprise skills and the catalog generation logic.
- **[amartelr/antigravity-workspace-manager](https://github.com/amartelr/antigravity-workspace-manager)**: Official Workspace Manager CLI companion to dynamically auto-provision subsets of skills across unlimited local development environments.

- **[obra/superpowers](https://github.com/obra/superpowers)**: The original "Superpowers" by Jesse Vincent.
- **[guanyang/antigravity-skills](https://github.com/guanyang/antigravity-skills)**: Core Antigravity extensions.
- **[diet103/claude-code-infrastructure-showcase](https://github.com/diet103/claude-code-infrastructure-showcase)**: Infrastructure and Backend/Frontend Guidelines.
- **[ChrisWiles/claude-code-showcase](https://github.com/ChrisWiles/claude-code-showcase)**: React UI patterns and Design Systems.
- **[travisvn/awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills)**: Loki Mode and Playwright integration.
- **[zebbern/claude-code-guide](https://github.com/zebbern/claude-code-guide)**: Comprehensive Security suite & Guide (Source for ~60 new skills).
- **[alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills)**: Senior Engineering and PM toolkit.
- **[karanb192/awesome-claude-skills](https://github.com/karanb192/awesome-claude-skills)**: A massive list of verified skills for Claude Code.
- **[VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills)**: Curated collection of 61 high-quality skills including official team skills from Sentry, Trail of Bits, Expo, Hugging Face, and comprehensive context engineering suite (v4.3.0 integration).
- **[zircote/.claude](https://github.com/zircote/.claude)**: Shopify development skill reference.
- **[vibeforge1111/vibeship-spawner-skills](https://github.com/vibeforge1111/vibeship-spawner-skills)**: AI Agents, Integrations, Maker Tools (57 skills, Apache 2.0).
- **[coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills)**: Marketing skills for CRO, copywriting, SEO, paid ads, and growth (23 skills, MIT).
- **[Silverov/yandex-direct-skill](https://github.com/Silverov/yandex-direct-skill)**: Yandex Direct (API v5) advertising audit skill — 55 automated checks, A-F scoring, campaign/ad/keyword analysis for the Russian PPC market (MIT).
- **[vudovn/antigravity-kit](https://github.com/vudovn/antigravity-kit)**: AI Agent templates with Skills, Agents, and Workflows (33 skills, MIT).
- **[affaan-m/everything-claude-code](https://github.com/affaan-m/everything-claude-code)**: Complete Claude Code configuration collection from Anthropic hackathon winner - skills only (8 skills, MIT).
- **[whatiskadudoing/fp-ts-skills](https://github.com/whatiskadudoing/fp-ts-skills)**: Practical fp-ts skills for TypeScript – fp-ts-pragmatic, fp-ts-react, fp-ts-errors (v4.4.0).
- **[webzler/agentMemory](https://github.com/webzler/agentMemory)**: Source for the agent-memory-mcp skill.
- **[sstklen/claude-api-cost-optimization](https://github.com/sstklen/claude-api-cost-optimization)**: Save 50-90% on Claude API costs with smart optimization strategies (MIT).
- **[Wittlesus/cursorrules-pro](https://github.com/Wittlesus/cursorrules-pro)**: Professional .cursorrules configurations for 8 frameworks - Next.js, React, Python, Go, Rust, and more. Works with Cursor, Claude Code, and Windsurf.

### Inspirations

- **[f/awesome-chatgpt-prompts](https://github.com/f/awesome-chatgpt-prompts)**: Inspiration for the Prompt Library.
- **[leonardomso/33-js-concepts](https://github.com/leonardomso/33-js-concepts)**: Inspiration for JavaScript Mastery.

---

## Repo Contributors

<a href="https://github.com/sickn33/antigravity-awesome-skills/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=sickn33/antigravity-awesome-skills" />
</a>

Made with [contrib.rocks](https://contrib.rocks).

We officially thank the following contributors for their help in making this repository awesome!

- [@sck000](https://github.com/sck000)
- [@munir-abbasi](https://github.com/munir-abbasi)
- [@sickn33](https://github.com/sickn33)
- [@Mohammad-Faiz-Cloud-Engineer](https://github.com/Mohammad-Faiz-Cloud-Engineer)
- [@Dokhacgiakhoa](https://github.com/Dokhacgiakhoa)
- [@IanJ332](https://github.com/IanJ332)
- [@chauey](https://github.com/chauey)
- [@PabloSMD](https://github.com/PabloSMD)
- [@GuppyTheCat](https://github.com/GuppyTheCat)
- [@Tiger-Foxx](https://github.com/Tiger-Foxx)
- [@arathiesh](https://github.com/arathiesh)
- [@liyin2015](https://github.com/liyin2015)
- [@1bcMax](https://github.com/1bcMax)
- [@ALEKGG1](https://github.com/ALEKGG1)
- [@ar27111994](https://github.com/ar27111994)
- [@BenedictKing](https://github.com/BenedictKing)
- [@whatiskadudoing](https://github.com/whatiskadudoing)
- [@LocNguyenSGU](https://github.com/LocNguyenSGU)
- [@yubing744](https://github.com/yubing744)
- [@SuperJMN](https://github.com/SuperJMN)
- [@truongnmt](https://github.com/truongnmt)
- [@viktor-ferenczi](https://github.com/viktor-ferenczi)
- [@c1c3ru](https://github.com/c1c3ru)
- [@ckdwns9121](https://github.com/ckdwns9121)
- [@fbientrigo](https://github.com/fbientrigo)
- [@junited31](https://github.com/junited31)
- [@KrisnaSantosa15](https://github.com/KrisnaSantosa15)
- [@sstklen](https://github.com/sstklen)
- [@taksrules](https://github.com/taksrules)
- [@zebbern](https://github.com/zebbern)
- [@vuth-dogo](https://github.com/vuth-dogo)
- [@mvanhorn](https://github.com/mvanhorn)
- [@rookie-ricardo](https://github.com/rookie-ricardo)
- [@evandro-miguel](https://github.com/evandro-miguel)
- [@raeef1001](https://github.com/raeef1001)
- [@devchangjun](https://github.com/devchangjun)
- [@jackjin1997](https://github.com/jackjin1997)
- [@ericgandrade](https://github.com/ericgandrade)
- [@sohamganatra](https://github.com/sohamganatra)
- [@Nguyen-Van-Chan](https://github.com/Nguyen-Van-Chan)
- [@8hrsk](https://github.com/8hrsk)
- [@Wittlesus](https://github.com/Wittlesus)
- [@Vonfry](https://github.com/Vonfry)
- [@ssumanbiswas](https://github.com/ssumanbiswas)
- [@amartelr](https://github.com/amartelr)
- [@fernandorych](https://github.com/fernandorych)

---

## License

MIT License. See [LICENSE](LICENSE) for details.

---

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=sickn33/antigravity-awesome-skills&type=date&legend=top-left)](https://www.star-history.com/#sickn33/antigravity-awesome-skills&type=date&legend=top-left)

If Antigravity Awesome Skills has been useful, consider ⭐ starring the repo or [buying me a book](https://buymeacoffee.com/sickn33).

---

## GitHub Topics

For repository maintainers, add these topics to maximize discoverability:

```text
claude-code, gemini-cli, codex-cli, antigravity, cursor, github-copilot, opencode,
agentic-skills, ai-coding, llm-tools, ai-agents, autonomous-coding, mcp,
ai-developer-tools, ai-pair-programming, vibe-coding, skill, skills, SKILL.md, rules.md, CLAUDE.md, GEMINI.md, CURSOR.md
```
