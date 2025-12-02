# Basic-10: BASIC to IC10 Compiler for Stationeers

![Basic-10 Logo](screenshots/Basic10_Logo.png)

**Version 2.0.0** | By Dog Tired Studios

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

## Built-in Documentation

### Quick Start Guide

![Quick Start Guide](screenshots/QuickStartGuide.png)

Get started immediately with:
- Your first program walkthrough
- Main loop pattern explanation
- Device connection basics
- Property read/write examples

### Language Reference

![Language Reference](screenshots/Language%20Reference.png)

Complete syntax reference including:
- Variables & constants
- Device declarations
- Device property access
- Labels & jumps
- Control structures
- All operators

### Full Documentation Window

![Documentation](screenshots/Documentation.png)

Access comprehensive documentation with the Help menu or F1.

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

1. **Download** the latest release: [BasicToMips_v2.0.0.zip](https://github.com/jtwm-0677/Basic-10-Download/releases/latest)

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

## License

Copyright (c) 2024 Dog Tired Studios. All rights reserved.

This software is provided for personal use in playing Stationeers. The source code is not publicly available.

---

*Built for the Stationeers community*
