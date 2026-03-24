---
url: /docs/guide/usage/linter/rules/typescript/class-literal-property-style.md
---

### What it does

Enforces a consistent style for exposing literal values on classes.

### Why is this bad?

Mixing readonly fields and trivial literal getters for the same kind of value
makes class APIs inconsistent and harder to scan.

### Examples

Examples of **incorrect** code for this rule (default `"fields"`):

```ts
class C {
  get name() {
    return "oxc";
  }
}
```

Examples of **correct** code for this rule:

```ts
class C {
  readonly name = "oxc";
}
```

## Configuration

This rule accepts one of the following string values:

type: `"fields" | "getters"`

## How to use

## References
