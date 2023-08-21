+++
title = "Install LPM"
description = "Install LPM"
date = 2023-07-24T10:49:06
draft = false
weight = 1
sort_by = "weight"
template = "docs/page.html"
in_search_index = true

[extra]
lead = "If you don't have Cargo (Rust's package manager) installed, you need to first install it. You can find installation instructions in the <a target='_blank' href='https://doc.rust-lang.org/cargo/getting-started/installation.html'> Cargo Getting Started Guide</a>."
+++

## Install with Cargo

To install LPM from a specific branch, run the following command:

```sh
cargo install --git https://github.com/lodosgroup/lpm --branch main
```

Alternatively, you can install it from tags:

```sh
cargo install --git https://github.com/lodosgroup/lpm --branch <tag>
```

To confirm a successful LPM installation, simply execute the `lpm -v` or `lpm --version` command.

## Build LPM from Source

If you prefer building LPM from its source code (usually preferred for development), follow these steps:

1. **Clone the lpm repository from GitHub**:

   ```sh
   git clone https://github.com/lodosgroup/lpm
   ```

2. **Change into the cloned repository directory**:

   ```sh
   cd lpm
   ```

3. **Build the lpm executable**:
    

   ```sh
   cargo build --release # exclude the `--release` flag for debugging
   ```

After the building, you will be able to use the lpm executable under`target/{debug/release}` directory.