+++
title = "install"
description = "Simple guide for installing packages with Lod Package Manager."
date = 2023-07-24T10:49:06
draft = false
weight = 2
sort_by = "weight"
template = "docs/page.html"

[extra]
lead = "LPM provides a seamless and advanced approach to installing packages on your system."
+++

- **Install package**:

    You can easily install packages using the following command:

    ```sh
    # args: <package-name>
    sudo lpm --install lzip
    ```

- **Version constraints**:

    By default, LPM will search for the most recent version available in the repository for the requested package.
    To install a particular version of any package, use the version constraint by appending it with `@` to the package name:

    ```sh
    sudo lpm --install "package-name@version-constraint"
    ```

    When defining a version constraint, you have access to various operators that help you specify the range of acceptable versions:

    Use `=` for an exact version match.

    Use `>` for versions greater than the specified version.

    Use `>=` for versions greater than or equal to the specified version.

    Use `<` for versions less than the specified version.

    Use `<=` for versions less than or equal to the specified version.

    For example, if you wish to install version 1.23.0 or any version greater than or equal to it of the lzip package, you can use the following command:

    ```sh
    # args: <package-name@version-constraint>
    sudo lpm --install "lzip@>=1.23.0"
    ```

    LPM will then install the specified version of the package that meets the version constraint you provided.

- **Installing a local package**:

    If you want to install a package from your filesystem, you can do so by executing the following command:

    ```sh
    # args: <package-name>, <package-path>
    sudo lpm --install $path_to_lod_package --local
    ```