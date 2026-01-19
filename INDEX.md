# WitcherScript - Complete Index

Welcome to **WitcherScript**, a programming language inspired by The Witcher 3: Wild Hunt!

## 📚 Documentation Guide

Start here based on your needs:

### 🚀 Getting Started
- **New to WitcherScript?** → Start with [QUICK_START.md](QUICK_START.md)
  - Basic syntax
  - Hello World program
  - Common patterns
  - Tips for beginners

- **Want quick reference?** → See [CHEAT_SHEET.md](CHEAT_SHEET.md)
  - All keywords at a glance
  - Syntax examples
  - Built-in functions
  - Common mistakes

### 📖 Complete Documentation
- **Full language specification** → [LANGUAGE_REFERENCE.md](LANGUAGE_REFERENCE.md)
  - Detailed syntax explanation
  - All operators and keywords
  - All built-in functions with examples
  - Complete feature reference

- **Project overview** → [README.md](README.md)
  - What is WitcherScript
  - How to install and run
  - Project structure
  - Game references

- **Language spec overview** → [WitcherLang.md](WitcherLang.md)
  - Quick language specification
  - Keywords and signs
  - Data types
  - Example structure

### 🔍 Project Details
- **Project summary** → [PROJECT_SUMMARY.md](PROJECT_SUMMARY.md)
  - What was implemented
  - Testing results
  - Code quality
  - Achievements

## 🎮 Example Programs

8 complete, working examples in `example_programs/`:

| Example | Topics | Level |
|---------|--------|-------|
| [01_hello_world.witcher](example_programs/01_hello_world.witcher) | Output, strings | Beginner |
| [02_monster_hunt.witcher](example_programs/02_monster_hunt.witcher) | Variables, conditionals | Beginner |
| [03_casting_signs.witcher](example_programs/03_casting_signs.witcher) | Functions, returns | Beginner |
| [04_bestiary.witcher](example_programs/04_bestiary.witcher) | Arrays, loops | Intermediate |
| [05_alchemy.witcher](example_programs/05_alchemy.witcher) | Complex conditionals | Intermediate |
| [06_quest_system.witcher](example_programs/06_quest_system.witcher) | Multiple functions | Intermediate |
| [07_combat.witcher](example_programs/07_combat.witcher) | Complex loops, logic | Advanced |
| [08_fibonacci.witcher](example_programs/08_fibonacci.witcher) | Recursion | Advanced |

### Run Examples
```bash
# Run any example with:
python3 witcher_interpreter.py example_programs/NAME.witcher

# Examples:
python3 witcher_interpreter.py example_programs/01_hello_world.witcher
python3 witcher_interpreter.py example_programs/02_monster_hunt.witcher
python3 witcher_interpreter.py example_programs/03_casting_signs.witcher
```

## 🔧 Main Components

### witcher_interpreter.py
The complete interpreter (1000+ lines):
- **Lexer** - Tokenizes source code
- **Parser** - Builds abstract syntax tree
- **Interpreter** - Executes the program

```bash
# Interactive mode
python3 witcher_interpreter.py

# Run a file
python3 witcher_interpreter.py program.witcher
```

## 🎓 Learning Path

**Recommended order for learning:**

1. **Read** → [QUICK_START.md](QUICK_START.md) (5 min)
   - Understand basic concepts
   - Try Hello World

2. **Reference** → [CHEAT_SHEET.md](CHEAT_SHEET.md) (5 min)
   - Quick syntax lookup
   - Built-in functions

3. **Practice** → Examples 01-04 (15 min)
   - Run examples
   - Modify them
   - Experiment

4. **Learn Details** → [LANGUAGE_REFERENCE.md](LANGUAGE_REFERENCE.md) (15 min)
   - Deep dive into features
   - Study all operators
   - Understand scoping

5. **Build** → Examples 05-08 (20 min)
   - Study advanced examples
   - Create your own programs
   - Combine concepts

## 💡 Quick Facts

