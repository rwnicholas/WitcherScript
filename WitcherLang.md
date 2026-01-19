# Witcher 3 Programming Language Specification

## Overview
WitcherScript is a programming language inspired by The Witcher 3, featuring Witcher signs, monsters, potions, and Witcher lore throughout its syntax and built-in functions.

## Keywords & Signs

### Witcher Signs (Control Flow)
- `igni` - if statement (Fire Sign - ignites conditions)
- `quen` - while loop (Protection Sign - repeats protection)
- `yrden` - for loop (Slow Time Sign - structured iteration)
- `aard` - function definition (Blast Sign - initiates force)
- `axii` - switch/case (Charm Sign - multiple paths)

### Basic Keywords
- `contract` - variable declaration (Witcher taking a contract)
- `hunt` - return statement (Witcher hunting/returning)
- `elixir` - else statement
- `mutation` - constant declaration
- `medallion` - print/output statement

## Data Types
- `number` - integers and floats
- `text` - strings
- `truth` / `falsehood` - booleans (true/false)
- `bestiary` - array/list (collection of monsters)

## Operators
- Arithmetic: `+`, `-`, `*`, `/`, `%`
- Comparison: `==`, `!=`, `>`, `<`, `>=`, `<=`
- Logical: `and`, `or`, `not`
- Assignment: `=`, `+=`, `-=`, `*=`, `/=`

## Built-in Functions
- `medallion(value)` - print output
- `sigh(message)` - input/read
- `witcher_speed(n)` - string repeat
- `monster_count(bestiary)` - length
- `add_to_bestiary(bestiary, value)` - append
- `hunter_instinct(text)` - type checking
- `potion_effect(a, b)` - arithmetic operations

## Structure

```witcher
aard main
  contract greeting = "Greetings, Witcher"
  medallion(greeting)
hunt
```

## Example Programs
See example_programs/ directory for more examples.
