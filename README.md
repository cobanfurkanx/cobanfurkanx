# Furkan Çoban

> Software & Applied AI Engineer building production web systems, auditable browser extensions, and resilient data pipelines.

I build complete products with verified operational boundaries—not throwaway demos—and contribute upstream to open-source SDKs and research infrastructure. I currently build **[Shepard AI](https://shepardai.pro)** (live crypto market-intelligence SaaS), **[GuruGuard](https://guruguard.shepardai.pro)** (auditable Chrome Manifest V3 extension & Cloudflare D1 directory for inspecting public Instagram marketing claims), and **[TrendCatcher](https://trendcatcher-shepardai.pages.dev/)**.

<p>
  <a href="https://cobanfurkanx.github.io"><img src="https://img.shields.io/badge/Portfolio-cobanfurkanx.github.io-111827?style=for-the-badge" alt="Portfolio" /></a>
  <a href="https://shepardai.pro"><img src="https://img.shields.io/badge/Shepard_AI-live-06b6d4?style=for-the-badge" alt="Shepard AI" /></a>
  <a href="https://guruguard.shepardai.pro"><img src="https://img.shields.io/badge/GuruGuard-live-10b981?style=for-the-badge" alt="GuruGuard" /></a>
  <a href="https://trendcatcher-shepardai.pages.dev/"><img src="https://img.shields.io/badge/TrendCatcher-demo-7c3aed?style=for-the-badge" alt="TrendCatcher demo" /></a>
</p>

## About me

- **BSc Computer Engineering**, Bülent Ecevit University, Türkiye (2024 — present)
- **Exchange Semester in Computer Science (Informatik)**, Hochschule Schmalkalden, Germany (Oct 2025 — Mar 2026, Erasmus+ EU Grant recipient)
- Focused on **backend & edge systems**, **applied AI with deterministic guardrails**, and **product engineering**
- Open to **software engineering roles**, **technical collaborations**, and **full-time summer/autumn internships**

## Selected projects & engineering teardowns

### 1. [Shepard AI](https://shepardai.pro) — Crypto Market Intelligence SaaS
Live platform that turns noisy crypto market feeds into readable bullish, bearish, and neutral sentiment with calibrated directional signals.
- **Architecture:** Separates 15-minute scheduled market/RSS ingestion (with 24-hex SHA-256 RSS deduplication) from cache-first dashboard reads across Docker PostgreSQL (PostgREST gateway, covering B-tree indexes) and Supabase Auth, paired with a multi-provider free LLM router (`Gemini`, `NVIDIA`, `OpenRouter`, `Groq`) with `Retry-After` cooldown recovery.
- **Links:** [Live Product](https://shepardai.pro) · [Engineering Teardown](https://cobanfurkanx.github.io/shepard-case-study/) · [Python Engine (`shepard-engine`)](https://github.com/cobanfurkanx/shepard-engine)

### 2. [GuruGuard](https://guruguard.shepardai.pro) — Auditable Instagram Claim Reviewer & Feed Filter
Chrome Manifest V3 extension and Cloudflare Pages + D1 platform for inspecting public Instagram marketing claims, browsing source-linked community discussions (23+ curated accounts across 10 regions), and hiding or blocking unwanted accounts.
- **Architecture:** Split between a private core (`Cloudflare Pages/Worker`, `D1 SQLite`, memory-only admin moderation, Creem webhook ledger) and a standalone MIT-licensed public extension (`guruguard-extension`). Runs a 3-stage pipeline: D1 community directory lookup → deterministic v8 text & URL rules (`marketing-policy.json` with verbatim quote evidence, HTTPS lookalike host rejection, and negation/warning suppression) → optional AI explanation guarded by an atomic 30-day free trial (5 checks/UTC day) and D1 credit ledger.
- **Usage:** Browse the keyset-paginated web directory by region/category, submit anonymous 2-field account suggestions, or load the unpacked MV3 extension in Chrome for automatic profile checks, reversible Shadow DOM hiding (`inert`, up to 500 local handles), and native Instagram block confirmation handoff. Verified by **256 core tests + 70 standalone extension tests** and full-history Gitleaks CI.
- **Links:** [Live Web Directory](https://guruguard.shepardai.pro) · [Engineering Teardown](https://cobanfurkanx.github.io/guruguard-case-study/) · [Public Extension Source (MIT)](https://github.com/cobanfurkanx/guruguard-extension) · [Download MV3 (`.zip`)](https://guruguard.shepardai.pro/guruguard-extension.zip)

### 3. [TrendCatcher](https://trendcatcher-shepardai.pages.dev/) — Builder Research Desk
Research desk for discovering emerging products abroad and translating them into sourced insights and scoped MVP plans for the Turkish market.
- **Links:** [Live Demo](https://trendcatcher-shepardai.pages.dev/) · [Source Code](https://github.com/cobanfurkanx/trend-arbitrage-radar)

## Open-source & security contributions

### Merged
- **Adyen Node.js SDK (`Adyen/adyen-node-api-library`):** [PR #1796](https://github.com/Adyen/adyen-node-api-library/pull/1796) *(Merged Oct 15, 2026)* — Added missing endpoint configuration validation for `TerminalCloudAPI` and unit regression tests across Node 18/20/22 CI.

### Open / Under Review
- **Adyen .NET SDK (`Adyen/adyen-dotnet-api-library`):** [PR #1885](https://github.com/Adyen/adyen-dotnet-api-library/pull/1885) — Added required `bool` and `Guid` null guards in OpenAPI `JsonConverter.mustache` templates across 25 generated models in 9 APIs (68 new regression tests, 981/981 unit tests passing).
- **Adyen Python SDK (`Adyen/adyen-python-api-library`):** [PR #511](https://github.com/Adyen/adyen-python-api-library/pull/511) — Added PAL-based service URL version handling in `_set_url_version` (#474) with unit tests.
- **Apify Python SDK (`apify/apify-sdk-python`):** [PR #1194](https://github.com/apify/apify-sdk-python/pull/1194) — Deprecated `exit_code` and `status_message` in the `Actor` constructor with deprecation warnings and regression tests.
- **ScaDS.AI KGpipe (`ScaDS/KGpipe`):** [PR #23](https://github.com/ScaDS/KGpipe/pull/23) — Lazy-loaded heavy ML dependencies (`torch`, `transformers`, `sentence_transformers`) in core and task modules.
- **TIB Hannover (`TIBHannover/eln-smw-adapter` & `ckanext-multiuploader`):** [PR #4](https://github.com/TIBHannover/eln-smw-adapter/pull/4), [PR #14](https://github.com/TIBHannover/ckanext-multiuploader/pull/14), [PR #15](https://github.com/TIBHannover/ckanext-multiuploader/pull/15) — Handled empty SMW `ask` query results in `specimen_exists` and added unit test suites for CKAN controller helpers and redirect branches.
- **GoodData Python SDK (`gooddata/gooddata-python-sdk`):** [PR #1865](https://github.com/gooddata/gooddata-python-sdk/pull/1865) — Updated `gooddata-eval` skill tracking to read `set_skills` tool results rather than requested arguments.
- **iyzico Python SDK (`iyzico/iyzipay-python`):** [PR #108](https://github.com/iyzico/iyzipay-python/pull/108) — Proposed constant-time `hmac.compare_digest` signature verification, boolean return values, and thread-safe per-request headers.
- **Craftgate Python SDK (`craftgate/craftgate-python-client`):** [PR #49](https://github.com/craftgate/craftgate-python-client/pull/49) — Fixed webhook HMAC signature verification for Python 3.11+ `Enum` formatting and added CI test coverage.
- **Trendyol (`Trendyol/gurubu` & `Trendyol/transmission`):** [PR #446](https://github.com/Trendyol/gurubu/pull/446), [PR #70](https://github.com/Trendyol/transmission/pull/70) — Replaced room-creation magic numbers with `GroomingType` enums and configured RenovateBot dependency automation.

## Technical stack

- **Languages:** Python, TypeScript, JavaScript, SQL (PostgreSQL / SQLite), C#, Java, C/C++, R
- **Backend, Edge & Data:** FastAPI, Celery, Cloudflare Workers & D1 (SQLite), Supabase (PostgreSQL / PostgREST), Node.js, Flask
- **Frontend & Client:** React, Next.js, Chrome Extensions (Manifest V3 / Shadow DOM), Tailwind CSS
- **AI & Verification:** Multi-provider LLM routing (Gemini, OpenRouter, NVIDIA, Groq), Vitest/Pytest, GitHub Actions CI, Docker, Gitleaks

## Contact

- **Portfolio:** [cobanfurkanx.github.io](https://cobanfurkanx.github.io/)
- **LinkedIn:** [linkedin.com/in/furkancoban1337](https://linkedin.com/in/furkancoban1337)
- **Email:** [furkancobanbusiness@gmail.com](mailto:furkancobanbusiness@gmail.com)
