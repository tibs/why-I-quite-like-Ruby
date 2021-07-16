======================================
Why I like Python, and quite like Ruby
======================================

Written as a talk for CamPUG_

History
~~~~~~~

The talk was (will be) given at CamPUG_ on Tuesday 2nd August 2021.

The article
~~~~~~~~~~~

The material of the talk is also available as an article.

The source for the article are in `<why-i-quite-like-ruby.rst>`_

(Note that github will present the ``.rst`` files in rendered form as HTML,
albeit using their own styling (which makes notes a bit odd). If you want
to see the original reStructuredText source, you have to click on the "Raw"
link at the top of the file's page.)

For convenience, there will also be a PDF rendering of the article,
`<why-i-quite-like-ruby.pdf>`_

The slides
~~~~~~~~~~
The slides are written using reStructuredText_, and thus intended to be
readable as plain text.

The sources for the slides are in `<ruby-slides.rst>`_.

(Note that github will present the ``.rst`` files in rendered form as HTML,
albeit using their own styling (which makes notes a bit odd). If you want
to see the original reStructuredText source, you have to click on the "Raw"
link at the top of the file's page.)

The 16x9 aspect ratio slides are `<ruby-slides-16x9.pdf>`_ and are stored here
for convenience. The 4x3 slides aren't provided because I'd need to do more
work to make them well-formatted, which doesn't seem worth doing when I'm not
going to be presenting in a physical venue.

The PDF files may not always be as up-to-date as the source files, so check
their timestamps.

Making the PDF files
~~~~~~~~~~~~~~~~~~~~
For convenience, you can use the Makefile to create the PDF files.
For instance::

  $ make pdf

to make them all.

For what the Makefile can do, use::

  $ make help

I use poetry_ to manage the dependencies needed to build the PDFs, and
rst2pdf_ and its dependencies to do the actual work.

.. _poetry: https://python-poetry.org/
.. _rst2pdf: https://rst2pdf.org/

You will also need an appropriate ``make`` program if you want to use the
Makefile.

.. _CamPUG: https://www.meetup.com/CamPUG/
.. _pandoc: https://pandoc.org/
.. _docutils: http://docutils.sourceforge.net/
.. _reStructuredText: http://docutils.sourceforge.net/rst.html
.. _TeX: https://www.ctan.org/starter

--------

  |cc-attr-sharealike|

  This slideshow and its related files are released under a `Creative Commons
  Attribution-ShareAlike 4.0 International License`_.

.. |cc-attr-sharealike| image:: images/cc-attribution-sharealike-88x31.png
   :alt: CC-Attribution-ShareAlike image

.. _`Creative Commons Attribution-ShareAlike 4.0 International License`: http://creativecommons.org/licenses/by-sa/4.0/
