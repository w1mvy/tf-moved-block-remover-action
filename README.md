# tf-moved-block-remover-action

This GitHub Actions removed [terraform moved block](https://www.terraform.io/language/modules/develop/refactoring#moved-block-syntax) and create Pull Request

## Usage

```
on:
  schedule:
    - cron: "0 1 * * 1-5"

jobs:
  removed_job:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - id: foo
        uses: w1mvy/tf-moved-block-remover-action@v1
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
```
