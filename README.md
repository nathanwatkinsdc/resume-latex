# LaTeX Resume Template
A clean, modular LaTeX resume template that I built for my own use. I got tired of wrestling with Word formatting and wanted something that would look consistent every time I compiled it. 

## Why I Made This
It should come as no surprise that it's really hard and tedious to use MS Word to type up math proofs, so when professors required typed responses for math classes in college, I'd turn to LaTeX, a mathematical markup language that's beautifully flexible. 

When I started applying for jobs recently, I realized what a pain it was to tailor resumes for each and every job application in MS Word. I started to wonder, wouldn't this be easier in LaTeX?

In a short while, I went from wondering to drafting a template that is...

- **Modular**: Each section lives in its own file so you’re not scrolling through a massive document
- **Easy to customize**: Want to change colors or spacing? Everything’s in one place
- **Version control friendly**: Perfect for tracking changes in git
- **Overleaf ready**: Works great in [Overleaf](https://overleaf.com) if you prefer browser-based editing

## File Structure

```
/
├── main.tex                 # Main document (compile this one)
├── resume_class.tex         # All the styling and custom commands
└── sections/
    ├── summary.tex          # Professional summary
    ├── experience.tex       # Work experience
    └── education.tex        # Education section
```

## Getting Started

### Option 1: Overleaf (Recommended)

1. Create a new blank project in Overleaf
1. Upload all these files maintaining the folder structure
1. Set `main.tex` as your main document
1. Hit compile!

### Option 2: Local LaTeX Installation

1. Clone this repo
1. Make sure you have a LaTeX distribution installed (TeX Live, MiKTeX, etc.)
1. Compile with: `pdflatex main.tex`

## Customization

### Personal Info

Update your details in `main.tex`:

```latex
\name{Your Name}
\address{Your Location}
\email{your.email@example.com}
\website{https://yourwebsite.com}
\phone{(123) 456-7890}
```

### Colors

Don’t like the blue headers? Change them in `resume_class.tex`:

```latex
\definecolor{headercolor}{RGB}{51, 102, 153}  % Header color
\definecolor{sectioncolor}{RGB}{51, 102, 153} % Section headers
```

### Adding New Sections

Want to add a Skills section? Just:

1. Create `sections/skills.tex`
1. Add `\input{sections/skills}` to `main.tex`
1. Use the standard `\section{Skills}` format

## Custom Commands

I built a few helper commands to keep things consistent:

- `\experienceentry{title}{company}{location}{dates}` - for job entries
- `\educationentry{degree}{school}{year}` - for education entries
- `\makeheader` - generates the header with your contact info

## Tips

- Keep bullet points concise - LaTeX doesn’t like overly long lines
- Use `\$` to escape dollar signs in salary/budget figures
- The template assumes US letter size, but you can change to A4 in `resume_class.tex`

## Contributing

This template works for my needs, but if you find bugs or have suggestions, feel free to open an issue or submit a PR. I’m always looking to improve it.

## License

MIT License - use it however you want. If it helps you land a job, buying me a coffee would be appreciated but definitely not required ☕️