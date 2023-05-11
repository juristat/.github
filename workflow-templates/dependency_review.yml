name: 'Dependency Review'
on: [pull_request]

permissions:
  contents: read
  pull-requests: write

jobs:
  dependency-review:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repository
        uses: actions/checkout@v3
      - name: Dependency Review
        uses: actions/dependency-review-action@v3
        with:
          config-file: './.github/dependency-review-config.yaml'
          fail-on-severity: high
          comment-summary-in-pr: true
          deny-licenses: AGPL-1.0-or-later, AGPL-3.0-or-later
