# Actions for Porla and plugins

Some common actions and workflows.


## Usage

Add `.github/workflows/plugin.yml` to the plugin repository:

```yaml
name: Plugin

on:
  pull_request:
  push:
    tags: ["v*"]

jobs:
  plugin:
    uses: porla/actions/.github/workflows/plugin.yml@<sha>
    permissions:
      contents: write
    with:
      porla-version: v0.55.0
      files: |
        *.lua
```

