# BasIC-10: BASIC to IC10 Compiler for Stationeers

![Downloads](https://img.shields.io/github/downloads/jtwm-0677/Basic-10-Download/total)

**Version 2.6.1** | By Dog Tired Studios

BasIC-10 is a powerful IDE that lets you write programs in BASIC and compiles them to IC10 (MIPS) assembly for use in the game Stationeers.

## Key Features

**Code Editor**
- Syntax highlighting and auto-completion
- Real-time error detection with Problems Panel
- Code folding and bookmarks
- Multiple tabs for several scripts

**BASIC Language Support**
- Variables, constants, and arrays (DIM)
- Control flow: IF/THEN/ELSE, WHILE/WEND, FOR/NEXT, GOSUB/RETURN
- Compound assignments and increment/decrement operators
- Bitwise operations and device I/O with aliases

**Device Integration**
- Pin aliases and named device references
- Extensible database with 1500+ Stationeers devices
- Logic type auto-completion for device properties

**IC10 Simulator & Debugger**
- Step-through debugging with register inspection
- Device simulation and execution speed control
- Stack visualization and variable inspector

**Device & Logic Hash Database**
- Browse 1513 devices with prefab names and hash values
- Reference 280 logic types for device properties
- Hash calculator for custom strings

**Integrated Documentation**
- Eight reference tabs covering syntax, functions, devices, and IC10
- 19 ready-to-use example scripts
- Embedded Stationeers Wiki access

## What's New in v2.6.1

**Bug Fixes:**
- **Named Device Memory Access**: Compiler now correctly detects and reports an error when `.Memory[]` is used with named devices (requires pin aliases d0-d5)
- **DIM Initializer**: Fixed `DIM x = CONST_NAME` and expression initializers generating invalid code

## Installation

**Requirements:** Windows 10/11 (64-bit), self-contained executable

1. Download BasIC-10v2.6.1.zip
2. Extract to preferred directory
3. Run Basic_10.exe

## Quick Start Example

The documentation demonstrates connecting devices with aliases and creating main loops with control flow structures, helping new users understand fundamental programming patterns for game automation.

---

**Support:** Visit the Issues page for bug reports or feature requests

**License:** Copyright (c) 2025 Dog Tired Studios. All rights reserved. For personal use in Stationeers.
