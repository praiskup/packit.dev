---
title: February 2022
date: 2022-02-08
weight: 64
---

## Week 5 (January 31th - February 7th)

- A new option `--no-require-autosetup` for `source-git init` command has been
  introduced. Please note that source-git repositories not using `%autosetup` may
  not be properly initialized. ([packit#1470](https://github.com/packit/packit/pull/1470))
- Packit-service now supports re-triggering against failed task using comment on
  pull request `/packit rebuild-failed` and similarly for testing farm: `/packit retest-failed`.
  ([packit-service#1303](https://github.com/packit/packit-service/pull/1303))

## Week 6 (February 8th - February 14th)

- Packit now correctly handles colons in git trailer values in source-git commits.
  ([packit#1478](https://github.com/packit/packit/pull/1478))

## Week 7 (February 14th❤️ - February 18th)

- Synchronization of default files can now be disabled using a new config
  `files_to_sync`. Key `sync_files` is now deprecated.
  ([packit#1483](https://github.com/packit/packit/pull/1483))
  ([packit.dev#390](https://github.com/packit/packit.dev/pull/390))
- `python3-setuptools_scm` is now available by default in the sandbox.

## Week 8 (February 18th - February 28th)

- Packit now allows specifying more test distros for one build target
  to test on in Testing Farm in the configuration. The checks for the
  test job will also contain the name of the actual test distro
  (and not the build target as previously).
- A new option, `srpm_build_deps`, in the packit configuration file  
  can be used. Which is a list of RPM dependencies that are needed for
  the actions to be run when building SRPM and is an indicator to build
  the SRPMs in Copr.
