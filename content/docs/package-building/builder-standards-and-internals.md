+++
title = "Builder standards and internals"
description = "Simple guide about builder standards internals of Lod Package Manager."
date = 2023-07-24T10:49:06
draft = false
weight = 0
sort_by = "weight"
template = "docs/page.html"
in_search_index = true

[extra]
lead = "Let's take a detailed look into the inner workings of the lpm-builder module."
+++

## Template structure

### stage0 dir

The `stage0` directory contains scripts that run on the builder module level. The following files should be included in the `stage0` directory:

- `init`: This file is used to download and verify the necessary environments and files before the building phase.
- `build`: This file is used to build the program.
- `install_files`: This file is used to install the program files into the lod package with the same paths that lpm should install them on the system.
- `post_install_files`: This file is optional and is used for any additional work that needs to be done after installing the files into the lod package.


### stage1 dir

The stage1 directory is optional and contains scripts that run on the lpm core level. The following files can be included in the stage1 directory:

- `pre_install`: This file is an optional step that can be used if additional work needs to be done before installing the package.
- `post_install`: This file is an optional step that can be used if additional work needs to be done after installing the package.
- `pre_delete`: This file is an optional step that can be used if additional work needs to be done before deleting the package.
- `post_delete`: This file is an optional step that can be used if additional work needs to be done after deleting the package.
- `pre_downgrade`: This file is an optional step that can be used if additional work needs to be done before downgrading the package.
- `post_downgrade`: This file is an optional step that can be used if additional work needs to be done after downgrading the package.
- `pre_upgrade`: This file is an optional step that can be used if additional work needs to be done before upgrading the package.
- `post_upgrade`: This file is an optional step that can be used if additional work needs to be done after upgrading the package.


### template file

`JSON` file that contains almost all the informations about the package.

- `name`: The name of the package.
- `description`: A description of what the package does.
- `maintainer`: Contact information for the maintainer of the package.
- `source_repository`(optional):  The URL of the source code repository for the package.
- `homepage`(optional): The URL of the package's homepage.
- `arch`: The architecture of the package.
- `kind`: The type of package.
- `file_checksum_algo`: The algorithm used to compute the checksum of the package files.
- `tags`: A list of tags or keywords that describe the package.
- `version`: An object that contains version information for the package.
- `license`(optional): The license under which the package is distributed.
- `mandatory_dependencies.runtime`(optional): A list of the package's mandatory dependencies for runtime.
- `mandatory_dependencies.build`(optional): A list of the package's mandatory dependencies for building it.
- `suggested_dependencies.runtime`(optional): A list of the package's suggested dependencies for runtime.
- `suggested_dependencies.build`(optional): A list of the package's suggested dependencies for building it.


## stage0 built-in functions

The lpm-builder module provides the following built-in functions that can be used in `stage0` scripts:

- `validate_checksum(file_path, sha256_checksum)`: This function takes two arguments: the path of the file to validate, and the SHA256 checksum of the file. It validates the checksum of the file and throws an error if it doesn't match the provided checksum.
- `install_to_package(source_file_path, dest_path)`: This function puts files into the lod package. It takes two arguments: the path of the source file to be added to the package, and the path where lpm should install the file when the package is installed.
- `copy_to_package(source_dir_path, dest_path)`: This function puts copies directory into the lod package. It takes two arguments: the path of the source directory to be added to the package, and the path where lpm should install the directory when the package is installed.

