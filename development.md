---
layout: page
title: Development
permalink: /development/
---

## fedfred

<div align="center">
  <img src="https://raw.githubusercontent.com/nikhilxsunder/fedfred/v4-dev/docs/source/_static/fedfred_banner_transparent.png" alt="fedfred banner">
</div>

<table>
  <tr>
    <td valign="top">
    <a href="https://github.com/nikhilxsunder/fedfred">
        <img src="https://opengraph.githubassets.com/1/nikhilxsunder/fedfred"
            alt="fedfred" width="400"
            style="width:100%; max-width:400px; height:auto;">
    </a>
    </td>
    <td valign="top">
      <table>
        <tr>
          <td><strong>Security</strong></td>
          <td><a href="https://www.bestpractices.dev/projects/10158"><img src="https://www.bestpractices.dev/projects/10158/badge" alt="Best Practices"></a></td>
        </tr>
        <tr>
          <td><strong>Coverage</strong></td>
          <td><a href="https://codecov.io/gh/nikhilxsunder/fedfred"><img src="https://codecov.io/gh/nikhilxsunder/fedfred/graph/badge.svg?token=VVEK415DF6" alt="Coverage"></a></td>
        </tr>
        <tr>
          <td><strong>Packaging</strong></td>
          <td><a href="https://repology.org/project/python%3Afedfred/versions"><img src="https://repology.org/badge/tiny-repos/python%3Afedfred.svg" alt="Repology"></a></td>
        </tr>
        <tr>
          <td><strong>License</strong></td>
          <td><a href="https://github.com/nikhilxsunder/fedfred/blob/main/LICENSE"><img src="https://img.shields.io/pypi/l/fedfred.svg" alt="License"></a></td>
        </tr>
        <tr>
          <td><strong>Usage</strong></td>
          <td>
            <a href="https://pepy.tech/projects/fedfred"><img src="https://static.pepy.tech/badge/fedfred" alt="PyPI Downloads"></a>
            <a href="https://anaconda.org/conda-forge/fedfred"><img src="https://anaconda.org/conda-forge/fedfred/badges/downloads.svg" alt="Conda Downloads"></a>
          </td>
        </tr>
        <tr>
          <td><strong>Research / Index</strong></td>
          <td><a href="https://doi.org/10.5281/zenodo.17635942"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.17635942.svg" alt="DOI"></a></td>
        </tr>
      </table>
    </td>
  </tr>
</table>

fedfred is a feature-rich Python client for the Federal Reserve Economic Data (FRED) API, designed to make working with economic time series ergonomic and production-ready. It provides full coverage of the FRED, ALFRED, and GeoFRED/Maps endpoints behind a clean, typed interface, with first-class support for returning data as pandas, polars, or dask objects (and GeoDataFrames for geospatial series). Built for serious use, it includes both synchronous and asynchronous clients, built-in rate limiting and caching to respect API limits, and defensive type-safe handling of responses, making it suitable for everything from interactive research notebooks to automated data pipelines.

