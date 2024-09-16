Check first whether there are any files that fail the formatting check

```shell
prettier . --check
```

```shell
prettier . --list-different
```

Do a commit, to have the current file versions available if `prettier` messes up.

Let `prettier` make formatting changes. This is done in place!

```shell
prettier . --write
```

See what changes `prettier` has made.

```shell
git diff
```
