Steps to reproduce:

1. Clone this repository
2. `npm install -g ember-cli@2.14`
3. `ember build --environment 'production'`
4. `grep sourceMappingURL dist/assets/sourcemap-test-*.js`
  Result: `//# sourceMappingURL=https://example.com/assets/sourcemap-test-219e2f6e4d66995a385d696cae88146b.map`
5. Note that `sourceMappingURL` is missing the `rootURL`. It should be `https://example.com/subpath/assets/sourcemap-test-219e2f6e4d66995a385d696cae88146b.map`
