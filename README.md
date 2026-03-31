# LaTeX Template for University Projects

This is a professional LaTeX template optimized for reports, dissertations, and academic projects at the **Universitat Politècnica de València (UPV)**.

Designed to be modular, clean, and compliant with academic standards.

---

## 📁 Project Structure

```text
.
├── main.tex              # Main file (compile this one)
├── refs.bib              # Bibliographic database (BibTeX)
├── logos/                # Institutional assets
│   ├── telecom.png       # School logo
│   ├── UPV.png           # University logo
│   └── background.png    # Title page watermark
└── Chapters/             # Content folder
    ├── Agradecimientos.tex
    ├── intro.tex
    ├── chapter1.tex
    └── ...
```

## Installation & Requirements
### 1. Compiler

It is highly recommended to use Overleaf, pdfLaTeX or LuaLaTeX.


Since this template uses the `minted` package for code blocks, you must compile with the `-shell-escape` flag enabled.

- **Overleaf:** Handled automatically.

- **Local (VS Code / Texmaker):** You must enable it in your compiler settings.

- **Python:** minted requires Pygments installed on your system.

### 2. Required Packages

Ensure you have a full LaTeX distribution (TeX Live or MiKTeX). Key packages used:

- **titlesec**, **tocloft** (Heading and TOC formatting)

- **fancyhdr** (Page styling)

- **biblatex** (Reference management)

- **wallpaper** (Background image support)

- **minted** (Source code highlighting)

## Usage Instructions

1. **Project Metadata:** Open main.tex and update the student names, professor, and document title.

2. **Chapters:** Create or edit .tex files in the Chapters/ directory. Link them in the main body using \input{Chapters/filename}.

3. **Bibliography:** Add your BibTeX entries to refs.bib and cite them in your text using \cite{key}.

4. **Compilation Steps:** To ensure all references and indices are updated, run the following sequence:
```
pdflatex -shell-escape main.tex
biber main
pdflatex -shell-escape main.tex
pdflatex -shell-escape main.tex
```

## Contributing

If you are a student at UPV and wish to improve this template (add new section formats, fix margin issues, or enhance the title page), Pull Requests are more than welcome!