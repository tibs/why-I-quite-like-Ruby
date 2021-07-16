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

Note that some of the material here is borrowed from
my own `An amble through some of Python's history`_, which talks about the
history of Python (and its features) from the early days until Python 3.6.

Finding Python
--------------

I don't remember exactly when I first found Python, but my first dated Python
script is from 1994, and that would fit, as it is when Python 1.0 and 1.1 were
released.

My background had been with BCPL, Fortran and C (and also Emacs Lisp and
TeX/LaTeX).

Work had tasked me with looking for a programming language we could embed into
our object oriented database. At that time, the obvious choices were things
like Tcl and various small lisps or schemes. But I also found Python, and fell
in love with it, in large part because it was what I already wrote down when
writing pseudo-code (with the exception of the colons - more on them later
too). It also had much of the feel I had liked from using VMS DCL (Digital
Command Language - a relatively sophisticated Basic descendant, with close
integration with the operating system).

As it happened, we didn't choose any of my found languages (we ended up with a
simplified Pascal clone from Byte magazine), and I think at the time we would
have thought Python was too much work to embed.

(For reference, Java 1.0 is 1995, as is Ruby 0.95)

Significant indentation, and the aim to be readable
---------------------------------------------------

"Runnable pseudocode**

Multi-paradigm
--------------

The language is object oriented. But the programs do not need to be.

(Discuss)

High level datastructures built in
----------------------------------

*So boring* to have to rewrite these again and again in C or whatever.

(although proper sets not until 2.3 in 2003)

Dictionaries all the way down
-----------------------------


Introspection and self-modification
-----------------------------------

"Exposing its innards"

*Can* modify things doesn't mean *will* modify things

"Safe and sane"
---------------

Python programmers do not have a reputation for being wild and wacky in their
code - I think this is a good thing!

Batteries included
------------------

Really - compare with the other languages I was used to.

The community and a gentle sense of humour
------------------------------------------

Not, by any means, unique to Python.

The ``ni`` module (new import) in Python 1.3

Docstrings - these came later
-----------------------------

Python 1.2, 1995, having been "play tested" before that.

The Zen of Python
-----------------

A joke by Tim Peters from 1999

  |  Beautiful is better than ugly.
  |  Explicit is better than implicit.
  |  Simple is better than complex.
  |  Complex is better than complicated.
  |  Flat is better than nested.
  |  Sparse is better than dense.
  |  Readability counts.
  |  Special cases aren't special enough to break the rules.
  |  Although practicality beats purity.
  |  Errors should never pass silently.
  |  Unless explicitly silenced.
  |  In the face of ambiguity, refuse the temptation to guess.
  |  There should be one-- and preferably only one --obvious way to do it.
  |  Although that way may not be obvious at first unless you're Dutch.
  |  Now is better than never.
  |  Although never is often better than *right* now.
  |  If the implementation is hard to explain, it's a bad idea.
  |  If the implementation is easy to explain, it may be a good idea.
  |  Namespaces are one honking great idea -- let's do more of those!



Why I like Ruby
===============

Why did I learn Ruby?
---------------------

It's not an obvious language to learn if you already know Python.

Team moved in July 2019 from Python/Django to Ruby/Rails.

Caveat: I use Rails
-------------------

I've learnt Ruby in the Rails context, so my views on the language itslf may
be as skewed as the views of a Python programmer who learnt the language to
use Django. In particular, Rails likes "magic" even more than Django does.

Also, remember I've only been using Ruby for a short while, and have not seen
its history "in action", whereas for Python I remember the evolution of the
language and its <surroundings> (??FIND A BETTER WORD??)

Ruby's inspirations
-------------------

Smalltalk, Lisp, Perl, etc.

*Not* Python - Matz knew Python well so knew what he didn't like.


Why do I say I only "quite" like Ruby?
--------------------------------------

Because I don't really like some of the stylistic choices - it errs a little
too much on the magic side for me (this is *very* much a matter of choice!).

Note: this is meant to be a talk about the things I like in both languages, so
don't expect me to look for things that I'm not keen on or think could be done
better. There is no perfect programming language, and moreover different
programming languages suit different programmers.

Matz
----

Yukihiro Matsumoto

https://en.wikipedia.org/wiki/Yukihiro_Matsumoto

The inventor of Ruby.

"Matz is nice so we are nice"

Readability / writability
-------------------------

Python strongly errs toward being readable, even if that makes it slightly
harder to write.

Ruby wants to make programming a joy for programmers, so it wants code that is
easy/fun to write, as well as easy to read.

Begin and end and things
------------------------

