# Contributing

## Recommendations

The project provides [pre-commit] hooks. Feel free to install them:

```shell
# install pre-commit with uv: uv tool install pre-commit
pre-commit install
```

## Packaging

Install [snapcraft]:

```shell
sudo snap install --classic snapcraft
```

Build and package the snap:

```shell
snapcraft pack
```

The above command will create a file in the format of
`rocminfo_<version>_amd64.snap`. Install the snap:

```shell
sudo snap install --dangerous rocminfo*.snap
```

ROCmInfo uses the runtime supplied by the `rocm-inference` content snap.
Connect it after installing both snaps:

```shell
sudo snap install rocm-inference
sudo snap connect rocminfo:rocm rocm-inference:runtime
```

The snap also plugs privileged interfaces that may not auto-connect for a
locally-built snap installed with `--dangerous`. Check the current state and
connect the interfaces you need:

```shell
sudo snap connect rocminfo:kernel-module-observe
```

[pre-commit]: https://pre-commit.com/
[snapcraft]: https://github.com/canonical/snapcraft
