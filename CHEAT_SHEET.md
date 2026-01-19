# WitcherScript Cheat Sheet

## Syntax at a Glance

### Variables
```witcher
contract gold = 100              # Variable (can be changed)
mutation MAX_LEVEL = 99          # Constant (cannot be changed)
```

### Output
```witcher
medallion("Hello")               # Print text
medallion(42)                    # Print number
medallion(truth)                 # Print boolean
```

### Arithmetic
```witcher
contract x = 10 + 5              # Addition
contract y = 10 - 5              # Subtraction
contract z = 10 * 5              # Multiplication
contract a = 10 / 5              # Division
contract b = 10 % 3              # Modulo
```

### Comparison & Logic
```witcher
x == 5                           # Equal
x != 5                           # Not equal
x > 5                            # Greater than
x < 5                            # Less than
x >= 5                           # Greater or equal
x <= 5                           # Less or equal

x and y                          # AND
x or y                           # OR
not x                            # NOT
```

### IF Statement (IGNI)
```witcher
igni x > 10 {
    medallion("Greater than 10")
} elixir {
    medallion("Not greater than 10")
}
```

### WHILE Loop (QUEN)
```witcher
contract count = 0
quen count < 5 {
    medallion(count)
    count = count + 1
}
```

### FOR Loop (YRDEN)
```witcher
contract items = ["sword", "shield", "potion"]
yrden item -> items {
    medallion(item)
}
```

### Functions (AARD)
```witcher
aard add(a, b) {
    contract result = a + b
    hunt result                  # Return the result
}

contract sum = add(10, 20)
medallion(sum)                   # Output: 30
```

### Arrays (Bestiary)
```witcher
contract monsters = ["Griffin", "Basilisk", "Drowner"]

medallion(monsters[0])           # First element: "Griffin"
medallion(monster_count(monsters))  # Length: 3
add_to_bestiary(monsters, "Leshen")  # Append
```

### Comments
```witcher
# This is a comment
medallion("test")  # End-line comment
```

## Built-in Functions Reference

| Function | Purpose | Example |
|----------|---------|---------|
| `medallion(x)` | Print | `medallion("Hello")` |
| `sigh(prompt)` | Input | `contract name = sigh("Name: ")` |
| `witcher_speed(text, n)` | Repeat | `witcher_speed("Ha", 3)` → `"HaHaHa"` |
| `monster_count(arr)` | Length | `monster_count([1,2,3])` → `3` |
| `add_to_bestiary(arr, x)` | Append | `add_to_bestiary(arr, "new")` |
| `hunter_instinct(x)` | Type | `hunter_instinct(42)` → `"number"` |
| `potion_effect(a, b)` | Add | `potion_effect(50, 30)` → `80` |

## Keywords Quick Reference

| Keyword | Type | Purpose |
|---------|------|---------|
| `igni` | Control | If statement |
| `quen` | Control | While loop |
| `yrden` | Control | For loop |
| `aard` | Function | Define function |
| `hunt` | Function | Return value |
| `elixir` | Control | Else clause |
| `contract` | Variable | Declare variable |
| `mutation` | Variable | Declare constant |
| `medallion` | I/O | Print output |
| `truth` | Value | Boolean true |
| `falsehood` | Value | Boolean false |
| `and` | Logic | AND operator |
| `or` | Logic | OR operator |
| `not` | Logic | NOT operator |

## Data Types

```witcher
contract number = 42             # Number type
contract decimal = 3.14          # Float type
contract text = "Geralt"         # Text/String type
contract bool_true = truth       # Boolean true
contract bool_false = falsehood  # Boolean false
contract array = [1, 2, 3]       # Array/Bestiary type
```

## Control Flow Patterns

### Check a Condition
```witcher
igni condition {
    medallion("true")
}
```

### Check a Condition with Alternative
```witcher
igni condition {
    medallion("true")
} elixir {
    medallion("false")
}
```

### Loop While True
```witcher
quen condition {
    medallion("looping")
}
```

### Loop Through Items
```witcher
yrden item -> items {
    medallion(item)
}
```

### Define and Use Function
```witcher
aard my_func(x) {
    hunt x * 2
}

contract result = my_func(5)
```

## Operator Precedence (Highest to Lowest)

1. Parentheses `()`
2. Unary `-`, `not`
3. Multiplication `*`, `/`, `%`
4. Addition `+`, `-`
5. Comparison `<`, `>`, `<=`, `>=`
6. Equality `==`, `!=`
7. Logical AND `and`
8. Logical OR `or`
9. Assignment `=`

## Common Mistakes & Solutions

### Mistake: Forgetting braces
```witcher
# ❌ Wrong
igni x > 5
    medallion("yes")

# ✅ Correct
igni x > 5 {
    medallion("yes")
}
```

### Mistake: Using = instead of ==
```witcher
# ❌ Wrong
igni x = 5 {
    medallion("yes")
}

# ✅ Correct
igni x == 5 {
    medallion("yes")
}
```

### Mistake: Forgetting hunt
```witcher
# ❌ Wrong
aard add(a, b) {
    contract result = a + b
}

# ✅ Correct
aard add(a, b) {
    contract result = a + b
    hunt result
}
```

### Mistake: Division by zero
```witcher
# ❌ Wrong
contract x = 10 / 0  # Error!

# ✅ Correct
contract y = 10 / 2
```

## Tips & Tricks

### String Multiplication
```witcher
contract attack = witcher_speed("SLASH ", 3)
medallion(attack)  # "SLASH SLASH SLASH "
```

### Check Variable Type
```witcher
contract type = hunter_instinct(42)
# Returns: "number"
```

### Create and Use Arrays
```witcher
contract arr = [10, 20, 30]
medallion(arr[0])           # 10
medallion(monster_count(arr))  # 3
add_to_bestiary(arr, 40)
```

### Countdown Loop
```witcher
contract x = 10
quen x > 0 {
    medallion(x)
    x = x - 1
}
```

### Conditional Assignment
```witcher
contract damage = 50
igni is_critical {
    damage = damage * 2
}
medallion(damage)
```

## Example Programs Structure

```witcher
# 1. Declare variables
contract player_hp = 100

# 2. Perform calculations
contract damage = 25
contract new_hp = player_hp - damage

# 3. Control flow
igni new_hp <= 0 {
    medallion("Defeated!")
} elixir {
    medallion("Still fighting!")
}

# 4. Use loops
yrden i -> [1, 2, 3] {
    medallion(i)
}

# 5. Define functions
aard calculate(x) {
    hunt x * 2
}

# 6. Output results
medallion(calculate(50))
```

## Running Programs

### Interactive Mode
```bash
python3 witcher_interpreter.py
```

### Run File
```bash
python3 witcher_interpreter.py program.witcher
```

### Run Examples
```bash
python3 witcher_interpreter.py example_programs/01_hello_world.witcher
python3 witcher_interpreter.py example_programs/02_monster_hunt.witcher
python3 witcher_interpreter.py example_programs/03_casting_signs.witcher
# ... etc
```

---

**Quick Reference Complete!** For more details, see [LANGUAGE_REFERENCE.md](LANGUAGE_REFERENCE.md)
