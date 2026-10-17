# Furkan Çoban

Software Engineer — Full-Stack, Backend & Applied AI.  
BSc Computer Engineering at Bülent Ecevit University (TR) · Exchange semester at Hochschule Schmalkalden (DE, Oct 2025 – Mar 2026).

<p>
  <a href="https://cobanfurkanx.github.io"><img src="https://img.shields.io/badge/Portfolio-cobanfurkanx.github.io-111827?style=for-the-badge" alt="Portfolio" /></a>
  <a href="https://shepardai.pro"><img src="https://img.shields.io/badge/Shepard_AI-live-06b6d4?style=for-the-badge" alt="Shepard AI" /></a>
  <a href="https://guruguard.shepardai.pro"><img src="https://img.shields.io/badge/GuruGuard-live-10b981?style=for-the-badge" alt="GuruGuard" /></a>
  <a href="https://trendcatcher-shepardai.pages.dev/"><img src="https://img.shields.io/badge/TrendCatcher-demo-7c3aed?style=for-the-badge" alt="TrendCatcher demo" /></a>
</p>

## Projects

### [Shepard AI](https://shepardai.pro) — Crypto Market Intelligence SaaS
- **System:** 15-min Binance & SHA-256 deduplicated RSS ingestion, 4-provider LLM router (`Gemini`, `NVIDIA`, `OpenRouter`, `Groq`) with `Retry-After` failover, and cache-first reads on Docker PostgreSQL + Supabase.
- **Links:** [Live App](https://shepardai.pro) · [Engineering Teardown](https://cobanfurkanx.github.io/shepard-case-study/) · [Engine Repo](https://github.com/cobanfurkanx/shepard-engine)

### [GuruGuard](https://guruguard.shepardai.pro) — Instagram Claim Reviewer & Feed Filter
- **System:** Chrome MV3 extension + Cloudflare Pages/Worker + D1 SQLite. Runs D1 community lookups (23+ sourced accounts across 10 regions) → v8 deterministic text/URL rules (quote evidence, HTTPS host checks, negation suppression) → optional AI summary guarded by atomic SQLite trial/credit quotas.
- **Usage:** Browse the web directory by region/category, submit anonymous account suggestions, or load the unpacked MV3 extension for profile checks, local Shadow DOM hiding (`inert`), and native Instagram block handoff. Covered by **326 automated tests** (256 core + 70 extension).
- **Links:** [Web Directory](https://guruguard.shepardai.pro) · [Engineering Teardown](https://cobanfurkanx.github.io/guruguard-case-study/) · [Extension Repo (MIT)](https://github.com/cobanfurkanx/guruguard-extension) · [Download MV3 `.zip`](https://guruguard.shepardai.pro/guruguard-extension.zip)

### [TrendCatcher](https://trendcatcher-shepardai.pages.dev/) — Product Research Desk
- **System:** Tracks emerging software products and turns them into sourced market notes and scoped MVP plans.
- **Links:** [Live Demo](https://trendcatcher-shepardai.pages.dev/) · [Source](https://github.com/cobanfurkanx/trend-arbitrage-radar)

## Open Source Contributions

### Merged
- **[`Adyen/adyen-node-api-library#1796`](https://github.com/Adyen/adyen-node-api-library/pull/1796)** — `TerminalCloudAPI` endpoint configuration validation and unit tests (Node 18/20/22).

### Open / Under Review
- **[`Adyen/adyen-dotnet-api-library#1885`](https://github.com/Adyen/adyen-dotnet-api-library/pull/1885)** — `bool` and `Guid` null guards in OpenAPI `JsonConverter.mustache` across 25 generated models in 9 APIs (68 new tests).
- **[`Adyen/adyen-python-api-library#511`](https://github.com/Adyen/adyen-python-api-library/pull/511)** — PAL service URL version handling in `_set_url_version` with unit tests.
- **[`apify/apify-sdk-python#1194`](https://github.com/apify/apify-sdk-python/pull/1194)** — Deprecated `exit_code` and `status_message` in `Actor.__init__` with warnings and tests.
- **[`ScaDS/KGpipe#23`](https://github.com/ScaDS/KGpipe/pull/23)** — Lazy-loaded `torch`, `transformers`, and `sentence_transformers` imports in core and task modules.
- **[`TIBHannover/eln-smw-adapter#4`](https://github.com/TIBHannover/eln-smw-adapter/pull/4), [`ckanext-multiuploader#14`](https://github.com/TIBHannover/ckanext-multiuploader/pull/14), [`#15`](https://github.com/TIBHannover/ckanext-multiuploader/pull/15)** — Empty SMW `ask` response handling in `specimen_exists` and CKAN controller unit tests.
- **[`gooddata/gooddata-python-sdk#1865`](https://github.com/gooddata/gooddata-python-sdk/pull/1865)** — Updated `gooddata-eval` skill tracking to read `set_skills` tool results.
- **[`iyzico/iyzipay-python#108`](https://github.com/iyzico/iyzipay-python/pull/108)** — Constant-time `hmac.compare_digest` signature verification and thread-safe per-request headers.
- **[`craftgate/craftgate-python-client#49`](https://github.com/craftgate/craftgate-python-client/pull/49)** — Fixed webhook HMAC verification for Python 3.11+ `Enum` formatting.
- **[`Trendyol/gurubu#446`](https://github.com/Trendyol/gurubu/pull/446), [`Trendyol/transmission#70`](https://github.com/Trendyol/transmission/pull/70)** — `GroomingType` enum refactor and RenovateBot dependency config.

## Stack

- **Languages:** Python, TypeScript, JavaScript, SQL (PostgreSQL / SQLite), C#, Java, C/C++
- **Backend & Edge:** FastAPI, Celery, Cloudflare Workers & D1, Supabase (PostgreSQL / PostgREST), Node.js, Docker
- **Frontend & Client:** React, Next.js, Chrome Extensions (Manifest V3 / Shadow DOM), Tailwind CSS

## Contact

[cobanfurkanx.github.io](https://cobanfurkanx.github.io/) · [linkedin.com/in/furkancoban1337](https://linkedin.com/in/furkancoban1337) · [furkancobanbusiness@gmail.com](mailto:furkancobanbusiness@gmail.com)
