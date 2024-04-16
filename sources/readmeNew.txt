Latex:
---------

For writing the thesis it is recommended to use Latex2e. A short guide about Latex 2e(in Italian) can be found at this link http://ctan.mirror.garr.it/mirrors/CTAN/info/lshort/italian/itlshort.pdf.
Latex is a document-producing system that follows the same logic of programming languages. As such, the first step to take during the writing of the thesis is to prepare some latex sources (for the various chapters,
appendices and bibliography), which will need to be compiled to produce the thesis in the dvi format, which can be converted into postscript (viewable through ghostview) or pdf (viewable through acrobat reader). 
The files in the directory already provide a template to use during the writing of the thesis.

The following guide illustrates the steps needed for the installation of
the necessary Latex packages that enable the use of the provided template:

Linux Environment:
---------------
These instructions refer to the installation of Texmaker on a
Red Hat-like GNU/Linux distribution.

Installation:
- Open a terminal window as root;
- Install Texmaker and the necessray Latex packages with the following command:
	yum install texmaker texlive-babel-italian texlive-hyphen-italian texlive-subfigmat texlive-appendix
 The dependencies will be automatically installed during the execution of the command.
 In case one wishes to recompile the template itself, install the package texlive-lipsum.

Building procedure:
- Open the Thesis.tex file with Texmaker;
- Compile Thesis.tex with PDFLaTeX;
- Compile Thesis.tex with BibTeX;
- Compile Thesis.tex with PDFLaTeX 2 times;

Windows Enviornment:
-----------------
With Windows one can use the integrated development environment TeXstudio (http://texstudio.sourceforge.net/) or TeXnicCenter (http://www.texniccenter.org/). It is recommended to install (in the following order) the compiler miktex (http://www.miktex.org/), the poststscript interpreter (http://www.ghostscript.com/), the ghostview application (http://pages.cs.wisc.edu/~ghost/gsview/index.htm) and at the end TeXstudio or TeXnicCenter. To build the thesis it is sufficient to build the Thesis.tex file multiple times.

To allow for the ability to copy-paste from the produced pdf, it is recommended to use the sequence of compilation commands latex --> dvips --> ps2pdf or latex --> dvipdfm or pdflatex (recommended for this template). In addition, accented letters need to be inserted with the proper latex commands “\`a“, “\`e“, “\'e“, “\`{\i}“, “\`o“, “\`u” and not with the keys on your Italian keyboard. It is possible to use accented letters from your keyboard only if the latex files are saved in the UTF8 format and the package “inputenc” gets added with the option utf8 (via \usepackage[utf8]{inputenc}). 

Fonts:
-------

The PDF thesis can only make use of type 1 fonts. This verification can be made through Acrobat by going to File->Properties->Fonts. The header of thesis.tex (in the examples) already imposes the use of Type 1 fonts, but in the case such fonts aren't installed in the machine others will be used (es. Type 3 ones). In the case fonts different than Type 1 are used in the thesis, the package cm-super needs to be install and the thesis rebuilt. Under linux, the package can be installed like any other Latex package. Under Windows, using Miktex, it can be installed through the package manager (All Programs -> Miktex -> maintenance (Admin) -> Package Manager): you just need to search for cm-super anc click with the right mouse button to request installation (the package is installed only when the field "Installed On" reports a date).

File contents:
----------------------

The true contents of the thesis are contained in the files inside the directories:

- front: contains the start of the thesis (cover, summary, 
  dedications, introduction);
- main: contains the main chapters of the thesis;
- back: contains the conclusion, the appendices and the acknowledgements;
- bib: contains the Bibliography.bib file to fill following BibTeX's syntax

Structure of the thesis:
--------------------------

The thesis needs to be organized in chapters and needs to include in the end the indication of all the bilbiographic sources from which information has been gathered. Usually, the first chapter of the thesis introduces the context in which the work was carried on, the problem tackled in that context, the idea behind the proposed solution and in the end the indication of how the rest of the thesis is structured. Similarly, the last chapter of the thesis usually summarized the work done and provides suggestions regarding future developments. The suggested number of pages sits between 30 and 50.