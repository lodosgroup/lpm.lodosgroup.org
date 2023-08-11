+++
title = "Delete Package"
description = "Simple guide for deleting packages with Lod Package Manager."
date = 2023-07-24T10:49:06
draft = false
weight = 3
sort_by = "weight"
template = "docs/page.html"
+++

You can easily delete packages using the following command:

```sh
# args: <package-name>
sudo lpm --delete lzip
```

LPM will then delete the package from your system along with its associated dependencies if there are any.
