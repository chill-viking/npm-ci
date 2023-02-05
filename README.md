# chill-viking/npm-ci

Install npm dependencies, using cache if already cached. Cache based on available `package-lock.json` files in source.

Will log a warning if `node_modules` folder is not found after installing the dependencies.

## Usage

```yml
steps:
  - uses: chill-viking/npm-ci@latest
    name: Install dependencies
    with:
      working_directory: './npm-root-folder/'
```

The `latest` tag will be used for the latest release created, but specific version tags will be created if need to use a specific version up to the minor version. See [releases](https://github.com/chill-viking/npm-ci/releases) for details on releases, or [tags](https://github.com/chill-viking/npm-ci/tags) to view other tags that are available.

## Inputs

| Name                | Description                                 | Required | Default |
|---------------------|---------------------------------------------|----------|---------|
| `working_directory` | The directory to run the workflow from. 1️⃣ | No       | `./`    |

Notes:
1️⃣ Make sure to suffix `working_directory` path with `/`, as `node_modules` will be appended to specify folder to be cached
