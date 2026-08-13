---
layout: page
title: Research
permalink: /research/
---

# Research

Peer-reviewed papers and citable software artifacts. My work centers on state-space models, spectral decomposition of non-stationary time series, and the data infrastructure that makes reproducible econometric research possible.

| Work | Venue | Year | Type |
|---|---|---|---|
| [Adaptive Spectral Emission Heads and Frequency Modulation](#nssdn-ii) | Under review | 2026 | Paper |
| [Non-Stationary Spectral Decomposition Network for Econometric Time Series Forecasting](#nssdn-i) | FLAIRS-39 | 2026 | Paper |
| [fedfred](#fedfred) | Zenodo | 2025 | Software |

---

<h2 id="nssdn-ii">Non-Stationary Spectral Decomposition Network: Adaptive Spectral Emission Heads and Frequency Modulation</h2>

<p>
  <img src="https://img.shields.io/badge/status-under%20review-orange.svg" alt="Status: under review">
  <img src="https://img.shields.io/badge/type-conference%20paper-blue.svg" alt="Conference paper">
</p>

**Nikhil Sunder** · 2026

The second paper in the NS-SDN arc, extending the base architecture with adaptive spectral emission heads and explicit frequency modulation. Where the FLAIRS paper established that a recurrent latent state can emit interpretable amplitude, frequency, and phase trajectories, this work examines how the emission mechanism itself should be parameterized — and what that choice implies for the model's ability to track regime transitions in the frequency domain.

Preprint and full details to follow once the review process concludes.

---

<h2 id="nssdn-i">Non-Stationary Spectral Decomposition Network for Econometric Time Series Forecasting</h2>

<p>
  <a href="https://doi.org/10.32473/flairs.39.1.141588"><img src="https://img.shields.io/badge/DOI-10.32473%2Fflairs.39.1.141588-blue.svg" alt="DOI"></a>
  <img src="https://img.shields.io/badge/venue-FLAIRS--39-005030.svg" alt="FLAIRS-39">
  <img src="https://img.shields.io/badge/access-open-brightgreen.svg" alt="Open access">
</p>

**Nikhil Sunder** · *The International FLAIRS Conference Proceedings*, vol. 39, no. 1 · May 2026

NS-SDN represents an economic time series as a time-varying trend plus a sum of latent sinusoidal components whose amplitude, instantaneous frequency, and phase are emitted at each step from a recurrent latent state — an adaptive, state-driven spectral decomposition rather than a fixed-basis Fourier or stationary spectral model. The architecture draws on implicit neural representations with periodic activations, instantaneous-frequency analysis in the spirit of the Hilbert–Huang transform, and nonlinear state-space econometrics. It functions as both a conditional one-step forecaster and an interpretable spectral-analysis tool, exposing regime-dependent trend, amplitude, and frequency dynamics — demonstrated on the 10-Year Treasury yield through the 2020 macroeconomic shock.

[Read on FLAIRS](https://journals.flvc.org/FLAIRS/article/view/141588) · [PDF](https://journals.flvc.org/FLAIRS/article/download/141588/147150/293304) · [Code](https://github.com/nikhilxsunder/ns-sdn)

<details>
<summary><strong>Read inline</strong></summary>

<iframe
  src="https://journals.flvc.org/plugins/generic/pdfJsViewer/pdf.js/web/viewer.html?file=https%3A%2F%2Fjournals.flvc.org%2FFLAIRS%2Farticle%2Fdownload%2F141588%2F147150%2F293304"
  width="100%" height="800"
  style="border: 1px solid #ddd; border-radius: 4px;"
  title="Non-Stationary Spectral Decomposition Network for Econometric Time Series Forecasting"
  allowfullscreen webkitallowfullscreen></iframe>

</details>

<details>
<summary><strong>Citation (BibTeX)</strong></summary>

{% highlight bibtex %}
@article{Sunder_2026,
    title   = {Non-Stationary Spectral Decomposition Network for Econometric Time Series Forecasting},
    author  = {Sunder, Nikhil},
    journal = {The International FLAIRS Conference Proceedings},
    volume  = {39},
    number  = {1},
    year    = {2026},
    month   = {May},
    doi     = {10.32473/flairs.39.1.141588},
    url     = {https://journals.flvc.org/FLAIRS/article/view/141588}
}
{% endhighlight %}

</details>

---

<h2 id="fedfred">fedfred: A Python client for the Federal Reserve Economic Database (FRED) API</h2>

<p>
  <a href="https://doi.org/10.5281/zenodo.17635942"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.17635942.svg" alt="DOI"></a>
  <img src="https://img.shields.io/badge/type-software-blue.svg" alt="Software">
  <a href="https://pypi.org/project/fedfred/"><img src="https://img.shields.io/pypi/v/fedfred.svg" alt="PyPI version"></a>
</p>

**Nikhil Sunder** · Zenodo · v3.0.0 · 2025

A citable software artifact providing full-coverage access to the Federal Reserve's FRED, ALFRED, and GeoFRED/Maps endpoints through a typed Python interface, with sync and async clients, built-in rate limiting and caching, and native returns to pandas, polars, dask, and GeoPandas. Archived on Zenodo so that analyses depending on it can cite an exact, permanently resolvable version.

[Zenodo record](https://doi.org/10.5281/zenodo.17635942) · [Documentation](https://nikhilxsunder.github.io/fedfred/) · [Code](https://github.com/nikhilxsunder/fedfred) · [Project detail →](/development/#fedfred)

<details>
<summary><strong>Citation (BibTeX)</strong></summary>

{% highlight bibtex %}
@software{fedfred,
  author    = {Sunder, Nikhil},
  title     = {fedfred: A Python client for the Federal Reserve Economic Database (FRED) API},
  version   = {3.0.0},
  year      = {2025},
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.17635942},
  url       = {https://github.com/nikhilxsunder/fedfred}
}
{% endhighlight %}

</details>