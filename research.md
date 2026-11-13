---
layout: page
title: Research
permalink: /research/
---

Peer-reviewed papers and citable software artifacts. My work centers on state-space models, spectral decomposition of non-stationary time series, and the data infrastructure that makes reproducible econometric research possible. Every software artifact below is archived on Zenodo release by release, so an analysis can cite the exact version it ran on.

| Work | Venue | Year | Type |
|---|---|---|---|
| [ns-sdn: the Non-Stationary Spectral Decomposition Network](#nssdn-software) | Zenodo | 2026 | Software |
| [Non-Stationary Spectral Decomposition Network: Adaptive Spectral Emission Heads and Frequency Modulation](#nssdn-ii) | IEEE-ORSS 2026 | 2026 | Paper |
| [cultivars: Research-grade time series econometrics for Python](#cultivars) | Zenodo | 2026 | Software |
| [Non-Stationary Spectral Decomposition Network for Econometric Time Series Forecasting](#nssdn-i) | FLAIRS-39 | 2026 | Paper |
| [fedfred: A Python client for the Federal Reserve Economic Database (FRED) API](#fedfred) | Zenodo | 2025 | Software |

---

<h2 id="nssdn-software">ns-sdn: Non-Stationary Spectral Decomposition Network</h2>

<p>
  <a href="https://doi.org/10.5281/zenodo.23368625"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.23368625.svg" alt="DOI"></a>
  <img src="https://img.shields.io/badge/type-software-blue.svg" alt="Software">
  <a href="https://pypi.org/project/ns-sdn/"><img src="https://img.shields.io/pypi/v/ns-sdn.svg" alt="PyPI version"></a>
</p>

**Nikhil Sunder** · Zenodo · v1.0.0 · 2026

The reference implementation of the NS-SDN architecture as a stable Python package: a validated specification whose defaults reproduce the IEEE-ORSS DGS10 experiment to its 58,849 parameters, a frozen result carrying every path of the decomposition (trend, amplitude, instantaneous frequency, phase, gate, per-component contributions and latent state) on the original scale, conditional one-step and recursive forecasting, and a `SpectralState` that reads the decomposition as a time-local measure on the frequency axis with centroid, dispersion, entropy, effective component count, Wasserstein velocity and a disentanglement score. Signed releases, a documentation site deriving the model equation by equation, and a one-command reproduction of the published experiment. Archived on Zenodo so that work building on the model can cite an exact, permanently resolvable version.

[Zenodo record](https://doi.org/10.5281/zenodo.23368625) · [Documentation](https://nikhilxsunder.github.io/ns-sdn/stable/) · [Code](https://github.com/nikhilxsunder/ns-sdn) · [Project detail →](/development/#ns-sdn)

<details>
<summary><strong>Citation (BibTeX)</strong></summary>

{% highlight bibtex %}
@software{sunder_nssdn,
  author    = {Sunder, Nikhil},
  title     = {ns-sdn: the Non-Stationary Spectral Decomposition Network},
  year      = {2026},
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.23368625},
  url       = {https://github.com/nikhilxsunder/ns-sdn}
}
{% endhighlight %}

</details>

---

<h2 id="nssdn-ii">Non-Stationary Spectral Decomposition Network: Adaptive Spectral Emission Heads and Frequency Modulation</h2>

<p>
  <a href="https://doi.org/10.1109/ORSS71174.2026.11684282"><img src="https://img.shields.io/badge/DOI-10.1109%2FORSS71174.2026.11684282-blue.svg" alt="DOI"></a>
  <img src="https://img.shields.io/badge/venue-IEEE%20ORSS%202026-00629B.svg" alt="IEEE ORSS 2026">
  <img src="https://img.shields.io/badge/type-conference%20paper-blue.svg" alt="Conference paper">
</p>

**Nikhil Sunder, Maikel Leon** · *2026 IEEE Opportunity Research Scholars Symposium (ORSS)*, Atlanta, GA, pp. 1–5 · IEEE Xplore · 2026

The second paper in the NS-SDN arc, and the formulation the package implements. Where the FLAIRS paper introduced the architecture and its spectral emission equation, this work evaluates the emission heads themselves as instruments: the state-conditioned heads for trend, amplitude, instantaneous frequency and phase, plus a learned gating head that selects which components participate at each step, with the phase integrating the emitted frequency so that frequency is modulated directly by the latent dynamics rather than recovered from phase increments. Evaluated on the 10-Year Treasury yield (DGS10, daily from 2000, last 365 days held out) under conditional one-step forecasting, the model reconstructs the history with negligible error and tracks the holdout closely (RMSE 3.87 × 10⁻² and MAPE 0.61% on the level scale); the contribution, though, is what the heads reveal rather than the forecast: frequency paths drift slowly under stable conditions and converge during the 2020 macroeconomic shock while amplitude concentrates, which the paper reads as adaptive spectral compression, a learned reduction in the effective dimensionality of the series that fixed-basis methods cannot produce. The paper positions NS-SDN as a neural spectral-analysis framework rather than solely a forecasting model.

[Read on IEEE Xplore](https://ieeexplore.ieee.org/document/11684282) · [Code](https://github.com/nikhilxsunder/ns-sdn) · [Reproduce the experiment](https://nikhilxsunder.github.io/ns-sdn/stable/auto_examples/plot_03_reproduce_orss.html)

<details>
<summary><strong>Citation (BibTeX)</strong></summary>

{% highlight bibtex %}
@inproceedings{sunder2026orss,
  title     = {Non-Stationary Spectral Decomposition Network: Adaptive Spectral Emission Heads and Frequency Modulation},
  author    = {Sunder, Nikhil and Leon, Maikel},
  booktitle = {2026 IEEE Opportunity Research Scholars Symposium (ORSS)},
  address   = {Atlanta, GA, USA},
  publisher = {IEEE},
  pages     = {1--5},
  year      = {2026},
  doi       = {10.1109/ORSS71174.2026.11684282},
  url       = {https://ieeexplore.ieee.org/document/11684282}
}
{% endhighlight %}

</details>

---

<h2 id="cultivars">cultivars: Research-grade time series econometrics for Python</h2>

<p>
  <a href="https://doi.org/10.5281/zenodo.23028870"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.23028870.svg" alt="DOI"></a>
  <img src="https://img.shields.io/badge/type-software-blue.svg" alt="Software">
  <a href="https://pypi.org/project/cultivars/"><img src="https://img.shields.io/pypi/v/cultivars.svg?include_prereleases" alt="PyPI version"></a>
</p>

**Nikhil Sunder** · Zenodo · v1.0.0a4 · 2026

A citable software artifact covering the econometric time-series toolkit on one estimation surface: univariate models from ARIMA through the GARCH family, stochastic volatility and regime switching; reduced-form, large-dimensional Bayesian, nonlinear and time-varying-parameter VARs; structural identification by recursive, long-run, sign, narrative, instrument and heteroskedasticity schemes; a linear-Gaussian state-space substrate with nonlinear and particle filters; spectral methods; and forecast evaluation and diagnostics. Every model is a specification whose `fit()` or `identify()` returns an immutable, self-describing result, and estimation is kept separate from identification so that an impulse response can always be traced to the assumption that signed it. Archived on Zenodo so that analyses depending on it can cite an exact, permanently resolvable version.

[Zenodo record](https://doi.org/10.5281/zenodo.23028870) · [Documentation](https://nikhilxsunder.github.io/cultivars/stable/) · [Code](https://github.com/nikhilxsunder/cultivars) · [Project detail →](/development/#cultivars)

<details>
<summary><strong>Citation (BibTeX)</strong></summary>

{% highlight bibtex %}
@software{sunder_cultivars,
  author    = {Sunder, Nikhil},
  title     = {cultivars: Research-grade time series econometrics for Python},
  year      = {2026},
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.23028870},
  url       = {https://github.com/nikhilxsunder/cultivars}
}
{% endhighlight %}

</details>

---

<h2 id="nssdn-i">Non-Stationary Spectral Decomposition Network for Econometric Time Series Forecasting</h2>

<p>
  <a href="https://doi.org/10.32473/flairs.39.1.141588"><img src="https://img.shields.io/badge/DOI-10.32473%2Fflairs.39.1.141588-blue.svg" alt="DOI"></a>
  <img src="https://img.shields.io/badge/venue-FLAIRS--39-005030.svg" alt="FLAIRS-39">
  <img src="https://img.shields.io/badge/access-open-brightgreen.svg" alt="Open access">
</p>

**Nikhil Sunder** · *The International FLAIRS Conference Proceedings*, vol. 39, no. 1 · May 2026

The paper that introduced NS-SDN. It represents an economic time series as a time-varying trend plus a sum of latent sinusoidal components whose amplitude, instantaneous frequency, and phase are emitted at each step from a recurrent latent state — an adaptive, state-driven spectral decomposition rather than a fixed-basis Fourier or stationary spectral model. The architecture draws on implicit neural representations with periodic activations, instantaneous-frequency analysis in the spirit of the Hilbert–Huang transform, and nonlinear state-space econometrics. It functions as both a conditional one-step forecaster and an interpretable spectral-analysis tool, exposing regime-dependent trend, amplitude, and frequency dynamics — demonstrated on the 10-Year Treasury yield through the 2020 macroeconomic shock. The IEEE-ORSS paper above takes the emission heads as its subject, and the `ns-sdn` package implements that formulation.

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
@article{sunder2026flairs,
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