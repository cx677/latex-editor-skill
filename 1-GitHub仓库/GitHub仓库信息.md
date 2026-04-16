# LaTeX Editor Skill - GitHub Repository

## Repository Information

**Repository Name:** latex-editor-skill
**GitHub URL:** https://github.com/cx677/latex-editor-skill
**Created Date:** 2026-04-17
**License:** MIT License

## Repository Structure

```
latex-editor-skill/
├── SKILL.md                 # Skill definition file
├── README.md                # English documentation
├── README_zh.md             # Chinese documentation
├── scripts/
│   ├── compile_latex.py     # LaTeX compilation script
│   └── format_latex.py      # LaTeX formatting script
├── references/
│   ├── ieee_template.tex    # IEEE conference template
│   └── acm_template.tex     # ACM SIG template
└── examples/
    ├── sample_ieee.tex       # IEEE paper example
    └── sample_acm.tex        # ACM paper example
```

## GitHub Actions CI/CD

```yaml
# .github/workflows/lint.yml
name: LaTeX Lint
on: [push, pull_request]
jobs:
  lint:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: '3.9'
      - name: Install dependencies
        run: pip install pylint
      - name: Lint scripts
        run: pylint scripts/*.py
```

## Installation Instructions

### For WorkBuddy Users
```bash
# Copy skill folder to ~/.workbuddy/skills/
cp -r latex-editor-skill ~/.workbuddy/skills/latex-editor
```

### For Standalone Use
```bash
# Clone repository
git clone https://github.com/cx677/latex-editor-skill.git

# Install Python dependencies
pip install -r requirements.txt

# Run examples
python scripts/compile_latex.py examples/sample_ieee.tex
```

## Version History

| Version | Date | Changes |
|:--------|------|---------|
| v1.0.0 | 2026-04-17 | Initial release |

## Contributing

Pull requests are welcome! Please read the contributing guidelines first.
