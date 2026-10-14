---
layout: page
title: Development
permalink: /development/
---

Open-source Python infrastructure for computational economics, built as one stack: acquisition libraries pull from primary sources, representation layers give the data typed structure, and modeling libraries sit on top. Each package is independently useful and released to the same standard — full type coverage, sync/async parity where there is I/O, defensive validation, documentation generated from doctested docstrings, signed releases, and archived versions with citable DOIs.

| Layer | Project | Status |
|---|---|---|
| Acquisition | [`fedfred`](#fedfred) — Federal Reserve data | Released (3.0.0)|
| Acquisition | [`edgar-sec`](#edgar-sec) — SEC EDGAR filings | Released (2.0.1) |
| Representation | [`toros`](#toros) — self-validating financial objects | In development |
| Modeling | [`cultivars`](#cultivars) — time series econometrics | Pre-released (1.0.0a4) |
| Modeling | [`ns-sdn`](#ns-sdn) — neural spectral state space | Released (1.0.0) |
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
  <a href="https://codecov.io/gh/nikhilxsunder/cultivars"><img src="https://codecov.io/gh/nikhilxsunder/cultivars/graph/badge.svg?token=59TQ2HO8BW" alt="Coverage"></a>
  <a href="https://pypi.org/project/cultivars/"><img src="https://img.shields.io/pypi/v/cultivars.svg?include_prereleases" alt="PyPI version"></a>
  <a href="https://pypi.org/project/cultivars/"><img src="https://img.shields.io/pypi/pyversions/cultivars.svg" alt="Python versions"></a>
  <a href="https://github.com/nikhilxsunder/cultivars/blob/main/LICENSE"><img src="https://img.shields.io/pypi/l/cultivars.svg" alt="License"></a>
  <a href="https://pepy.tech/projects/cultivars"><img src="https://static.pepy.tech/badge/cultivars" alt="PyPI Downloads"></a>
  <a href="https://repology.org/project/python%3Acultivars/versions"><img src="https://repology.org/badge/tiny-repos/python%3Acultivars.svg" alt="Repology"></a>
  <a href="https://doi.org/10.5281/zenodo.23028870"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.23028870.svg" alt="DOI"></a>
</p>

> **Research-grade time series econometrics for Python: ARIMA to state space, VAR to structural identification, Bayesian and spectral methods, on one estimation surface.**

cultivars is a single, typed, dependency-light library for the econometric time-series toolkit, written so that a research result can be reproduced from the summary it prints. Every model is a class holding a specification; `fit()` (or `identify()`) returns an immutable record that renders the same way everywhere, carries its own diagnostics, and refuses to report what its assumptions do not support. Estimation and identification are separate acts: a reduced form is fitted once and reports only what the data determine, and anything that needs an assumption — a causal ordering, a sign pattern, an instrument, a prior — is constructed from that result and restates the assumption in its own summary, so an impulse response can always be traced to what signed it.

The modeling surface is now complete across ten areas: univariate models from ARIMA and SARIMAX through the GARCH family, stochastic volatility, unobserved components and regime-switching autoregressions; reduced-form VARs, VECMs, panel, mixed-frequency and global VARs; large-dimensional Bayesian VARs with Minnesota, hierarchical and shrinkage priors, dynamic factor models and FAVAR; nonlinear, quantile and time-varying-parameter VARs with Markov switching; structural identification by recursive, long-run, sign, narrative, instrument, heteroskedasticity and non-Gaussian schemes, set-identification bounds, and perturbation-solved DSGE estimation; a linear-Gaussian state-space substrate with nonlinear and particle filters; spectral and wavelet analysis; Bayesian diagnostics and model combination; forecast evaluation; and the standard battery of unit-root, cointegration, break and stability tests. Dependencies are `numpy`, `scipy` and `fedfred`, so it reads FRED directly and forms the modeling layer of the acquisition-to-model stack above.

```shell
pip install --pre cultivars
```

[Docs](https://nikhilxsunder.github.io/cultivars/stable/) · [PyPI](https://pypi.org/project/cultivars/) · [GitHub](https://github.com/nikhilxsunder/cultivars) · [Zenodo](https://doi.org/10.5281/zenodo.23028870)

---

<h2 id="ns-sdn">ns-sdn</h2>

<div align="center">
  <img src="https://raw.githubusercontent.com/nikhilxsunder/ns-sdn/main/assets/exported/ns-sdn_banner.png" alt="ns-sdn banner">
</div>

<p align="center">
  <a href="https://codecov.io/gh/nikhilxsunder/ns-sdn"><img src="https://codecov.io/gh/nikhilxsunder/ns-sdn/graph/badge.svg" alt="Coverage"></a>
  <a href="https://pypi.org/project/ns-sdn/"><img src="https://img.shields.io/pypi/v/ns-sdn.svg" alt="PyPI version"></a>
  <a href="https://pypi.org/project/ns-sdn/"><img src="https://img.shields.io/pypi/pyversions/ns-sdn.svg" alt="Python versions"></a>
  <a href="https://github.com/nikhilxsunder/ns-sdn/blob/main/LICENSE"><img src="https://img.shields.io/pypi/l/ns-sdn.svg" alt="License"></a>
  <a href="https://pepy.tech/projects/ns-sdn"><img src="https://static.pepy.tech/badge/ns-sdn" alt="PyPI Downloads"></a>
  <a href="https://doi.org/10.5281/zenodo.23368625"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.23368625.svg" alt="DOI"></a>
  <a href="https://doi.org/10.32473/flairs.39.1.141588"><img src="https://img.shields.io/badge/FLAIRS--39-10.32473%2Fflairs.39.1.141588-blue.svg" alt="FLAIRS-39 DOI"></a>
  <a href="https://doi.org/10.1109/ORSS71174.2026.11684282"><img src="https://img.shields.io/badge/IEEE%20ORSS-10.1109%2FORSS71174.2026.11684282-blue.svg" alt="IEEE ORSS DOI"></a>
</p>

> **A neural state-space model that decomposes a non-stationary time series into a trend and a few sinusoids whose amplitude, frequency and participation move with a latent state, and reads the decomposition back as coordinates.**

ns-sdn is the Non-Stationary Spectral Decomposition Network as a stable, citable Python package. At each step a GRU latent state emits a trend and $K$ sinusoids through parallel linear heads — amplitude, instantaneous frequency, phase offset and a gate per component — and the phase integrates the frequency, so every component is a chirp the state can steer. The network is trained as a one-step predictor with drift penalties on the amplitudes and frequencies, and read as an adaptive, state-driven spectral decomposition rather than a fixed-basis Fourier or stationary spectral model, drawing together implicit neural representations with periodic activations (SIREN), instantaneous-frequency analysis in the spirit of the Hilbert–Huang transform, and nonlinear state-space econometrics. It is the formulation of the IEEE-ORSS 2026 paper (Sunder and Leon) and the architecture introduced at FLAIRS-39, demonstrated on the 10-Year Treasury yield through the 2020 macroeconomic shock.

Version 1.0.0 freezes the API in the cultivars model-fit-result pattern: `NSSDN` is the validated specification, whose defaults reproduce the published DGS10 run to its 58,849 parameters; `fit()` returns a frozen `NSSDNResult` carrying every path the papers' figures are drawn from — trend, amplitude, frequency, phase, gate, components and latent state — on the original scale, with conditional one-step prediction and recursive forecasting; and `SpectralState` reads the decomposition as a time-local measure on the frequency axis, reporting centroid, dispersion, entropy, effective component count, Wasserstein velocity and a disentanglement score, so a regime claim such as the spectral compression around 2020 is made in coordinates that survive a refit rather than in component indices. The documentation site derives the model equation by equation, the API reference carries the mathematics in every docstring, and the example gallery includes a one-command reproduction of the ORSS experiment. Developed as fellowship research under the ICSRI Fellows Program at the University of Miami Herbert Business School; MIT-licensed, with signed releases and a Zenodo DOI per version.

Within the broader stack it supplies the nonlinear spectral state space (the NSSM formulation) that the autofed reinforcement-learning agent trains inside, serving as the nonlinear counterpart to cultivars' linear structural time-series models.

```shell
pip install ns-sdn
```

[Docs](https://nikhilxsunder.github.io/ns-sdn/stable/) · [PyPI](https://pypi.org/project/ns-sdn/) · [GitHub](https://github.com/nikhilxsunder/ns-sdn) · [Zenodo](https://doi.org/10.5281/zenodo.23368625) · [Paper (IEEE-ORSS 2026)](https://doi.org/10.1109/ORSS71174.2026.11684282) · [Paper (FLAIRS-39)](https://doi.org/10.32473/flairs.39.1.141588)

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