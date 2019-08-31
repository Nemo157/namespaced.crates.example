A test of using DNS namespaced crate registries

Setup a symlink so that there's a well-known path for the registry `file://`
urls to use.

```console
> ln -s "$(pwd)" /tmp/namespaced.crates.example
```

An example of depending on dependencies from multiple crates:

```console
> cd example-lib
> cargo build
```

An example of relying on a crate without having to know where its dependencies
come from:

```console
> cd example-lib2
> cargo build
```
