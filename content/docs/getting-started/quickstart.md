+++
title = "Quickstart"
description = "Quickstart of Lod Package Manager."
date = 2023-07-24T10:49:06
draft = false
weight = 2
sort_by = "weight"
template = "docs/page.html"

[extra]
lead = "LPM is a robust tool for securely managing software packages on your system. This quickstart guide will guide you through the fundamental steps to become familiar with LPM."
+++

1. **Migrate LPM database**:

    The first step is to migrate the LPM database. This process initializes the core database files required for LPM to function effectively.

    ```sh
    sudo lpm --update --db
    ```

2. **Add repository**:

    Adding a repository is essential for LPM to access and manage packages. A repository acts as the source of packages for your system. Let's add the `linux-amd64-default` repository as an example.

    ```sh
    # args: <repository-name> <repository-url>
    sudo lpm --repository --add linux-amd64-default linux-amd64-default.lpm.lodosgroup.org
    ```

    Once you've added the repository, LPM will synchronize with the package indexes sourced from the added repository. This indicates that you are all set to install packages.

3. **Install a package**:

    Installing packages using LPM is straightforward. Simply use the following command, replacing <package-name> with the name of the package you want to install.

    ```sh
    # args: <package-name>
    sudo lpm --install lzip
    ```

    To confirm the successful completion of the installation, you can check by running the command `lzip --version`.

4. **Delete the installed package**:

    If you want to delete a package from your system, use the delete command followed by the package name.

    ```sh
    # args: <package-name>
    sudo lpm --delete lzip
    ```

These steps cover the basic operations to quickly start using the LOD Package Manager. You can explore the advanced features of LPM from commands section on this website.