- **Language**: Python (interpreter)
- **Version**: 1.0
- **Status**: Fully functional ✅
- **File Extension**: `.witcher`
- **Lines of Code**: 1000+
- **Examples**: 8 working programs
- **Test Status**: All examples pass ✅

## 🎯 Key Keywords

| Category | Keywords |
|----------|----------|
| **Control** | igni (if), quen (while), yrden (for), elixir (else) |
| **Functions** | aard (def), hunt (return) |
| **Variables** | contract (var), mutation (const) |
| **I/O** | medallion (print), sigh (input) |
| **Logic** | and, or, not, truth, falsehood |

## 🚀 Getting Started Now

### 1. Interactive Mode
```bash
python3 witcher_interpreter.py
witcher> medallion("Greetings!")
Greetings!
```

### 2. Create a File
```bash
cat > hello.witcher << 'EOF'
medallion("Welcome, Witcher!")
EOF

python3 witcher_interpreter.py hello.witcher
```

### 3. Run Example
```bash
python3 witcher_interpreter.py example_programs/01_hello_world.witcher
```

## 📝 File Structure

```
TestClaude/
│
├── 📄 README.md                    # Main documentation
├── 📄 QUICK_START.md               # Quick start guide
├── 📄 CHEAT_SHEET.md               # Syntax cheat sheet
├── 📄 LANGUAGE_REFERENCE.md        # Complete reference
├── 📄 WitcherLang.md               # Language spec
├── 📄 PROJECT_SUMMARY.md           # Project details
├── 📄 INDEX.md                     # This file
│
├── 🐍 witcher_interpreter.py       # Main interpreter
│
└── 📁 example_programs/            # Example programs
    ├── 01_hello_world.witcher
    ├── 02_monster_hunt.witcher
    ├── 03_casting_signs.witcher
    ├── 04_bestiary.witcher
    ├── 05_alchemy.witcher
    ├── 06_quest_system.witcher
    ├── 07_combat.witcher
    └── 08_fibonacci.witcher
```

## 🎮 Witcher References

Language inspired by The Witcher 3:
- **Signs**: Igni (fire), Quen (shield), Yrden (stasis), Aard (blast), Axii (charm)
- **Monsters**: Griffin, Basilisk, Wraith, Drowner, Leshen
- **Mechanics**: Contracts, alchemy, bestiary, mutations
- **Characters**: Geralt, Yennefer, Triss

## ❓ FAQ

**Q: How do I run a program?**
A: `python3 witcher_interpreter.py program.witcher`

**Q: What's the difference between contract and mutation?**
A: `contract` is a variable (can change), `mutation` is a constant (cannot change)

**Q: How do I print output?**
A: Use `medallion("text")` or `medallion(variable)`

**Q: How do I create a loop?**
A: Use `quen condition { }` for while or `yrden item -> array { }` for for-loop

**Q: How do I create a function?**
A: Use `aard function_name(params) { hunt result }`

**Q: Can I use recursion?**
A: Yes! See example 08_fibonacci.witcher

**Q: What about arrays?**
A: Use `contract arr = [1, 2, 3]` and access with `arr[0]`

## 🔗 Quick Links

- 📖 [Quick Start](QUICK_START.md) - Learn fast
- 📋 [Cheat Sheet](CHEAT_SHEET.md) - Quick reference
- 📚 [Full Reference](LANGUAGE_REFERENCE.md) - Complete guide
- 📘 [README](README.md) - Main documentation
- 📊 [Project Summary](PROJECT_SUMMARY.md) - What was built

## 🎓 Next Steps

1. Read [QUICK_START.md](QUICK_START.md)
2. Try the examples in `example_programs/`
3. Create your own programs
4. Check [LANGUAGE_REFERENCE.md](LANGUAGE_REFERENCE.md) for advanced features

## 🎉 Have Fun!

Start your witcher journey and create amazing programs with WitcherScript!

```witcher
medallion("May your code be swift and your monsters fall!")
```

---

**Questions?** Check the appropriate documentation file above.
**Ready to code?** Start with [QUICK_START.md](QUICK_START.md)!
