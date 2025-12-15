# BasIC-10: BASIC to IC10 Compiler for Stationeers

[![Basic-10 Logo](screenshots/Basic10_Logo.png)](https://github.com/jtwm-0677/Basic-10-Download/releases/latest)

**Version 2.4.0** | By Dog Tired Studios

[![Download NOW](https://img.shields.io/badge/Download_NOW-v2.4.0-blue?style=for-the-badge&logo=windows)](https://github.com/jtwm-0677/Basic-10-Download/releases/download/v2.4.0/BasIC-10v2.4.0.zip)
[![Buy Me A Coffee](https://img.shields.io/badge/Buy_Me_A_Coffee-Support_Development-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/dogtired.thunderduck)

Basic-10 is a powerful IDE that lets you write programs in BASIC and compiles them to IC10 (MIPS) assembly for use in the game [Stationeers](https://store.steampowered.com/app/544550/Stationeers/).

---

## Main Editor

![Main Editor Window](screenshots/MainEditorWindow.png)

The main editor features:
- **BASIC code editor** (left) with syntax highlighting and auto-completion
- **IC10 output panel** (bottom-left) showing compiled assembly in real-time
- **Symbols panel** (left sidebar) tracking variables, constants, labels, aliases, and arrays
- **Documentation panel** (right) with quick reference always available
- **Problems panel** (bottom) showing errors and warnings with clickable line numbers

---

## Features

### Code Editor
- Syntax highlighting for BASIC keywords, variables, and IC10 output
- Auto-completion for keywords, device names, and logic types
- Code folding for loops, conditionals, and subroutines
- Bookmarks and breakpoints for navigation
- Real-time error detection with Problems Panel
- Multiple tabs for working with several scripts

### BASIC Language Support
- Variables, constants, and arrays (`DIM`)
- Control flow: `IF/THEN/ELSE`, `WHILE/WEND`, `FOR/NEXT`, `GOSUB/RETURN`
- Compound assignments: `+=`, `-=`, `*=`, `/=`
- Increment/decrement: `++i`, `--i`, `i++`, `i--`
- Bitwise operations: `AND`, `OR`, `XOR`, `NOT`, `<<`, `>>`
- Device I/O with aliases and named device references

### Device Integration
- **Pin aliases** (`ALIAS furnace d0`) for hardware connections
- **Named device references** (`DEVICE furnace "Furnace"`) to bypass the 6-pin limit
- **Extensible device database** with 1500+ Stationeers devices
- **Logic type auto-completion** for device properties

---

## IC10 Simulator & Debugger

![Simulator Window](screenshots/SimulatorWindow.png)

Test your code without launching Stationeers:
- **Step-through debugging** - execute one instruction at a time
- **Register inspection** - view all 18 registers in real-time
- **Device simulation** - set device values for testing
- **Execution speed control** - run slow for debugging or fast for testing
- **Stack visualization** - monitor the call stack

### Variable Inspector

![Variable Inspector](screenshots/VariableInspector.png)

- View BASIC variables mapped to registers
- See constants and their values
- Edit values during simulation
- Track variable changes line-by-line

---

## Device & Logic Hash Database

![Device Database](screenshots/DeviceAndLogicDatabase_DevicesTab.png)

Browse the complete Stationeers device database:
- **1513 devices** with prefab names and hash values
- **280 logic types** for reading/writing device properties
- **31 slot types** for inventory management
- **Sorting classes** for sorting machines
- **Hash calculator** for custom strings

### Logic Types Reference

![Logic Types](screenshots/DeviceAndLogicDatabase_LogicTypesTab.png)

Quick lookup for all device properties like Temperature, Pressure, On, Setting, and more.

### Hash Calculator

![Hash Calculator](screenshots/DeviceAndLogicDatabase_HashCalculatorTab.png)

Calculate CRC32 hashes for any string - useful for custom device references.

---

## Integrated Documentation Pane

The Documentation pane is always available in the right panel, with 8 tabs covering everything you need:

### Start Tab - Quick Start Guide

![Start Tab](screenshots/DocumentsPane_StartTab.png)

Get started immediately:
- Welcome and introduction to Basic-10
- Your first program walkthrough
- Understanding the code explanations
- The main loop pattern (with YIELD warning)
- Connecting devices basics

### Syntax Tab - Complete Language Reference

![Syntax Tab](screenshots/DocumentsPane_SyntaxTab.png)

Complete BASIC syntax reference:
- Variables & constants (VAR, CONST, DEFINE, LET)
- Device declarations (ALIAS, DEVICE)
- Device property access with examples
- Labels & jumps (GOTO, GOSUB, RETURN)

### Funcs Tab - Built-in Functions

![Functions Tab](screenshots/DocumentsPane_FunctionsTab.png)

All built-in functions with examples:
- **Math functions**: ABS, SQRT, MIN, MAX, CEIL, FLOOR, ROUND, TRUNC, SGN, RND
- **Trigonometry**: SIN, COS, TAN, ASIN, ACOS, ATAN (with radians tip)
- Usage examples for each function

### Devices Tab - Device Properties Reference

![Devices Tab](screenshots/DocumentsPane_DevicesTab.png)

Device property reference organized by category:
- **Device Pins**: d0-d5, db, THIS
- **Universal Properties**: On, Power, Error, Lock, PrefabHash, etc.
- **Atmosphere Sensors**: Temperature, Pressure, RatioOxygen, etc.
- **Valves, Pumps & Vents**: Setting, Mode, and more
- Temperature conversion tips included

### IC10 Tab - MIPS Instruction Reference

![IC10 Tab](screenshots/DocumentsPane_IC10Tab.png)

Complete IC10 assembly reference:
- **Registers**: r0-r15, sp, ra, d0-d5, db
- **Math Operations**: add, sub, mul, div, mod, exp, log, sqrt, etc.
- **Trigonometry**: sin, cos, tan, asin, acos, atan
- **Logic & Comparison**: and, or, xor, nor, not, sll, srl, sra, slt, sgt, etc.
- **Branching & Jumps**: Listed below the reference

### Tips Tab - Tips, Tricks & Patterns

![Tips Tab](screenshots/DocumentsPane_TipsAndTricksTab.png)

Essential programming patterns:
- **The Main Loop** - proper structure with YIELD
- **Hysteresis** - prevent rapid switching with dead bands
- **Edge Detection** - detect button presses (not holds)
- **State Machine** - for complex multi-step processes like airlocks

### Examples Tab - 19 Ready-to-Use Scripts

![Examples Tab](screenshots/DocumentsPane_ExampleScriptsTab.png)

19 complete example scripts you can load directly:
1. Blink Light
2. Button Toggle
3. Thermostat
4. Pressure Regulator
5. Oxygen Monitor
6. Solar Tracker
7. Battery Backup
8. Airlock Controller
9. Furnace Controller
10. Batch Solar Array
11. Item Sorter
12. Base Status Monitor
13. Dial Pump Control
14. Math Demo
15. Greenhouse Controller
16. Counter with Increment/Decrement
17. Smooth Value Adjustment
18. Bit Flag Status System
19. Loop with BREAK/CONTINUE

### Wiki Tab - Integrated Stationeers Wiki

![Wiki Tab](screenshots/InEditorWikiAccess.png)

Browse the Stationeers Wiki without leaving the editor:
- Full wiki access with navigation
- Search for devices, items, and game mechanics
- Look up crafting recipes and requirements

![Wiki Example Page](screenshots/DocumentsPane_GameWikiExamplePageTab.png)

View detailed wiki pages with tables, images, and specifications.

---

## Problems Panel

![Problems Panel](screenshots/ProblemsPanel.png)

Real-time error detection:
- Syntax errors highlighted as you type
- Clickable line numbers to jump to issues
- Clear error messages with suggestions
- IC10 line count tracking (128 line limit)

---

## Installation

### Requirements
- Windows 10/11 (64-bit)
- No additional dependencies required (self-contained)

### Steps

1. **Download** the latest release: [BasIC-10v2.4.0.zip](https://github.com/jtwm-0677/Basic-10-Download/releases/latest)

2. **Extract** the ZIP file to a folder of your choice (e.g., `C:\Games\Basic-10\`)

3. **Run** `Basic_10.exe` from the extracted folder

4. **Optional:** Create a desktop shortcut to `Basic_10.exe`

### First Launch
On first launch, Basic-10 will create a settings file in `%LOCALAPPDATA%\BasicToMips\`. The default script demonstrates aliases, variables, loops, and subroutines.

---

## Quick Start Example

```basic
' Atmosphere Monitor - Basic-10 Example
ALIAS sensor d0       ' Gas sensor
ALIAS vent d1         ' Active vent

CONST TARGET = 101.325
CONST TOLERANCE = 5

VAR pressure = 0

main:
    pressure = sensor.Pressure

    IF pressure < TARGET - TOLERANCE THEN
        vent.On = 1
    ELSEIF pressure > TARGET + TOLERANCE THEN
        vent.On = 0
    ENDIF

    YIELD
    GOTO main
```

---

## Changelog

### v2.4.0 - Advanced IC10 Features
- **New Feature: POKE Instruction** - Write directly to stack memory addresses with `POKE address, value`
- **New Feature: Batch Slot Operations** - Read/write slot properties across all devices of a type
  - `BATCHSLOT(hash, slot, "Property", mode)` - Read with Average/Sum/Min/Max modes
  - `BATCHSLOT_WRITE(hash, slot, "Property", value)` - Write to all matching device slots
  - Compiles to IC10 `lbs`/`sbs` (and `lbns`/`sbns` for named variants)
- **New Feature: Indirect Register Access** - Dynamic register addressing with computed indices
  - `REG(index)` - Read from register r{index}
  - `REGSET(index, value)` - Write to register r{index}
  - Uses IC10 indirect addressing (`rr0`-`rr15`) for variable indices
- **New Feature: Indirect Device Access** - Dynamic device pin addressing
  - `DEVICE(index).Property` - Read/write device d{index}
  - `DEVICE(index).Slot[n].Property` - Slot access with computed device index
  - Uses IC10 indirect addressing (`dr0`-`dr5`) for variable indices
  - Perfect for iterating over all 6 device pins in a loop

### v2.3.0 - Bug Fixes
- **Language Detection Fix**: Fixed BASIC code with `#` comments being incorrectly detected as IC10
- **Extended Script Mode**: Fixed line limit enforcement (128 vanilla / 512 extended)
- **BATCHWRITE Statement**: Fixed `BATCHWRITE(hash, "Property", value)` not compiling
- **Autosave Recovery**: Fixed recovery prompt appearing for default welcome script

### v2.2.3 - Improved Decompiler
- **Improved Decompiler** - Now preserves alias names when decompiling (e.g., `RoomSensor` instead of `var0`)
- Unknown device hashes labeled as `[DEVICE_UNKNOWN:hash]` to prompt user to fill in
- Unknown name hashes labeled as `[NAME_UNKNOWN:hash]` for clarity

### v2.2.2 - External Memory Access
- **New Feature: External Memory Access** - Read/write external memory devices using `device.Memory[address]` syntax
- Supports Logic Memory, Stack Chips, Queue Chips, and Memory Utility Chips
- Compiles to `get`/`put` for pin aliases, `getd`/`putd` for named devices
- Example: `mem.Memory[0]` to read, `mem.Memory[5] = 42` to write

### v2.2.1 - Extended Script Mode
- **New Feature: Extended Script Mode (512 Lines)** - Enable "Extended (512)" checkbox in toolbar to allow scripts up to 512 lines
- Requires the **"More Lines of Code"** mod by **jixxed**: [Steam Workshop](https://steamcommunity.com/sharedfiles/filedetails/?id=3265272725)
- First-time warning dialog explains mod requirement with option to open Steam Workshop page
- Color-coded line count: Green (0-99), Orange (100-128), Purple (129-450 extended), Red (over limit)
- Scripts saved in extended mode include mod requirement in IC10 header and instruction.xml

### v2.2.0 - Hotfix
- **Critical bug fix**: Jump target calculation now correctly ignores comment lines
- IC10 doesn't count comments as instructions, but the compiler was - this caused all control flow (loops, GOTOs, IF/ELSE, WHILE, FOR) to jump to wrong lines when comments were present

### v2.1.0
- **Critical bug fix**: Fixed jump target miscalculation in single-line IF statements with assignments
- **Critical bug fix**: Fixed unconditional jump instructions using label names instead of numeric offsets
- **Critical bug fix**: Fixed IC10 output including label definitions which caused scripts to fail silently in-game
- Comments and user labels now correctly excluded from instruction counting
- Improved code generation reliability for all jump-based constructs

### v2.0.0
- Array support with `DIM` statements
- Compound assignments (`+=`, `-=`, `*=`, `/=`)
- Increment/decrement operators (`++i`, `--i`, `i++`, `i--`)
- Bitwise shift operators (`<<`, `>>`)
- Enhanced Problems Panel with all warnings
- Improved default script with practical examples
- New snippets: Counter, Accumulator, Bit Flags
- Bracket auto-completion for `.Name[""]`
- Updated documentation with 19 examples

### v1.7.3
- MCP server integration via HTTP API
- Auto-save functionality
- Script metadata settings
- Dynamic device aliases
- Named device references

---

## Support

For bug reports and feature requests, please visit the [Issues](https://github.com/jtwm-0677/Basic-10-Download/issues) page.

---

## Support Development

If you find Basic-10 useful, consider buying me a coffee!

[![Buy Me A Coffee](https://img.shields.io/badge/Buy_Me_A_Coffee-Support_Development-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/dogtired.thunderduck)

---

## License

Copyright (c) 2025 Dog Tired Studios. All rights reserved.

This software is provided for personal use in playing Stationeers. The source code is not publicly available.

---

*Built for the Stationeers community*
