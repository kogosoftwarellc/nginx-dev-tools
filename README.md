# nginx-dev-tools
> A collection of tools to aid in nginx module development.

## Installation

```
git clone git@github.com:kogosoftwarellc/nginx-dev-tools
export PATH="$PWD/nginx-dev-tools:$PATH"
```

## Sample usage

```
ngx-add-source-to-project
ngx-configure
ngx-make-module
ngx-run-module
```

## Configuration

Configuration is stored in your project as a `.ngxrc` shell file.  The following
variables are supported:

* `NGX_VERSION` e.g. `1.11.5`
* `NGX_TEST_SRCS` e.g. `test/fixtures/nginx.conf dist/module.so`

## Scripts

* `ngx-configure` - Configures nginx source to compile the module.
* `ngx-make-module` - Runs `make modules` in the nginx source with the module.
* `ngx-run-module` - Copies files needed to run the module to /tmp and uses docker
  to run nginx inside a container with the provided files.
* `ngx-add-source-to-project` - Assumes you have the following directories in your
  project: `libs/`, `include/`.  Downloads nginx source code (specified by the
  `--nginx-version` option).  Source is placed under `libs/<nginx-version>` and
  header files are symlinked to `include/`.