Ruby doesn't have significant indentation, but it does have decent sane block
delineation (unlike, for instance, C-derived languages).

In particular, the *end* of a block is always indicated by ``end``:

.. code:: Ruby

   begin
     ...
   end

.. code:: Ruby

   if choice
     ...
   elsif
     ...
   end

and so on.

(and yes, ``elsif`` takes a bit of getting used to for a Python programmer)

Line continuation
-----------------

.. code:: Ruby

   difference = minimum -
                maximum

I don't think I need to say any more...

Definitely Object Oriented
--------------------------

Although does a lot to make this less painful:

* "bare" methods (is that even a term)
* value access - see below

Object values
-------------

Ruby uses setter and getter methods for (almost) all value access, but it
makes it so easy to create those that you don't really think about it.

...compare Python "start as a variable and make a method when needed" to
Ruby's ``attr_reader`` / ``attr_writer`` / etc.

``def xxx=`` for setting - I like that

No ``self``
-----------

Like many mainstream OO languages, it is not necessary to say ``this`` in
almost all cases.

Use of ``@`` to indicate equivalent of ``self.`` for values *inside* methods
of the same class. But seems to be only when necessary, otherwise just use the
accessor methods.

Method naming conventions from lisp
-----------------------------------

Although it's not 100% followed, use of ``method?`` and ``method!`` to mean
"is it a" and "do it regardless" are clearly borrowed from the lisp world, and
are rather nice.

Symbols
-------

What is a symbol?

More-or-less, a constant whose value is itself.

.. Ruby::

  :symbol

Ruby uses this a lot, and is good at converting symbols to their string
representation when necessary (``:symbol`` becomes ``symbol``)

CHECK THIS SECTION carefully

Why doesn't Python have symbols, if they're so usful?

My suspicion is that they're a little bit hard to understand when you first
come across them, and so that didn't fit the idea of simplicity that
(especially early) Python was striving for.

They're very much a part of lisps, though, so it was probably inevitable that
Ruby would gain such a useful thing.

Messages from smalltalk
-----------------------

In Ruby, the documentation would have it that:

.. code:: Ruby

   obj.thing

sends the ``thing`` message to the object ``obj``, which will respond
appropriately if it knows that message (in the normal OO manner).

Ruby is quite serious about this description, and to cope with unrecognised
messages on can do things like:

<Give a good example - perhaps something from the Ruby koans?>

Ruby and monkey patching
------------------------

It certainly used to be that Ruby had a reputation in the Python world as
glorying in (what Python people saw as) the over use of monkey patching -
reaching back into a class definition and changing it at run time.

And there's *some* justice to this, except that "monkey patching" in Ruby
isn't the same thing as in Python, because both the philosophy and the
technology are different.

For a start, since Ruby thinks about sending messages to objects, it seems
quite reasonable to intercept a message, either one that would normally not
correspond to a method, or one that would be specified by the class or one of
its super classes (or interfaces - I haven't mentioned interfaces before, but
they're another thing that Ruby has - DO I NEED TO CHECK WHAT I MEAN HERE /
EXPLAIN A BIT MORE?).

