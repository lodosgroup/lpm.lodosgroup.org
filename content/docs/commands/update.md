+++
title = "update"
description = "Simple guide on update operations of Lod Package Manager."
date = 2023-07-24T10:49:06
draft = false
weight = 4
sort_by = "weight"
template = "docs/page.html"
in_search_index = true

[extra]
lead = "LPM offers several update operations to ensure both your system and LPM itself remain up-to-date. This documentation elaborates on these update operations."
+++

- **Update everything**:

    If you want to make sure everything is up to date, follow the approach below:

    ```sh
    sudo lpm --update
    # or
    sudo lpm --update --all
    ```

- **Update all packages**:

    If you want to update all the packages currently installed on your system, follow the approach below:

    ```sh
    sudo lpm --update --packages
    ```

- **Update a particular package**:

    To update a particular package, follow the approach below:

    ```sh
    # args: <package-name>
    sudo lpm --update lzip
    ```

- **Migrate LPM**:
    If you want to bring LPM up to date with the latest changes(like important updates to the core database), follow the approach below:

    ```sh
    sudo lpm --update --db
    ```

- **Sync package indexes**:

    If you want to get the most recent package indexes of repositories added to LPM, follow the approach below:

    ```sh
    sudo lpm --update --index
    ```

- **Update a particular package from local package**:

    If you want to update a particular package using a locally stored `.lod` file, follow the approach below:

    ```sh
    # args: <package-name>, <package-path>
    sudo lpm --update lzip --local $path_to_lod_package
    ```
