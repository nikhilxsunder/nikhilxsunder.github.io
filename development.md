---
layout: page
title: Development
permalink: /development/
---

Open-source Python infrastructure for computational economics, built as one stack: acquisition libraries pull from primary sources, representation layers give the data typed structure, and modeling libraries sit on top. Each package is independently useful and released to the same standard — full type coverage, sync/async parity, defensive validation, and archived releases with citable DOIs.

| Layer | Project | Status |
|---|---|---|
| Acquisition | [`fedfred`](#fedfred) — Federal Reserve data | Released |
| Acquisition | [`edgar-sec`](#edgar-sec) — SEC EDGAR filings | Released |
| Representation | [`toros`](#toros) — self-validating financial objects | In development |
| Modeling | [`cultivars`](#cultivars) — Bayesian &amp; structural VAR | In development |
| Modeling | [`ns-sdn`](#ns-sdn) — neural spectral state space | In development |
| Application | [`autofed`](#autofed) — RL for monetary policy | Research |

---

<h2 id="fedfred">fedfred</h2>

<div align="center">
  <img src="https://raw.githubusercontent.com/nikhilxsunder/fedfred/v4-dev/docs/source/_static/fedfred_banner_transparent.png" alt="fedfred banner">
</div>

<p align="center">
  <a href="https://www.bestpractices.dev/projects/10158"><img src="https://www.bestpractices.dev/projects/10158/badge" alt="OpenSSF Best Practices"></a>
  <a href="https://codecov.io/gh/nikhilxsunder/fedfred"><img src="https://codecov.io/gh/nikhilxsunder/fedfred/graph/badge.svg?token=VVEK415DF6" alt="Coverage"></a>
  <a href="https://pypi.org/project/fedfred/"><img src="https://img.shields.io/pypi/v/fedfred.svg" alt="PyPI version"></a>
  <a href="https://pypi.org/project/fedfred/"><img src="https://img.shields.io/pypi/pyversions/fedfred.svg" alt="Python versions"></a>
  <a href="https://github.com/nikhilxsunder/fedfred/blob/main/LICENSE"><img src="https://img.shields.io/pypi/l/fedfred.svg" alt="License"></a>
  <a href="https://pepy.tech/projects/fedfred"><img src="https://static.pepy.tech/badge/fedfred" alt="PyPI Downloads"></a>
  <a href="https://anaconda.org/conda-forge/fedfred"><img src="https://anaconda.org/conda-forge/fedfred/badges/downloads.svg" alt="Conda Downloads"></a>
  <a href="https://repology.org/project/python%3Afedfred/versions"><img src="https://repology.org/badge/tiny-repos/python%3Afedfred.svg" alt="Repology"></a>
  <a href="https://doi.org/10.5281/zenodo.17635942"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.17635942.svg" alt="DOI"></a>
</p>

> **A modern Python package for interacting with the Federal Reserve Bank of St. Louis FRED, GeoFRED, ALFRED, and FRASER APIs.**

fedfred is a feature-rich Python client for the Federal Reserve Economic Data (FRED) API, designed to make working with economic time series ergonomic and production-ready. It provides full coverage of the FRED, ALFRED, and GeoFRED/Maps endpoints behind a clean, typed interface, with first-class support for returning data as pandas, polars, or dask objects — and GeoDataFrames for geospatial series. Built for serious use, it includes both synchronous and asynchronous clients, built-in rate limiting and caching to respect API limits, and defensive type-safe handling of responses, making it suitable for everything from interactive research notebooks to automated data pipelines.

```shell
pip install fedfred
```

[Docs](https://nikhilxsunder.github.io/fedfred/) · [PyPI](https://pypi.org/project/fedfred/) · [conda-forge](https://anaconda.org/conda-forge/fedfred) · [GitHub](https://github.com/nikhilxsunder/fedfred)

---

<h2 id="edgar-sec">edgar-sec</h2>

<div align="center">
  <img src="https://raw.githubusercontent.com/toros-dev/edgar-sec/main/assets/exported/edgar-sec_banner.png" alt="edgar-sec banner">
</div>

<p align="center">
  <a href="https://www.bestpractices.dev/projects/10210"><img src="https://www.bestpractices.dev/projects/10210/badge" alt="OpenSSF Best Practices"></a>
  <a href="https://codecov.io/gh/toros-dev/edgar-sec"><img src="https://codecov.io/gh/toros-dev/edgar-sec/graph/badge.svg" alt="Coverage"></a>
  <a href="https://pypi.org/project/edgar-sec/"><img src="https://img.shields.io/pypi/v/edgar-sec.svg" alt="PyPI version"></a>
  <a href="https://pypi.org/project/edgar-sec/"><img src="https://img.shields.io/pypi/pyversions/edgar-sec.svg" alt="Python versions"></a>
  <a href="https://github.com/toros-dev/edgar-sec/blob/main/LICENSE"><img src="https://img.shields.io/pypi/l/edgar-sec.svg" alt="License"></a>
  <a href="https://pepy.tech/projects/edgar-sec"><img src="https://static.pepy.tech/badge/edgar-sec" alt="PyPI Downloads"></a>
  <a href="https://anaconda.org/conda-forge/edgar-sec"><img src="https://anaconda.org/conda-forge/edgar-sec/badges/downloads.svg" alt="Conda Downloads"></a>
  <a href="https://repology.org/project/python%3Aedgar-sec/versions"><img src="https://repology.org/badge/tiny-repos/python%3Aedgar-sec.svg" alt="Repology"></a>
</p>

> **A feature-rich Python package for interacting with the US Securities and Exchange Commission API: EDGAR.**

edgar-sec is a research-grade, fully-typed Python SDK for the entire SEC EDGAR REST API — the structural twin of fedfred for federal securities-disclosure data. It provides ergonomic, discoverable access to the full endpoint surface (submissions, company concepts, company facts, frames, and CIK/ticker resolution) through a small public front door, with every response returned as a typed dataclass rather than a raw dict for IDE autocomplete and mypy safety. Built to the same quality bar as its sibling, it offers strict parity between synchronous and asynchronous clients, a built-in rate limiter that respects EDGAR's fair-access rules, optional local caching, and defensive type-safe handling of responses throughout.

Currently in redevelopment as the acquisition layer of the toros stack, feeding filings into `toros` for structured representation.

```shell
pip install edgar-sec
```

[Docs](https://toros-dev.github.io/edgar-sec/) · [PyPI](https://pypi.org/project/edgar-sec/) · [conda-forge](https://anaconda.org/conda-forge/edgar-sec) · [GitHub](https://github.com/toros-dev/edgar-sec)

---

<h2 id="toros">toros</h2>

<div align="center">
  <img src="https://raw.githubusercontent.com/toros-dev/toros/main/assets/exported/toros_banner.png" alt="toros banner">
</div>

<p align="center">
  <img src="https://img.shields.io/badge/status-in%20development-orange.svg" alt="Status: in development">
  <a href="https://github.com/toros-dev/toros"><img src="https://img.shields.io/github/last-commit/toros-dev/toros.svg" alt="Last commit"></a>
</p>

> **A powerful DataFrame extension for representing complex financial objects.**

toros is a pandas-backed data representation library that turns SEC filing data into self-validating financial objects. It uses registered DataFrame accessors to enforce financial semantics — type, unit, period, and taxonomy constraints — directly within the pandas backend, and layers specialized frame types (such as financial-statement representations) on top through inheritance. It serves as the interactive, semantically-aware data container that edgar-sec materializes filings into, giving researchers pandas ergonomics with domain-correct structure and validation rather than raw, untyped tables.

Flagship project of [toros-dev](https://github.com/toros-dev).

[GitHub](https://github.com/toros-dev/toros)

---

<h2 id="cultivars">cultivars</h2>

<div align="center">
  <img src="https://raw.githubusercontent.com/nikhilxsunder/cultivars/main/assets/exported/cultivars_banner_transparent.png" alt="cultivars banner">
</div>

<p align="center">
  <img src="https://img.shields.io/badge/status-in%20development-orange.svg" alt="Status: in development">
  <a href="https://github.com/nikhilxsunder/cultivars"><img src="https://img.shields.io/github/last-commit/nikhilxsunder/cultivars.svg" alt="Last commit"></a>
</p>

> **A modern computing library in Python for vector autoregressions and other autoregressive economic models.**

cultivars is a research-grade Python SDK for autoregressive time-series modeling, built to cover the Bayesian and time-varying methods that existing Python tooling handles poorly or not at all. Where reduced-form VAR and ARIMA are treated as table stakes, its focus is the harder surface: Bayesian VAR at scale (Minnesota, NIW, SSVS, horseshoe, and hierarchical priors), time-varying-parameter VAR with stochastic volatility, and structural identification beyond Cholesky — sign, narrative, and proxy/IV schemes passed as composable strategy objects rather than bespoke classes.

Every model, from univariate AR through TVP-SVAR-SV, composes through a single state-space substrate and decomposes into an immutable `Spec`, a transient `Estimator`, and a serializable `Result`, giving a typed, dataclass-shaped API with consistent fit, forecast, IRF, and FEVD surfaces. Designed to integrate directly with fedfred and edgar-sec, it forms the modeling layer of a FRED-to-model-to-analysis stack that no other Python library currently offers.

[GitHub](https://github.com/nikhilxsunder/cultivars)

---

<h2 id="ns-sdn">ns-sdn</h2>

<div align="center">
  <img src="https://raw.githubusercontent.com/nikhilxsunder/ns-sdn/main/assets/exported/ns-sdn_banner.png" alt="ns-sdn banner">
</div>

<p align="center">
  <img src="https://img.shields.io/badge/status-in%20development-orange.svg" alt="Status: in development">
  <a href="https://journals.flvc.org/FLAIRS/article/view/141588"><img src="https://img.shields.io/badge/DOI-10.32473%2Fflairs.39.1.141588-blue.svg" alt="FLAIRS DOI"></a>
  <a href="https://github.com/nikhilxsunder/ns-sdn"><img src="https://img.shields.io/github/last-commit/nikhilxsunder/ns-sdn.svg" alt="Last commit"></a>
</p>

> **A modern neural architecture in Python for decomposing non-stationary time series into interpretable trend and spectral components.**

ns-sdn (Non-Stationary Spectral Decomposition Network) is a PyTorch implementation of the neural state-space architecture of the same name, packaging the model components developed across the repository's research notebooks so that the results in its companion papers are fully reproducible and the architecture is reusable beyond them.

NS-SDN represents a time series as a time-varying trend plus a sum of latent sinusoidal components whose amplitude, instantaneous frequency, phase, and a learned gating weight are emitted at each step from a recurrent latent state through parallel projection heads — an adaptive, state-driven spectral decomposition rather than a fixed-basis Fourier or stationary spectral model. It draws together implicit neural representations with periodic activations (SIREN), instantaneous-frequency analysis in the spirit of the Hilbert–Huang transform, and nonlinear state-space econometrics, and it doubles as both a conditional one-step forecaster and an interpretable neural spectral-analysis tool that exposes regime-dependent trend, amplitude, frequency, and gating dynamics — demonstrated on the 10-Year Treasury yield through the 2020 macroeconomic shock.

Within the broader stack it supplies the nonlinear spectral state space (the NSSM formulation) that the autofed reinforcement-learning agent trains inside, serving as the nonlinear counterpart to cultivars' linear structural time-series models.

[Paper (FLAIRS-39)](https://journals.flvc.org/FLAIRS/article/view/141588) · [GitHub](https://github.com/nikhilxsunder/ns-sdn)

---

<h2 id="autofed">autofed</h2>

<div align="center">
  <img src="https://raw.githubusercontent.com/erskordi/Autonomous_Fed/src/assets/exported/autofed_banner.png" alt="autofed banner">
</div>

<p align="center">
  <img src="https://img.shields.io/badge/status-research%20project-blueviolet.svg" alt="Status: research project">
</p>

> **Reinforcement learning for optimal monetary policy under model uncertainty.**

Autonomous Fed is a reinforcement learning research project that reframes monetary policy as a control problem, in which an RL agent learns the central bank's reaction function rather than having a fixed Taylor rule imposed on it. Benchmarked against Hinterlang &amp; Tänzer's Bundesbank work (Discussion Paper No. 51/2021), it replicates their RL environment and extends it by training policy agents inside two distinct economic environments — a linear one built on TVP-SVAR and a nonlinear one built on the NSSM state-space formulation that links to the NS-SDN project — then comparing learned policy behavior across both.

The aim is a clean replication-plus-extension contribution targeting *Computational Economics*, demonstrating how optimal monetary policy under uncertainty changes when the agent's model of the economy moves from linear structural dynamics to a richer nonlinear spectral state space.

[GitHub](https://github.com/erskordi/Autonomous_Fed)