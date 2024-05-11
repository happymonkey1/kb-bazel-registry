# Kablunk Bazel Registry

## Overview

Public Kablunk internal Bazel registry, forked from the [Bazel Central Registry](https://github.com/bazelbuild/bazel-central-registry).

To use this registry, add the following to your `.bazelrc`
```
common --registry=https://raw.githubusercontent.com/happymonkey1/kb-bazel-registry/mainline
```

By default, adding a registry override disables the Bazel Central Registry, add the following to retain access
```
common --registry=https://bcr.bazel.build
```

The order of the registries in `.bazelrc` determines the order in which `bazel` tries to resolve depedendencies
