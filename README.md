# LaTeX Resume

A clean and professional resume template built with LaTeX, featuring a modern design and easy customization options.

## Preview

This resume template includes:
- Modern and clean design
- Professional typography
- Sections for summary, projects, technical skills, and education
- Font Awesome icons for contact information
- Customizable colors and spacing

## Prerequisites

To build this resume, you'll need either:
- A LaTeX distribution installed on your system
- OR Docker installed (recommended for ease of use)

## Quick Start with Docker

1. Clone this repository:
```bash
git clone https://github.com/[your-username]/latex-resume
cd latex-resume
```

2. Build the PDF using Docker:
```bash
docker run --rm -i --user="$(id -u):$(id -g)" -v `pwd`:/data mingc/latex pdflatex /data/resume.tex
```

This command explanation:
- `--rm`: Removes the container after use
- `-i`: Runs in interactive mode
- `--user="$(id -u):$(id -g)"`: Runs as your user ID to avoid permission issues
- `-v pwd:/data`: Mounts current directory to /data in container
- `mingc/latex`: Uses the mingc/latex Docker image
- `pdflatex /data/resume.tex`: Runs pdflatex on your resume.tex file

## Manual Build

If you have LaTeX installed locally:

```bash
pdflatex resume.tex
```

## Customization

1. Open `resume.tex` in your preferred text editor
2. Modify the following sections:
   - Personal information in the header
   - Summary section
   - Projects section
   - Technical skills
   - Education details

### Color Customization

The template uses custom colors that can be modified:
```latex
\definecolor{linkcolor}{HTML}{000000}
\definecolor{sectioncolor}{HTML}{000000}
```

## Required LaTeX Packages

- fullpage
- titlesec
- marvosym
- color
- verbatim
- enumitem
- hyperref
- fancyhdr
- babel
- tabularx
- fontawesome
- xcolor

## License

MIT License - feel free to modify and reuse this template for your own personal or professional use.

## Acknowledgments

This template is inspired by modern resume designs and optimized for technical professionals in software development.