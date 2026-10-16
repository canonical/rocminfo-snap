# ROCmInfo Snap

[![rocminfo][snap-badge]][snap-link]
[![CI][ci-badge]][ci-link]

This is a snap packaging of [ROCmInfo][rocminfo source], the ROCm application
for reporting system info.

## Install

```shell
sudo snap install rocminfo
```

This snap consumes ROCm runtime libraries provided by `rocm-inference`, which
should be installed automatically, but might need a manual interface connection:

```shell
sudo snap install rocm-inference
sudo snap connect rocminfo:rocm rocm-inference:runtime
```

([Don't have snapd installed?][snapd-setup])

## Use

For usage instructions refer to the [ROCmInfo documentation].

[ci-badge]: https://github.com/canonical/rocminfo-snap/actions/workflows/ci.yaml/badge.svg
[ci-link]: https://github.com/canonical/rocminfo-snap/actions/workflows/ci.yaml
[rocminfo documentation]: https://rocm.docs.amd.com/projects/rocminfo/en/latest/index.html
[rocminfo source]: https://github.com/ROCm/rocm-systems/tree/develop/projects/rocminfo
[snap-badge]: https://snapcraft.io/rocminfo/badge.svg
[snap-link]: https://snapcraft.io/rocminfo
[snapd-setup]: https://snapcraft.io/docs/core/install
