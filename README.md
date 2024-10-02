# gh-devclone

Clone a GitHub repository to local development directory, preserving the `OWNER/REPO` directory structure.
This command is a thin wrapper over `gh repo clone`.

## Installation

```bash
gh ext install mkaput/gh-devclone
```

## Usage

```bash
gh devclone OWNER/REPO
```

By default, the repository is cloned to `~/Developer/OWNER/REPO`.
The root directory can be customized by setting the `GH_DEVCLONE_ROOT` environment variable (globally)
or by passing it via the `--root` argument.

```bash
GH_DEVCLONE_ROOT=~/Projects gh devclone OWNER/REPO
```

```bash
gh devclone OWNER/REPO --root ~/Projects
```

If the `OWNER/` portion of the `OWNER/REPO` repository argument is omitted,
it defaults to the name of the authenticating user.