# VS Code Extension for WitcherScript - Complete Setup

## 📦 What You Have

A complete, production-ready VS Code extension with full intellisense support!

```
vscode-witcherscript/
├── package.json                          # Extension manifest
├── language-configuration.json           # Language configuration
├── README.md                             # Quick feature overview
├── INSTALLATION.md                       # Installation instructions
├── EXTENSION_GUIDE.md                    # Complete user guide
├── .vscode-settings.json                 # Recommended VS Code settings
├── syntaxes/
│   └── witcherscript.tmLanguage.json    # Syntax highlighting (TextMate grammar)
└── snippets/
    └── witcherscript.json               # 30+ code snippets
```

## 🚀 Installation (3 Steps)

### Step 1: Find Your Extensions Folder
- **Linux/Mac**: `~/.vscode/extensions/`
- **Windows**: `%USERPROFILE%\.vscode\extensions\`

### Step 2: Copy the Extension
```bash
# Linux/Mac
cp -r vscode-witcherscript ~/.vscode/extensions/witcherscript-1.0.0

# Windows (PowerShell)
Copy-Item -Recurse vscode-witcherscript $env:USERPROFILE\.vscode\extensions\witcherscript-1.0.0
```

### Step 3: Restart VS Code
- Close all VS Code windows
- Reopen VS Code
- Create/open any `.witcher` file

**That's it! ✅ Intellisense is now active!**

## ✨ Features

### 1. **Syntax Highlighting** 🎨
```witcher
# Colored syntax for easy reading
contract gold = 100           # Keywords highlighted
igni gold > 50 {              # Control flow in color
    medallion("Rich!")         # Built-in functions highlighted
}
```

### 2. **30+ Code Snippets** 📝

Type any of these and press **Tab** to auto-expand:

| Snippet | Expands To |
|---------|-----------|
| `contract` | Variable declaration |
| `mutation` | Constant declaration |
| `igni` | If/else statement |
| `quen` | While loop |
| `yrden` | For loop |
| `aard` | Function definition |
| `hunt` | Return statement |
| `medallion` | Print output |
| `array` | Array literal |
| `true` | Boolean true |
| `false` | Boolean false |

**Example:**
```
Type: aard
Press: Tab
Result:
    aard function_name(params) {
        // code
        hunt result
    }
