# Type Guard Issue with string | null in TypeScript

This example demonstrates a common error when using type guards with the `string | null` type in TypeScript.  The type guard correctly handles `null`, but it fails to handle `undefined`, resulting in a runtime error.

The `greet` function attempts to safely handle nullish values, but it only explicitly checks for `null`.  When `undefined` is passed, it bypasses the null check and throws an error during string interpolation.

The solution involves explicitly handling `undefined` or using a more comprehensive type guard.