# Groovy to Painless Cheatsheet

## How to contribute

See contributing.MD

## Examples

### Test if field exists

Groovy

```
if (ctx._source.user)
```

Painless

```
if (ctx._source.user != null)
```

or alternatively:

```
boolean isValue(def x){ x != null } if (isValue(ctx._source.user))
```

## TODO

A list of Groovy examples/snippets/functions that need Painless equivalent examples.

  - this.binding.getVariable("Foo")
  - this.binding.hasVariable("Bar")
  - submit a PR to add more...