But secondly, the *mechanism* for monkey patching is not the same (DOUBLE
CHECK THIS - I'M WRITING FROM MEMORY). In Ruby changing the behaviour of an
object at run-time also inserts a "shim" layer around that object - the monkey
patching is kept much more hygenic (and introspectable?) than in Python.

In some respects, Python can only monkey patch by doing very low level
manipulations, wherea Ruby has proper support for it.

That doesn't mean one should go wild with this - it can still be a practical
problem - but Ruby has definitely thought more about what should be possible
to do cleanly here.

Meanwhile, `The Ruby Styleguide` says:

    **No Needless Metaprogramming**

    Avoid needless metaprogramming.

    **No Monkey Patching**

    Do not mess around in core classes when writing libraries (do not monkey-patch them).

Blocks
------

I think everyone is required to mention blocks when talking about Ruby.

Not really possible to have a nice syntax for this in Python, because of
significant indentation. But that's OK, we don't have to have everything!

Things to mention:

* the way ``yield`` is (sort of) lexically replaced by the block
* block arguments, and how (for instance) iterating over a hash (dictionary)
  with a block with one argument will give you each key, while with two it
  will give you key and value.
* the fact this engenders a different way of programming, which takes some
  getting used to - so programming Ruby like a Python programmer will *not*
  take advantage of this


Who needs a ``for`` loop?
-------------------------

``2.times`` and ``1..3.each``.

Closed and open intervals:

* ``1..3`` == 1, 2
* ``1...3`` == 1, 2, 3

(or is it the other way round?)

Lisp-1 or Lisp-2
----------------

At the start of https://bugs.ruby-lang.org/issues/15799#note-29 Matz says:

    Unlike JavaScript and Python (Lisp-1 like languages), Ruby is a Lisp-2
    like language, in which methods and variable have separated namespaces. In
    Lisp-1 like languages, ``f1 = function; f1()`` calls function (single
    namespace).

So in Python we expect to be able to do:

.. code:: Python

   fn = len
   fn([1, 2, 3])

or even pass ``fn`` as an argument to a callable, without needing to do
anything special. On the other hand:

.. code:: Python

   a = 3
   def a(): print('A')

does not give us two different things called ``a``

In Ruby, those are not the case, and doing the equivalent things takes a
little more work. Although it has to be said that this has just about never
arisen in my Ruby career so far - perhaps because a programming style that
uses blocks leads to a different sort of code.

THINK ABOUT THIS

DSLs
----

You'll sometimes

In Python:

.. code:: Python

   callable

just "sits there" (well, except in the REPL, where it will report what it is)

You need to use the ``()`` (call) operators (!) to make something happen:

.. code:: Python

   callable()

and to call with arguments you need to put those arguments inside the ``()``:

.. code:: Python

   callable(1, 2, 3)


In Ruby:

.. code:: Ruby

   callable

will call the method of that name (if there is one). Of course, because Ruby
allows a value and a method to have the same name, it does have to do a little
guesswork in some contexts to decide which is needed.

Omitting ``()``
---------------

On the other hand, because (IS THIS A BECAUSE?) Ruby knows that a method is
not a value, it is free to treat it differently. And that means, in partcular,
that the ``()`` in a method call are optional.

(There are stylistic guidelines, of course - specifically, see `The Ruby
Styleguide`_ sectin `DSL Method Calls`_)

So instead of:

.. code:: Ruby

   method(1, 2, 3)

it's quite possible (and often colloquial) to do:

.. code:: Ruby

   method 1 2 3

It is worth saying that this can often be *much more readable.*

Sort of DSLs
------------

A DSL is a Domain Specific Language.

Examples are things like:

* Cucumber
* ... give more examples ...

Ruby is often said to be good for "creating" domain specific languages, but
what I think that actually means is that, given blocks and the ability to
elide ``()`` when calling methods, one can end up with something that already
looks like a DSL.




DSL example 1: bundle/gem files
-------------------------------

Very nice configuration files that read naturally, but are actually Ruby code.

(so perhaps people *could* overuse this if they wanted? not sure)

DSL example 2: rspec
--------------------

``rspec`` gets close to a Cucumber language in pure Ruby, and also provides
Hamcrest abilities as well.



Remember to mention the ability to do:

.. code:: Ruby

   one
     .two
     .three

which also makes things more readable.


The community
-------------

As I said earlier, not unique to Python.

I've only attended one Ruby conference so far, Euruko 2021, which
unfortunately had to be virtual. But all the evidence I've seen leads me to
think that the Ruby community is just as friendly and helpful (although
possibly slightly smaller outside Japan) as the Python community.

(and, for what it's worth, I also found that Write the Docs conferences are
lovely - nothing to do with Python or Ruby!)

Python, Ruby and "unexpected consequences"
==========================================

Because Python has significant indentation, it can't really (easily) have
blocks.

(note to self: what was that language I though might be Python-inspired and
have blocks?)

Because Ruby is a Lisp-2, it has to do some guesswork, sometimes, to decide
whether to use a value or a method.

Because Ruby allows leaving off ``()`` when calling methods, which it can
safely do because it is a Lisp-2, it also allows the creation of (apparent)
DSLs, like ``rspec`` and the bundle/gem file format

So where next?
==============

My heart is with Python, and I'm currently paid to write in Ruby,

=======
Addenda
=======

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

* My own `An amble through some of Python's history`_ from which some of the
  text in `Why I like Python`_ is adapted.

.. _`About Ruby`: https://www.ruby-lang.org/en/about/
.. _`Why did Ruby creator chose to use the concept of Symbols?`:
   https://softwareengineering.stackexchange.com/questions/328029/
   why-did-ruby-creator-chose-to-use-the-concept-of-symbols
.. _`Ruby's lisp features`_
   http://blade.nagaokaut.ac.jp/cgi-bin/scat.rb/ruby/ruby-talk/179642
.. _`23 years of Ruby`: https://changelog.com/podcast/202
.. _My own `An amble through some of Python's history`: https://github.com/tibs/python-history

.. _`The Ruby Style Guide`: https://rubystyle.guide/
.. _`DSL Method Calls`: https://rubystyle.guide/#no-dsl-decorating
