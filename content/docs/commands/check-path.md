+++
title = "check-path"
description = "Simple guide for checking if a file or directory is owned by any installed application"
date = 2023-07-24T10:49:06
draft = false
weight = 7
sort_by = "weight"
template = "docs/page.html"
in_search_index = true

[extra]
lead = "With LPM, you can easily determine whether a file or directory is owned by any of the applications installed on your system."
+++

- **Example Usage**:

    It's super simple as demonstrated in the example below (the path can be in any form, whether relative or absolute):

    ```sh
    # args: <target-path>
    lpm --check-path ./xyz
    ```