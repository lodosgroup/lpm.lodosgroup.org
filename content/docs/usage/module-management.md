+++
title = "Dynamic Module Management"
description = "Simple guide for managing dynamic modules with Lod Package Manager."
date = 2023-07-24T10:49:06
draft = false
weight = 6
sort_by = "weight"
template = "docs/page.html"
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