```

### 3. **Auto-completion** ⚡
- Auto-closing brackets: `(` → `()`
- Auto-closing quotes: `"` → `""`
- Auto-closing braces: `{` → `{}`
- Smart indentation
- Code folding

### 4. **Intellisense Features** 🧠
- File type association (`.witcher`)
- Comment syntax highlighting
- Bracket matching
- Code structure recognition
- Proper indentation

## 💡 Pro Tips

### Keyboard Shortcuts
```
Ctrl+Space        Trigger Intellisense / Show Snippets
Ctrl+/            Comment/uncomment line
Ctrl+Shift+/      Block comment
Tab               Expand snippet or indent
Shift+Tab         Unindent
Ctrl+Shift+[      Fold code block
Ctrl+Shift+]      Unfold code block
```

### Working with Snippets
1. Type snippet name (e.g., `igni`, `aard`, `quen`)
2. Press **Tab** to expand
3. Press **Tab** again to jump to next placeholder
4. Type your content
5. Press **Enter** to finish

### Example Workflow
```witcher
# Type 'contract' and press Tab
contract count = 0

# Type 'quen' and press Tab
quen count < 5 {
    # Type 'medallion' and press Tab
    medallion(count)
    count = count + 1
}
```

## 📚 Documentation

Included guides:
- **README.md** - Quick feature overview
- **INSTALLATION.md** - Detailed installation
- **EXTENSION_GUIDE.md** - Complete user guide (advanced)

Parent project guides:
- **QUICK_START.md** - Learn WitcherScript fast
- **CHEAT_SHEET.md** - Quick reference
- **LANGUAGE_REFERENCE.md** - Complete specification

## 🎨 Color Scheme

Colors automatically match your VS Code theme:
- **Keywords**: Blue/Purple (bold)
- **Built-in Functions**: Yellow/Cyan
- **Constants**: Green/Teal (bold)
- **Strings**: Red/Orange
- **Numbers**: Green
- **Comments**: Gray

## 🔧 Customization

Add to your VS Code `settings.json` for custom behavior:

```json
"[witcherscript]": {
  "editor.tabSize": 4,
  "editor.insertSpaces": true,
  "editor.autoIndent": "full",
  "editor.formatOnPaste": true
}
```

## ✅ Verification Checklist

After installation, verify:
- [ ] `.witcher` files have color highlighting
- [ ] Type `contract` and press Tab → expands to `contract name = value`
- [ ] Type `igni` and press Tab → expands to if/else template
- [ ] Type `(` and `)` appears automatically
- [ ] Type `{` and `}` appears automatically
- [ ] Comments start with `#` and are gray

## 🐛 Troubleshooting

| Issue | Solution |
|-------|----------|
| Extension not loading | Check file in correct extensions folder, restart VS Code |
| No syntax highlighting | Verify file has `.witcher` extension |
| Snippets not working | Press Ctrl+Space in a `.witcher` file |
| Wrong colors | Switch VS Code theme or customize settings.json |
| Bracket auto-close disabled | Check language configuration in VS Code settings |

## 📦 File Breakdown

### `package.json` - Extension Manifest
Defines the extension metadata and configuration

### `language-configuration.json` - Language Settings
- Comment syntax (`#`)
- Bracket pairs
- Auto-closing pairs
- Code folding markers

### `syntaxes/witcherscript.tmLanguage.json` - Syntax Highlighting
TextMate grammar for proper color coding of:
- Keywords (igni, quen, aard, etc.)
- Built-in functions
- Strings and numbers
- Comments and operators

### `snippets/witcherscript.json` - Code Snippets
30+ ready-to-use code templates for:
- Variables and constants
- Control flow statements
- Function definitions
- Built-in function calls
- Operators and expressions

## 🎯 Quick Reference

**Most Used Snippets:**
```
contract       → Variable
aard          → Function
igni          → If statement
quen          → While loop
yrden         → For loop
medallion     → Print
hunt          → Return
```

**Pro Tip**: You can also use Intellisense to autocomplete function names:
- Type `medal` → Intellisense suggests `medallion`
- Type `mon` → Intellisense suggests `monster_count`
- Type `hunt` → Intellisense suggests `hunter_instinct`

## 🚀 Next Steps

1. **Install the extension** → Copy to VS Code extensions folder
2. **Create a .witcher file** → Open in VS Code
3. **Start typing** → Use Ctrl+Space for intellisense
4. **Expand snippets** → Type prefix and press Tab
5. **Run your code** → Use the WitcherScript interpreter

## 📋 Snippet Categories

### Variables (2)
- contract
- mutation

### Control Flow (6)
- igni (if/else)
- igni-only (if only)
- quen (while)
- yrden (for)
- elixir (else) - *not needed, included in igni*

### Functions (3)
- aard (define)
- call (call function)
- hunt (return)

### I/O & Data (8)
- medallion (print)
- input (read)
- array (literal)
- true (truth)
- false (falsehood)
- len (length)
- append (add)
- typeof (type)

### Operators (10)
- Addition (+)
- Subtraction (-)
- Multiplication (*)
- Division (/)
- Modulo (%)
- Equal (==)
- Not equal (!=)
- Greater than (>)
- Less than (<)
- And others...

---

## 🎉 Summary

You now have:
✅ Full syntax highlighting for WitcherScript
✅ 30+ code snippets for rapid coding
✅ Auto-completion and bracket matching
✅ Smart indentation and code folding
✅ Built-in function recognition
✅ Complete documentation

**Ready to write WitcherScript with intellisense!** 🧙‍♂️⚔️

For questions, refer to the extension guides or main WitcherScript documentation.
