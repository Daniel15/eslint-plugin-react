# Enforce boolean attributes notation in JSX (jsx-boolean-value)

In JSX when using a boolean attribute you can set the attribute value to `true` or omit the value. This rule will enforce one or the other to keep consistency in your code.

## Rule Details

This rule takes one argument. If it is `"always"` then it warns whenever an attribute is missing it's value. If `"never"` then it warns if an attribute has a `true` value. The default value of this option is `"never"`.

The following patterns are considered warnings when configured `"never"`:

```js
var Hello = <Hello personal={true} />;
```

The following patterns are not considered warnings when configured `"never"`:

```js
var Hello = <Hello personal />;
```

The following patterns are considered warnings when configured `"always"`:

```js
var Hello = <Hello personal />;
```

The following patterns are not considered warnings when configured `"always"`:

```js
var Hello = <Hello personal={true} />;
```

## When Not To Use It

If you do not want to enforce any style for boolean attributes, then you can disable this rule.
