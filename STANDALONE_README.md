# 🧙‍♂️ WitcherScript - Standalone Distribution

**A complete programming language inspired by The Witcher 3: Wild Hunt**

## Quick Installation (30 seconds)

### Linux/Mac
```bash
cd /path/to/WitcherScript
./install.sh

# Add to shell config (~/.bashrc or ~/.zshrc)
export PATH="$HOME/.local/bin:$PATH"

# Restart terminal and run:
witcher example_programs/01_hello_world.witcher
```

### Windows (with Python)
```bash
# Copy witcher_interpreter.py and witcher script to a directory in PATH
# Or use: pip install -e .
```

## What is WitcherScript?

A full-featured programming language with:
- **Witcher 3 Theming**: Keywords based on Witcher Signs (Igni, Quen, Yrden, Aard)
- **Complete Interpreter**: Lexer, Parser, Tree-walking Evaluator
- **Modern Features**: Variables, functions, arrays, recursion, modules
- **Grimoire System**: Import functions from other .witcher files
- **VS Code Extension**: Full syntax highlighting and 31+ snippets
- **Zero Dependencies**: Pure Python, runs anywhere

## Running Programs

### After Installation
```bash
witcher program.witcher
witcher example_programs/10_grimoire_import.witcher
```

### Direct Execution
```bash
python3 witcher_interpreter.py program.witcher
./witcher program.witcher
```

## Simple Example

Create `hello.witcher`:
```witcher
# Comments start with #
contract greeting = "Hail, Witcher!"
medallion(greeting)  # medallion = print
```

Run it:
```bash
witcher hello.witcher
# Output: Hail, Witcher!
```

## Language Features

### Variables & Functions
```witcher
contract x = 42
aard add(a, b) {
    hunt a + b
}
medallion(add(x, 8))  # Output: 50.0
```

### Control Flow
```witcher
igni x > 100 {
    medallion("Big")
} elixir {
    medallion("Small")
}
```

### Loops
```witcher
# While loop (quen = Protection Sign)
quen x < 5 {
    medallion(x)
    x = x + 1
}

# For loop (yrden = Slow Time Sign)
yrden monster -> ["Griffin", "Basilisk"] {
    medallion(monster)
}
```

### Arrays & Grimoire
```witcher
# Create bestiary (array)
contract monsters = ["Griffin", "Basilisk"]
medallion(monster_count(monsters))

# Import functions from another file
grimoire "lib/helpers.witcher"
medallion(my_function(42))
```

## Files in Distribution

| File | Purpose |
|------|---------|
| `witcher` | Command-line wrapper (executable) |
| `witcher_interpreter.py` | Core interpreter engine |
| `setup.py` | pip installation config |
| `install.sh` | Automated installer |
| `example_programs/` | 10 example programs |
| `lib/` | Reusable libraries |
| `DEPLOYMENT.md` | Detailed installation guide |
| `README.md` | Full documentation |

## Installation Methods

### Method 1: Using install.sh (Recommended)
```bash
./install.sh
```

### Method 2: Manual (Add to PATH)
```bash
export PATH="/path/to/witcherscript:$PATH"
```

### Method 3: pip Installation
```bash
pip install -e .
# Or: pip install witcherscript (when published)
```

### Method 4: System-wide (Linux/Mac)
```bash
sudo cp witcher /usr/local/bin/
sudo cp witcher_interpreter.py /usr/local/bin/
```

## Usage

```bash
# Run a program
witcher program.witcher

# Run an example
witcher example_programs/01_hello_world.witcher

# Interactive mode
witcher
witcher> medallion("Hello!")

# Get help
witcher
```

## 10 Example Programs

1. **01_hello_world.witcher** - Basic output
2. **02_monster_hunt.witcher** - Variables & conditionals
3. **03_casting_signs.witcher** - Functions
4. **04_bestiary.witcher** - Arrays
5. **05_alchemy.witcher** - Complex conditionals
6. **06_quest_system.witcher** - Multiple functions
7. **07_combat.witcher** - Loops
8. **08_fibonacci.witcher** - Recursion
9. **10_grimoire_import.witcher** - Module imports ⭐
10. **11_multiple_grimoires.witcher** - Multiple imports ⭐

