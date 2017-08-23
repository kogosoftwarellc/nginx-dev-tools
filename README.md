# nginx-dev-tools
> A collection of tools to aid in nginx module development.

## Installation

```
git clone git@github.com:kogosoftwarellc/nginx-dev-tools
export PATH="$PWD/nginx-dev-tools:$PATH"
```

## Scripts

* `ngx-add-source-to-project` - Assumes you have the following directories in your
  project: `libs/`, `include/`.  Downloads nginx source code (specified by the
  `--nginx-version` option).  Source is placed under `libs/<nginx-version>` and
  header files are symlinked to `include/`.
