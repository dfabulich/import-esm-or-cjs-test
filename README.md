This is how an ESM client can import an dual-package CJS/ESM package and get the expected results.

In the initial commit, the ESM client prints "Hello CJS" because the library's `package.json` doesn't include an `"exports"` section.

In the latest commit, the library's `package.json` includes an `"exports"` section; the ESM client now prints "Hello ESM".

In the "tricky" branch of this repository, the library uses a mix of CJS and ESM, putting all ESM in an `esm/` subdirectory, by including a one-liner `esm/package.json` file that just says `{"type": "module"}`.