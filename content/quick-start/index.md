---
title: "Quick Start"
description: "A quick start to Hyas Images — one pager."
lead: "A quick start to Hyas Images — one pager."
date: 2020-04-17T12:17:54+00:00
lastmod: 2020-04-17T12:17:54+00:00
draft: false
images: []
---

## Requirements

- [Node.js](https://nodejs.org/) — latest LTS version or newer

## Installation

```bash
npm i @hyas/images -D
```

## Setup

Add to `./config/_default/module.toml`:

```toml
[[mounts]]
  source = "node_modules/@hyas/images/layouts"
  target = "layouts"

[[mounts]]
  source = "layouts"
  target = "layouts"
```

Add to `./config/_default/params.toml`:

```bash
# lazyimg
[lazyimg]
  resizer = "auto"
  renderer = "lqip-webp"

  # Resizer options:
  lqipSize = "120x Gaussian"
  maxSize = "1920x"
  responsiveSizes = [ "320x", "640x", "768x", "1024x", "1366x", "1600x", "1920x" ]
  resizeOptions = "Lanczos q95"

  # Renderer options:
  class = "img-fluid"
  # alt = ""
  noscript = true

  errorHandler = "warning"
```

## Usage

See the [Hyas Docs](https://gethyas.com/) + [Demo page](/demo/)

## Credits

Based on [hugo-mods/lazyimg](https://github.com/hugo-mods/lazyimg)
