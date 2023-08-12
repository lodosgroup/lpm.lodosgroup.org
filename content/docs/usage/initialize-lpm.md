+++
title = "Initialize LPM"
description = "Simple guide for initializing and setting up LPM for the first time."
date = 2023-07-24T10:49:06
draft = false
weight = 1
sort_by = "weight"
template = "docs/page.html"
+++

This section outlines the one-time setup required to initialize LPM and get it up and running on your system.
Follow these instructions carefully to ensure a smooth setup process.


1. **Update LPM Database**:

    Updating the LPM Database is the first step in initializing the necessary files(e.g., core database), required for LPM to function properly.

    ```sh
    sudo lpm --update --db
    ```

2. **Add Repository**:

    Adding a repository is essential for LPM to access and manage packages. The repository you add will serve as the source of packages for your system.

    In this example, we will add the linux repository for amd64 architecture.

    ```sh
    # args: <repository-name> <repository-url>
    sudo lpm --repository --add linux-amd64-default linux-amd64-default.lpm.lodosgroup.org
    ```

    Once you've added the repository, LPM will synchronize with the package indexes sourced from the added repository. This indicates that you are all set to install packages.