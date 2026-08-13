---
layout: page
title: Groups
permalink: /groups/
---

# Affiliations

Research and engineering groups I work within — one academic, one open-source.

---

## Intelligent Computer Systems Research Institute

<p>
  <img src="https://img.shields.io/badge/role-Research%20Fellow-blue.svg" alt="Research Fellow">
  <img src="https://img.shields.io/badge/University%20of%20Miami-005030.svg" alt="University of Miami">
</p>

Approaching its 40th anniversary, ICSRI assembles researchers across machine learning, neuro-symbolic AI, platforms, personalized medicine, and AI ethics, advancing theoretical and computational work while probing the behavioral dynamics of how people interact with intelligent systems. As a center of excellence within the University of Miami Herbert Business School, it conducts and disseminates leading-edge research, advises industry and policymakers, and convenes conferences and workshops for the wider community.

**My work there** sits on the machine-learning-for-economics side: neural state-space architectures for non-stationary time series, and the interpretability question of what a learned spectral decomposition actually tells you about a regime change. The NS-SDN line of papers is the primary output.

[Institute page](https://www.herbert.miami.edu/faculty-research/research-labs-centers-institutes/icsri/index.html)

**Output**

| Work | Type | Status |
|---|---|---|
| Non-Stationary Spectral Decomposition Network: Adaptive Spectral Emission Heads and Frequency Modulation | Paper | Under review |
| [Non-Stationary Spectral Decomposition Network for Econometric Time Series Forecasting](https://journals.flvc.org/FLAIRS/article/view/141588) | Paper | FLAIRS-39, 2026 |
| [`ns-sdn`](https://github.com/nikhilxsunder/ns-sdn) — neural architecture for decomposing non-stationary time series into interpretable trend and spectral components | Software | In development |

---

## toros-dev

<p>
  <img src="https://img.shields.io/badge/role-Founder%20%26%20Lead%20Developer-blue.svg" alt="Founder and Lead Developer">
  <a href="https://github.com/toros-dev"><img src="https://img.shields.io/badge/GitHub-toros--dev-181717.svg?logo=github&logoColor=white" alt="toros-dev on GitHub"></a>
</p>

toros-dev is a research-oriented engineering group building high-quality, open-source infrastructure for the acquisition, transformation, and analysis of financial disclosure data, with an emphasis on reliable, reproducible, model-ready systems spanning structured extraction, XBRL parsing, and the reconstruction of consistent financial time series across filings, companies, and reporting regimes.

Its flagship project, **toros**, is a modular Python toolkit that represents complex financial objects as first-class typed structures behind a clean, extensible dataframe interface — emphasizing deterministic pipelines, robust API and SDK design, cross-filing normalization and entity resolution, and integration with modern data workflows including pandas, polars, and dask. Surrounding it is a set of source-specific acquisition libraries, beginning with **edgar-sec**, a client for the SEC EDGAR API that handles retrieval, rate limiting, and parsing.

**My role** is founder and lead developer: I set the architecture, own the public API surface across the stack, and maintain the release and distribution pipeline. The group's philosophy is grounded in research-grade software engineering — combining econometrics, machine learning, and systems design to produce tools suitable for both academic research and production analytics.

[Organization](https://github.com/toros-dev)

**Output**

| Project | Role in the stack | Status |
|---|---|---|
| [`toros`](https://github.com/toros-dev/toros) — DataFrame extension for representing complex financial objects | Representation | In development |
| [`edgar-sec`](https://github.com/toros-dev/edgar-sec) — Python client for the SEC EDGAR API | Acquisition | Released |

[Full project detail →](/development/)