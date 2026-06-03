# LaTeX PhD Thesis Template

This repository contains a LaTeX template designed for writing a PhD thesis. 

## 🌟 Key Features
* **Global & Local Tables of Contents:** Includes a general Table of Contents at the beginning, as well as individual mini-tables of contents (`minitoc`) at the start of each chapter.
* **Per-Chapter Bibliography:** Bibliographies are managed independently for each chapter.
* **Real-world Example:** A complete PhD thesis successfully written and defended using this exact template is available on HAL: [tel-04093846v2](https://theses.hal.science/tel-04093846v2).

---

## 🛠️ Configuration & Customization

### Personalization
* **Custom Commands:** Remember to modify or add your own shortcuts, macros, and `\renewcommand` declarations in the `new_command.tex` file.
* **Language Switch (French to English):** If you wish to write your thesis in English, open `Preambule.tex` and update the following packages:
    ```latex
    \usepackage[english]{babel}
    \usepackage[english]{minitoc}
    ```

### Package Management Warning
> ⚠️ **Important:** Avoid changing the order of the packages loaded in `Preambule.tex`, as LaTeX package conflicts can easily occur. If you need to remove any packages, delete them **one by one** and compile between each deletion to ensure no errors are introduced.

---

## 🚀 Compilation Guide

This template has been tested and verified **locally** using **Texmaker** and **MiKTeX**. To ensure all cross-references, bibliographies, and mini-TOCs render correctly, follow this precise compilation sequence:

1.  **Initial Layout:** Compile `main.tex` twice using **PdfLaTeX + View PDF**.
2.  **Chapter Bibliographies:** Run **BibTeX** twice on *each individual chapter file* that contains a bibliography (do not run it on chapters without references).
3.  **Final Integration:** Recompile `main.tex` **three times** (twice to integrate the bibliography citations and once more to resolve the `backref` links).

ℹ️ Note on Overleaf: This template has not been deployed on Overleaf because the compilation time - even for this minimal working example - exceeds the timeout limits of Overleaf's free tier. Local compilation is highly recommended.

---

## 📁 Repository Structure & Useful Files

### Bibliography Styles (`.bst`)
* `apalike-fr.bst`: Used for author-date citation styles adapted for French text.
* `unsrtnat.bst`: Used for numerical citation styles sorted by order of appearance, compatible with `natbib`.

### The "others" Folder
This directory contains helper tools for data visualization and figure generation:
* `notebook.txt`: Contains the boilerplate preamble configuration used for generating Python figures that match the thesis style.
* `bone_violet.json`: A custom colormap designed and used for displaying medical images (X-rays and CT scans).

---

## 💡 Pro-Tips for Writing

* **Importing external documents (Word, etc.):** If you need to include external pages (e.g., appended papers or certificates), avoid standard "Export to PDF" functions from Word, as they can sometimes degrade image quality. Instead, use the **"Print to PDF"** option using a virtual PDF printer to preserve maximum sharpness.
