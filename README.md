# WitcherScript - A Witcher 3-Inspired Programming Language

Welcome to **WitcherScript**, a programming language inspired by The Witcher 3: Wild Hunt. This language brings the magic, monsters, and lore of the game into a functional programming environment.

## 🧙 What is WitcherScript?

WitcherScript is a complete programming language featuring:
- **Witcher Signs as Keywords**: Use game signs (Igni, Quen, Yrden, Aard, Axii) for control flow
- **Monster-Themed Functions**: Functions inspired by witcher alchemy and hunting
- **Witcher Lore Integration**: Variables, functions, and concepts based on The Witcher 3 universe
- **Full Language Features**: Variables, functions, loops, conditionals, arrays, and more

## 📋 Quick Reference

### Witcher Signs (Control Flow)
| Sign | Keyword | Purpose |
|------|---------|---------|
| 🔥 Igni | `igni` | If statement |
| 🛡️ Quen | `quen` | While loop |
| ⏱️ Yrden | `yrden` | For loop |
| 💥 Aard | `aard` | Function definition |
| ✨ Axii | `axii` | Switch/case (reserved) |

### Basic Keywords
- `contract` - Declare a variable (like taking a Witcher contract)
- `mutation` - Declare a constant (permanent mutation)
- `medallion` - Print output (Witcher medallion alerts)
- `hunt` - Return from a function
- `elixir` - Else branch
- `grimoire` - Import another .witcher file (module system)

## 🚀 Getting Started

### Installation

No dependencies required! Just Python 3.6+

```bash
# Clone or download the project
cd /path/to/WitcherScript

# Run the interpreter
python3 witcher_interpreter.py
```

### Running Programs

#### Interactive Mode
```bash
python3 witcher_interpreter.py
witcher> medallion("Greetings, Witcher")
```

#### Run from File
```bash
python3 witcher_interpreter.py example_programs/01_hello_world.witcher
```

## 📚 Examples

### Hello World
```witcher
medallion("Hail, fellow Witcher!")
```

### Variables & Arithmetic
```witcher
contract gold = 100
contract reward = 50
contract total = gold + reward
medallion(total)  # Output: 150
```

### Functions (Casting Signs)
```witcher
aard cast_igni(intensity) {
    contract damage = 50 * intensity
    hunt damage
}

contract fire_damage = cast_igni(3)
medallion(fire_damage)  # Output: 150
```

### Loops
```witcher
contract counter = 1
quen counter <= 5 {
    medallion(counter)
    counter = counter + 1
}
```

### Arrays (Bestiary)
```witcher
contract monsters = ["Griffin", "Basilisk", "Drowner"]

yrden monster -> monsters {
    medallion(monster)
}

medallion(monster_count(monsters))  # Output: 3
```

### Conditional (IGNI Sign)
```witcher
contract monster_hp = 30

igni monster_hp <= 0 {
    medallion("Victory!")
} elixir {
    medallion("Still fighting!")
}
```

## 📁 Project Structure

```
WitcherScript/
├── witcher_interpreter.py          # Main interpreter (Lexer, Parser, Interpreter)
├── WitcherLang.md                  # Quick specification
├── LANGUAGE_REFERENCE.md           # Complete language reference
├── GRIMOIRE_GUIDE.md               # Module/import system documentation
├── README.md                        # This file
├── lib/                             # Reusable library files
│   ├── monster_helpers.witcher     # Monster utility functions
│   └── math_utils.witcher          # Math utility functions
└── example_programs/
    ├── 01_hello_world.witcher      # Basic output
    ├── 02_monster_hunt.witcher     # Variables & conditionals
    ├── 03_casting_signs.witcher    # Functions
    ├── 04_bestiary.witcher         # Arrays
    ├── 05_alchemy.witcher          # Complex conditionals
    ├── 06_quest_system.witcher     # Functions & arithmetic
    ├── 07_combat.witcher           # Loops & logic
    ├── 08_fibonacci.witcher        # Recursion
    ├── 09_bubble_sort.witcher      # Sorting algorithm
    ├── 10_grimoire_import.witcher  # Module imports
    └── 11_multiple_grimoires.witcher # Multiple imports
```

