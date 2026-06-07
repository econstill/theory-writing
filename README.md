# Econ Theory Writing And Slides Context

This thread/workspace is intended to serve as reusable context for writing economics theory papers and Beamer slides. When continuing this work in another Codex thread or on another machine, read this file first and treat it as standing background.

## Working Style

- Help write, revise, and organize economics theory papers and presentation slides.
- Prefer clean mathematical exposition: clear primitives, assumptions, propositions, proofs, examples, intuition, and economic interpretation.
- For slides, optimize for oral presentation rather than document-style completeness.
- Keep a separate backup/appendix layer for technical details, robustness, extra tables, and derivations.
- When drafting slides from a theory paper, make each slide carry one conceptual step or result.

## Beamer Defaults From `beamer_tips.pdf`

Source: `D:/Papers_PDF/Incoming/beamer_tips.pdf`, "Tips + Tricks with Beamer for Economists" by Paul Goldsmith-Pinkham, dated March 11, 2019.

### Core Design Principles

- Aim for minimalist slides, but not boring slides.
- Make one point well on each slide.
- Do not overwhelm the audience with text.
- Use slides to guide attention; put dense material in backup slides.
- Prefer 16:9 aspect ratio for modern presentation layouts and easier figure/text combinations.

### Text And Spacing

- Use section transition frames instead of ordinary section-title frames when moving between major parts.
- Use a spacious itemize environment, such as a custom `wideitemize`, to discourage overfull slides.
- Rule of thumb: about 45-75 characters per line.
- Rule of thumb: one sentence should fit on one line when possible.
- Do not reduce font size just to fit more text. If a slide becomes busy, move the detail to backup.
- A roadmap at each section is optional. If used, add a Beamer `\AtBeginSection` table-of-contents frame.

### Color

- Avoid relying on red/blue contrasts alone because colorblindness is common.
- Use two or three recurring colors throughout a deck.
- Suggested Okabe-Ito style colors:
  - Blue: `RGB(0,114,178)`
  - Red/orange: `RGB(213,94,0)`
  - Yellow: `RGB(240,228,66)`
  - Green: `RGB(0,158,115)`
- Use blue as the main accent, red/orange for contrast or emphasis, green as a secondary accent, and yellow for transition slides.
- Consider an off-white background for readability, for example `RGB(255,253,218)`.
- In large auditoriums, consider a black background with white text for stronger contrast.
- Match figure backgrounds to slide backgrounds, or use transparent figure backgrounds.

### Fonts And Readability

- Changing fonts can materially improve slides.
- The reference deck uses Lato; consider `\usepackage[default]{lato}`.
- Graph labels, axis labels, legends, and annotations need to be much larger than they appear to need on a laptop.
- If something looks slightly too large on the computer, it may be appropriate for the audience.

### Figures

- Make the figure central whenever possible.
- Use simple sizing commands such as `\resizebox{0.7\linewidth}{!}{\includegraphics{...}}`.
- Remember that `\linewidth` depends on the current environment, such as a column.
- Center figures unless there is a deliberate reason not to.
- For iterative explanation, reveal related figures or effects with `\only<...>`, keeping axes and scale consistent across reveals.
- Use TikZ annotations or overlays to highlight research design, timing, formulas, and relevant parts of figures.

### Tables

- Do not use the floating `table` environment in Beamer unless there is a specific reason.
- Use `\makebox[\linewidth][c]{...}` to center tables that need to fit the slide.
- Change `[c]` to `[l]` when left alignment is better.
- Use TikZ or overlay tools to highlight important cells.
- Sequentially revealing rows or columns with `\onslide` can be useful, but do not overuse it.
- If using sequential reveals, practice the talk so the click-through does not feel artificial.
- Sometimes showing full context is better than controlling visibility.

### Math And Theory Slides

- Do not overload slides with equations, regressions, or theorems.
- Use color, labels, braces, and short text to highlight the part of the formula currently being discussed.
- For theory papers, translate formal results into slides by separating primitives, mechanism, proposition, intuition, and proof sketch.
- Put full proofs, edge cases, and algebra-heavy derivations in backup slides.

### Beamer Mechanics

- Remove navigation symbols.
- Use frame numbers in the footline.
- Use named frame labels for backup links.
- Use `\appendix` so backup slides restart numbering after the main talk.
- Use `\hyperlink{label}{object}` and Beamer buttons to jump to backup slides and back.
- Use Beamer notes with `\note{...}` for speaker prompts.

### Useful Frame Types To Keep Around

- Section transition frame.
- Two-column frame.
- Table frame.
- Figure frame.
- Figure-with-commentary frame.
- Research-design timeline frame.
- Equation-highlight frame.
- Backup detail frame linked from the main talk.

## Default Beamer Preamble Preferences

```tex
\documentclass[aspectratio=169]{beamer}

\usepackage[default]{lato}

\definecolor{blue}{RGB}{0,114,178}
\definecolor{red}{RGB}{213,94,0}
\definecolor{yellow}{RGB}{240,228,66}
\definecolor{green}{RGB}{0,158,115}
\definecolor{MyBackground}{RGB}{255,253,218}

\setbeamercolor{background canvas}{bg=MyBackground}
\setbeamercolor{frametitle}{fg=blue}
\setbeamercolor{title}{fg=black}
\setbeamertemplate{footline}[frame number]
\setbeamertemplate{navigation symbols}{}
\setbeamercolor{itemize item}{fg=blue}
\setbeamercolor{itemize subitem}{fg=blue}
\setbeamercolor{enumerate item}{fg=blue}
\setbeamercolor{enumerate subitem}{fg=blue}
\setbeamercolor{button}{bg=MyBackground,fg=blue}

\newenvironment{transitionframe}
  {\setbeamercolor{background canvas}{bg=yellow}\begin{frame}}
  {\end{frame}}
```

## Future Instruction For Codex

When helping with econ theory slides in this workspace:

- Start from the paper's economic logic, not from decorative slide design.
- Enforce low text density and high readability.
- Prefer one result, mechanism, assumption, figure, or intuition per slide.
- Build appendix/backup slides aggressively for anything dense.
- Use Beamer links to backup material when a main-slide claim needs technical support.
- Keep colors consistent and colorblind-friendly.
- Make figures and tables presentation-sized, not paper-sized.
- When possible, compile and visually inspect Beamer output before final delivery.
