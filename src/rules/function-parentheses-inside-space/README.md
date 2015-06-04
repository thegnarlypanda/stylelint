# function-parentheses-inside-space

Require or disallow a single space on the inside of the parentheses of a function.

```css
    a { transform: translate( 1, 1 ); }
/**                         ↑      ↑
 * The space inside these two parentheses */
```

## Options

`string`: `"always"|"never"`

### `"always"`

There *must always* be a single space inside the parentheses.

The following patterns are considered warnings:

```css
a { transform: translate(1, 1); }
```

```css
a { transform: translate(1, 1 ); }
```

The following patterns are *not* considered warnings:

```css
a { transform: translate( 1, 1 ); }
```

### `"never"`

There *must never* be whitespace on the inside the parentheses.

The following patterns are considered warnings:

```css
a { transform: translate( 1, 1 ); }
```

```css
a { transform: translate(1, 1 ); }
```

The following patterns are *not* considered warnings:

```css
a { transform: translate(1, 1); }
```