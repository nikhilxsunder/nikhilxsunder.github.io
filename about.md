---
layout: page
title: About
permalink: /about/
---

I build research software for economics, and I do research that needs it.

Most quantitative economics runs on code that was never meant to survive the paper it was written for — notebooks that depend on a specific CSV in a specific folder, scrapers that break when a government website changes its markup, estimators reimplemented from scratch by every researcher who needs them. The result is a field where reproducing a result is often harder than producing it. I have spent the last two years building the alternative: installable, typed, tested, documented, citable packages that handle the parts of the pipeline nobody should have to rewrite.

That work started with `fedfred`, a client for the Federal Reserve's FRED family of APIs, which I wrote because I needed macroeconomic series for a project and found the existing options unmaintained or incomplete. It now has a few tens of thousands of downloads and a DOI. `edgar-sec` followed for SEC EDGAR disclosure data. `toros` is the representation layer those clients materialize into — financial objects with enforced semantics rather than untyped tables — and `cultivars` is the modeling layer above them, targeting the Bayesian and time-varying VAR methods that Python handles poorly compared to R and MATLAB.

The research side runs in parallel and sets the agenda. My main line is NS-SDN, a neural state-space architecture that decomposes a time series into a time-varying trend plus latent oscillatory components whose amplitude, frequency, and phase are emitted at each step from a recurrent state — an adaptive spectral decomposition rather than a fixed Fourier basis. The first paper was published at FLAIRS-39; a second on adaptive spectral emission heads is under review. It grew out of a question about the 10-Year Treasury through the 2020 shock that no stationary spectral method could answer cleanly. A related project reframes monetary policy as a control problem, training reinforcement-learning agents to learn a central bank's reaction function inside both linear TVP-SVAR and nonlinear state-space economies, benchmarked against Hinterlang and Tänzer's Bundesbank work.

I care about the engineering as much as the econometrics, and I think the separation between them is largely artificial. A model you cannot install is a claim, not a result.

---

## Education

**University of Miami**, Herbert Business School — Coral Gables, FL
B.S.B.A., Quantitative Economics &amp; Finance · Minor in Mathematics

Coursework across real analysis, abstract algebra, probability theory, mathematical statistics, and graduate econometrics.

**Next:** pursuing MSc / MScR study in computer science and computational science in Europe, with a research focus on state-space methods, spectral representation learning, and reinforcement learning for economic control problems.

---

## Appointments

**Research Fellow** — Intelligent Computer Systems Research Institute (ICSRI), University of Miami

**Founder &amp; Lead Developer** — toros-dev, an open-source engineering group building financial data infrastructure

---

## How I work

A few commitments that show up in everything I publish:

**Correctness over convenience.** Full type annotations, `mypy`-clean, explicit key-existence checks, specific exception classes, no silent failure. If a response shape is wrong, the library says so rather than returning `None`.

**Sync and async as first-class peers.** Not a wrapper bolted on afterward — strict parity, so the async client is never the second-class citizen with missing endpoints.

**Reproducibility as a deliverable.** OpenSSF Best Practices certification, Codecov coverage gates, conda-forge distribution alongside PyPI, and Zenodo-archived releases with DOIs, so a paper can cite an exact version that will still resolve in ten years.

**Design before code.** Every package here started as a specification argument — what the public surface should be, what belongs in private internals, where the layer boundaries fall — before any implementation existed. The interesting work is in those decisions, not in the typing.

---

## Technical

**Primary:** Python 3.13 · PyTorch · NumPy · pandas · Polars · Dask · httpx

**Also:** Swift · C# / .NET · LaTeX · Git

**Domains:** time-series econometrics · state-space modeling · Bayesian estimation · reinforcement learning · API and SDK architecture · scientific packaging and distribution

---

## Contact

Email: [nsunder724@gmail.com](mailto:nsunder724@gmail.com)
GitHub: [nikhilxsunder](https://github.com/nikhilxsunder) · [toros-dev](https://github.com/toros-dev)
ORCID: [0009-0007-3323-1760](https://orcid.org/0009-0007-3323-1760)
LinkedIn: [nikhil-sunder](https://www.linkedin.com/in/nikhil-sunder)

Open to research collaboration and graduate program inquiries.