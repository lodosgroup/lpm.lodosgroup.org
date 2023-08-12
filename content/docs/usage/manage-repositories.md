+++
title = "Manage Repositories"
description = "Simple guide for managing repositories with Lod Package Manager."
date = 2023-07-24T10:49:06
draft = false
weight = 5
sort_by = "weight"
template = "docs/page.html"
+++

- **Add repository**:
    You can easily add repository using the following command:

    ```sh
    # args: <repository-name> <repository-url>
    sudo lpm --repository --add linux-amd64-default linux-amd64-default.lpm.lodosgroup.org
    ```

    LPM will then add the repository along with its associated package indexes.

- **Delete repositories**:

    If you want to delete repositories, follow the approach below:

    ```sh
    # args: <repository-name>, <repository-name>, <repository-name>, ...
    sudo lpm --repository --delete linux-amd64-default
    ```

- **List repositories**:

    If you want to see list of all repositories added to LPM, follow the approach below:

    ```sh
    sudo lpm --repository --list
    ```