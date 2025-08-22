# Utilib

A collection of miscellaneous helpers for Alusus programming language.

---

## Misc Helpers

### charsPtrOrDefault

```
macro charsPtrOrDefault [val, default]
```

Returns the provided CharsPtr value, or the provided default if the value is 0.

### envVarOrDefault

```
macro envVarOrDefault [varName, defaultVal]
```

Fetch an environment variable or return a default string if the env var is not defined.

**Parameters**
* `varName` (CharsPtr) — name of the environment variable.
* `defaultVal` (CharsPtr) — fallback value if the env var is unset.

---

## AST Generation Helpers

These macros insert AST nodes at preprocessing time via `Spp.astMgr`.

### strLiteralFromVal

```
macro strLiteralFromVal [val]
```

Insert a string-literal AST from a raw `CharsPtr`.

**Parameters**
* `val` (CharsPtr) — the character data for the literal.

```
macro strLiteralFromVal [val, default]
```

Same as above, but uses `default` if `val` is null.

### strLiteralFromEnvVar

```
macro strLiteralFromEnvVar [varName]
```

Shortcut to create a string literal from an environment variable. The env var must be defined.

```
macro strLiteralFromEnvVar [varName, default]
```

Same as above with a fallback value.

### macro intLiteralFromInt [val]

Insert an integer-literal AST from a numeric `val`.

**Parameters**
* `val` (integral) — an integer value.

### intLiteralFromCharsPtr

```
macro intLiteralFromCharsPtr [val]
```

Insert an integer-literal AST from a string. The string must contain a number.

```
macro intLiteralFromCharsPtr [val, default]
```

Same as the above, but with a fallback value if the provided value is null.

### intLiteralFromEnvVar

```
macro intLiteralFromEnvVar [varName]
```

Create an integer‐literal AST from an environment variable string. The env var must be set.

```
macro intLiteralFromEnvVar [varName, default]
```

Same as the above, but With fallback default.

---

## Time/Date Helpers

### getCurrentStringDateTime

```
function getCurrentStringDateTime () => String
```

Return the current system date and time as a formatted string.

**Returns**

A `String` in the format: `YYYY-MM-DD HH:MM:SS`

```
function getCurrentStringDateTime (timestmap: ArchInt) => String
```

Return the date and time for the given timestamp as a formatted string.

**Returns**

A `String` in the format: `YYYY-MM-DD HH:MM:SS`

