Tsundoku: books and libraries templates
=======================================

This repository holds a collection of custom and raw templates based on
different tools such us cookiecutter and pandoc, for either writing source code
libraries or academical essays. 

> The name "Tsundoku" is a term from Japanese language which refers to the
> action of buying any kind of readable materials but which will never be
> completely read because of their insane amount.


Essay template
--------------

<img align="left" width="200px" src="screenshots/preview_essay.png">

Some time ago, I found an old book titled "El Universo y nosotros" by A. F.
Marfeld. It contains the most beautiful format I have ever seen within a volume
and wanted to recreate it in an easy way by making use of Markdown, LaTeX and
pandoc.

The table of contents is controlled by a file called `toctree.txt` which holds
different links to markdown files inside the `src/` directory. Each one of those
is assumed to be a chapter of the final essay. Any kind of figure must be placed
inside the `fig/` directory in order to be properly linked once compiling all
source files.

Future ideas and improvements for this template are still being considered:
check suitable font family, simplify LaTeX files, convert into cookiecutter
project...
