# SonarQube Cache

Cache [SonarQube](https://www.sonarsource.com/products/sonarqube/) packages.

[![LICENSE](https://img.shields.io/github/license/sonaractions/cache?color=blue)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/sonaractions/cache?style=social)](https://github.com/sonaractions/cache)

## Usage

### Pre-requisites

Create a workflow `.yml` file in your repositories `.github/workflows` directory. For more information, reference the GitHub Help Documentation for [Creating a workflow file](https://help.github.com/en/articles/configuring-a-workflow#creating-a-workflow-file).

### Cache Details

This action currently caches the following directory:

- `~/.sonar/cache`

### Example workflow

```yaml
- uses: actions/checkout@v4

- uses: actions/setup-java@v4
  with:
    distribution: 'temurin'
    java-version: '17'
    cache: 'maven'

- uses: sonaractions/cache@v1

- uses: sonarsource/sonarqube-scan-action@v2
```

## Contributing

Check out [Contributing guide](.github/CONTRIBUTING.md) for ideas on contributing and setup steps for getting our repositories up.

## License

Licensed under the [MIT License](LICENSE).

