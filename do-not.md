I was wondering if it’s possible to check for syntax with Vale.
Like if I want to check for all uses of `do not` except when there is emphasis of some sort on the `not` (like `do **not**` in Markdown).
Is that easily achievable?

```yaml
extends: existence
message: "Don't use '%s'"
level: suggestion
ignorecase: true
# No markup processing.
scope: raw
tokens:
  - do not
```

In general, if you need to match against markup syntax in some way, use `scope: raw.