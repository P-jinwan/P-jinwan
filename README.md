👋 Hi there, I'm jinwan

😄 I'm learning Python and I'm very interested in AI!

🔥 It's still not enough, but I'll study hard and become the best IT person! Can you help me grow up together?


name: PR Labeler
on:
  pull_request:
    types: [opened]

jobs:
  pr-labeler:
    runs-on: ubuntu-latest
    steps:
      - uses: TimonVS/pr-labeler-action@v3
        with:
          configuration-path: .github/pr-labeler.yml # optional, .github/pr-labeler.yml is the default value
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }} 
