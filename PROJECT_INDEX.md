# WitcherScript v1.1 - Complete Project Guide

**WitcherScript is now complete with module system (grimoire) support!** ✨

## 🎯 What is WitcherScript?

A complete, functional programming language inspired by The Witcher 3: Wild Hunt. Features Witcher Signs as keywords, monster-themed functions, and full language capabilities including a module system.

## 🆕 What's New in v1.1?

**Grimoire Module System** - Import functions from other .witcher files!

```witcher
grimoire "lib/utils.witcher"
medallion(my_function(42))
```

## 📋 Quick Navigation

### Getting Started (Pick One)
- **First time?** → [QUICK_START.md](QUICK_START.md)
- **Want overview?** → [00_START_HERE.txt](00_START_HERE.txt)
- **New to v1.1?** → [WHATS_NEW.md](WHATS_NEW.md)

### Grimoire (Module System)
- **Quick reference** → [GRIMOIRE_SUMMARY.txt](GRIMOIRE_SUMMARY.txt)
- **Full guide** → [GRIMOIRE_GUIDE.md](GRIMOIRE_GUIDE.md)
- **Technical details** → [GRIMOIRE_IMPLEMENTATION.md](GRIMOIRE_IMPLEMENTATION.md)
- **Status report** → [GRIMOIRE_STATUS.txt](GRIMOIRE_STATUS.txt)

### Language Features
- **Cheat sheet** → [CHEAT_SHEET.md](CHEAT_SHEET.md)
- **Complete reference** → [LANGUAGE_REFERENCE.md](LANGUAGE_REFERENCE.md)
- **Language spec** → [WitcherLang.md](WitcherLang.md)

### Learn by Example
- **All examples** → [example_programs/](example_programs/)
- **01_hello_world.witcher** - Basic output
- **02_monster_hunt.witcher** - Variables & conditionals
- **03_casting_signs.witcher** - Functions
- **04_bestiary.witcher** - Arrays
- **05_alchemy.witcher** - Complex conditionals
- **06_quest_system.witcher** - Multiple functions
- **07_combat.witcher** - While loops
- **08_fibonacci.witcher** - Recursion
- **09_bubble_sort.witcher** - Sorting algorithm
- **10_grimoire_import.witcher** - Single import demo ⭐
- **11_multiple_grimoires.witcher** - Multiple imports demo ⭐

### Reusable Libraries
- **monster_helpers.witcher** - Monster hunting functions
- **math_utils.witcher** - Math utilities

## 🚀 Quick Start (60 seconds)

### Installation
```bash
# No dependencies, just Python 3.6+
cd /path/to/WitcherScript
```

### Run Your First Program
```bash
python3 witcher_interpreter.py example_programs/01_hello_world.witcher
```

### Try Grimoire (New!)
```bash
python3 witcher_interpreter.py example_programs/10_grimoire_import.witcher
```

### Interactive Mode
```bash
python3 witcher_interpreter.py
witcher> medallion("Hello, Witcher!")
```

## 💡 Usage Examples

### Basic Output
```witcher
medallion("Greetings!")
```

### Variables & Conditionals
```witcher
contract gold = 100
igni gold > 50 {
    medallion("Rich!")
}
```

### Functions
```witcher
aard greet(name) {
    hunt "Hello, " + name
}

medallion(greet("Geralt"))
```

### Loops
```witcher
yrden i -> [1, 2, 3, 4, 5] {
    medallion(i)
}
```

### Grimoire (NEW!)
```witcher
grimoire "lib/helpers.witcher"
medallion(calculate_reward(18))
```

## 🎮 Language Keywords

| Keyword | Purpose | Example |
|---------|---------|---------|
| `igni` | If statement | `igni x > 5 { ... }` |
| `quen` | While loop | `quen x < 10 { ... }` |
| `yrden` | For loop | `yrden i -> array { ... }` |
| `aard` | Function def | `aard func(x) { ... }` |
| `hunt` | Return | `hunt result` |
| `elixir` | Else | `} elixir { ...` |
| `contract` | Variable | `contract x = 5` |
| `mutation` | Constant | `mutation PI = 3.14` |
| `medallion` | Print | `medallion(x)` |
| `grimoire` | Import | `grimoire "lib/file.witcher"` |

## 📊 Project Statistics

- **Interpreter:** 1090 lines of Python
- **Keywords:** 15
- **Built-in Functions:** 7
- **Data Types:** 4
- **Example Programs:** 10
- **Library Files:** 2
- **Documentation Files:** 14

## ✨ Key Features

✅ Full lexer with 17 token types
✅ Recursive descent parser with proper precedence
✅ Tree-walking interpreter with scope management
✅ Variables and constants
✅ Functions with parameters and returns
✅ Arrays with element assignment
✅ String concatenation with type conversion
✅ Control flow (if/else, while, for)
✅ Recursion support
✅ Comments
✅ **Module system (grimoire)** ⭐ NEW
✅ Circular import detection
✅ Clear error messages

## 🎯 Common Tasks

### Create a Library File

Create `lib/my_utils.witcher`:
```witcher
aard square(x) {
    hunt x * x
}

aard is_positive(x) {
    hunt x > 0
}
```

