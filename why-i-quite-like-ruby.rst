======================================
Why I like Python, and quite like Ruby
======================================

:author: Tibs
:email: tibs@tonyibbs.co.uk
:abstract:

    A short explanation of particular reasons I like Python, followed by
    a discussion of some of the things that also make me like Ruby, with
    comparison between the two languages.

Why I like Python
=================




Why I like Ruby
===============




Why only "quite" like?
----------------------




Yukihiro Matsumoto = Matz

Lisp-1 versus Lisp-2
====================

.. |lisp1| replace:: Lisp\ :sub:`1`
.. |lisp1| replace:: Lisp\ :sub:`2`

* In the threads at https://bugs.ruby-lang.org/issues/15799, an specifically
  at https://bugs.ruby-lang.org/issues/15799#note-29, Matz
  (Yukihiro Matsumoto) says:

    Unlike JavaScript and Python (Lisp-1 like languages), Ruby is a Lisp-2
    like language, in which methods and variable have separated namespaces. In
    Lisp-1 like languages, ``f1 = function; f1()`` calls function (single
    namespace).

* `Lisp-1 vs Lisp-2`_ - a nice simple overview by hornbeck, 2009
* `Technical Issues of Separation in Function Cells and Value Cells`_ by
  Richard P. Gabriel and Kent M. Pitman, 2001, actually introduces the
  concepts, giving history and implications (this article is also available on
  `Kent Pitman's site`_).

  This article uses subscripts for the numbers, |lisp1| and |lisp2|, which I
  think is clearer as it doesn't look like language version numbers. As the
  articles says:

    * |lisp1| has a single namespace that serves a dual role as the function
      namespace and value namespace; that is, its function namespace and value
      namespace are not distinct. In |lisp1|, the functional position of a
      form and the argument positions of forms are evaluated according to the
      same rules. Scheme and ... are |lisp1| dialects.

    * |lisp2| has distinct function and value namespaces. In |lisp2|, the
      rules for evaluation in the functional position of a form are distinct
      from those for evaluation in the argument positions of the form. Common
      Lisp is a |lisp2| dialect.

* Xah Lee has a nice piece from 2008 explaining `why not to use the terms
  Lisp-1 and Lisp-2`_ (the page starts with an overview of the terms),
  suggesting that:

  * “lisp-2” should be called multi-value-name languages.
  * “lisp-1” should be called single-value-name languages.

* Xah Lee also has an article `Ruby Creator Matz: How Emacs changed my
  life`_ - it's an annotated transcript of the slides from a talk by Matz.

.. _`Lisp-1 vs Lisp-2`:
   https://hornbeck.wordpress.com/2009/07/05/lisp-1-vs-lisp-2/
.. _`Technical Issues of Separation in Function Cells and Value Cells`:
   https://dreamsongs.com/Separation.html
.. _`Kent Pitman's site`:
   http://www.nhplace.com/kent/Papers/Technical-Issues.html
.. _`why not to use the terms lisp-1 and lisp-2`:
   http://ergoemacs.org/emacs/lisp1_vs_lisp2.html
.. _`Ruby Creator Matz: How Emacs changed my life`:
   http://ergoemacs.org/emacs/Matz_Ruby_how_emacs_changed_my_life.html


Possibly useful links
=====================

* `About Ruby`_ at https://www.ruby-lang.org/
* `Why did Ruby creator chose to use the concept of Symbols?`_
* `Ruby's lisp features`_ - Matz explaining why Ruby has lisp features (2006):

      Ruby is a language designed in the following steps:

      * take a simple lisp language (like one prior to CL).
      * remove macros, s-expression.
      * add simple object system (much simpler than CLOS).
      * add blocks, inspired by higher order functions.
      * add methods found in Smalltalk.
      * add functionality found in Perl (in OO way).

      So, Ruby was a Lisp originally, in theory.

      Let's call it MatzLisp from now on. ;-)

* `23 years of Ruby`_ (podcast interview with Matz from 2016, with a transcript)

* https://en.wikipedia.org/wiki/Ruby_(programming_language) quotes Matz from 1999:

  I was talking with my colleague about the possibility of an object-oriented
  scripting language. I knew Perl (Perl4, not Perl5), but I didn't like it
  really, because it had the smell of a toy language (it still has). The
  object-oriented language seemed very promising. I knew Python then. But I
  didn't like it, because I didn't think it was a true object-oriented
  language – OO features appeared to be add-on to the language. As a language
  maniac and OO fan for 15 years, I really wanted a genuine object-oriented,
  easy-to-use scripting language. I looked for but couldn't find one. So I
  decided to make it.

.. _`About Ruby`: https://www.ruby-lang.org/en/about/
.. _`Why did Ruby creator chose to use the concept of Symbols?`:
   https://softwareengineering.stackexchange.com/questions/328029/
   why-did-ruby-creator-chose-to-use-the-concept-of-symbols
.. _`Ruby's lisp features`_
   http://blade.nagaokaut.ac.jp/cgi-bin/scat.rb/ruby/ruby-talk/179642
.. _`23 years of Ruby`: https://changelog.com/podcast/202
