# Coditory Multi Setup GitHub Action

Single action to setup all kinds environments for building projects.

## Sample usage

```yml
name: Build

on:
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
        with:
          fetch-depth: 0

      - name: Setup
        uses: coditory/multi-setup-action@v1
        with:
          java-version: 21

      - name: Build
        run: ./gradlew build
```

## References

See:
- [Other Coditory actions](https://github.com/topics/coditory-actions)
- [Coditory workflows](https://github.com/topics/coditory-workflows)

