# ZONEMINDER

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-surveillance_camera-lightgrey)

> Anticloud-hardened packaging of the upstream project `ZONEMINDER` in category **SURVEILLANCE CAMERA**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** SURVEILLANCE CAMERA · **Upstream:** https://github.com/ZoneMinder/zoneminder · **Upstream pin:** `e2f7bf49f22f3aa00a082bc227de64237d8e7699` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

ZoneMinder
==========

[![Join Slack](https://github.com/ozonesecurity/ozonebase/blob/master/img/slacksm.png?raw=true)](https://join.slack.com/t/zoneminder-chat/shared_invite/enQtNTU0NDkxMDM5NDQwLTdhZmQ5Y2M2NWQyN2JkYTBiN2ZkMzIzZGQ0MDliMTRmM2FjZWRlYzUwYTQ2MjMwMTVjMzQ1NjYxOTdmMjE2MTE "Join Slack")
<a href="https://discord.gg/tHYyP9k66q" title="Join Discord Server"><img src="https://assets-global.website-files.com/6257adef93867e50d84d30e2/636e0a6a49cf127bf92de1e2_icon_clyde_blurple_RGB.png" alt="drawing" width="50"/></a>

All documentation for ZoneMinder is now online at https://zoneminder.readthedocs.org

## Overview

ZoneMinder is an integrated set of applications which provide a complete surveillance solution allowing capture, analysis, recording and monitoring of any CCTV or security cameras attached to a Linux based machine. It is designed to run on distributions which support the Video For Linux (V4L) interface and has been tested with video cameras attached to BTTV cards, various USB cameras and also supports most IP network cameras. 

## Contacting the Development Team
Before creating an issue in our github forum, please read our posting rules:
https://github.com/ZoneMinder/ZoneMinder/wiki/Github-Posting-Rules

## Our Dockerfile has moved
Please file issues against the ZoneMinder Dockerfile here: 
https://github.com/ZoneMinder/zmdockerfiles

## Installation Methods

### Install from a Package project

This is the recommended method to install ZoneMinder onto your system. ZoneMinder packages are maintained for the following distros:

- Ubuntu via [Isaac Connor's PPA](https://launchpad.net/~iconnor)
- Debian from their [default project](https://packages.debian.org/search?searchon=names&keywords=zoneminder) 
- RHEL/CentOS and clones via [RPM Fusion](http://rpmfusion.org)
- Fedora via [RPM Fusion](http://rpmfusion.org)
- OpenSuse via [third party project](https://wiki.zoneminder.com/Installing_using_ZoneMinder_RPMs_for_SuSE)
- Mageia from their default project
- Arch via the [AUR](https://aur.archlinux.org/packages/zoneminder/)
- Gentoo via [Portage Overlays](http://gpo.zugaina.org/www-misc/zoneminder)

If a project that hosts ZoneMinder packages is not available for your distro, then you are encouraged to build your own package, rather than build from source.  While each distro is different in ways that set it apart from all the others, they are often similar enough to allow you to adapt another distro's package building instructions to your own.

### Building from Source is Discouraged

Historically, installing ZoneMinder onto your system required building from source code by issuing the traditional configure, make, make install commands.  To get ZoneMinder to build, all of its dependencies had to be determined and installed beforehand. Init and logrotate scripts had to be manually copied into place following the build.  Optional packages such as jscalendar and Cambozola had to be manually installed. Uninstalls could leave stale files around, which could cause problems during an upgrade.  Speaking of upgrades, when it comes time to upgrade all these manual steps must be repeated again.

Better methods exist today that do much of this for you. The current development team, along with other volunteers, have taken great strides in providing the resources necessary to avoid building from source.  

### Building a ZoneMinder Package ###

Building ZoneMinder into a package is not any harder than building from source.  As a matter of fact, if you have successfully built ZoneMinder from source in the past, then you may find these steps to be easier. 

When building a package, it is best to do this work in a separate environment, dedicated to development purposes. This could be as simple as creating a virtual machine, using Docker, or using mock.  All it takes is one “Oops” to regret doing this work on your production server.

Lastly, if you desire to build a development snapshot from the master branch, it is recommended you first build your package using an official release of ZoneMinder. This will help identify whether any problems you may encounter are caused by the build process or is a new issue in the master branch.

Please visit our [ReadtheDocs site](https://zoneminder.readthedocs.org/en/stable/installationguide/index.html) for distro specific instructions.

### Package Maintainers
Many of the ZoneMinder configuration variable default values are not configurable at build time through autotools or cmake.  A new tool called *zmeditconfigdata.sh* has been added to allow package maintainers to manipulate any variable stored in ConfigData.pm without patching the source. 

For example, let's say I have created a new ZoneMinder package that contains the cambozola javascript file.  However by default cambozola support is turned off.  To fix that, add this to the packaging script:
```bash
./utils/zmeditconfigdata.sh ZM_OPT_CAMBOZOLA yes
```

Note that zmeditconfigdata.sh is intended to be called, from the root build folder, prior to running cmake or configure.

#### Docker

Docker is a system to run applications inside isolated containers. ZoneMinder, and the ZM webserver, will run using the 
Dockerfile contained in this project. However, there is still work needed to ensure that the main ZM features work 
properly and are documented. 

## Contribution Model and Development

* Source hosted at [GitHub](https://github.com/ZoneMinder/ZoneMinder/)
* Report issues at [GitHub Issues](https://github.com/ZoneMinder/ZoneMinder/issues)
* Questions/feature requests in [Slack](https://zoneminder-chat.slack.com/) or [forums](https://forums.zoneminder.com)

Pull requests are very welcome!  If you would like to contribute, please follow
the following steps.  While step 3 is optional, it is preferred.

1. Fork the project
2. Open an issue at our [GitHub Issues Tracker](https://github.com/ZoneMinder/ZoneMinder/issues).
   Follow the issue template to describe the bug or security issue you foun

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **C/C++ / CMake** (manifests: CMakeLists.txt; scanned in UPSTREAM_CLONE)
- Top-level source layout: `cmake/`, `conf.d/`, `db/`, `dep/`, `distros/`, `email_content/`, `fonts/`, `icons/`, `misc/`, `onvif/`, `scripts/`, `src/`
- Snapshot size: **6288 files**, **721005 lines of code** (measured; see Benchmarks)
- Primary languages: `.pm` (3102), `.php` (1036), `.js` (295), `.sql` (293), `.ctp` (255), `.css` (168)
- Upstream commit pinned for this packaging: `e2f7bf49f22f3aa00a082bc227de64237d8e7699`

---

## Installation

No installation section was found in the upstream readme, so the commands below are generated from the manifests detected in this project directory.

```sh
cmake -B build && cmake --build build    # or: ./configure && make
```

Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

- Mageia from their default project
- Arch via the [AUR](https://aur.archlinux.org/packages/zoneminder/)
- Gentoo via [Portage Overlays](http://gpo.zugaina.org/www-misc/zoneminder)

If a project that hosts ZoneMinder packages is not available for your distro, then you are encouraged to build your own package, rather than build from source.  While each distro is different in ways that set it apart from all the others, they are often similar enough to allow you to adapt another distro's package building instructions to your own.

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

The upstream API surface is defined by the `ZONEMINDER` source tree vendored in `UPSTREAM_CLONE/` (C/C++ / CMake ecosystem). Public entry points:

- Source modules: `cmake/`, `conf.d/`, `db/`, `dep/`, `distros/`, `email_content/`, `fonts/`, `icons/`
- The snapshot declares 50 dependency references across 3 ecosystem(s); see Dependencies below.
- Overlay API: `anticloud/cli.py` exposes 13 subcommands with JSON stdout; `anticloud/bench/runner.py` runs the 16-check suite; `anticloud/provenance/chain.py` exposes the SHA3-256 + Ed25519 provenance chain.

---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | C/C++ / CMake |
| Manifests detected | CMakeLists.txt |
| Files in snapshot | 6288 |
| Lines of code | 721005 |
| Dependency references | 50 |
| Dependencies by ecosystem | conan: 1, native: 30, npm: 19 |
| Upstream license | GPL-2.0 |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| native | LibUnwind | - | CMakeLists.txt |
| native | ZLIB | - | CMakeLists.txt |
| native | CURL | - | CMakeLists.txt |
| native | JPEG | - | CMakeLists.txt |
| native | LibJWT | - | CMakeLists.txt |
| native | jwt-cpp | - | CMakeLists.txt |
| native | OpenSSL | - | CMakeLists.txt |
| native | MOSQUITTO | - | CMakeLists.txt |
| native | MOSQUITTOPP | - | CMakeLists.txt |
| native | FFMPEG | - | CMakeLists.txt |
| native | Boost | - | CMakeLists.txt |
| native | GSOAP | - | CMakeLists.txt |
| native | V4L2 | - | CMakeLists.txt |
| native | nlohmann_json | - | CMakeLists.txt |
| native | Perl | - | CMakeLists.txt |
| ... | (35 more) | | |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

Better methods exist today that do much of this for you. The current development team, along with other volunteers, have taken great strides in providing the resources necessary to avoid building from source.

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

*Excerpt from upstream `CONTRIBUTING.md`:*

# Contributing

The ZoneMinder project was originally written by Philip Coombes in 2001. It has since moved to Github and is maintained by just a few who volunteer their spare time.  

Over the years, ZoneMinder has accumulated a rather large user base. This presents a challenge to the development team when it comes to managing communications. Welcome to the world of software development, right?

In order to keep the kinds of issues, which require changes to the source code, separate from all other questions and comments, our methods of communication are organized in the following manner:

- The ZoneMinder Github forum is intended for bug reports and serious feature requests only
- The ZoneMinder user forum is intended for general questions and tech support
- The ZoneMinder IRC channel is intended for general questions and tech support

More details can be found in our [Github Posting Rules](https://github.com/ZoneMinder/ZoneMinder/wiki/Github-Posting-Rules). Please read this before creating an issue in our Github forum.

Knowledge of Github is a necessary first step to contribute to the project. To contribute, one must generate a pull request. For those just starting out, [this guide](https://github.com/ZoneMinder/ZoneMinder/wiki/Understanding-Github-and-Pull-Requests) will step you through the process. 

Note that pasting code into our Github forum, with the expectation we will do the work for you, is not acceptable.

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: GPL-2.0** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
		    GNU GENERAL PUBLIC LICENSE
		       Version 2, June 1991

 Copyright (C) 1989, 1991 Free Software Foundation, Inc.
     59 Temple Place, Suite 330, Boston, MA  02111-1307  USA
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.

			    Preamble

  The licenses for most software are designed to take away your
freedom to share and change it.  By contrast, the GNU General Public
License is intended to guarantee your freedom to share and change free
software--to make sure the software is free for all its users.  This
General Public License applies to most of the Free Software
Foundation's software and to any other program whose authors commit to
using it.  (Some other Free Software Foundation software is covered by
the GNU Library General Public License instead.)  You can apply it to
your programs, too.

```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original GPL-2.0 terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `GPL-2.0` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `ZONEMINDER` (category: SURVEILLANCE CAMERA)
- **Upstream URL:** https://github.com/ZoneMinder/zoneminder
- **Pinned commit (SHA):** `e2f7bf49f22f3aa00a082bc227de64237d8e7699`
- **Branch:** master
- **Pin provenance:** resolved during the second documentation pass. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`a651d010483a06c9ba857681ef062800c684cd9404c778ad74e09bf03854038a`.

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

