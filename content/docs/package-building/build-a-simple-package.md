+++
title = "Build a simple package"
description = "Simple guide for building a package with lpm-builder module on Lod Package Manager."
date = 2023-07-24T10:49:06
draft = false
weight = 2
sort_by = "weight"
template = "docs/page.html"
+++

In this example, we will demonstrate how to build a package for the [sbs(simple background setter)](https://github.com/ozkanonur/sbs) tool.

Begin by preparing the necessary files for building [sbs](https://github.com/ozkanonur/sbs).

```sh
mkdir sbs_build_template
cd sbs_build_template

mkdir stage0
touch stage0/init
touch stage0/build
touch stage0/install_files

touch template
```

Copy the following content into `stage0/init`

```sh
curl -L https://github.com/ozkanonur/sbs/archive/refs/tags/v1.0.0.tar.gz > sbs.tar.gz
validate_checksum "sbs.tar.gz" "aa4da5b2315046fc2059599b19c530f08bb870e63ed17111a55991b1ae911367"
tar -xvzf sbs.tar.gz --strip 1 -C $SRC
```

Copy the following content into `stage0/build`

```sh
make sbs
```

Copy the following content into `stage0/install_files`

```sh
install_to_package sbs /usr/bin/sbs
```

Copy the following content into `template`

```json
{
    "name": "sbs",
    "description": "Simple background setter",
    "maintainer": "Lpm Core Maintainer <contact@onurozkan.dev>",
    "source_repository": "https://github.com/ozkanonur/sbs",
    "homepage": "https://github.com/ozkanonur/sbs",
    "arch": "amd64",
    "kind": "util",
    "file_checksum_algo": "sha256",
    "tags": [
        "x11",
        "background-setter"
    ],
    "version": {
        "readable_format": "1.0.0",
        "major": 1,
        "minor": 0,
        "patch": 0
    },
    "license": "MIT"
}
```

Now, you can run the following command to generate the `sbs.lod` package along with its repository index (a patch for the LPM repository database):

```sh
lpm --module builder --build .
```

Refer to the [package-builds](https://github.com/lodosgroup/package-builds/tree/linux-amd64-default/builds) to examine more package templates created for the `linux-amd64-default` repository.