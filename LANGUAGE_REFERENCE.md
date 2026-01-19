# WitcherScript Language Reference

A complete programming language inspired by The Witcher 3, featuring Witcher signs, monsters, potions, and witcher lore.

## Table of Contents
1. [Quick Start](#quick-start)
2. [Keywords & Signs](#keywords--signs)
3. [Data Types](#data-types)
4. [Variables](#variables)
5. [Operators](#operators)
6. [Control Flow](#control-flow)
7. [Functions](#functions)
8. [Built-in Functions](#built-in-functions)
9. [Examples](#examples)

## Quick Start

### Hello, Geralt!
```witcher
medallion("Greetings, Witcher")
```

### Basic Arithmetic
```witcher
contract gold_reward = 100 + 50
medallion(gold_reward)
```

## Keywords & Signs

### Witcher Signs (Inspired by actual game signs)

| Keyword | Purpose | Inspiration | Example |
|---------|---------|-------------|---------|
| `igni` | Conditional (if) | Fire Sign - Ignites conditions | `igni x > 0 { ... }` |
| `quen` | Loop (while) | Protection Sign - Repeats guarded code | `quen x < 10 { x = x + 1 }` |
| `yrden` | Loop (for) | Slow Time Sign - Structured iteration | `yrden item -> items { ... }` |
| `aard` | Function definition | Blast Sign - Launches into action | `aard hunt_monster(name) { ... }` |
| `axii` | Multiple choices | Charm Sign - Multiple paths (reserved) | Future: `axii` |
| `elixir` | Alternative branch | Potions - Alternative effects | `igni ... { } elixir { }` |
| `contract` | Variable declaration | Witcher contract | `contract gold = 100` |
| `hunt` | Return from function | Witcher hunting/returning | `hunt result` |
| `mutation` | Constant declaration | Permanent mutation | `mutation MAX_LEVEL = 99` |
| `medallion` | Print output | Witcher medallion (output) | `medallion(message)` |

## Data Types

### Supported Types

```witcher
# Numbers (int and float)
contract damage = 50
contract critical_multiplier = 1.5

# Text (strings)
contract message = "Wolves hunt in packs"

# Booleans
contract monster_defeated = truth
contract medallion_vibrating = falsehood

# Arrays (bestiary - collection of monsters)
contract monsters = ["Griffin", "Basilisk", "Drowner"]
```

## Variables

### Declaration with `contract`
```witcher
contract player_level = 1
contract current_location = "White Orchard"
contract inventory = ["Steel Sword", "Silver Sword"]
```

### Declaration with `mutation` (constants)
```witcher
mutation MAX_STAMINA = 100
mutation WITCHER_NAME = "Geralt"
```

### Assignment
```witcher
contract gold = 0
gold = gold + 50  # Assignment
```

## Operators

### Arithmetic
```witcher
contract a = 10 + 5      # Addition
contract b = 10 - 5      # Subtraction
contract c = 10 * 5      # Multiplication
contract d = 10 / 5      # Division
contract e = 10 % 3      # Modulo (remainder)
```

### Comparison
```witcher
truth  == falsehood      # Equal
truth  != falsehood      # Not equal
10 > 5                   # Greater than
10 < 5                   # Less than
10 >= 10                 # Greater or equal
10 <= 10                 # Less or equal
```

### Logical
```witcher
truth and truth          # AND
truth or falsehood       # OR
not truth                # NOT
```

## Control Flow

### If Statement (IGNI)
```witcher
contract monster_hp = 30

igni monster_hp < 0 {
    medallion("Monster defeated!")
} elixir {
    medallion("Monster still alive!")
}
```

### While Loop (QUEN)
```witcher
contract stamina = 100

quen stamina > 0 {
    medallion(stamina)
    stamina = stamina - 10
}
```

### For Loop (YRDEN)
```witcher
contract monster_names = ["Griffin", "Wyvern", "Basilisk"]

yrden name -> monster_names {
    medallion("Hunting: ")
    medallion(name)
}
```

## Functions

### Defining Functions (AARD)
```witcher
aard cast_igni(enemies_count) {
    contract damage = 50 * enemies_count
    hunt damage
}
```

### Calling Functions
```witcher
contract fire_damage = cast_igni(3)
medallion(fire_damage)
```

### Functions with Multiple Parameters
```witcher
aard calculate_total_damage(base_damage, critical_chance) {
    contract total = base_damage + (base_damage * critical_chance)
    hunt total
}

contract damage = calculate_total_damage(100, 0.5)
medallion(damage)  # Output: 150
```

## Built-in Functions

### medallion(value) - Print Output
```witcher
medallion("Slay them all!")
medallion(42)
medallion(truth)
```

### sigh(prompt) - Read Input
```witcher
contract player_name = sigh("Enter your name: ")
medallion(player_name)
```

### witcher_speed(text, times) - Repeat String
```witcher
contract attack = witcher_speed("SLASH ", 3)
medallion(attack)  # Output: SLASH SLASH SLASH
```

### monster_count(bestiary) - Get Length
```witcher
contract inventory = ["Sword", "Potion", "Bomb"]
contract item_count = monster_count(inventory)
medallion(item_count)  # Output: 3
```

### add_to_bestiary(bestiary, value) - Append to Array
```witcher
contract potions = ["White Honey", "Swallow"]
add_to_bestiary(potions, "Tawny Owl")
medallion(potions)
```

### hunter_instinct(value) - Get Type Info
```witcher
contract value = 42
contract type_info = hunter_instinct(value)
medallion(type_info)  # Output: number
```

### potion_effect(a, b) - Combine Values
```witcher
contract effect1 = 50
contract effect2 = 30
contract total_effect = potion_effect(effect1, effect2)
medallion(total_effect)  # Output: 80
```

## Array Access

```witcher
contract swords = ["Balmoral", "Renfri's Gift", "Meteor"]
medallion(swords[0])  # Output: Balmoral
medallion(swords[1])  # Output: Renfri's Gift
```

## Comments

Use `#` for comments:
```witcher
# This is a comment
medallion("Fighting monsters")  # End-line comment
```

## Complete Examples

See the `example_programs/` directory for full examples.