```shell
pip install fedfred
```
| [Docs](https://nikhilxsunder.github.io/fedfred/) | [PyPI](https://pypi.org/project/fedfred/) | [Conda-Forge](https://anaconda.org/channels/conda-forge/packages/fedfred/overview) | [Github](https://github.com/nikhilxsunder/fedfred) |

## cultivars

<div align="center">
  <img src="https://raw.githubusercontent.com/nikhilxsunder/cultivars/main/logos/exported/cultivars_banner_transparent.png" alt="cultivars banner">
</div>

<table>
  <tr>
    <td valign="top">
    <a href="https://github.com/nikhilxsunder/cultivars">
        <img src="https://opengraph.githubassets.com/1/nikhilxsunder/cultivars"
            alt="cultivars" width="400"
            style="width:100%; max-width:400px; height:auto;">
    </a>
    </td>
    
  </tr>
</table>

cultivars is a research-grade Python SDK for autoregressive time-series modeling, built to cover the Bayesian and time-varying methods that existing Python tooling handles poorly or not at all. Where reduced-form VAR and ARIMA are treated as table stakes, its focus is the harder surface: Bayesian VAR at scale (Minnesota, NIW, SSVS, horseshoe, and hierarchical priors), time-varying-parameter VAR with stochastic volatility, and structural identification beyond Cholesky — sign, narrative, and proxy/IV schemes passed as composable strategy objects rather than bespoke classes. Every model, from univariate AR through TVP-SVAR-SV, composes through a single state-space substrate and decomposes into an immutable Spec, a transient Estimator, and a serializable Result, giving a typed, dataclass-shaped API with consistent fit, forecast, IRF, and FEVD surfaces. Designed to integrate directly with fedfred and edgar-sec, it forms the modeling layer of a FRED-to-model-to-analysis stack that no other Python library currently offers.

```shell
pip install cultivars
```

| [Docs]() | [PyPI](https://pypi.org/project/cultivars/) | [Conda-Forge]() | [Github](https://github.com/nikhilxsunder/cultivars) |

## edgar-sec

<div align="center">
  <img src="https://raw.githubusercontent.com/edgar-sec-dev-team/edgar-sec/main/assets/exported/edgar-sec_banner.png" alt="edgar-sec banner">
</div>

<table>
  <tr>
    <td valign="top">
    <a href="https://github.com/edgar-sec-dev-team/edgar-sec">
        <img src="https://opengraph.githubassets.com/1/edgar-sec-dev-team/edgar-sec"
            alt="edgar-sec" width="400"
            style="width:100%; max-width:400px; height:auto;">
    </a>
    </td>
    <td valign="top">
      <table>
        <tr>
          <td><strong>Security</strong></td>
          <td><a href="https://www.bestpractices.dev/projects/10210"><img src="https://www.bestpractices.dev/projects/10210/badge" alt="Best Practices"></a></td>
        </tr>
        <tr>
          <td><strong>Coverage</strong></td>
          <td><a href="https://codecov.io/gh/nikhilxsunder/edgar-sec"><img src="https://codecov.io/gh/nikhilxsunder/edgar-sec/graph/badge.svg?token=VVEK415DF6" alt="Coverage"></a></td>
        </tr>
        <tr>
          <td><strong>Packaging</strong></td>
          <td><a href="https://repology.org/project/python%3Aedgar-sec/versions"><img src="https://repology.org/badge/tiny-repos/python%3Aedgar-sec.svg" alt="Repology"></a></td>
        </tr>
        <tr>
          <td><strong>License</strong></td>
          <td><a href="https://github.com/nikhilxsunder/edgar-sec/blob/main/LICENSE"><img src="https://img.shields.io/pypi/l/edgar-sec.svg" alt="License"></a></td>
        </tr>
        <tr>
          <td><strong>Usage</strong></td>
          <td>
            <a href="https://pepy.tech/projects/edgar-sec"><img src="https://static.pepy.tech/badge/edgar-sec" alt="PyPI Downloads"></a>
            <a href="https://anaconda.org/conda-forge/edgar-sec"><img src="https://anaconda.org/conda-forge/edgar-sec/badges/downloads.svg" alt="Conda Downloads"></a>
          </td>
        </tr>
        <tr>
          <td><strong>Research / Index</strong></td>
          <td><a href="https://doi.org/10.5281/zenodo.17635942"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.17635942.svg" alt="DOI"></a></td>
        </tr>
      </table>
    </td>
  </tr>
</table>

edgar-sec is a research-grade, fully-typed Python SDK for the entire SEC EDGAR REST API — the structural twin of fedfred for federal securities-disclosure data. It provides ergonomic, discoverable access to the full endpoint surface (submissions, company concepts, company facts, frames, and CIK/ticker resolution) through a small public front door, with every response returned as a typed dataclass rather than a raw dict for IDE autocomplete and mypy safety. Built to the same quality bar as its sibling, it offers strict parity between synchronous and asynchronous clients, a built-in rate limiter that respects EDGAR's fair-access rules, optional local caching, and defensive type-safe handling of responses throughout. Distributed on PyPI, conda-forge, and Anaconda, it is designed as a durable data-infrastructure layer — the foundation for planned higher-order tooling like an XBRL parser, a pandas-subclassed financial dataframe, and a taxonomy×value×time tensor representation of filings.

```shell
pip install edgar-sec
```

| [Docs](https://edgar-sec-dev-team.github.io/edgar-sec/) | [PyPI](https://pypi.org/project/edgar-sec/) | [Conda-Forge](https://anaconda.org/channels/conda-forge/packages/edgar-sec/overview) | [Github](https://github.com/edgar-sec-dev-team/edgar-sec) |

## toros

toros is a pandas-backed data representation library that turns SEC filing data into self-validating financial objects. It uses registered DataFrame accessors to enforce financial semantics — type, unit, period, and taxonomy constraints — directly within the pandas backend, and layers specialized frame types (such as financial-statement representations) on top through inheritance. It serves as the interactive, semantically-aware data container that edgar-sec materializes filings into, giving researchers pandas ergonomics with domain-correct structure and validation rather than raw, untyped tables.

```shell
pip install toros
```

## autonomous-fed

Autonomous Fed is a reinforcement learning research project that reframes monetary policy as a control problem, in which an RL agent learns the central bank's reaction function rather than having a fixed Taylor rule imposed on it. Benchmarked against Hinterlang & Tänzer's Bundesbank work (Discussion Paper No. 51/2021), it replicates their RL environment and extends it by training policy agents inside two distinct economic environments — a linear one built on TVP-SVAR and a nonlinear one built on the NSSM state-space formulation that links to the NS-SDN project — then comparing learned policy behavior across both. The aim is a clean replication-plus-extension contribution targeting Computational Economics, demonstrating how optimal monetary policy under uncertainty changes when the agent's model of the economy moves from linear structural dynamics to a richer nonlinear spectral state space.

## ns-sdn

DESCRIPTION COMING SOON