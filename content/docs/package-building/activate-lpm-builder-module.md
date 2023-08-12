+++
title = "Activate lpm-builder module"
description = "Simple guide for deleting packages with Lod Package Manager."
date = 2023-07-24T10:49:06
draft = false
weight = 1
sort_by = "weight"
template = "docs/page.html"
+++

To build the lpm-builder module from source, follow these steps:

```sh
git clone https://github.com/lodosgroup/lpm-modules.git
cd lpm-modules/lpm-builder
make build
```

To utilize the lpm-builder module, you must add the dynamic library to the database using the following LPM command:

```sh
sudo lpm --module --add builder {path to liblpm_builder.so}
```

To confirm its successful addition, you can execute `lpm --module --list`, which will provide a list of all modules added to LPM and ensures that the integration of the `lpm-builder` module into LPM is successful and ready for utilization.