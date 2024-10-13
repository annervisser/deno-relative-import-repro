## Broken:
```shell
deno install --force --global --name=deno-relative-import-repro main.ts
deno-relative-import-repro # results in error
```
Outputs error:
```text
error: Relative import path "@std/log" not prefixed with / or ./ or ../
  hint: If you want to use a JSR or npm package, try running `deno add jsr:@std/log` or `deno add npm:@std/log`
    at file:///home/anner/code/deno-relative-import-repro/main.ts:1:22
```

## Works:
```shell
deno install --force --config deno.json --global --name=deno-relative-import-repro main.ts
deno-relative-import-repro # works correctly
```
Output:
```text
INFO Hello World
```
