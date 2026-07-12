# aux4 releaser install

## help

### should list the --force flag

```execute
aux4 aux4 releaser install --help
```

```expect:partial
--force
```

### should describe the --force flag

```execute
aux4 aux4 releaser install --help
```

```expect:partial
ignoring dependents
```

### should still list the --dir flag

```execute
aux4 aux4 releaser install --help
```

```expect:partial
--dir
```
