# Grimoire (Module System) Guide

The **grimoire** keyword allows you to import functions and variables from other `.witcher` files, enabling code reuse and modular programming.

## Syntax

```witcher
grimoire "path/to/file.witcher"
```

## How It Works

1. The grimoire statement loads and executes another `.witcher` file
2. All functions and variables defined in that file become available in the current scope
3. Circular imports are detected and prevented
4. File paths can be relative or absolute

## Examples

### Basic Import

`lib/utils.witcher`:
```witcher
aard add(a, b) {
    hunt a + b
}

aard multiply(a, b) {
    hunt a * b
}
```

`main.witcher`:
```witcher
grimoire "lib/utils.witcher"

medallion(add(5, 3))      # Output: 8.0
medallion(multiply(4, 7)) # Output: 28.0
```

### Multiple Imports

```witcher
grimoire "lib/math_utils.witcher"
grimoire "lib/string_utils.witcher"
grimoire "lib/array_utils.witcher"

# Now all functions from all three files are available
medallion(factorial(5))
medallion(to_uppercase("hello"))
medallion(sum_array([1, 2, 3, 4, 5]))
```

### Organizing Code

Create a `lib/` directory for reusable functions:

```
project/
├── main.witcher
├── lib/
│   ├── monster_helpers.witcher
│   ├── math_utils.witcher
│   └── quest_system.witcher
└── example_programs/
```

Then import what you need:
```witcher
grimoire "lib/monster_helpers.witcher"
grimoire "lib/math_utils.witcher"
```

## Path Resolution

- **Relative paths** are resolved relative to the current working directory
- **Absolute paths** work as well
- File must have a `.witcher` extension

## Circular Import Detection

If File A imports File B, and File B tries to import File A, you'll get an error:

```
Error: Circular import detected: lib/utils.witcher
```

## Error Handling

If a grimoire file has syntax errors or doesn't exist:

```
Error importing lib/utils.witcher: File not found
Error importing lib/utils.witcher: Parser error at 5:1: ...
```

## Best Practices

1. **Organize by functionality** - Put related functions in the same grimoire file
2. **Use clear names** - Name your grimoire files descriptively
3. **Keep files focused** - One grimoire should have one clear purpose
4. **Document your functions** - Add comments explaining what functions do
5. **Avoid circular dependencies** - Design your module structure carefully

## Real-World Example

See [example_programs/10_grimoire_import.witcher](../example_programs/10_grimoire_import.witcher) and [example_programs/11_multiple_grimoires.witcher](../example_programs/11_multiple_grimoires.witcher) for complete working examples.

## Importing vs. Executing

- When you `grimoire "file.witcher"`, the file is **executed immediately**
- Functions are **defined in global scope** and can be called from anywhere
- Variables are also added to global scope
- If you import the same file twice, it's only executed the first time (tracked internally)
