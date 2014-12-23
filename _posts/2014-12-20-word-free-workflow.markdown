---
layout: post
title:  "Finally... the Word-free manuscript workflow?"
date:   2014-12-23 14:40:00
categories: science word microsoft references
---

While I have used Microsoft Word&#174; for 20 years or so, it always
frustrated the hell out of me, and apparently I'm [not the only
one](https://www.facebook.com/pages/I-Hate-Microsoft-Word/237942199602618
). The extreme bugginess (anyone ever managed to create a stable
document longer than 50 pages?), the difficult formatting, the ugly
equations, the annoying theming features, the proprietary file format
(only partially solved with _.docx_), and so on. Why it is perfectly
fine for writing a letter, for writing research papers it is pretty
far from ideal. Obviously I have been continuosly looking around for
alternatives for writing manuscripts, but the real _Word-free_
workflow has so far eluded me.

# ![Word]({{ site.url }}/assets/word.jpg)

__OpenOffice__ is a potential alternative to Word, and it is a fairly
nice product (and free), but its main drawback is that it is not fully
compatible with Word. Especially its review functionality (showing
notes, deletions, additions, etc) is not compatible. And that is the
most important functionality when writing a research
paper in collaboration with Word-users...

__LaTeX__ is another obvious alternative. It actually has many
advantages over Word: it is text-based (so no file degradation and easy version
control), has beautiful typesetting, nice-looking equations, easy
compilation to PDF, etc. For many manuals and reports that
did not require collaboration I have used LaTeX a lot, and (learned to) love
it. However, I work in a research field that is only partially made up
of engineers, and LaTeX's steep learning curve is not something that
excites many of my collaborators. Which is no critique of them, I can
easily see that LaTeX can be more frustrating than
Word.

Over the last few years, __RStudio__ has evolved into the
indispensible IDE for R, and by offering support for __markdown__,
__knitr__, and __pandoc__ it offers a great workflow for creating PDF
manuscripts, and in a fully reproducible way too. Citations can be
added fairly easily using BibTex (although it would be nice to have a
simple reference manager in RStudio?). An almost perfect solution, one
is inclined to think, but not yet a full alternative to Word, since
the resulting manuscript (PDF) still has to be shared with
co-authors. This is less than perfect since some collaborators are
likely to have problems making notes and edits in PDF documents, and
any edits still have to be re-entered manually into the source document.

My usual workflow over the last few years has often been to start
drafting research papers in __Google Docs__, and move to Word (or RStudio)
when the time comes to add references and share the manuscript with
co-authors. It has been mostly the lack of a reference manager in Google
Docs that made it impractible to use for anything more complex than a
conference abstract. So - until recently - this was not a viable
alternative for research manuscripts either.

_So the perfect, 'Word-free' workflow does not exist?_

One would almost give up hope, but two recent new tools could turn out
to be game-changers:

1.  __RStudio and pandoc__ as of recently also support the _knitting_
of R-markdown documents straight to Word. This way you can keep your
co-authors happy by providing a Word document instead of PDF that they
can more easily edit. The only remaining hurdle with this workflow is
that collaborators' edits and comments still need to be entered into
the source document (unless the source document itself is
shared). Officially, we can't call this a _'Word-free'_ workflow, but at
least we don't have to actively write the document in Word, and we'll be
able to enjoy a frustration-free workday.

2.  the new reference manager __Paperpile__. On the surface, Paperpile
seems yet another reference manager, much like the already pretty
awesome Mendeley and Zotero. The latter two products were vast
improvements over the more 'corporate' (EndNote) or 'buggy' (Reference
Manager) tools that were in use when I was in grad school. However,
there is one extremely interesting aspect to
[Paperpile](https://paperpile.com/app), and that is that it is able to
cite articles from inside Google Docs. Therebey it basically removes Word
from the equation! Needless to say, collaboration features are
engrained into Google Docs, and even less tech-savvy collaborators
will likeley be able to open a Google Doc and edit, right? When it is time to
submit the paper to a journal, you'll still have to save to Word, but
this is probably as good as it gets at the moment.

These two developments are great news. Google Docs is probably a more
pleasing writing environment than RStudio, while the advantage of
RStudio is that manuscripts are created in a reproducible workflow. So
I'll still be using both tools, probably. The only thing left is for
someone to integrate RStudio Server into Google Docs in some way, and
we'll have the perfect collaborative cloud-based manuscript writing workflow...
