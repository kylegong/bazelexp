# Repro of bazel issue

```
bazel build ts:demo
```

Yields the following error:

```
ERROR: bazelexp/ts/BUILD.bazel:9:11: every rule of type ts_library implicitly depends upon the target '@npm//typescript:typescript__typings', but this target could not be found because of: no such target '@npm//typescript:typescript__typings': target 'typescript__typings' not declared in package 'typescript' defined by e105150ea7c712b5a55e3b888d9666e0/external/npm/typescript/BUILD.bazel
```

`bazel --version`

`bazel 5.1.1`