# LaTeX Template - Opinionated Starter

A comprehensive, modular LaTeX document template with beautiful, opinionated styling for academic papers, technical documents, and reports. Features a modern theming system for both document and code highlighting.

## Getting Started

### Prerequisites

**Ubuntu/Debian:**
```bash
sudo apt install texlive-full
```

**Verify Installation:**
```bash
pdflatex --version
latexmk --version
```

### Recommended Editor Setup

**VS Code:**
- Install the [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) extension
- The project is pre-configured with `.vscode/settings.json`
- Auto-compile on save is enabled

### Quick Start

1. Clone or download this template
2. Open `main.tex` in your editor
3. Compile the document:
```bash
latexmk -pdf -outdir=build main.tex
```

Or simply save the file in VS Code with LaTeX Workshop - it compiles automatically!

## What is This?

This is an **opinionated LaTeX starter template** designed to get you writing quickly without dealing with LaTeX configuration headaches. It includes:

- **Modern, beautiful styling** - Professional color schemes and typography
- **Theme system** - Easy switching between document and code themes
- **Modular structure** - Separate files for sections, styles, and commands
- **Syntax highlighting** - Beautiful code blocks for C++, Java, Python
- **Pre-configured** - Common packages and commands ready to use
- **Clean organization** - Everything in its right place

Perfect for academic papers, technical reports, documentation, and dissertations.

## Features

### Document Themes
- `default_light` - Professional light theme with eye-relaxing colors
  - Warm terracotta sections
  - Teal subsections
  - Sage subsubsections

### Code Themes
- `code_light` - Clean light background with vivid syntax colors
- `code_dark` - Dark background with rich syntax highlighting
  - No rendering artifacts at any zoom level
  - Beautiful colors for keywords, strings, comments, types
  - Supports C++, Java, Python out of the box

## Structure

```
latex_template/
├── main.tex                    # Main document
├── sections/                   # Content sections
│   ├── introduction.tex
│   ├── methodology.tex
│   ├── results.tex
│   ├── code_examples.tex
│   └── conclusion.tex
├── styles/                    # Style files
│   ├── packages.sty           # Package imports
│   ├── mathcommands.sty       # Math commands
│   ├── customcommands.sty     # General commands
│   └── formatting.sty         # Page formatting
├── themes/                    # Theme files
│   ├── default_light.sty      # Document theme (light)
│   ├── code_light.sty         # Code theme (light)
│   └── code_dark.sty          # Code theme (dark)
├── build/                     # Compiled output
└── .vscode/                   # Editor configuration
    └── settings.json
```

## Usage

### Basic Document

The template includes example sections. Edit them or add your own:

```latex
\input{sections/introduction}
\input{sections/your-section}
```

### Code Blocks

**C++ Example:**
```latex
\begin{lstlisting}[style=cpp, caption={Your C++ Code}]
#include <iostream>
auto main() -> {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
\end{lstlisting}
```

**Java Example:**
```latex
\begin{lstlisting}[style=java, caption={Java Example}]
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
\end{lstlisting}
```

### Math Commands

The template includes handy math shortcuts:

```latex
% Sets
$\R$, $\N$, $\Z$, $\Q$, $\C$, $\E$, $\K$

% Derivatives
$\deriv{f(x)}{x}$, $\pderiv{f}{x}$

% Vectors
$\vect{v}$, $\mat{A}$

% Operators
$\argmax$, $\argmin$, $\diag$, $\mspan$, $\tr$
```

## 🔧 Customization

### Switching Themes

**Document Theme:**
Edit `main.tex`:
```latex
\usepackage{themes/default_light}   % or create your own
```

**Code Theme:**
Edit `main.tex`:
```latex
\usepackage{themes/code_light}   % or themes/code_dark
```

### Creating Custom Themes

Copy an existing theme file and modify colors:

```latex
% themes/my_theme.sty
\definecolor{sectionColor}{RGB}{your, colors, here}
```

### Adding Sections

1. Create `sections/newsection.tex`
2. Add to `main.tex`: `\input{sections/newsection}`

### Custom Commands

Add to `styles/customcommands.sty`:
```latex
\newcommand{\mycommand}[1]{\textbf{#1}}
```

## Tips

- **Compilation**: The `.vscode/settings.json` configures automatic compilation on save
- **Output**: All build artifacts go to `build/` directory (keeps root clean)
- **Bibliography**: Uncomment bibliography sections in `main.tex` to enable
- **Fonts**: Code uses Fira Code/Fira Mono if available (falls back to monospace)
- **Line Numbers**: Code blocks include line numbers by default

## Requirements

- LaTeX distribution (TeX Live, MiKTeX, or MacTeX)
- latexmk (usually included with LaTeX distributions)
- biber (for bibliography, if used)

## License

This template is free to use and modify for any purpose.

## Contributing

Feel free to fork and customize this template for your needs!
