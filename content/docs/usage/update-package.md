+++
title = "Update Package"
description = "Simple guide on update operations of Lod Package Manager."
date = 2023-07-24T10:49:06
draft = false
weight = 4
sort_by = "weight"
template = "docs/page.html"
+++

If you want to make sure everything is up to date, follow the approach below:

```sh
sudo lpm --update
# or
sudo lpm --update --all
```

If you want to update all the packages currently installed on your system, follow the approach below:

```sh
sudo lpm --update --packages
```

To update a particular package, follow the approach below:

```sh
# args: <package-name>
sudo lpm --update lzip
```

If you want to bring LPM up to date with the latest changes(like important updates to the core database), follow the approach below:

```sh
sudo lpm --update --db
```

If you want to get the most recent package indexes of repositories added to LPM, follow the approach below:

```sh
sudo lpm --update --index
```

If you want to update a particular package using a locally stored `.lod` file, follow the approach below:

```sh
# args: <package-name>, <package-path>
sudo lpm --update lzip --local $path_to_lod_package
```