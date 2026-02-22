# Harvard Dissertation LaTeX Template for Overleaf

The template originally posted by GitHub user [suchow](https://github.com/suchow/Dissertate) does not compile in Overleaf out of the box, and does not satisfy the current Harvard format requirements (see list of specific changes below). Using these changes, I submitted my dissertation to Harvard Graduate School of Arts and Sciences in November 2025, and it was accepted by ProQuest/EDT.

This is not a replacement as I have not tested its local LaTeX compilation, and I have only kept files relevant to Harvard.

# How to Use

1. Download repo as a zip file (Green "<> Code" button > Download ZIP)
2. Upload to Overleaf (New Project > Upload Project), the initial compilation should look like [the pdf example](Harvard_Dissertation_Template.pdf)
3. Minor changes required in [`assets/schools/Harvard/style.sty`](assets/schools/Harvard/style.sty):
    - Line 58: Update copyright year with your year of completion
    - Line 71: If applicable, replace ``Dissertation'' with ``Thesis''
4. Update personal information in [`assets/latex-base/frontmatter`](assets/latex-base/frontmatter)
    - `personalize.tex`: Author, advisor, and degree information
    - `dedication.tex` brief dedication
    - `thanks.tex`: extended acknowledgements section
    - `authorlist.tex`: list authors who contributed to each chapter
    - `abstract.tex`: overarching abstract for entire dissertation
5. Write dissertation content inside of [`assets/latex-base/chapters`](assets/latex-base/chapters)
   - `chapter#.tex`: chapter title, chapter preface (before introduction), and *optional* footnote if material appears elsewhere 
   - `chatper#_manuscript.tex`: useful if copying contents over from a completed manuscript
   - `chapter\#_appendix.tex`: *optional* appendix for each chapter. *Not required by Harvard*

**Recommendations**
   - Renaming all `\label{label-name}` to `\label{ch#_label-name}` will avoid overlapping cross reference labels with other chapters. This is especially useful if pasting separate manuscripts in.
   - Captions in `\caption{}` appear on the listing of figures page. These can be limited to short descriptions, and detailed captions can be placed in `\subcaption{}`.

# Specific Changes in this Fork
- Adding optional appendices
- Included listing of figures (mandatory for Harvard)
- Included listing of authors (mandatory for Harvard)
- Fixing page numbering of table of contents and acknowledgements
- Adding the following pages to table of contents:
    - Title page
    - Copyright
    - Abstract
    - Table of Contents
    - List of figures
    - Author list
    - Acknowledgments
