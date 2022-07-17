# Assign Author

Github Action that sets author to assignee when assignee is not set in issue or pull_request.

## Usage

```yaml
uses: MichinaoShimizu/assign-author@v1
```

## Example

```yaml
name: Assign author

on:
  pull_request:
    types:
      - opened
      - reopened
  issues:
    types:
      - opened
      - reopened

jobs:
  assign:
    runs-on: ubuntu-20.04
    timeout-minutes: 3
    steps:
      - uses: MichinaoShimizu/assign-author@v1
```
