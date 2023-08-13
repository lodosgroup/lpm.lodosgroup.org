+++
title = "module"
description = "Simple guide for managing dynamic modules with Lod Package Manager."
date = 2023-07-24T10:49:06
draft = false
weight = 6
sort_by = "weight"
template = "docs/page.html"
in_search_index = true

[extra]
lead = "The module command of LPM enables you to use advanced features implemented in other languages for the LPM environment. This empowers you to seamlessly integrate and utilize capabilities from various languages within the LPM ecosystem."
+++

- **Add dynamic module**:
    You can easily add a dynamic module using the following command:

    ```sh
    # args: <module-name> <dynamic-library-path(e.g., .so file)>
    sudo lpm --module --add builder $path_to_dynamic_library
    ```

- **Delete dynamic modules**:

    If you want to delete dynamic modules, follow the approach below:

    ```sh
    # args: <module-name>, <module-name>, <module-name>, ...
    sudo lpm --repository --delete builder rpm-module
    ```

- **List dynamic modules**:

    If you want to see list of all dynamic modules added to LPM, follow the approach below:

    ```sh
    lpm --repository --list
    ```

- **Run a module**:

    To start a module, use the following approach below:

    ```sh
    # args: <module-name>
    lpm --module rpm-module
    ```

Refer to the [Build a simple package](/docs/package-building/build-a-simple-package/) documentation for a practical example of utilizing a dynamic module. This module is actively being used for building packages to LPM repositories.