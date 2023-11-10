+++
title = "Try in Docker"
description = "Try LPM in Docker"
date = 2023-11-10T10:49:06
draft = false
weight = 2
sort_by = "weight"
template = "docs/page.html"
in_search_index = true

+++

You don't need to install LPM on your host system just to play with it. You can use the docker image instead:

```sh
docker run -it ozkanonur/lpm:alpha
```

If you want to do some benchmarking with `perf` tool, you may need to add `--privileged` flag:

```sh
docker run -it --privileged ozkanonur/lpm:alpha
```

Now, you can play with LPM as you like in the container without touching your host system.