# labels

🏷️⚙️ Shared GitHub labels config

## Usage

### GitHub Actions

[EndBug/label-sync](https://github.com/EndBug/label-sync)

`.github/workflows/label-sync.yml`
```yml
name: Sync labels
on:
  workflow_dispatch:

jobs:
  sync:
    name: Run EndBug/label-sync
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: EndBug/label-sync@v2
        with:
          config-file: 'https://raw.githubusercontent.com/danielwerg/labels/master/labels.yml'
```

### CLI

[Financial-Times/github-label-sync](https://github.com/Financial-Times/github-label-sync)

```sh
yarn global add github-label-sync
```

```sh
github-label-sync --access-token XXX -l labels.yml --allow-added-labels danielwerg/labels
```