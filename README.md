# Basic-10: BASIC to IC10 Compiler for Stationeers

**Version 2.0.0** | By Dog Tired Studios

Basic-10 is a powerful IDE that lets you write programs in BASIC and compiles them to IC10 (MIPS) assembly for use in the game [Stationeers](https://store.steampowered.com/app/544550/Stationeers/).

![Basic-10 Main Editor](screenshots/main-editor.png)

## Features

### Code Editor
- **Syntax highlighting** for BASIC keywords, variables, and IC10 output
- **Auto-completion** for keywords, device names, and logic types
- **Code folding** for loops, conditionals, and subroutines
- **Bookmarks and breakpoints** for navigation
- **Real-time error detection** with Problems Panel
- **Multiple tabs** for working with several scripts

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
- **Extensible device database** with 200+ Stationeers devices
- **Logic type auto-completion** for device properties

### IC10 Output
- **Optimized code generation** targeting Stationeers' IC10 chips
- **Live compilation** as you type
- **Source mapping** to trace IC10 lines back to BASIC
- **Register allocation** and optimization

### Built-in Documentation
- Complete BASIC syntax reference
- IC10 instruction reference
- 19 example programs with explanations
- Code snippets for common patterns
- Tips and best practices

### Quality of Life
- **Auto-save** with configurable interval
- **Light and dark themes**
- **Retro visual effects** (scanlines, glow, custom fonts)
- **Customizable syntax colors**
- **Direct save to Stationeers** scripts folder

![IC10 Output Panel](screenshots/ic10-output.png)

## Installation

### Requirements
- Windows 10/11 (64-bit)
- No additional dependencies required (self-contained)

### Steps

1. **Download** the latest release: [BasicToMips_v2.0.0.zip](https://github.com/jtwm-0677/Basic-10-Download/releases/download/v2.0.0/BasicToMips_v2.0.0.zip)

2. **Extract** the ZIP file to a folder of your choice (e.g., `C:\Games\Basic-10\`)

3. **Run** `Basic_10.exe` from the extracted folder

4. **Optional:** Create a desktop shortcut to `Basic_10.exe`

### First Launch
On first launch, Basic-10 will create a settings file in `%LOCALAPPDATA%\BasicToMips\`. The default script demonstrates aliases, variables, loops, and subroutines.

## Usage

### Quick Start

1. Write your BASIC code in the left panel
2. IC10 output appears automatically in the right panel
3. Use **File > Save to Stationeers** to save directly to the game's scripts folder
4. In Stationeers, access your script from the IC chip's script selection

### Example: Simple Atmosphere Monitor

```basic
' Atmosphere Monitor - Basic-10 Example
ALIAS sensor d0
ALIAS vent d1

CONST TARGET_PRESSURE = 101.325
CONST TOLERANCE = 5

DIM pressure

MAIN:
    pressure = sensor.Pressure

    IF pressure < TARGET_PRESSURE - TOLERANCE THEN
        vent.On = 1
    ELSEIF pressure > TARGET_PRESSURE + TOLERANCE THEN
        vent.On = 0
    ENDIF

    YIELD
    GOTO MAIN
```

### Documentation
Press **F1** or click the **Docs** tab to access built-in documentation with syntax reference, examples, and tips.

![Documentation Panel](screenshots/documentation.png)

## Screenshots

| Main Editor | Problems Panel |
|-------------|----------------|
| ![Editor](screenshots/main-editor.png) | ![Problems](screenshots/problems-panel.png) |

| Documentation | Settings |
|---------------|----------|
| ![Docs](screenshots/documentation.png) | ![Settings](screenshots/settings.png) |

## Changelog

### v2.0.0 (2024)
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

## Support

For bug reports and feature requests, please visit the [Issues](https://github.com/jtwm-0677/Basic-10-Download/issues) page.

## License

Copyright (c) 2024 Dog Tired Studios. All rights reserved.

This software is provided for personal use in playing Stationeers. The source code is not publicly available.

---

*Built for the Stationeers community*
