# LaTeX Cheat Sheets

A collection of productivity and reference cheat sheets built with LaTeX.

## Contents

- **productivity-cheatsheet.tex** - Main productivity cheat sheet with common shortcuts and workflows
- **productivity-cheatsheet-mac.tex** - macOS-specific productivity cheat sheet
- **productivity-cheatsheet-windows.tex** - Windows-specific productivity cheat sheet
- **vim_cheat_sheet.tex** - Vim editor keyboard shortcuts and commands

## Building

### Prerequisites

Ensure you have `latexmk` installed. On macOS:
```bash
brew install latexmk
```

### Build Commands

Build all PDFs:
```bash
latexmk
```

Build a specific document:
```bash
latexmk src/productivity-cheatsheet-mac.tex
latexmk src/vim_cheat_sheet.tex
```

Clean build artifacts:
```bash
latexmk -c
```

Clean everything including PDFs:
```bash
latexmk -C
```

PDFs are output to the `build/` directory.

## Project Structure

- `src/` - LaTeX source files
- `build/` - Generated PDF output (created during build)
- `latexmkrc` - Build configuration for latexmk

## Code Style

- Self-contained `.tex` files with variant wrappers for OS-specific content
- OS variants use `\ifdefined\MACONLY` / `\ifdefined\WINONLY` conditionals
- Standard LaTeX packages only (multicol, xcolor, geometry, tcolorbox, etc.)
- CamelCase command naming with semantic names (e.g., `\sectioncolor`, `\windowscolor`)
- 2-space indentation, landscape orientation for cheat sheets
- Minimal margins (0.5in) for compact layout

## Configuration

Build behavior can be customized by editing `latexmkrc`.
