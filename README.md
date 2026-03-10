This repository watches for new `diesel_cli` releases and publishes rebuilt binaries.

It is intended for use by [OSRD](https://github.com/OpenRailAssociation/osrd)'s editoast container.
As such, the build is done using musl and with only postgres enabled. (Unlike the official diesel_cli build that use glibc)

- Every 6 hours, GitHub Actions checks crates.io for the latest `diesel_cli` version.
- If a release tag for that version does not already exist in this repo, it builds binaries.
- It publishes a release tagged like `diesel-cli-v2.3.6`.
- You can also trigger a manual build with `workflow_dispatch` and optionally provide a version.
