<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/theoros-space/theoros-brand/main/github/banners/docs-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/theoros-space/theoros-brand/main/github/banners/docs-light.png">
  <img src="https://raw.githubusercontent.com/theoros-space/theoros-brand/main/github/banners/docs-light.png" width="100%" alt="theoros-docs">
</picture>

<p><a href="LICENSE"><picture><source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/theoros-space/theoros-brand/main/github/badges/license-cc-by-4-0-dark.png"><img src="https://raw.githubusercontent.com/theoros-space/theoros-brand/main/github/badges/license-cc-by-4-0-light.png" height="31" alt="license: CC BY 4.0"></picture></a> <a href="https://github.com/theoros-space"><picture><source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/theoros-space/theoros-brand/main/github/badges/part-06-of-06-dark.png"><img src="https://raw.githubusercontent.com/theoros-space/theoros-brand/main/github/badges/part-06-of-06-light.png" height="31" alt="part: 06 of 06"></picture></a></p>

## Overview

The technical documentation for Theoros: what the product does, how one model
runs on every satellite, and the flight documents that come with each release.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/theoros-space/theoros-brand/main/github/diagrams/flow-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/theoros-space/theoros-brand/main/github/diagrams/flow-light.png">
  <img src="https://raw.githubusercontent.com/theoros-space/theoros-brand/main/github/diagrams/flow-light.png" width="100%" alt="How Theoros works">
</picture>

## Contents

| Section | What you will find |
|---|---|
| [Overview](docs/index.md) | What Theoros does and for whom |
| [Product](docs/product.md) | The six parts of the product |
| [Architecture](docs/architecture.md) | How one model runs on every satellite |
| [Glossary](docs/glossary.md) | Terms used across the documentation |
| Flight documents | Interface control document, resource budgets and test reports, published per release |

## Architecture at a glance

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/theoros-space/theoros-brand/main/github/diagrams/architecture-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/theoros-space/theoros-brand/main/github/diagrams/architecture-light.png">
  <img src="https://raw.githubusercontent.com/theoros-space/theoros-brand/main/github/diagrams/architecture-light.png" width="100%" alt="TheorosNet architecture">
</picture>

## Building the site

The site is built with [MkDocs](https://www.mkdocs.org) from [`docs/`](docs/).

```bash
pip install mkdocs-material
mkdocs serve
```

## Where it fits

| | Repository | Role |
|:-:|---|---|
| `01` | [theoros-models](https://github.com/theoros-space/theoros-models) | Multi-task model, training and the ground compiler |
| `02` | [theoros-edge](https://github.com/theoros-space/theoros-edge) | Onboard int8 runtime and flight targets |
| `03` | [theoros-delivery](https://github.com/theoros-space/theoros-delivery) | Signed model packages and over-the-air updates |
| `04` | [theoros-ground](https://github.com/theoros-space/theoros-ground) | Customer API, mission dashboard and result tracking |
| `05` | [theoros-bench](https://github.com/theoros-space/theoros-bench) | Open benchmark for onboard Earth observation AI |
| `06` | **theoros-docs** | Technical documentation and flight documents |

## License

Text and diagrams are licensed under [CC BY 4.0](LICENSE). The Theoros name and
logo are not; see [theoros-brand](https://github.com/theoros-space/theoros-brand).

---

<p align="center">
  <a href="https://github.com/theoros-space"><picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/theoros-space/theoros-brand/main/logo/svg/mark-signal.svg">
    <img src="https://raw.githubusercontent.com/theoros-space/theoros-brand/main/logo/svg/mark-signal.svg" width="28" alt="Theoros">
  </picture></a>
  <br>
  <sub>Theoros &nbsp;·&nbsp; Onboard AI for Earth observation &nbsp;·&nbsp; Baku and Helsinki &nbsp;·&nbsp; <a href="https://theoros.space">theoros.space</a></sub>
</p>
