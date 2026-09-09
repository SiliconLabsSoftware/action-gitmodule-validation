# Validate Gitmodules Branches

Composite action that checks listed submodules have a `branch` entry in `.gitmodules` matching the target branch (PR base branch, or the current branch on other events).

The caller must check out the repository first.

## Usage

```yaml
steps:
  - uses: actions/checkout@v7
    with:
      submodules: false

  - uses: SiliconLabsSoftware/action-gitmodule-validation@v1
    with:
      submodules: path/to/submodule another/submodule
```

## Inputs

| Input | Required | Default | Description |
| --- | --- | --- | --- |
| `submodules` | yes | n/a | Space-separated submodule paths to validate |
| `gitmodules-file` | no | `.gitmodules` | Path to the `.gitmodules` file |