## 🎮 Built-in Functions

| Function | Purpose | Example |
|----------|---------|---------|
| `medallion(value)` | Print output | `medallion("Attack!")` |
| `sigh(prompt)` | Read input | `contract name = sigh("Your name: ")` |
| `witcher_speed(text, times)` | Repeat string | `witcher_speed("SLASH ", 3)` |
| `monster_count(array)` | Get array length | `monster_count([1,2,3])` |
| `add_to_bestiary(array, value)` | Append to array | `add_to_bestiary(monsters, "Leshen")` |
| `hunter_instinct(value)` | Get type info | `hunter_instinct(42)` → `"number"` |
| `potion_effect(a, b)` | Combine values | `potion_effect(50, 30)` → `80` |

## 📖 Language Features

### Data Types
- **Numbers**: Integers and floats (e.g., `42`, `3.14`)
- **Text**: Strings (e.g., `"Geralt of Rivia"`)
- **Truth/Falsehood**: Booleans (e.g., `truth`, `falsehood`)
- **Bestiary**: Arrays/Lists (e.g., `["item1", "item2"]`)

### Operators
- **Arithmetic**: `+`, `-`, `*`, `/`, `%`
- **Comparison**: `==`, `!=`, `<`, `>`, `<=`, `>=`
- **Logical**: `and`, `or`, `not`

### Comments
Use `#` for comments:
```witcher
# This is a comment
medallion("test")  # End-line comment
```

## 🎯 Example Programs

Run example programs to see WitcherScript in action:

```bash
# Hello World
python3 witcher_interpreter.py example_programs/01_hello_world.witcher

# Monster Hunt (variables & conditionals)
python3 witcher_interpreter.py example_programs/02_monster_hunt.witcher

# Casting Signs (functions)
python3 witcher_interpreter.py example_programs/03_casting_signs.witcher

# Bestiary (arrays & loops)
python3 witcher_interpreter.py example_programs/04_bestiary.witcher

# Alchemy (complex logic)
python3 witcher_interpreter.py example_programs/05_alchemy.witcher

# Quest System (function returns)
python3 witcher_interpreter.py example_programs/06_quest_system.witcher

# Combat Simulator (complex loops)
python3 witcher_interpreter.py example_programs/07_combat.witcher

# Fibonacci (recursion)
python3 witcher_interpreter.py example_programs/08_fibonacci.witcher
```

## 🛠️ Architecture

### Components

1. **Lexer** (`Lexer` class)
   - Tokenizes source code
   - Recognizes keywords, identifiers, operators, literals
   - Handles comments and strings

2. **Parser** (`Parser` class)
   - Builds Abstract Syntax Tree (AST)
   - Implements recursive descent parsing
   - Handles operator precedence

3. **Interpreter** (`Interpreter` class)
   - Executes the AST
   - Manages variable scopes (global and local)
   - Implements built-in functions
   - Handles function calls and returns

## 🐛 Error Handling

The interpreter provides helpful error messages:

```witcher
contract x = undefined_var  # Error: Undefined variable: undefined_var
contract y = 10 / 0         # Error: Division by zero!
```

## 🎓 Learn More

- See [LANGUAGE_REFERENCE.md](LANGUAGE_REFERENCE.md) for complete language documentation
- Check [example_programs/](example_programs/) for code samples
- Read [WitcherLang.md](WitcherLang.md) for quick specification

## 🎬 Game References

The language is inspired by The Witcher 3: Wild Hunt featuring:
- **Geralt of Rivia**: Main protagonist
- **Witcher Signs**: Igni, Quen, Yrden, Aard, Axii - magical abilities
- **Alchemy**: Potions and mixtures (Swallow, Tawny Owl, etc.)
- **Bestiary**: Collection of monsters encountered
- **Contracts**: Witcher jobs/quests

## 📝 License

This is a creative fan project inspired by CD Projekt Red's The Witcher 3: Wild Hunt.

## 🎉 Have Fun!

Start your witcher journey and write code with WitcherScript!

```witcher
medallion("May your blade be sharp and your wits sharper!")
```

---

**Questions?** Check the examples or read the full language reference!
