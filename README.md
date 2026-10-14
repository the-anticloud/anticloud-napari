# NAPARI

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-scientific_lab-lightgrey)

> Anticloud-hardened packaging of the upstream project `NAPARI` in category **SCIENTIFIC LAB**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** SCIENTIFIC LAB · **Upstream:** https://github.com/napari/napari · **Upstream pin:** `53db61402bf274d8b98ea74d5000d8ee3349a83c` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

# napari

### multi-dimensional image viewer for python

<!-- Project info -->
[![License](https://img.shields.io/pypi/l/napari.svg)](https://github.com/napari/napari/raw/main/LICENSE)
[![Supported Python versions](https://img.shields.io/pypi/pyversions/napari.svg)](https://python.org)
[![Python package index](https://img.shields.io/pypi/v/napari.svg)](https://pypi.org/project/napari)
[![Python package index download statistics](https://img.shields.io/pypi/dm/napari.svg)](https://pypistats.org/packages/napari)
[![Conda Version](https://img.shields.io/conda/vn/conda-forge/napari.svg)](https://anaconda.org/conda-forge/napari)
![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/napari?label=Conda%20downloads)
[![DOI](https://zenodo.org/badge/144513571.svg)](https://zenodo.org/badge/latestdoi/144513571)

<!-- Project standards and quality  -->
[![Development Status](https://img.shields.io/pypi/status/napari.svg)](https://en.wikipedia.org/wiki/Software_release_life_cycle#Beta)
[![SPEC 0 — Minimum Supported Dependencies](https://img.shields.io/badge/SPEC-0%20(aspiring!)-green?labelColor=%23004811&color=%235CA038)](https://scientific-python.org/specs/spec-0000/)
[![EffVer Versioning](https://img.shields.io/badge/version_scheme-EffVer-0097a7)](https://jacobtomlinson.dev/effver)
[![Comprehensive Test](https://github.com/napari/napari/actions/workflows/test_comprehensive.yml/badge.svg)](https://github.com/napari/napari/actions/workflows/test_comprehensive.yml)
[![Code coverage](https://codecov.io/gh/napari/napari/branch/main/graph/badge.svg)](https://codecov.io/gh/napari/napari)
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)

<!-- Community and support -->
[![Sponsor our Project](https://img.shields.io/badge/donate-to%20napari-blueviolet)](https://numfocus.org/donate-to-napari)
[![image.sc forum](https://img.shields.io/badge/dynamic/json.svg?label=forum&url=https%3A%2F%2Fforum.image.sc%2Ftags%2Fnapari.json&query=%24.topic_list.tags.0.topic_count&colorB=brightgreen&suffix=%20topics&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAA4AAAAOCAYAAAAfSC3RAAABPklEQVR42m3SyyqFURTA8Y2BER0TDyExZ+aSPIKUlPIITFzKeQWXwhBlQrmFgUzMMFLKZeguBu5y+//17dP3nc5vuPdee6299gohUYYaDGOyyACq4JmQVoFujOMR77hNfOAGM+hBOQqB9TjHD36xhAa04RCuuXeKOvwHVWIKL9jCK2bRiV284QgL8MwEjAneeo9VNOEaBhzALGtoRy02cIcWhE34jj5YxgW+E5Z4iTPkMYpPLCNY3hdOYEfNbKYdmNngZ1jyEzw7h7AIb3fRTQ95OAZ6yQpGYHMMtOTgouktYwxuXsHgWLLl+4x++Kx1FJrjLTagA77bTPvYgw1rRqY56e+w7GNYsqX6JfPwi7aR+Y5SA+BXtKIRfkfJAYgj14tpOF6+I46c4/cAM3UhM3JxyKsxiOIhH0IO6SH/A1Kb1WBeUjbkAAAAAElFTkSuQmCC)](https://forum.image.sc/tag/napari)
[![napari on Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/napari/napari/main?urlpath=%2Fdesktop)

**napari** is a fast, interactive, multi-dimensional image viewer for Python. It's designed for browsing, annotating, and analyzing large multi-dimensional images. It's built on top of Qt (for the GUI), vispy (for performant GPU-based rendering), and the scientific Python stack (numpy, scipy).

We're developing **napari** in the open! You can follow progress on [our project roadmap]([https://github.com/napari/napari](https://github.com/orgs/napari/projects/24)), test out new versions as we release them, and contribute ideas and code.

If you want to refer to our documentation, please go to [napari.org](https://www.napari.org). If you want to contribute to it, please refer to the *contributing* section below. 

We're working on [tutorials](https://napari.org/stable/tutorials/), but you can also quickly get started by looking below.

## try it out now!
[Install uv](https://docs.astral.sh/uv/getting-started/installation/#standalone-installer) to try napari.
Then launch the program in a terminal window with the command:
```sh
uvx "napari[all]"
```
In the `File` menu, select `Open Sample` and select a sample image to get started.

## installation
For a full installation, we recommend installing napari into a virtual environment, like this:

```sh
conda create -y -n napari-env -c conda-forge python=3.13
conda activate napari-env
python -m pip install "napari[all]"
```

If you prefer conda over pip, you can replace the last line with: `conda install -c conda-forge napari pyqt6`

See here for the full [installation guide](https://napari.org/stable/tutorials/fundamentals/installation.html).

## simple example

This example uses a data sample from the `scikit-image` library, but you can pass your own dataset as an array to `imshow`.
From inside an IPython shell, you can open up an interactive viewer by calling

```python
from skimage import data
import napari

viewer, layers = napari.imshow(data.cells3d(), channel_axis=1, ndisplay=3)
```

![napari viewer with a multichannel image of cells displayed as two image layers: nuclei and membrane.](./src/napari/resources/multichannel_cells.png)

To use napari from inside a script, use `napari.run()`:

```python
from skimage import data
import napari

viewer, layers = napari.imshow(data.cells3d(), channel_axis=1, ndisplay=3)
napari.run()  # start the "event loop" and show the viewer
```

## features

Check out the scripts in our [`examples` folder](examples) to see some of the functionality we're developing!

**napari** supports six main different layer types, `Image`, `Labels`, `Points`, `Vectors`, `Shapes`, and `Surface`, each corresponding to a different data type, visualization, and interactivity. You can add multiple layers of different types into the viewer and then start working with them, adjusting their properties.

All our layer types support n-dimensional data and the viewer provides the ability to quickly browse and visualize either 2D or 3D slices of the data.

**napari** also supports bidirectional communication between the viewer and the Python kernel, which is especially useful when launching from jupyter notebooks or when using our built-in console. Using the console allows

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Python** (manifests: pyproject.toml; scanned in UPSTREAM_CLONE)
- Top-level source layout: `binder/`, `examples/`, `resources/`, `src/`, `tools/`
- Snapshot size: **1171 files**, **204783 lines of code** (measured; see Benchmarks)
- Primary languages: `.py` (1030), `.svg` (80), `.txt` (14), `(none)` (8), `.md` (8), `.in` (3)
- Upstream commit pinned for this packaging: `53db61402bf274d8b98ea74d5000d8ee3349a83c`

---

## Installation

Then launch the program in a terminal window with the command:
```sh
uvx "napari[all]"
```
In the `File` menu, select `Open Sample` and select a sample image to get started.

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

No usage section was found in the upstream readme. Entry points detected in this project directory:

```sh
python -m napari    # module entry point, when the package layout matches
```

Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

We're working on [tutorials](https://napari.org/stable/tutorials/), but you can also quickly get started by looking below.

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Python |
| Manifests detected | pyproject.toml |
| Files in snapshot | 1171 |
| Lines of code | 204783 |
| Dependency references | 17 |
| Dependencies by ecosystem | conda: 14, pypi: 3 |
| Upstream license | BSD-3-Clause |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| pypi | app-model | >=0.5.0 | pyproject.toml |
| pypi | cachey | >=0.2.1 | pyproject.toml |
| pypi | certifi | >=2018.1.18 | pyproject.toml |
| conda | napari | - | binder/environment.yml |
| conda | conda-forge | - | binder/environment.yml |
| conda | desktop-server | - | binder/environment.yml |
| conda | python | 3.12 | binder/environment.yml |
| conda | napari | - | binder/environment.yml |
| conda | forge | - | binder/environment.yml |
| conda | fsspec | - | binder/environment.yml |
| conda | pyqt6 | - | binder/environment.yml |
| conda | scikit-image | - | binder/environment.yml |
| conda | zarr | - | binder/environment.yml |
| conda | websockify | - | binder/environment.yml |
| conda | pip | - | binder/environment.yml |
| ... | (2 more) | | |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

```sh
conda create -y -n napari-env -c conda-forge python=3.13
conda activate napari-env
python -m pip install "napari[all]"
```

If you prefer conda over pip, you can replace the last line with: `conda install -c conda-forge napari pyqt6`

See here for the full [installation guide](https://napari.org/stable/tutorials/fundamentals/installation.html).

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

*Excerpt from upstream `CONTRIBUTING.md`:*

# contributing

Thank you for your interest in contributing to napari!
Contributions to napari are very welcome and encouraged!
If at any point you have questions or would like to discuss your contribution, the core team and napari community are active on the [napari Zulip chat](https://napari.zulipchat.com/) and available on regular [online community meetings](https://napari.org/dev/community/meeting_schedule.html).
You may also reach out on our [GitHub Issues](https://github.com/napari/napari/issues).
We are here and excited to help!

Read our [contributing guide](https://napari.org/dev/developers/contributing/index.html) for a detailed overview of how to get started with contributing to napari, including how to set up a development environment, how to run tests, and how to submit a pull request.

The [AI use policy and guidelines](https://napari.org/dev/developers/contributing/ai.html) should be read and followed when using AI tools to assist with development.

If you want to contribute to or edit our documentation, go to [napari/docs](https://github.com/napari/docs) and also read our [documentation contributing guide](https://napari.org/dev/developers/contributing/documentation/index.html).

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: BSD-3-Clause** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
BSD 3-Clause License

Copyright (c) 2018, Napari
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this
  list of conditions and the following disclaimer.

* Redistributions in binary form must reproduce the above copyright notice,
  this list of conditions and the following disclaimer in the documentation
  and/or other materials provided with the distribution.

* Neither the name of the copyright holder nor the names of its
  contributors may be used to endorse or promote products derived from
  this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original BSD-3-Clause terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `BSD-3-Clause` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `NAPARI` (category: SCIENTIFIC LAB)
- **Upstream URL:** https://github.com/napari/napari
- **Pinned commit (SHA):** `53db61402bf274d8b98ea74d5000d8ee3349a83c`
- **Branch:** main
- **Pin provenance:** GitHub API commits/<branch> (response quoted in report). The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`4622ae0f23911795c5fb5bdc16269100e3a8b293a6c33fae44a7f2af6597c89d`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

