#  SkyFlex manifest

The project manifest is a TOML file with the name `skyflex.toml`, placed in the top directory of a project, that describes an optional SkyFlex workspace and a SkyFlex package.

Any SkyFlex project shall contain the SkyFlex manifest in order to, for example, compile.

## Examples

### Website

The SkyFlex manifest for a website looks like the following:

```toml
[package]
name = "example"
version = "0.1.0"

[[source]]
path = "src"
include = true

[website]
enable = true

[dependencies]
```

### Library

The SkyFlex manifest for a library looks like the following:

```toml
[package]
name = "example.util"
version = "0.1.0"
author = "Me <me@example.com>"
license = "MIT or Apache-2.0"
description = "My utilities"

[[source]]
path = "src"
include = true

[dependencies]
```

### Command line interface

The SkyFlex manifest for a command line interface looks like the following:

```toml
[package]
name = "example"
version = "0.1.0"

[[source]]
path = "src"
include = true

[cli]
enable = true
main-class = "example.Example"

[dependencies]
```

### Workspace

The SkyFlex manifest for a workspace looks like the following:

```toml
[workspace]
members = [
    "packages/master",
    "packages/chief",
]
```