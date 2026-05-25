# instant-cluster

Container images for the Verda instant-cluster stack.

## Images

| Image | Description |
|---|---|
| [`slinky-login`](https://github.com/verda-cloud/instant-cluster/pkgs/container/instant-cluster%2Fslinky-login) | Slurm login pod image with kanidm integration. |
| [`slinky-slurmd`](https://github.com/verda-cloud/instant-cluster/pkgs/container/instant-cluster%2Fslinky-slurmd) | Slurm worker pod image with `iperf`, `iperf3`, and `ucx_perftest`. |

## Pulling

```bash
docker pull ghcr.io/verda-cloud/instant-cluster/slinky-login:25.11-kanidm-v1
docker pull ghcr.io/verda-cloud/instant-cluster/slinky-slurmd:25.11-v1
```

## Conventions

- **Tag format**: `<upstream-version>-<verda-rev>` (e.g. `25.11-v1`, `25.11-kanidm-v1`). Bump `-v<N>` when the Dockerfile or pinned dependencies change.
- **Production**: prefer digest pinning over tag pinning.
- **Visibility**: each package must be set to **Public** in GHCR settings after the first push.
