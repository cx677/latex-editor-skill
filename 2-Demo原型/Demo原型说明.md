# LaTeX Editor Skill - Demo & Prototype

## Interactive Demo

### Demo 1: AI-Assisted LaTeX Generation

**Scenario:** Generate a complete IEEE conference paper on AI4Math

```
User Input:
"Write an IEEE paper about neural theorem proving with 3 pages"

AI Output (LaTeX):
- Complete IEEEtran document structure
- Abstract, keywords, sections
- Mathematical notation and proofs
- Bibliography entries
```

### Demo 2: Real-time Compilation

**Scenario:** Compile LaTeX to PDF with error handling

```
User Input:
"Compile my paper.tex to PDF"

System Response:
1. Detecting LaTeX distribution... pdflatex found
2. Running pass 1/2...
3. Running pass 2/2...
4. PDF generated: paper.pdf (45KB)
```

### Demo 3: Auto-Formatting

**Scenario:** Format messy LaTeX code

```
Before:
\begin{equation}f(x)=x^2+2x+1\end{equation}

After:
\begin{equation}
    f(x) = x^2 + 2x + 1
\end{equation}
```

## Prototype Screenshots

### Workflow Diagram

```
┌─────────────────────────────────────────────────────────────┐
│                    LaTeX Editor Skill                        │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│   ┌──────────┐    ┌──────────┐    ┌──────────┐              │
│   │ Template │ -> │ Content  │ -> │ Compile  │              │
│   │ Selection│    │ Generation│    │   to PDF │              │
│   └──────────┘    └──────────┘    └──────────┘              │
│        │                │                │                   │
│        v                v                v                   │
│   ┌──────────┐    ┌──────────┐    ┌──────────┐              │
│   │ IEEE/ACM │    │ Math/Text│    │  Error   │              │
│   │  Styles  │    │  Code    │    │ Handling │              │
│   └──────────┘    └──────────┘    └──────────┘              │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

### Feature Matrix

| Feature | Status | Description |
|---------|--------|-------------|
| IEEE Template | ✅ | Full IEEEtran support |
| ACM Template | ✅ | Full acmart support |
| PDF Compilation | ✅ | Auto-detect pdflatex/xelatex |
| Code Formatting | ✅ | Auto-indent and lint |
| Math Rendering | ✅ | AMSMath/AMSLaTeX |
| Algorithm Typesetting | ✅ | algorithmicx |
| Code Listing | ✅ | listings package |
| Chinese Support | ✅ | ctex integration |

## Usage Examples

### Example 1: Academic Paper Generation

```latex
% User asks: "Write a paper about machine learning"
% AI generates:
\documentclass[conference]{IEEEtran}
\usepackage{amsmath,amssymb}
...
```

### Example 2: Mathematical Expression

```latex
% User asks: "Write the Bayes theorem equation"
\[
P(A|B) = \frac{P(B|A)P(A)}{P(B)}
\]
```

### Example 3: Table with booktabs

```latex
% User asks: "Create a comparison table"
\begin{table}[t]
    \caption{Experimental Results}
    \begin{tabular}{lcc}
        \toprule
        Method & Accuracy & F1 \\
        \midrule
        Ours & 95.2\% & 0.94 \\
        Baseline & 89.1\% & 0.87 \\
        \bottomrule
    \end{tabular}
\end{table}
```

## Performance Metrics

| Metric | Value |
|--------|-------|
| Template Generation Time | < 2s |
| PDF Compilation Time | < 30s |
| Formatting Check Time | < 1s |
| Success Rate | > 95% |
