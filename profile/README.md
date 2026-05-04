# The Loom Foundation

We are custodians of the [Loom Manifesto](https://theloommanifesto.org), the Loom Method, and the reference tooling. We foster their growth and nurture a healthy community around them.

## Repositories

| Repository | Description |
|---|---|
| [manifest](https://github.com/loom-foundation/manifest) | The west workspace manifest. |
| [org](https://github.com/loom-foundation/org) | Strategy, governance, brand. |
| [manifesto](https://github.com/loom-foundation/manifesto) | The manifesto and the site that publishes it. |
| [note](https://github.com/loom-foundation/note) | The Note methodology corpus: intent as Git-native artifacts. |

## Workspace

The foundation's repositories are assembled into one working tree with [west](https://docs.zephyrproject.org/latest/develop/west/index.html).

### Prerequisites

Git and [west](https://docs.zephyrproject.org/latest/develop/west/index.html).

  ```sh
  uv tool install west     # or: pipx install west
  ```

### Set up the workspace

Clones every repo into `./loom-foundation/`.

```sh
west init -m https://github.com/loom-foundation/manifest loom-foundation
cd loom-foundation
west update
```

### Quick reference

```sh
west update                            # sync the workspace to the manifest
west list                              # list the repositories
west status                            # git status across every repo
west forall -c "git pull --ff-only"    # pull every repo
west forall -c "<any command>"         # run a command in every repo
```
