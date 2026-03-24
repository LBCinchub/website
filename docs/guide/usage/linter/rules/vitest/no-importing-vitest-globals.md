---
url: /docs/guide/usage/linter/rules/vitest/no-importing-vitest-globals.md
---

### What it does

The rule disallows import any vitest global function.

### Why is this bad?

If the project is configured to use globals from vitest, the rule ensure
that never imports the globals from `import` or `require`.

### Examples

Examples of **incorrect** code for this rule:

```js
import { test, expect } from "vitest";

test("foo", () => {
  expect(1).toBe(1);
});
```

```js
const { test, expect } = require("vitest");

test("foo", () => {
  expect(1).toBe(1);
});
```

Examples of **correct** code for this rule:

```js
test("foo", () => {
  expect(1).toBe(1);
});
```

## How to use

## References
