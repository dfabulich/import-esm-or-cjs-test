This is how an ESM client can import an dual-package CJS/ESM package and get the expected results.

In the initial commit, the ESM client prints "Hello CJS" because the library's `package.json` doesn't include an `"exports"` section.

In the latest commit, the library's `package.json` includes an `"exports"` section; the ESM client now prints "Hello ESM".