Run any example:
```bash
witcher example_programs/10_grimoire_import.witcher
```

## System Requirements

- **Python:** 3.6+
- **OS:** Linux, macOS, Windows
- **Dependencies:** None
- **Disk Space:** ~100 KB

## VS Code Extension

Full IDE support available:
```bash
cp -r vscode-witcherscript ~/.vscode/extensions/witcherscript-1.0.0
```

Then restart VS Code and create `.witcher` files with:
- Syntax highlighting
- 31+ autocomplete snippets
- Code folding
- Auto-completion

## Documentation

Included documentation:
- **README.md** - Full guide
- **QUICK_START.md** - 5-minute intro
- **DEPLOYMENT.md** - Installation details
- **LANGUAGE_REFERENCE.md** - Complete specification
- **GRIMOIRE_GUIDE.md** - Module system guide
- **WHATS_NEW.md** - v1.1 changes
- **PROJECT_INDEX.md** - Navigation guide

## Language Keywords

| Keyword | Purpose |
|---------|---------|
| `contract` | Variable declaration |
| `mutation` | Constant declaration |
| `grimoire` | Import modules |
| `igni` | If statement |
| `quen` | While loop |
| `yrden` | For loop |
| `aard` | Function definition |
| `hunt` | Return value |
| `elixir` | Else branch |
| `medallion` | Print output |

## Quick Stats

- **Total Lines of Code:** 1090 (interpreter)
- **Keywords:** 15
- **Built-in Functions:** 7
- **Example Programs:** 10
- **Documentation Files:** 14+
- **VS Code Snippets:** 31+

## Troubleshooting

### "command not found: witcher"
Add to PATH: `export PATH="$HOME/.local/bin:$PATH"`

### "File not found"
Use correct path: `witcher ./program.witcher` or `witcher /path/to/program.witcher`

### "Python not found"
Install Python 3.6+: `sudo apt install python3` or visit python.org

## Getting Started

1. **Install WitcherScript**
   ```bash
   ./install.sh
   ```

2. **Create a program**
   ```bash
   cat > test.witcher << 'EOF'
   contract name = "Witcher"
   medallion("Hello, " + name)
   EOF
   ```

3. **Run it**
   ```bash
   witcher test.witcher
   ```

## Features Summary

✅ Full interpreter with lexer, parser, evaluator
✅ Variables, functions, arrays, recursion  
✅ Control flow (if/else, while, for)
✅ String concatenation & type conversion
✅ Module system (grimoire imports)
✅ Circular import detection
✅ Clear error messages
✅ Zero external dependencies
✅ Cross-platform (Linux, Mac, Windows)
✅ VS Code integration with 31+ snippets
✅ 10 working example programs
✅ Comprehensive documentation
✅ Production-ready

## Performance

- **Startup Time:** <100ms
- **Memory Usage:** 10-20 MB
- **Type:** Pure tree-walking interpreter
- **No JIT:** Direct AST evaluation

## Support & Resources

- **Issue Tracker:** GitHub Issues
- **Documentation:** See included .md files
- **Examples:** `example_programs/` directory
- **VS Code:** Install from `vscode-witcherscript/`

## License

MIT License - Free for personal and commercial use

## Version

**WitcherScript v1.1**
- Released: January 2026
- Status: Production Ready
- Latest Features: Grimoire Module System

---

**May your code compile cleanly and your monsters fall swiftly!** ⚔️🧙‍♂️✨

### Next Steps

1. Read [QUICK_START.md](QUICK_START.md)
2. Run example programs
3. Create your first .witcher program
4. Check out [GRIMOIRE_GUIDE.md](GRIMOIRE_GUIDE.md) for modules

**Happy Witching!** 🎮
