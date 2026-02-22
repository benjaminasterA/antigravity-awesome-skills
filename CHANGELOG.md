# Changelog

All notable changes to the **Antigravity Awesome Skills** collection are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [6.0.0] - 2026-02-22 - "Codex YAML Fix & Community PRs"

> **Major release: Codex frontmatter fixes, AWS Security & Compliance skills, Antigravity Workspace Manager CLI, and validation fixes.**

This release addresses Codex invalid YAML warnings (issue #108) via frontmatter fixes, adds AWS Security & Compliance skills and the official Antigravity Workspace Manager CLI companion, and fixes validation for nerdzao-elite skills.

## New Skills

- **AWS Security & Compliance** (PR #106): `aws-compliance-checker`, `aws-iam-best-practices`, `aws-secrets-rotation`, `aws-security-audit`.
- **nerdzao-elite**, **nerdzao-elite-gemini-high**: Elite workflow skills (validation fixes in-repo).

## Improvements

- **Frontmatter**: Fixed YAML frontmatter in code-reviewer, architect-review, c-pro, design-orchestration, haskell-pro, multi-agent-brainstorming, performance-engineer, search-specialist (PR #111) — reduces Codex "invalid YAML" warnings (fixes #108).
- **Antigravity Workspace Manager**: Official CLI companion to auto-provision skill subsets across environments (PR #110); documented in Community Contributors.
- **Registry**: Now tracking 889 skills.
- **Validation**: Added frontmatter and "When to Use" for nerdzao-elite / nerdzao-elite-gemini-high.

## Credits

- **@Vonfry** for frontmatter YAML fixes (PR #111)
- **@ssumanbiswas** for AWS Security & Compliance skills (PR #106)
- **@amartelr** for Antigravity Workspace Manager CLI (PR #110)
- **@fernandorych** for branch sync (PR #109)
- **@Rodrigolmti** for reporting Codex YAML issue (#108)

---

_Upgrade now: `git pull origin main` to fetch the latest skills._

## [5.10.0] - 2026-02-21 - "AWS Kiro CLI Integration"

> **Native support and integration guide for AWS Kiro CLI, expanding the repository's reach to the AWS developer community.**

This release adds comprehensive support for Kiro CLI, AWS's recently launched agentic IDE, enabling 883+ skills to enhance Kiro's autonomous operations across serverless, IaC, and AWS architectures. It also includes an important bugfix for the npm installer CLI.

## 🚀 Improvements

- **Integration Guide**: Added `docs/KIRO_INTEGRATION.md` detailing Kiro capabilities, installation instructions, AWS-recommended skills, and MCP usage.
- **Documentation**: Updated `README.md`, `docs/GETTING_STARTED.md`, and `docs/FAQ.md` to formally support Kiro CLI and add invocation examples.
- **Installer**: Added the `--kiro` flag to the CLI installer (`bin/install.js`) which correctly targets `~/.kiro/skills`.

## 🐛 Bug Fixes

- **Installer Path Consistency**: Fixed Issue #105 where the published `v5.9.0` npm install script contained an older version of `bin/install.js`, causing `--antigravity` installs to mistakenly target `.agent/skills` instead of the global `~/.gemini/antigravity/skills`. This release (`5.10.0`) properly bundles the corrected npm install script.

## 👥 Credits

A huge shoutout to our community contributors:

- **@ssumanbiswas** for the Kiro CLI support (PR #104)

---

## [5.9.0] - 2026-02-20 - "Apple HIG & Quality Bar"

> **Extensive Apple design guidelines and strict validation for the entire registry.**

This release adds the official Apple Human Interface Guidelines skills suite, enforces strict agentskills-ref metadata validation across all skills, and addresses critical path resolution bugs in the CLI installer along with dangling link validation to prevent agent token waste.

## 🚀 New Skills

### 🍎 [apple-hig-skills](skills/hig-platforms/)

**Comprehensive platform and UX guidelines for Apple ecosystems.**
Official guidelines covering iOS, macOS, visionOS, watchOS, and tvOS natively formatted for AI consumption.

- **Key Feature 1**: Deep dives into spatial layout, interactions, and modalities.
- **Key Feature 2**: Component-level guidelines for status bars, dialogs, charts, and input mechanisms (Pencil, Digital Crown).

> **Try it:** `Use @hig-platforms to review if our iPad app navigation follows standard iOS paradigms.`

### 👁️ [manifest](skills/manifest/)

**Observability plugin setup guide for AI agents.**
Walks through a 6-step setup for the Manifest observability platform, including troubleshooting for common errors.

- **Key Feature**: Complete configuration wizard from obtaining API keys to verifying traces.

> **Try it:** `Use @manifest to add observability to our local python agent.`

---

## 📦 Improvements

- **Registry Update**: Now tracking 883 skills.
- **CLI Installer**: Fixed the default `.agent/skills` path to properly default to `~/.gemini/antigravity/skills` and added an explicit `--antigravity` flag (fixes #101).
- **Validation**: Enforced strict folder-to-name matching and concise (<200 char) descriptions based on `agentskills-ref` (fixes #97).
- **Validation**: Added build-time Markdown dangling link validation to `validate_skills.py` to prevent agents from hallucinating relative paths (fixes #102).

## 👥 Credits

A huge shoutout to our community contributors:

- **@raintree-technology** for the Apple HIG Skills (PR #90)
- **@sergeyklay** for the skill quality validations (PR #97)
- **@SebConejo** for the manifest observability skill (PR #103)
- **@community** for identifying installer and link bugs (Issues #101, #102)

---

_Upgrade now: `git pull origin main` to fetch the latest skills._

## [5.8.0] - 2026-02-19 - "Domain-Driven Design Suite"

> **First full DDD skill suite: strategic design, context mapping, and tactical patterns for complex domains.**

This release introduces a comprehensive Domain-Driven Design skill suite (4 new skills) contributed by the community, plus playbook fixes for saga-orchestration and event-store-design, and new DDD-themed bundle and workflow entries.

## 🚀 New Skills

### 🏗️ [domain-driven-design](skills/domain-driven-design/)

**Entry point and router for all DDD adoption decisions.**
Covers viability checks, routing to strategic/tactical/evented sub-skills, and output requirements.

- **Key Feature**: Viability check gate — avoids over-engineering simple systems.
- **Key Feature**: Routing map to `@ddd-strategic-design`, `@ddd-context-mapping`, `@ddd-tactical-patterns`, CQRS, event sourcing, sagas, projections.

> **Try it:** `Use @domain-driven-design to assess if this billing platform should adopt full DDD.`

### 🗺️ [ddd-strategic-design](skills/ddd-strategic-design/)

**Subdomains, bounded contexts, and ubiquitous language.**
Produces subdomain classification tables, bounded context catalogs, and glossaries.

### 🔗 [ddd-context-mapping](skills/ddd-context-mapping/)

**Cross-context integration contracts and anti-corruption layers.**
Defines upstream/downstream ownership, translation rules, and versioning policies.

### 🧩 [ddd-tactical-patterns](skills/ddd-tactical-patterns/)

**Aggregates, value objects, repositories, and domain events in code.**
Includes a TypeScript aggregate example with invariant enforcement.

---

## 📦 Improvements

- **Registry Update**: Now tracking 868 skills.
- **saga-orchestration** and **event-store-design**: Added missing `resources/implementation-playbook.md`.
- **docs/BUNDLES.md**: Added DDD & Evented Architecture bundle section.
- **docs/WORKFLOWS.md** + **data/workflows.json**: New "Design a DDD Core Domain" workflow entry.

## 👥 Credits

A huge shoutout to our community contributors:

- **[@rcigor](https://github.com/rcigor)** for the full DDD skill suite (PR #98)

---

_Upgrade now: `git pull origin main` to fetch the latest skills._

---

## [5.7.0] - 2026-02-18 - "Yandex Direct Audit"

> **First agentic skill for the Russian PPC market, offering comprehensive Yandex Direct account auditing.**

### Added

- **New External Skill**: `yandex-direct-audit` (Silverov/yandex-direct-skill)
  - 55 automated checks for Yandex Direct (API v5).
  - A-F scoring system.
  - Comprehensive campaign, ad, and keyword analysis.

### Registry

- **Total Skills**: 864.
- **Generated Files**: Synced artifacts.

### Credits

- **[@Silverov](https://github.com/Silverov)** - Yandex Direct Audit skill (PR #95).

---

## [5.6.0] - 2026-02-17 - "Autonomous Agents & Trusted Workflows"

> **DBOS for reliable workflows, Crypto BD agents, and improved usage documentation.**

This release introduces official DBOS skills for building fault-tolerant applications in TypeScript, Python, and Go, plus a sophisticated autonomous Business Development agent for crypto, and a comprehensive usage guide to help new users get started.

### Added

- **DBOS Skills** (Official):
  - `dbos-typescript`: Durable workflows and steps for TypeScript.
  - `dbos-python`: Fault-tolerant Python applications.
  - `dbos-golang`: Reliable Go services.
- **New Skill**: `crypto-bd-agent` - Autonomous BD patterns for token discovery, scoring, and outreach with wallet forensics.
- **Documentation**: New `docs/USAGE.md` guide addressing post-installation confusion (how to prompt, where skills live).

### Registry

- **Total Skills**: 864 (from 860).
- **Generated Files**: Synced `skills_index.json`, `data/catalog.json`, and `README.md`.

### Contributors

- **[@maxdml](https://github.com/maxdml)** - DBOS Skills (PR #94).
- **[@buzzbysolcex](https://github.com/buzzbysolcex)** - Crypto BD Agent (PR #92).
- **[@copilot-swe-agent](https://github.com/apps/copilot-swe-agent)** - Usage Guide (PR #93).

---

## [5.5.0] - 2026-02-16 - "Laravel Pro & ReactFlow Architect"

> **Advanced Laravel engineering roles and ReactFlow architecture patterns.**

This release introduces professional Laravel capabilities (Expert & Security Auditor) and a comprehensive ReactFlow Architect skill for building complex node-based applications.

### Added

- **New Skill**: `laravel-expert` - Senior Laravel Engineer role for production-grade, maintainable, and idiomatic solutions (clean architecture, security, performance).
- **New Skill**: `laravel-security-audit` - Specialized security auditor for Laravel apps (OWASP, vulnerabilities, misconfigurations).
- **New Skill**: `react-flow-architect` - Expert ReactFlow patterns for interactive graph apps (hierarchical navigation, performance, customized state management).

### Changed

- **OpenCode**: Updated installation path to `.agents/skills` to align with latest OpenCode standards.

### Registry

- **Total Skills**: 860 (from 857).
- **Generated Files**: Synced `skills_index.json`, `data/catalog.json`, and `README.md`.

### Contributors

- **[@Musayrlsms](https://github.com/Musayrlsms)** - Laravel Expert & Security Audit skills (PR #85, #86).
- **[@mertbaskurt](https://github.com/mertbaskurt)** - ReactFlow Architect skill (PR #88).
- **[@sharmanilay](https://github.com/sharmanilay)** - OpenCode path fix (PR #87).

---

## [5.4.0] - 2026-02-16 - "CursorRules Pro & Go-Rod"

> **Community contributions: CursorRules Pro in credits and go-rod-master skill for browser automation with Go.**

This release adds CursorRules Pro to Community Contributors and a new skill for browser automation and web scraping with go-rod (Chrome DevTools Protocol) in Golang, including stealth and anti-bot-detection patterns.

### New Skills

#### go-rod-master ([skills/go-rod-master/](skills/go-rod-master/))

**Browser automation and web scraping with Go and Chrome DevTools Protocol.**
Comprehensive guide for the go-rod library: launch and page lifecycle, Must vs error patterns, context and timeouts, element selectors, auto-wait, and integration with go-rod/stealth for anti-bot detection.

- **Key features**: CDP-native driver, thread-safe operations, stealth plugin, request hijacking, concurrent page pools.
- **When to use**: Scraping or automating sites with Go, headless browser for SPAs, stealth/anti-bot needs, migrating from chromedp or Playwright Go.

> **Try it:** "Automate logging into example.com with Go using go-rod and stealth."

### Registry

- **Total Skills**: 857 (from 856).
- **Generated files**: README, skills_index.json, catalog, and bundles synced.

### Credits

- **[@Wittlesus](https://github.com/Wittlesus)** - CursorRules Pro in Community Contributors (PR #81).
- **[@8hrsk](https://github.com/8hrsk)** - go-rod-master skill (PR #83).

---

_Upgrade now: `git pull origin main` to fetch the latest skills._

---

## [5.3.0] - 2026-02-13 - "Advanced Three.js & Modern Graphics"

> **Enhanced Three.js patterns: performance, visual polish, and production practices.**

This release significantly upgrades our 3D visualization capabilities with a comprehensive Three.js skill upgrade, focusing on CDN-compatible patterns, performance optimizations, and modern graphics techniques like shadows, fog, and GSAP integration.

### Added

- **Modern Three.js Patterns**: Comprehensive guide for `r128` (CDN) and production environments.
- **Visual Polish**: Advanced sections for shadows, environment maps, and tone mapping.
- **Interaction Models**: Custom camera controls (OrbitControls alternative) and raycasting for object selection.
- **Production Readiness**: Integration patterns for GSAP, scroll-based animations, and build tool optimizations.

### Registry

- **Total Skills**: 856.
- **Metadata**: Fixed missing source and risk fields for `threejs-skills`.
- **Sync**: All discovery artifacts (README, Catalog, Index) updated and synced.

### Contributors

- **[@Krishna-hehe](https://github.com/Krishna-hehe)** - Advanced Three.js skill overhaul (PR #78).

---

> **New AI capabilities: Podcast Generation, Azure Identity, and Self-Evolving Agents.**

### Added

- **New Skill**: `podcast-generation` - Create multi-speaker podcasts from text/URLs using OpenAI Text-to-Speech (TTS) and pydub.
- **New Skill**: `weevolve` - Self-evolving knowledge engine with recursive improvement protocol.
- **Azure Skills Expansion**:
  - `azure-ai-agents-persistent-dotnet`: Persistent agent patterns for .NET.
  - `azure-ai-agents-persistent-java`: Persistent agent patterns for Java.
  - `azd-deployment`: Azure Developer CLI deployment strategies.
- **Python Enhancements**:
  - `pydantic-models-py`: Robust data validation patterns.
  - `fastapi-router-py`: Scalable API routing structures.

### Registry

- **Total Skills**: 856 (from 845).
- **Generated Files**: Synced `skills_index.json`, `data/catalog.json`, and `README.md`.

### Contributors

- **[@sickn33](https://github.com/sickn33)** - Podcast Generation & Azure skills sync (PR #74).
- **[@aro-brez](https://github.com/aro-brez)** - WeEvolve skill (Issue #75).

---

## [5.1.0] - 2026-02-12 - "Official Microsoft & Gemini Skills"

> **845+ skills: the largest single-PR expansion ever, powered by official vendor collections.**

Integrates the full official Microsoft skills collection (129 skills) and Google Gemini API development skills, significantly expanding Azure SDK coverage across .NET, Python, TypeScript, Java, and Rust, plus M365 Agents, Semantic Kernel, and wiki plugin skills.

### Added

- **129 Microsoft Official Skills** from [microsoft/skills](https://github.com/microsoft/skills):
  - Azure SDKs across .NET, Python, TypeScript, Java, and Rust
  - M365 Agents, Semantic Kernel, and wiki plugin skills
  - Flat structure using YAML `name` field as directory name
  - Attribution files: `docs/LICENSE-MICROSOFT`, `docs/microsoft-skills-attribution.json`
- **Gemini API Skills**: Official Gemini API development skill under `skills/gemini-api-dev/`
- **New Scripts & Tooling**:
  - `scripts/sync_microsoft_skills.py` (v4): Flat-structure sync with collision detection, stale cleanup, and attribution metadata
  - `scripts/tests/inspect_microsoft_repo.py`: Remote repo inspection
  - `scripts/tests/test_comprehensive_coverage.py`: Coverage verification
- **New npm scripts**: `sync:microsoft` and `sync:all-official` in `package.json`

### Fixed

- **`scripts/generate_index.py`**: Enhanced frontmatter parsing for unquoted `@` symbols and commas
- **`scripts/build-catalog.js`**: Deterministic `generatedAt` timestamp (prevents CI drift)

### Registry

- **Total Skills**: 845 (from 626). All generated files synced.

### Contributors

- [@ar27111994](https://github.com/ar27111994) - Microsoft & Gemini skills integration (PR #73)

---

## [5.0.0] - 2026-02-10 - "Antigravity Workflows Foundation"

> Workflows are now first-class: users can run guided, multi-skill playbooks instead of manually composing skills one by one.

### Added

- **New orchestration skill**: `antigravity-workflows`
  - `skills/antigravity-workflows/SKILL.md`
  - `skills/antigravity-workflows/resources/implementation-playbook.md`
- **New workflow documentation**: `docs/WORKFLOWS.md`
  - Introduces the Workflows model and differentiates it from Bundles.
  - Provides execution playbooks with prerequisites, ordered steps, and prompt examples.
- **New machine-readable workflow registry**: `data/workflows.json`
  - `ship-saas-mvp`
  - `security-audit-web-app`
  - `build-ai-agent-system`
  - `qa-browser-automation`

### Changed

- **README / Onboarding docs** updated to include Workflows discovery and usage:
  - `README.md` (TOC + "Antigravity Workflows" section)
  - `docs/GETTING_STARTED.md` (Bundles vs Workflows guidance)
  - `docs/FAQ.md` (new Q&A: Bundles vs Workflows)
- **Go browser automation alignment**:
  - Workflow playbooks now include optional `@go-playwright` hooks for Go-based QA/E2E flows.
- **Registry sync** after workflow skill addition:
  - `CATALOG.md`
  - `skills_index.json`
  - `data/catalog.json`
  - `data/bundles.json`

### Contributors

- [@sickn33](https://github.com/sickn33) - Workflows architecture, docs, and release integration

---

## [4.11.0] - 2026-02-08 - "Clean Code & Registry Stability"

> Quality improvements: Clean Code principles and deterministic builds.

### Changed

- **`clean-code` skill** - Complete rewrite based on Robert C. Martin's "Clean Code":
  - Systematic coverage: Meaningful names, functions, comments, formatting, objects, error handling, unit tests, and classes
  - Added F.I.R.S.T. test principles and Law of Demeter guidance
  - Fixed invalid heading format (`## ## When to Use` → `## When to Use`) that blocked validation
  - Added implementation checklist and code smell detection
- **Registry Stabilization** - Fixed `scripts/build-catalog.js` for deterministic CI builds:
  - Uses `SOURCE_DATE_EPOCH` environment variable for reproducible timestamps
  - Replaced `localeCompare` with explicit comparator for consistent sorting across environments
  - Prevents CI validation failures caused by timestamp drift

### Contributors

- [@jackjin1997](https://github.com/jackjin1997) - Clean Code skill update and registry fixes (PR #69, forged at [ClawForge](https://github.com/jackjin1997/ClawForge))

---

## [4.10.0] - 2026-02-06 - "Composio Automation + .NET Backend"

> A major expansion focused on practical app automation and stronger backend engineering coverage.

### Added

- **79 new skills total**.
- **78 Composio/Rube automation skills** (PR #64), with operational playbooks for:
- CRM and sales stacks (`HubSpot`, `Pipedrive`, `Salesforce`, `Zoho CRM`, `Close`).
- Collaboration and project tools (`Notion`, `ClickUp`, `Asana`, `Jira`, `Confluence`, `Trello`, `Monday`).
- Messaging and support channels (`Slack`, `Discord`, `Teams`, `Intercom`, `Freshdesk`, `Zendesk`).
- Marketing and analytics systems (`Google Analytics`, `Mixpanel`, `PostHog`, `Segment`, `Mailchimp`, `Klaviyo`).
- Infra/dev tooling (`GitHub`, `GitLab`, `CircleCI`, `Datadog`, `PagerDuty`, `Vercel`, `Render`).
- **1 new `dotnet-backend` skill** (PR #65) with:
- ASP.NET Core 8+ API patterns (Minimal APIs + controller-based).
- EF Core usage guidance, JWT auth examples, and background worker templates.
- Explicit trigger guidance and documented limitations.
- **Registry size increased to 713 skills** (from 634).

### Changed

- Regenerated and synced discovery artifacts after merging both PRs:
- `README.md` (counts + contributor updates)
- `skills_index.json`
- `CATALOG.md`
- `data/catalog.json`
- `data/bundles.json`
- `data/aliases.json`
- Release metadata updated for `v4.10.0`:
- `package.json` / `package-lock.json` version bump
- GitHub Release object published with release notes

### Contributors

- [@sohamganatra](https://github.com/sohamganatra) - 78 Composio automation skills (PR #64)
- [@Nguyen-Van-Chan](https://github.com/Nguyen-Van-Chan) - .NET backend skill (PR #65)

## [4.9.0] - 2026-02-05 - "OSS Hunter & Universal Skills"

> Automated contribution hunting and universal CLI AI skills (Audio, YouTube, Prompt Engineering).

### Added

- **New Skill**: `oss-hunter` – Automated tool for finding high-impact Open Source contributions (Good First Issues, Help Wanted) in trending repositories.
- **New Skill**: `audio-transcriber` – Transform audio recordings into professional Markdown with Whisper integration.
- **New Skill**: `youtube-summarizer` – Generate comprehensive summaries/notes from YouTube videos.
- **New Skill**: `prompt-engineer` (Enhanced) – Now includes 11 optimization frameworks (RTF, RISEN, etc.).
- **Registry**: 634 skills (from 626). Catalog regenerated.

### Changed

- **CLI AI Skills**: Merged core skills from `ericgandrade/cli-ai-skills`.

### Contributors

- [@jackjin1997](https://github.com/jackjin1997) - OSS Hunter (PR #61)
- [@ericgandrade](https://github.com/ericgandrade) - CLI AI Skills (PR #62)

## [4.7.0] - 2026-02-03 - "Installer Fix & OpenCode Docs"

> Critical installer fix for Windows and OpenCode documentation completion.

### Fixed

- **Installer**: Resolved `ReferenceError` for `tagArg` variable in `bin/install.js` ensuring correct execution on Windows/PowerShell (PR #53).

### Documentation

- **OpenCode**: Completed documentation for OpenCode integration in `README.md`.

---

## [4.6.0] - 2026-02-01 - "SPDD & Radix UI Design System"

> Agent workflow docs (SPDD) and Radix UI design system skill.

### Added

- **New Skill**: `radix-ui-design-system` – Build accessible design systems with Radix UI primitives (headless, theming, WCAG, examples).
- **Docs**: `skills/SPDD/` – Research, spec, and implementation workflow docs (1-research.md, 2-spec.md, 3-implementation.md).

### Registry

- **Total Skills**: 626 (from 625). Catalog regenerated.

---

## [4.5.0] - 2026-01-31 - "Stitch UI Design"

> Expert prompting guide for Google Stitch AI-powered UI design tool.

### Added

- **New Skill**: `stitch-ui-design` – Expert guide for creating effective prompts for Google Stitch AI UI design tool (Gemini 2.5 Flash). Covers prompt structure, specificity techniques, iteration strategies, design-to-code workflows, and 10+ examples for landing pages, mobile apps, and dashboards.

### Changed

- **Documentation**: Clarified in README.md and GETTING_STARTED.md that installation means cloning the full repo once; Starter Packs are curated lists to discover skills by role, not a different installation method (fixes [#44](https://github.com/sickn33/antigravity-awesome-skills/issues/44)).

### Registry

- **Total Skills**: 625 (from 624). Catalog regenerated.

### Credits

- [@ALEKGG1](https://github.com/ALEKGG1) – stitch-ui-design (PR #45)
- [@CypherPoet](https://github.com/CypherPoet) – Documentation clarity (#44)

---

## [4.4.0] - 2026-01-30 - "fp-ts skills for TypeScript"

> Three practical fp-ts skills for TypeScript functional programming.

### Added

- **New Skills** (from [whatiskadudoing/fp-ts-skills](https://github.com/whatiskadudoing/fp-ts-skills)):
  - `fp-ts-pragmatic` – Pipe, Option, Either, TaskEither without academic jargon.
  - `fp-ts-react` – Patterns for fp-ts with React 18/19 and Next.js 14/15 (state, forms, data fetching).
  - `fp-ts-errors` – Type-safe error handling with Either and TaskEither.

### Registry

- **Total Skills**: 624 (from 621). Catalog regenerated.

---

## [4.3.0] - 2026-01-29 - "VoltAgent Integration & Context Engineering Suite"

> 61 new skills from VoltAgent/awesome-agent-skills: official team skills and context engineering suite.

### Added

- **61 new skills** from [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills):
  - **Official (27)**: Sentry (commit, create-pr, find-bugs, iterate-pr), Trail of Bits (culture-index, fix-review, sharp-edges), Expo (expo-deployment, upgrading-expo), Hugging Face (hugging-face-cli, hugging-face-jobs), Vercel, Google Stitch (design-md), Neon (using-neon), n8n (n8n-code-python, n8n-mcp-tools-expert, n8n-node-configuration), SwiftUI, fal.ai (fal-audio, fal-generate, fal-image-edit, fal-platform, fal-upscale, fal-workflow), deep-research, imagen, readme.
  - **Community (34)**: Context suite (context-fundamentals, context-degradation, context-compression, context-optimization, multi-agent-patterns, memory-systems, evaluation), frontend-slides, linear-claude-skill, skill-rails-upgrade, terraform-skill, tool-design, screenshots, automate-whatsapp, observe-whatsapp, aws-skills, ui-skills, vexor, pypict-skill, makepad-skills, threejs-skills, claude-scientific-skills, claude-win11-speckit-update-skill, security-bluebook-builder, claude-ally-health, clarity-gate, beautiful-prose, claude-speed-reader, skill-seekers, varlock-claude-skill, superpowers-lab, nanobanana-ppt-skills, x-article-publisher-skill, ffuf-claude-skill.

### Registry

- **Total Skills**: 614 (from 553). Catalog and SOURCES.md updated.

### Credits

- VoltAgent/awesome-agent-skills and official teams (Sentry, Trail of Bits, Expo, Hugging Face, Vercel Labs, Google Labs, Neon, fal.ai).

---

## [4.0.0] - 2026-01-28 - "The Enterprise Era"

> **A massive integration of 300+ Enterprise skills, transforming Antigravity into a complete operating system for AI agents.**

### Added

- **Massive Skill Injection**: Merged 300+ Enterprise skills from `rmyndharis/antigravity-skills`.
- **New Categories**:
  - **Architecture & Design**: `backend-architect`, `c4-architecture`.
  - **Data & AI**: `rag-engineer`, `langchain-architecture`.
  - **Security**: `security-auditor`, `cloud-pentesting`.
- **Catalog System**: Introduced `CATALOG.md` and `scripts/build-catalog.js` for automated, table-based skill discovery.

### Changed

- **Documentation Overhaul**:
  - Removed the legacy 250+ row skill table from `README.md`.
  - Restructured `README.md` to focus on high-level domains.
  - Replaced static registry with dynamic `CATALOG.md`.
- **Version Bump**: Major version update to 4.0.0 reflecting the doubling of skill capacity (247 -> 550+).

### Credits

- **[@rmyndharis](https://github.com/rmyndharis)** - For the massive contribution of 300+ Enterprise skills and valid catalog logic.
- **[@sstklen](https://github.com/sstklen)** & **[@rookie-ricardo](https://github.com/rookie-ricard)** - Continued community support.

## [3.4.0] - 2026-01-27 - "Voice Intelligence & Categorization"

### Added

- **New Skill**: `voice-ai-engine-development` - Complete toolkit for building real-time voice agents (OpenAI Realtime, Vapi, Deepgram, ElevenLabs).
- **Categorization**: Major README update introducing a concise "Features & Categories" summary table.

### Changed

- **README**: Replaced text-heavy category lists with a high-level summary table.
- **Registry**: Synced generic skill count (256) across documentation.

### Contributors

- [@sickn33](https://github.com/sickn33) - Voice AI Engine (PR #33)
- [@community](https://github.com/community) - Categorization Initiative (PR #32)

## [3.3.0] - 2026-01-26 - "News & Research"

### Added

- **New Skills**:
  - `last30days`: Research any topic from the last 30 days on Reddit + X + Web.
  - `daily-news-report`: Generate daily news reports from multiple sources.

### Changed

- **Registry**: Updated `skills_index.json` and `README.md` registry (Total: 255 skills).

## [3.2.0] - 2026-01-26 - "Clarity & Consistency"

### Changed

- **Skills Refactoring**: Significant overhaul of `backend-dev-guidelines`, `frontend-design`, `frontend-dev-guidelines`, and `mobile-design`.
  - **Consolidation**: Merged fragmented documentation into single, authoritative `SKILL.md` files.
  - **Final Laws**: Introduced "Final Laws" sections to provide strict, non-negotiable decision frameworks.
  - **Simplification**: Removed external file dependencies to improve context retrieval for AI agents.

### Fixed

- **Validation**: Fixed critical YAML frontmatter formatting issues in `seo-fundamentals`, `programmatic-seo`, and `schema-markup` that were blocking strict validation.
- **Merge Conflicts**: Resolved text artifact conflicts in SEO skills.

## [3.1.0] - 2026-01-26 - "Stable & Deterministic"

### Fixed

- **CI/CD Drift**: Resolved persistent "Uncommitted Changes" errors in CI by making the index generation script deterministic (sorting by name + ID).
- **Registry Sync**: Synced `README.md` and `skills_index.json` to accurately reflect all 253 skills.

### Added (Registry Restore)

The following skills are now correctly indexed and visible in the registry:

- **Marketing & Growth**: `programmatic-seo`, `schema-markup`, `seo-fundamentals`, `form-cro`, `popup-cro`, `analytics-tracking`.
- **Security**: `windows-privilege-escalation`, `wireshark-analysis`, `wordpress-penetration-testing`, `writing-plans`.
- **Development**: `tdd-workflow`, `web-performance-optimization`, `webapp-testing`, `workflow-automation`, `zapier-make-patterns`.
- **Maker Tools**: `telegram-bot-builder`, `telegram-mini-app`, `viral-generator-builder`.

### Changed

- **Documentation**: Added `docs/CI_DRIFT_FIX.md` as a canonical reference for resolving drift issues.
- **Guidance**: Updated `docs/GETTING_STARTED.md` counts to match the full registry (253+ skills).
- **Maintenance**: Updated `MAINTENANCE.md` with strict protocols for handling generated files.

## [3.0.0] - 2026-01-25 - "The Governance Update"

### Added

- **Governance & Security**:
  - `docs/QUALITY_BAR.md`: Defined 5-point validation standard (Metadata, Risk, Triggers).
  - `docs/SECURITY_GUARDRAILS.md`: Enforced "Authorized Use Only" for offensive skills.
  - `CODE_OF_CONDUCT.md`: Adhered to Contributor Covenant v2.1.
- **Automation**:
  - `scripts/validate_skills.py`: Automated Quality Bar enforcement (Soft Mode supported).
  - `.github/workflows/ci.yml`: Automated PR checks.
  - `scripts/generate_index.py`: Registry generation with Risk & Source columns.
- **Experience**:
  - `docs/BUNDLES.md`: 9 Starter Packs (Essentials, Security, Web, Agent, Game Dev, DevOps, Data, Testing, Creative).
  - **Interactive Registry**: README now features Risk Levels (🔴/🟢/🟣) and Collections.
- **Documentation**:
  - `docs/EXAMPLES.md`: Cookbook with 3 real-world scenarios.
  - `docs/SOURCES.md`: Legal ledger for attributions and licenses.
  - Release announcements are documented in this CHANGELOG.

### Changed

- **Standardization**: All 250+ skills are now validated against the new Quality Bar schema.
- **Project Structure**: Introduced `docs/` folder for scalable documentation.

## [2.14.0] - 2026-01-25 - "Web Intelligence & Windows"

### Added

- **New Skill**:
  - `context7-auto-research`: Auto-research capability for Claude Code.
  - `codex-review`: Professional code review with AI integration.
  - `exa-search`: Semantic search and discovery using Exa API.
  - `firecrawl-scraper`: Deep web scraping and PDF parsing.
  - `tavily-web`: Content extraction and research using Tavily.
  - `busybox-on-windows`: UNIX tool suite for Windows environments.

### Changed

- **Documentation**: Updated `obsidian-clipper-template-creator` docs and templates.
- **Index & Registry**: Updated `skills_index.json` and `README.md` registry.

### Fixed

- **Skills**: Fixed YAML frontmatter quoting in `lint-and-validate`.

## [2.13.0] - 2026-01-24 - "NoSQL Expert"

### Added

- **New Skill**:
  - `nosql-expert`: Expert guidance for distributed NoSQL databases (Cassandra, DynamoDB), focusing on query-first modeling and anti-patterns.

### Changed

- **Index & Registry**: Updated `skills_index.json` and `README.md` registry.

### Contributors

- [@sickn33](https://github.com/sickn33) - PR #23

## [2.12.0] - 2026-01-23 - "Enterprise & UI Power"

### Added

- **New Skills**:
  - `production-code-audit`: Comprehensive enterprise auditing skill for production readiness.
  - `avalonia-layout-zafiro`: Zafiro layout guidelines for Avalonia UI.
  - `avalonia-viewmodels-zafiro`: ViewModel composition patterns for Avalonia.
  - `avalonia-zafiro-development`: Core development rules for Avalonia Zafiro applications.

### Changed

- **Index & Registry**: Updated `skills_index.json` and `README.md` registry (Total: 243 skills).

### Contributors

- [@SuperJMN](https://github.com/SuperJMN) - PR #20
- [@Mohammad-Faiz-Cloud-Engineer](https://github.com/Mohammad-Faiz-Cloud-Engineer) - PR #21

## [2.11.0] - 2026-01-23 - "Postgres Performance"

### Added

- **New Skill**:
  - `postgres-best-practices`: Comprehensive Supabase PostgreSQL performance optimization guide with 30+ rules covering query performance, connection management, RLS security, schema design, locking, and monitoring.

### Changed

- **Official Sources**: Added [supabase/agent-skills](https://github.com/supabase/agent-skills) to Credits & Sources.
- **Index & Registry**: Updated `skills_index.json` and `README.md` registry (Total: 239 skills).

### Contributors

- [@ar27111994](https://github.com/ar27111994) - PR #19

---

## [2.10.0] - 2026-01-22 - "Developer Excellence"

### Added

- **New Skills**:
  - `api-security-best-practices`: Comprehensive guide for secure API design and defense.
  - `environment-setup-guide`: Systematic approach to project onboarding and tool configuration.
  - `web-performance-optimization`: Methodologies for optimizing Core Web Vitals and loading speed.

### Changed

- **Enhanced Skill**:
  - `code-review-checklist`: Replaced with a much more detailed and systematic version covering functionality, security, and quality.

### Fixed

- **Index & Registry**: Updated `skills_index.json` and `README.md` registry (Total: 238 skills).

### Added

- **Automation Support**:
  - `scripts/update_readme.py`: Automated script to sync skill counts and regenerate the registry table.
  - Updated `MAINTENANCE.md` to reflect the new automated workflow.
- **Repository Quality**:
  - `MAINTENANCE.md` is now tracked in the repository (removed from `.gitignore`).
  - Improved contribution guidelines.

## [2.8.0] - 2026-01-22 - "Documentation Power"

### Added

- **API Documentation Generator**: New skill to automatically generate comprehensive API documentation (`skills/api-documentation-generator`).
- **Remotion Best Practices**: 28 modular rules for programmatic video creation (`skills/remotion-best-practices`).

## [2.7.0] - 2026-01-22 - "Agent Memory"

### Added

- **Agent Memory MCP**: New skill providing persistent, searchable knowledge management for AI agents (`skills/agent-memory-mcp`).

### Changed

- **Renamed Skill**: `agent-memory` was renamed to `agent-memory-mcp` to avoid naming conflicts.

---

## [2.6.0] - 2026-01-21 - "Everything Skills Edition"

### Added

- **8 Verified Skills** from [affaan-m/everything-claude-code](https://github.com/affaan-m/everything-claude-code):
  - `cc-skill-backend-patterns`
  - `cc-skill-clickhouse-io`
  - `cc-skill-coding-standards`
  - `cc-skill-continuous-learning`
  - `cc-skill-frontend-patterns`
  - `cc-skill-project-guidelines-example`
  - `cc-skill-security-review`
  - `cc-skill-strategic-compact`
- **Documentation**: New `docs/WALKTHROUGH.md` for import process details.

### Changed

- **Skill Cleanup**: Removed 27 unwanted agents, commands, and rules from the `everything-claude-code` import to focus strictly on skills.
- **Index**: Regenerated `skills_index.json` (Total: 233 skills).
- **Credits**: Updated README credits and registry.

## [1.0.0] - 2026-01-19 - "Marketing Edition"

### Added

- **23 Marketing & Growth skills** from [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills):
  - **CRO**: `page-cro`, `signup-flow-cro`, `onboarding-cro`, `form-cro`, `popup-cro`, `paywall-upgrade-cro`
  - **Content**: `copywriting`, `copy-editing`, `email-sequence`
  - **SEO**: `seo-audit`, `programmatic-seo`, `schema-markup`, `competitor-alternatives`
  - **Paid**: `paid-ads`, `social-content`
  - **Growth**: `referral-program`, `launch-strategy`, `free-tool-strategy`
  - **Analytics**: `ab-test-setup`, `analytics-tracking`
  - **Strategy**: `pricing-strategy`, `marketing-ideas`, `marketing-psychology`
- New "Marketing & Growth" category in Features table

### Changed

- Total skills count: **179**

---

## [0.7.0] - 2026-01-19 - "Education Edition"

### Added

- **Moodle External API Development** skill via PR #6
- Comprehensive Moodle LMS web service API development

### Changed

- Total skills count: **156**

---

## [0.6.0] - 2026-01-19 - "Vibeship Integration"

### Added

- **57 skills** from [vibeforge1111/vibeship-spawner-skills](https://github.com/vibeforge1111/vibeship-spawner-skills):
  - AI Agents category (~30 skills)
  - Integrations & APIs (~25 skills)
  - Maker Tools (~11 skills)
- Alphabetically sorted skill registry

### Changed

- Total skills count: **155**

---

## [0.5.0] - 2026-01-18 - "Agent Manager"

### Added

- **Agent Manager Skill** - Multi-agent orchestration via tmux
- Major repository expansion with community contributions

### Changed

- Total skills count: **131**

---

## [0.4.0] - 2026-01-18 - "Security Fortress"

### Added

- **60+ Cybersecurity skills** from [zebbern/claude-code-guide](https://github.com/zebbern/claude-code-guide):
  - Ethical Hacking Methodology
  - Metasploit Framework
  - Burp Suite Testing
  - SQLMap, Active Directory, AWS Pentesting
  - OWASP Top 100 Vulnerabilities
  - Red Team Tools
- `claude-code-guide` skill

### Changed

- Total skills count: ~90

---

## [0.3.0] - 2026-01-17 - "First Stable Registry"

### Added

- Complete skill registry table in README
- GitHub workflow automation
- SEO optimizations

### Changed

- Total skills count: **71**

---

## [0.2.0] - 2026-01-16 - "Official Skills"

### Added

- **Official Anthropic skills** integration
- **Vercel Labs skills** integration
- BlockRun: Agent Wallet for LLM Micropayments
- 7 new skills from GitHub analysis

### Changed

- Total skills count: **~65**

---

## [0.1.0] - 2026-01-15 - "Initial Release"

### Added

- **58 core skills** aggregated from community:
  - [obra/superpowers](https://github.com/obra/superpowers) - Original Superpowers
  - [guanyang/antigravity-skills](https://github.com/guanyang/antigravity-skills) - Core extensions
  - [diet103/claude-code-infrastructure-showcase](https://github.com/diet103/claude-code-infrastructure-showcase) - Infrastructure skills
  - [ChrisWiles/claude-code-showcase](https://github.com/ChrisWiles/claude-code-showcase) - React UI patterns
  - [travisvn/awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills) - Loki Mode
  - [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) - Senior Engineering
- Universal **SKILL.md** format
- Compatibility with Claude Code, Gemini CLI, Cursor, Copilot, Antigravity

---

## Credits

See [README.md](README.md#credits--sources) for full attribution.

## License

MIT License - See [LICENSE](LICENSE) for details.
