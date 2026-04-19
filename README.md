# osu_accessible_thesis_template

Repository with instructions and reference template for writing a thesis at Oregon State University. This template is designed for digital accessibility and based on the original beavtex.cls that was used at the School of Electrical Engineering and Computer Science (EECS).

Please note: this is **NOT** an official template by Oregon State University. Unfortunately, there is [quite a bit of misleading information out there](https://accessibility.oregonstate.edu/digital-accessibility/resource-page/pdf-decision-tree-instructional-materials) on the accessibility of PDFs. For LaTeX, you should check the following resources:
* [LaTeX Tagging Project: Usage Instructions](https://latex3.github.io/tagging-project/documentation/usage-instructions) how to ensure accessible PDFs when using LaTeX
* [LaTeX Tagging Project: Tagging Status of LaTeX Packages](https://latex3.github.io/tagging-project/tagging-status/) to check if your package is marked as compatible with tagging (this is an ongoing development)

## ⭐ About:
### Motivation:

* Make sure LaTeX can be used in the future
* The old template provided by OSU has/had compatibility issues: [EECS template](https://engineering.oregonstate.edu/EECS/myeecs/current-graduate-students/forms) (note, this link might stop working after April 24, 2026)
* Ensure compatibility with the [previous requirements](https://web.archive.org/web/20220218044531/https://gradschool.oregonstate.edu/sites/gradschool.oregonstate.edu/files/2021-08/thesisguide2022-v2.pdf) of the Graduate School. Note that the [new requirements](https://graduate.oregonstate.edu/current-students/thesis-guide/formatting-thesis-or-dissertation) are largely the same but now include 'dubious' requirements such as: "All headings, regardless of level, must be the same font size" that are not aligned with the needs of the majority of readers while also not improving digital accessibility for which proper tagging is needed (independent of font size)
* LaTeX issues are a great way to procrastinate; but we want to be productive! 👍 😄
* Make sure LaTeX best-practices are followed

### 🟠 Status: 

This repository is a *work in progress*. The digital accessibility status of this template is as follows:
* Ally/UDOIT (Canvas): 100% accessibility
* [VeraPDF (PDF/UA-1)](https://dev.verapdf-rest.duallab.com/): passes
* Acrobat (accessibility): passes "Check for accessibility" and also compliance against PDF/UA-1 (Preflight)

Note: the legal requirement is WCAG 2.1 Level AA. The PDF standards PDF/UA-1 (and PDF/UA-2) have varying degrees of overlap with this but do not replace accessibility checking. Acrobat has separate checking tools for accessibility and PDF/UA compliance (this is called Preflight). For PDF/UA compliance, VeraPDF is recommended. The combination of accessibility features with PDF/UA-1 should provide "substantially equivalent or greater accessibility" compared to what is legally required. PDF/UA-2 is newer than the legislation on digital accessibility.

### ✨ Code Style:
None specifically. It is important to keep the directory structure. Additional notes:
* Each line of text in your .tex should be a separate line (if using GIT, to help GIT versioning)
* thesis.pdf should not be committed using GIT regularly (see .gitignore)
* Only occasionally, commit your pdf using a separate file name; or upload to Box.com
* Do not use mathmode in any chapter/section/etc.-command (i.e., anything that would show up in the Table of Contents)
* Remember to pay attention to the accessibility features (alt text, reading order for tables, etc.)
* When clearing auxiliary files, please make sure to remove also *-luamml-mathml.html

### Workflow for Including References

* use Zotero and biber exclusively (**not** bibtex)

*IMPORTANT 1*: this thesis template requires biber for creating the bibliography. For historical reasons, bibtex is set as the default in TexStudio (and possibly other IDEs). Please double-check how your IDE is configured!

*IMPORTANT 2*: when using Zotero to export references, select "Format: Better BibLaTeX" (*NOT* Better BibTeX)

### Workflow for Creating Tables

* Be lazy, be smart, and use a generator for creating tables
* [Option 1:](https://www.tablesgenerator.com/latex_tables) This online tables generator can also import from .csv 
* Option 2: LyX (view code, copy into your document)
* Follow proper typesetting guidelines: use booktabs style for your table

### Workflow for Creating Figures/Plots

There are three different directories for figures:
* figures_external: for external figures not created by you; you are strongly encouraged to make a fair use determination to ensure you are permitted using this figure. A Markdown template is provided as an example to guide this process.
* figures_internal: any figure created by you but outside of LaTeX or without a Makefile
* figures: what I (Vincent) use in combination with a Makefile to externalize the process of building plots, figures, etc. (matplotlib, gnuplot, pgfplots, IPE, etc.)

### Workflow for Creating Algorithms

Very briefly tested only:
* algorithm with algpseudocode appears to work (algpseudocodex uses a too light gray causing color contrast issues)
* algorithm2e currently does not work
* Creating a list of algorithms currently does not work

### Overleaf

*IMPORTANT*: should you use this on Overleaf, name your Overleaf project and .tex file as follows:
* type_thesis_firstname_lastname
* type = {hc, ms, phd, other}
* for example: ms_thesis_benny_beaver
* this is especially important when sharing your Overleaf project with your advisor
* _do not_ name your thesis "mythesis" or other non-identifying descriptions

**Note: ENGR students get a free Premium Overleaf account through OSU!**

Why is a Premium Overleaf account important? Because otherwise, compile time of your document is too limited for large documents (such as, our thesis template).

[Sign up to Overleaf](https://www.overleaf.com/edu/oregonstate) using your preferred email as _primary_ email (does not have to be your OSU address). Then, under account preferences/settings, add your onid@ENGR.oregonstate.edu address as _professional_ email. Note the additional ENGR which is probably never needed in any other context.

### Helpful LaTeX Links

* [Find that Symbol](https://detexify.kirelabs.org/classify.html) Website to draw a symbol to get the corresponding LaTeX code (best match)
* [Slides on ISO80000 Compliant Equations](https://oregonstate.box.com/s/4hk1nea2ku4ponemff6ssj4z37w3krdv) What I created for the EECS Graduate Student Association
* [Author Guidelines for Preparing Accessible Mathematics Content](https://epubs.siam.org/pb-assets/author_guidelines_accessible_mathematics.pdf)
* [AMS Guidance for Making Mathematics Accessible Online](https://www.ams.org/accessibility/accessibility-guidance)

### Acknowledgements

Creating this thesis template has been a collaborative effort by multiple people affiliated with Oregon State University: Heidi Schellmann, David A Craig, Ross Hatton, and Vincent Immler.
