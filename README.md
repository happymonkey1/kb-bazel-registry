# Kablunk Bazel Registry

## Overview

Public Kablunk internal Bazel registry, forked from the [Bazel Central Registry](https://github.com/bazelbuild/bazel-central-registry).

To use this registry, add the following to your `.bazelrc`
```
common --registry=https://raw.githubusercontent.com/happymonkey1/kb-bazel-registry/main
```

By default, adding a registry override disables the Bazel Central Registry, add the following to retain access
```
common --registry=https://bcr.bazel.build
```

The order of the registries in `.bazelrc` determines the order in which `bazel` tries to resolve depedendencies

## SHA256 SRI Integrity Checksum

Archives and patch files require a sha256 integrity checksum, below is one method to generate using bash
```
echo -n sha256-; \
    cat PATH_TO_FILE | \ 
    openssl dgst -sha256 -binary | \
    base64
```
