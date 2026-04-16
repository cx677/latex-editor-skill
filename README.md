# LaTeX Editor Skill

A comprehensive LaTeX editing and compilation toolkit for WorkBuddy AI agent, supporting academic paper writing with IEEE/ACM templates.

## Features

- **Smart LaTeX Generation**: AI-assisted academic paper writing
- **PDF Compilation**: Auto-detect and use available LaTeX distributions
- **Code Formatting**: Automatic LaTeX code linting and formatting
- **Template Support**: IEEE and ACM conference paper templates
- **Chinese Support**: Full ctex integration for Chinese academic writing
- **Math Environments**: Definition, theorem, lemma, proof environments
- **Algorithm Typesetting**: algorithmicx for pseudocode
- **Code Listings**: listings package for code snippets

## Installation

### For WorkBuddy Users

```bash
# Copy the skill folder to your WorkBuddy skills directory
cp -r latex-editor ~/.workbuddy/skills/
```

### For Standalone Use

```bash
# Clone this repository
git clone https://github.com/cx677/latex-editor-skill.git
cd latex-editor-skill

# Install Python dependencies (optional, for scripts only)
pip install -r requirements.txt
```

## Usage

### Via WorkBuddy AI

Simply describe what you need in natural language:

```
"Write an IEEE paper about neural theorem proving"
"Compile my paper.tex to PDF"
"Format this LaTeX code"
"Create a table with booktabs style"
```

### Via Command Line

```bash
# Compile LaTeX to PDF
python scripts/compile_latex.py input.tex -o output_dir

# Format and lint LaTeX
python scripts/format_latex.py input.tex --check
python scripts/format_latex.py input.tex --fix
```

## Scripts

### compile_latex.py

Compiles LaTeX files to PDF.

```bash
python scripts/compile_latex.py <input.tex> [-o output_dir] [-c compiler] [-p passes]
```

Options:
- `-o, --output`: Output directory (default: same as tex file)
- `-c, --compiler`: Compiler choice (pdflatex/xelatex/lualatex, auto-detect by default)
- `-p, --passes`: Number of compilation passes (default: 2)

### format_latex.py

Formats and lints LaTeX source code.

```bash
python scripts/format_latex.py <input.tex> [--check] [--fix]
```

Options:
- `--check`: Only check for issues, do not modify
- `--fix`: Automatically fix issues (default)

## Templates

### IEEE Template

Located at `references/ieee_template.tex`, includes:
- IEEEtran document class
- Chinese language support (ctex)
- Math environments
- Algorithm environment
- Code listing support
- Booktabs tables

### ACM Template

Located at `references/acm_template.tex`, includes:
- acmart document class
- Same auxiliary packages as IEEE template
- ACM-Reference-Format bibliography

## Requirements

- Python 3.6+
- LaTeX distribution (TeX Live, MiKTeX, or MacTeX)
- For Chinese support: ctex package

## Project Structure

```
latex-editor/
├── SKILL.md                 # Skill definition for WorkBuddy
├── README.md                # This file
├── scripts/
│   ├── compile_latex.py     # LaTeX compilation script
│   └── format_latex.py      # LaTeX formatting script
└── references/
    ├── ieee_template.tex    # IEEE conference template
    └── acm_template.tex      # ACM SIG template
```

## License

MIT License - see LICENSE file for details.

## Acknowledgments

Built with WorkBuddy AI Agent framework.
