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
      - name: Install dependencies
        run: npm ci
      - name: Install playwright browsers
        run: npx playwright install --with-deps
      - name: Run Playwright tests
        run: npx playwright test
```

## Disclaimer

This is "only" a wrapper for the mcr.microsoft.com/playwright image, which e.g. can be used in GitLab CI.
