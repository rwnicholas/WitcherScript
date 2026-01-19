# Quick Start Guide - WitcherScript

## Installation
No dependencies needed! Just Python 3.6+

## Running Your First Program

### 1. Hello World
```witcher
medallion("Greetings, Witcher!")
```

Save as `hello.witcher` and run:
```bash
python3 witcher_interpreter.py hello.witcher
```

### 2. Variables & Math
```witcher
contract gold = 100
contract bounty = 50
contract total = gold + bounty

medallion("Total gold: ")
medallion(total)
```

### 3. Conditionals (IGNI Sign)
```witcher
contract level = 45

igni level >= 50 {
    medallion("You are a master witcher!")
} elixir {
    medallion("You must train more, witcher.")
}
```

### 4. Loops (QUEN Sign)
```witcher
contract count = 1
quen count <= 5 {
    medallion(count)
    count = count + 1
}
```

### 5. Arrays & For Loops (YRDEN Sign)
```witcher
contract swords = ["Steel", "Silver", "Leather"]

yrden sword -> swords {
    medallion(sword)
}
```

### 6. Functions (AARD Sign)
```witcher
aard greet(name) {
    medallion("Greetings, ")
    medallion(name)
    hunt
}

greet("Geralt")
```

### 7. Functions with Returns
```witcher
aard calculate_damage(base_damage, multiplier) {
    contract total = base_damage * multiplier
    hunt total
}

contract damage = calculate_damage(50, 1.5)
medallion(damage)
```

## Interactive Mode
Run without arguments to use interactive mode:
```bash
python3 witcher_interpreter.py
witcher> contract x = 10
witcher> medallion(x)
10
witcher> quit
```

## Key Concepts

### Contract (Variable)
Think of `contract` like taking a Witcher contract - it's an agreement to store a value:
```witcher
contract gold = 100
```

### Mutation (Constant)
A permanent mutation - unchangeable throughout the program:
```witcher
mutation MAX_LEVEL = 99
```

### Medallion (Output)
Your Witcher medallion vibrates with output:
```witcher
medallion("Message")
medallion(42)
```

### Hunting (Return)
Returning from a contract hunt with your prize:
```witcher
aard hunt_monster(monster_type) {
    contract reward = 500
    hunt reward  # Return the reward
}
```

### Signs (Control Flow)

**IGNI** - Fire Sign (if statement):
```witcher
igni condition {
    medallion("True branch")
} elixir {
    medallion("False branch")
}
```

**QUEN** - Protection Sign (while loop):
```witcher
quen x < 10 {
    x = x + 1
}
```

**YRDEN** - Slow Time Sign (for loop):
```witcher
yrden item -> items {
    medallion(item)
}
```

**AARD** - Blast Sign (function definition):
```witcher
aard my_function(param1, param2) {
    hunt param1 + param2
}
```

## Common Patterns

### Repeating Action
```witcher
contract times = 3
yrden i -> [1, 2, 3] {
    medallion("Attack!")
}
```

### Conditional Execution
```witcher
igni monster_hp <= 0 {
    medallion("Victory!")
}
```

### Counting Down
```witcher
contract x = 10
quen x > 0 {
    medallion(x)
    x = x - 1
}
```

### Collecting Results
```witcher
aard sum(a, b, c) {
    contract total = a + b + c
    hunt total
}

contract result = sum(10, 20, 30)
medallion(result)  # 60
```

## Operators

| Operator | Purpose | Example |
|----------|---------|---------|
| `+` | Add | `10 + 5` |
| `-` | Subtract | `10 - 5` |
| `*` | Multiply | `10 * 5` |
| `/` | Divide | `10 / 5` |
| `%` | Modulo | `10 % 3` |
| `==` | Equal | `x == 5` |
| `!=` | Not equal | `x != 5` |
| `>` | Greater | `x > 5` |
| `<` | Less | `x < 5` |
| `>=` | Greater/equal | `x >= 5` |
| `<=` | Less/equal | `x <= 5` |
| `and` | Logical AND | `x and y` |
| `or` | Logical OR | `x or y` |
| `not` | Logical NOT | `not x` |

## Built-in Functions

```witcher
# Print
medallion("text")

# Input (read from user)
contract input = sigh("Enter something: ")

# String repeat
contract repeated = witcher_speed("Ha", 3)  # "HaHaHa"

# Array length
contract length = monster_count([1, 2, 3])  # 3

# Append to array
add_to_bestiary(my_array, new_item)

# Get type
contract type = hunter_instinct(42)  # "number"

# Combine
contract sum = potion_effect(50, 30)  # 80
```

## Tips & Tricks

1. **Comments** - Use `#` for comments:
   ```witcher
   # This is a comment
   medallion("test")  # End-line comment
   ```

2. **Multi-line programs** - Separate statements with newlines or use `;`

3. **Nested functions** - Call functions inside functions:
   ```witcher
   aard outer() {
       contract x = inner_function()
       hunt x
   }
   ```

4. **Array indexing** - Access elements:
   ```witcher
   contract arr = [10, 20, 30]
   medallion(arr[0])  # 10
   ```

## Next Steps

1. Check out the example programs in `example_programs/`
2. Read [LANGUAGE_REFERENCE.md](LANGUAGE_REFERENCE.md) for complete documentation
3. Experiment with your own programs!

Enjoy your WitcherScript journey! 🧙‍♂️⚔️
