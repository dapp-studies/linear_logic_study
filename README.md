# Linear Logic study document
This document serves the generation of flashcarts to remember and study
[Frank Pfenning's 2012 Course on Linear Logic](http://www.cs.cmu.edu/~fp/courses/15816-s12/schedule.html).

## Usage
1. Install and Get familiar with Anki: http://ankisrs.net/
(I use it on PC + Phone)
2. Install ang get familiar with Latex Import: http://reh.math.uni-duesseldorf.de/~zibrowius/LatexNoteImporter/
3. You will need a custom anki not type:
    * create a new custom note type with the name Latex
    * import the `linear_logic.apkg` in your anki
    * from here on you can import `doc.tex` into the linear logic dec
4. Sync & enjoy

### VIM
I use the following snippet in ultisnips to generate a card boilerplate:

```
global !p
from uuid import uuid4
def uuid():
	return str(uuid4())
endglobal

snippet note "Anki note" b
\begin{note}
  \xplain{`!p if not snip.c: snip.rv = uuid()`}
  \begin{field}
		${1}
  \end{field}
  \begin{field}
		${2}
  \end{field}
\end{note}

endsnippet
```
