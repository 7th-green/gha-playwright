# playwright GitHub Action

This is a playwright GitHub Action that helps you run, playwright wihtout the hassle of waiting for the packages to be installed.


## Example usage

```yaml
name: Playwight

on:
  push:
    tags:
      - "**"

jobs:
  Playwright:
    runs-on: ubuntu-latest
    strategy:
      fail-fast: false
    steps:
      - uses: actions/checkout@v1
      - uses: 7th-green/playwright@v1
```
