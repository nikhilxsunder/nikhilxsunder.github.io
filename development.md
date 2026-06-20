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