### Use the Library

Create `main.witcher`:
```witcher
grimoire "lib/my_utils.witcher"

medallion(square(5))
medallion(is_positive(-3))
```

### Run
```bash
python3 witcher_interpreter.py main.witcher
```

## 📚 Documentation Organization

**For Learning:**
1. [00_START_HERE.txt](00_START_HERE.txt) - Overview
2. [QUICK_START.md](QUICK_START.md) - Getting started
3. [CHEAT_SHEET.md](CHEAT_SHEET.md) - Quick reference
4. Run example programs

**For Reference:**
1. [LANGUAGE_REFERENCE.md](LANGUAGE_REFERENCE.md) - Complete spec
2. [GRIMOIRE_GUIDE.md](GRIMOIRE_GUIDE.md) - Module system
3. [WitcherLang.md](WitcherLang.md) - Language overview

**For Implementation Details:**
1. [PROJECT_SUMMARY.md](PROJECT_SUMMARY.md) - Architecture
2. [GRIMOIRE_IMPLEMENTATION.md](GRIMOIRE_IMPLEMENTATION.md) - Module system details

**For Project Status:**
1. [WHATS_NEW.md](WHATS_NEW.md) - Version 1.1 changes
2. [GRIMOIRE_STATUS.txt](GRIMOIRE_STATUS.txt) - Module system status
3. [COMPLETE_PROJECT_OVERVIEW.md](COMPLETE_PROJECT_OVERVIEW.md) - Full status

## 🆘 Troubleshooting

**"File not found: ..."**
- Check the file path in your grimoire statement
- Use relative paths from current directory or absolute paths

**"Circular import detected: ..."**
- Your import structure has a cycle (A imports B, B imports A)
- Redesign your module structure

**"Parser error ..."**
- Check syntax in your .witcher file
- Look at example programs for correct syntax

**"Undefined variable/function ..."**
- Make sure you imported the file with grimoire
- Check spelling of function/variable name

## 🎓 Learning Path

1. **Basics** (5 min)
   - Read: [QUICK_START.md](QUICK_START.md)
   - Try: `example_programs/01_hello_world.witcher`

2. **Variables & Control Flow** (15 min)
   - Read: [CHEAT_SHEET.md](CHEAT_SHEET.md)
   - Try: Examples 02-07

3. **Functions & Recursion** (20 min)
   - Read: [LANGUAGE_REFERENCE.md](LANGUAGE_REFERENCE.md)
   - Try: Examples 03, 06, 08

4. **Advanced Features** (20 min)
   - Read: [GRIMOIRE_GUIDE.md](GRIMOIRE_GUIDE.md)
   - Try: Examples 09-11

5. **Build Something!** (∞ time)
   - Create your own programs
   - Organize code into libraries
   - Share and enjoy!

## 🎮 Why "WitcherScript"?

The language uses Witcher Signs as keywords, monster-themed functions, and lore from The Witcher 3. This makes programming feel like casting spells and hunting monsters! 🧙‍♂️⚔️

## 📄 All Files

**Core:**
- `witcher_interpreter.py` - The interpreter (lexer, parser, evaluator)

**Libraries:**
- `lib/monster_helpers.witcher` - Monster utilities
- `lib/math_utils.witcher` - Math functions

**Examples:**
- `example_programs/01-09_*.witcher` - Various language features
- `example_programs/10_grimoire_import.witcher` - Single import
- `example_programs/11_multiple_grimoires.witcher` - Multiple imports

**Documentation:**
- `README.md` - Main documentation
- `QUICK_START.md` - Getting started guide
- `CHEAT_SHEET.md` - Quick reference
- `LANGUAGE_REFERENCE.md` - Complete specification
- `WitcherLang.md` - Language overview
- `PROJECT_SUMMARY.md` - Implementation details
- `GRIMOIRE_GUIDE.md` - Module system guide
- `GRIMOIRE_IMPLEMENTATION.md` - Technical details
- `GRIMOIRE_STATUS.txt` - Status report
- `WHATS_NEW.md` - Version 1.1 changes
- `COMPLETE_PROJECT_OVERVIEW.md` - Project overview
- `INDEX.md` - Documentation index

## 🚀 What's Next?

Possible future enhancements:
- Standard library with more utilities
- File I/O support
- More advanced data structures
- Performance optimizations
- Compiler/bytecode interpreter
- Debugger support

## ✅ Verification

All tests passing:
- ✓ Existing programs (01-09) still work
- ✓ Single grimoire import works (10)
- ✓ Multiple grimoires work (11)
- ✓ Circular imports detected
- ✓ File not found errors handled
- ✓ 100% backward compatibility

## 📞 Support

For questions or issues:
1. Check the documentation for your topic
2. Review example programs
3. Read error messages carefully
4. Check LANGUAGE_REFERENCE.md

## 🎉 Ready?

Start here: [QUICK_START.md](QUICK_START.md)

Or jump to grimoire: [GRIMOIRE_GUIDE.md](GRIMOIRE_GUIDE.md)

Or see all examples: [example_programs/](example_programs/)

---

**May your code compile cleanly and your monsters fall swiftly!** ⚔️🧙‍♂️✨
