# ci

共通CIワークフロー集

## Workflows

### `docker-build-push.yml`

DockerイメージをビルドしてGHCRにプッシュする。

**使い方:**

```yaml
jobs:
  build-and-push:
    uses: kkato/ci/.github/workflows/docker-build-push.yml@main
    permissions:
      contents: read
      packages: write
```

**inputs:**

| name | default | description |
|------|---------|-------------|
| `context` | `.` | Dockerビルドコンテキスト |
| `tags` | `ghcr.io/{repository}:latest` | イメージタグ |
