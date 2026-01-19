# 🧙‍♂️ WitcherScript Autocomplete Reference - Updated for Grimoire

## All Autocomplete Snippets (32)

| Snippet | Prefix | Description |
|---------|--------|-------------|
| `contract` | contract | Declare a variable |
| `mutation` | mutation | Declare a constant |
| `grimoire` ⭐ | grimoire | Import functions from another file |
| `igni` | igni | If statement with else |
| `igni-only` | igni-only | If statement without else |
| `quen` | quen | While loop |
| `yrden` | yrden | For loop |
| `aard` | aard | Function definition |
| `call` | call | Function call |
| `hunt` | hunt | Return statement |
| `print` | print | Print output |
| `array` | array | Create array |
| `true` | true | Boolean true |
| `false` | false | Boolean false |
| `input` | input | Read user input |
| `len` | len | Get array length |
| `append` | append | Add to array |
| `typeof` | typeof | Get type information |
| `repeat` | repeat | Repeat string |
| `+` | + | Addition/concatenation |
| `-` | - | Subtraction |
| `*` | * | Multiplication |
| `/` | / | Division |
| `%` | % | Modulo |
| `==` | == | Equal comparison |
| `!=` | != | Not equal comparison |
| `>` | > | Greater than |
| `<` | < | Less than |
| `>=` | >= | Greater or equal |
| `<=` | <= | Less or equal |
| `and` | and | Logical AND |
| `or` | or | Logical OR |

## Grimoire - NEW in v1.1 ⭐

### Autocomplete Template

Type: `grimoire`  
Press: `Tab` or `Ctrl+Space`  
Result:
```
grimoire "lib/file.witcher"
         ↑
      Cursor here - ready for path
```

### Usage Examples

**Single import:**
```witcher
grimoire "lib/monster_helpers.witcher"
medallion(get_difficulty(18))
```

**Multiple imports:**
```witcher
grimoire "lib/math_utils.witcher"
grimoire "lib/monster_helpers.witcher"

medallion(factorial(5))
medallion(get_difficulty(18))
```

**Relative paths:**
```witcher
grimoire "lib/utils.witcher"
grimoire "../shared/helpers.witcher"
```

## How to Use Autocomplete

### Method 1: Snippet Prefix
1. Type the prefix (e.g., `grimoire`)
2. Press `Tab` to expand

### Method 2: Intellisense
1. Type the prefix (e.g., `grimoire`)
2. Press `Ctrl+Space` (or `Cmd+Space` on Mac)
3. Select from dropdown
4. Press `Tab` to insert

### Method 3: Manual Entry
1. Start typing
2. VS Code shows autocomplete suggestions
3. Click to select or press `Enter`

## Syntax Highlighting

All keywords are now properly color-coded:

```witcher
# Keywords: Dark Blue
contract gold = 100
mutation PI = 3.14
grimoire "lib/helpers.witcher"

# Signs/Control: Dark Blue
igni gold > 50 {
    medallion("Rich!")
}

# Functions: Yellow/Cyan
aard greet(name) {
    hunt "Hello, " + name
}

# Comments: Gray
# This is a comment
```

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl+Space` | Show autocomplete |
| `Tab` | Expand snippet |
| `Ctrl+/` | Toggle comment |
| `Ctrl+[` | Decrease indent |
| `Ctrl+]` | Increase indent |
| `Alt+Up` | Move line up |
| `Alt+Down` | Move line down |

## Pro Tips

1. **Combine Snippets:** Build complex structures by nesting snippets
   ```
   Type: aard
   Tab: Creates function
   Tab again inside: Add nested if statement with igni
   ```

2. **Quick Comments:** Use `#` for single-line comments
   ```witcher
   # This is a comment
   medallion("test")  # End-of-line comment
   ```

3. **Bracket Matching:** Use arrow keys to navigate between matching brackets
   ```witcher
   [ ... ] ← Jump between brackets
   { ... } ← VS Code highlights matching pair
   ( ... ) ← Easy to see scope
   ```

4. **Auto-closing:** Type opening bracket, closing appears automatically
   ```
   Type: {
   Result: {}  ← Cursor between them
   ```

5. **Smart Indentation:** Press Tab for automatic proper indentation
   ```witcher
   aard func() {
   [TAB]medallion("indented")
   }
   ```

## Recent Addition: Grimoire Support

With v1.1, grimoire imports now have full IDE support:

✅ **Syntax Highlighting:** `grimoire` keyword is color-coded  
✅ **Autocomplete:** Type `grimoire` and press Tab  
✅ **Code Folding:** Fold grimoire blocks  
✅ **Error Detection:** Invalid paths flagged (if using language server)

### Grimoire Autocomplete in Action

```
File: main.witcher

1. Type: grimoire
2. Press: Tab
3. Cursor: grimoire "lib/file.witcher"
                     ↑
4. Type: monster_helpers.witcher
5. Result: grimoire "lib/monster_helpers.witcher"
6. Press: Enter to go to next line

File will now have access to all functions from monster_helpers.witcher!
```

## Need Help?

- **Snippets not working?** Make sure extension is installed and enabled
- **No autocomplete?** Press `Ctrl+Space` to manually trigger
- **Syntax highlighting off?** Check file is saved with `.witcher` extension
- **Can't find snippet?** See table above for complete list

---

**Complete Autocomplete Ready - 32 Snippets + Grimoire Support! ⚔️🧙‍♂️**
