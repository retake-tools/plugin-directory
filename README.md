# Retake Plugin Directory

A lightweight, curated list of Retake Packages that can be installed directly
from their GitHub source repositories.

This directory is intentionally not a Package Registry or marketplace. It does
not host Package archives, resolve dependency graphs, auto-update code, rank
Packages, or replace each repository's license and security review.

## Install from GitHub

Retake resolves a GitHub ref to an exact commit, validates and builds only the
declared Package files, and records the exact commit and content digest in the
workspace lock. Updates are discovered from the same moving ref and remain an
explicit user action.

```text
github:<owner>/<repository>@<ref>#subdirectory=<package-root>
```

Use a moving branch such as `main` when you want update notifications. Use a
tag or commit when you want an intentionally pinned installation.

## Official Packages

### Retake Image Studio

- Repository: [retake-tools/image-studio](https://github.com/retake-tools/image-studio)
- Package ID: `design.retake.image-studio`
- Package root: `plugin`
- Current version: `0.11.0`
- Stable source:
  `github:retake-tools/image-studio@main#subdirectory=plugin`
- Immutable release:
  `github:retake-tools/image-studio@v0.11.0#subdirectory=plugin`
- Development source:
  `github:retake-tools/image-studio@develop#subdirectory=plugin`
- License: Apache-2.0
- Status: Official, bundled with Retake Whiteboard
- Validated: 2026-08-01 with Retake Whiteboard `0.1.3`

### Retake Video Studio

- Repository: [retake-tools/video-studio](https://github.com/retake-tools/video-studio)
- Package ID: `design.retake.video-studio`
- Package root: `package`
- Current version: `0.1.3`
- Stable source:
  `github:retake-tools/video-studio@main#subdirectory=package`
- Immutable release:
  `github:retake-tools/video-studio@v0.1.3#subdirectory=package`
- Development source:
  `github:retake-tools/video-studio@develop#subdirectory=package`
- License: Apache-2.0
- Status: Official, optional; not bundled with Retake Whiteboard by default
- Validated: 2026-07-29 with Retake Whiteboard `0.1.3`

Whiteboard's bundled Image Studio copy remains available offline. Video Studio
is an optional GitHub-source installation. A moving `main` source receives update
notifications; use the listed release tag when an intentionally immutable
installation is required.

## Submit a Package

Open a pull request that adds one entry containing:

- repository URL and Package ID;
- exact Package root when it is not the repository root;
- recommended moving ref and optional pinned release ref;
- license;
- short capability summary;
- validation date and compatible Whiteboard version.

Listing is curatorial metadata, not code trust. Whiteboard still validates the
resolved source, permissions, Package identity, compatibility, and content
digest before activation.

## License

The directory content is available under the
[Apache License 2.0](./LICENSE). Required attribution notices are provided in
[NOTICE](./NOTICE). Linked Packages retain their own licenses.
