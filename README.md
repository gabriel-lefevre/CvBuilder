# CvBuilder 📄

A clean LaTeX CV template with easy customization - just clone, edit, and generate your PDF.

## 🎯 Features

- **Modern Design**: Professional layout with clean typography and attractive colors
- **Modular Structure**: Each section in a separate file for easy editing
- **Universal Compatibility**: Uses only standard LaTeX packages - works on any distribution
- **Smart Fallback**: Automatically uses example files if personal files don't exist
- **ATS-Friendly**: Optimized for Applicant Tracking Systems
- **One-Page Layout**: Designed to fit all content on a single page

## 🚀 Quick Start

### 1. Clone the Repository
```bash
git clone https://github.com/gabriel-lefevre/CvBuilder.git
cd CvBuilder
```

### 2. Copy Example Files
```bash
cp -r examples/ personal/
```

### 3. Edit Your Information
Edit the files in the `personal/` folder with your own information:

- **`header.tex`** - Name, contact info, and social links
- **`summary.tex`** - Professional summary or objective
- **`skills.tex`** - Technical skills organized by category
- **`experience.tex`** - Work experience with achievements
- **`education.tex`** - Education and degrees
- **`projects.tex`** - Personal projects and contributions
- **`certifications.tex`** - Certifications and languages

### 4. Generate Your CV
```bash
pdflatex main.tex
```

Your CV will be generated as `main.pdf`!

## 📁 Project Structure

```
CvBuilder/
├── main.tex              # Main template file (don't edit)
├── .gitignore            # Protects your personal files
├── README.md             # This file
├── examples/             # Example files (reference)
│   ├── header.tex
│   ├── summary.tex
│   ├── skills.tex
│   ├── experience.tex
│   ├── education.tex
│   ├── projects.tex
│   └── certifications.tex
└── personal/             # Your personal files (gitignored)
    ├── header.tex        # Edit these with your info
    ├── summary.tex
    ├── skills.tex
    ├── experience.tex
    ├── education.tex
    ├── projects.tex
    └── certifications.tex
```

## ✏️ Editing Guide

### Header Information
In `personal/header.tex`, update these variables:
```latex
\newcommand{\firstname}{Your}
\newcommand{\lastname}{Name}
\newcommand{\jobtitle}{Your Job Title}
\newcommand{\cvphone}{+1-234-567-8900}
\newcommand{\cvemail}{your.email@example.com}
\newcommand{\cvlinkedin}{your-linkedin-username}
\newcommand{\cvgithub}{your-github-username}
\newcommand{\cvwebsite}{} % Optional: www.yourwebsite.com
```

### Experience Entries
In `personal/experience.tex`, use this format:
```latex
\cventry{Company Name}{Date Range}{\textit{Job Title}}{
\begin{itemize}
\item Achievement or responsibility with quantified results
\item Another accomplishment showing impact
\item Technical skills used or projects completed
\end{itemize}
}{}{}
```

### Skills Categories
In `personal/skills.tex`, organize by category:
```latex
\textbf{Category Name} Technology, Tools, Languages \\
\textbf{Another Category} More technologies, frameworks \\
```

### Projects
In `personal/projects.tex`:
```latex
\cvproject{Project Name}{Date Range}{
\begin{itemize}
\item Brief description of the project
\item Technologies used and your role
\item Results or impact achieved
\end{itemize}
}{}
```

## 🛠️ Requirements

- **LaTeX Distribution**: TeX Live, MiKTeX, or MacTeX
- **Required Packages**: All packages used are standard (article, geometry, xcolor, etc.)
- **Compiler**: pdflatex

### Installation
- **Windows**: Install [MiKTeX](https://miktex.org/)
- **macOS**: Install [MacTeX](https://www.tug.org/mactex/)
- **Linux**: Install TeX Live via package manager
  ```bash
  # Ubuntu/Debian
  sudo apt-get install texlive-full
  
  # Fedora
  sudo dnf install texlive-scheme-full
  ```

## 🎨 Customization

### Colors
To change the color scheme, edit these lines in `main.tex`:
```latex
\definecolor{headercolor}{RGB}{45, 130, 120}  % Section headers
\definecolor{linecolor}{RGB}{218, 165, 32}    % Section lines
```

### Layout
- Adjust margins in the `\geometry{}` section
- Modify section spacing in `\titlespacing{}`
- Change font sizes by editing the document class: `[10pt,a4paper]`

## 🔒 Privacy

Your personal information is protected:
- The `personal/` folder is automatically ignored by Git
- Only example files are committed to the repository
- Your real CV data stays local and private
