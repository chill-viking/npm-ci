# The NPM Dependency Installer

[![MegaLinter](https://github.com/chill-viking/npm-ci/workflows/MegaLinter/badge.svg?branch=main)](https://github.com/chill-viking/npm-ci/actions?query=workflow%3AMegaLinter+branch%3Amain)

## chill-viking/npm-ci

This GitHub action will install npm dependencies, using cache if already cached. The cache is based on available `package-lock.json` files in source.

Will log a warning if `node_modules` folder is not found after installing the dependencies.

## Usage

```yml
steps:
  - uses: chill-viking/npm-ci@latest
    name: Install dependencies
    with:
      working_directory: './npm-root-folder/'
```

The `latest` tag will be used for the latest release created, but specific version tags will be created if you need to use a specific version up to the minor version. See [releases](https://github.com/chill-viking/npm-ci/releases) for details on releases, or [tags](https://github.com/chill-viking/npm-ci/tags) to view other tags that are available.

Make sure to check out the repository before using this action.

```yml
steps:
  - uses: actions/checkout@v3
    name: Checkout repository

  - uses: chill-viking/npm-ci@latest
    name: Install dependencies
```

## Inputs

| Name                | Description                                                                 | Required | Default |
|---------------------|-----------------------------------------------------------------------------|----------|---------|
| `working_directory` | The directory to install dependencies in (location of `package-lock.json`). | No       | `./`    |

## Compatibility

[![Test chill-viking/npm-ci](https://github.com/chill-viking/npm-ci/actions/workflows/test-action.yml/badge.svg)](https://github.com/chill-viking/npm-ci/actions/workflows/test-action.yml)

The following runners and Node.js versions are checked in the workflow `Test chill-viking/npm-ci`

| Runner           | Node.js                |
|------------------|------------------------|
| `ubuntu-latest`  | `14.x`, `16.x`, `18.x` |
| `windows-latest` | `18.x`                 |
| `macos-latest`   | `18.x`                 |
