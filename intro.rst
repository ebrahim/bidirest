.. include:: bidi.rst

بسم الله الرحمن الرحیم

==============================================
  Writing bidi documents in reStructuredText
==============================================

----------------
  Introduction
----------------

Study source of this document carefully to see how to use helpers.

Accompanying styles are suited for right-to-left documents containing some
left-to-right parts. If you're going the other way, you must be able to
easily create your own styles based on these ones.

For generating ODT output, you may want to have LTR alternative of more
than just ``textbody`` style. In that case you should edit custom styles of
``rtl.odt`` (or just start off Docutils' ``styles.odt``) using LibreOffice
or OpenOffice and add your own styles.

.. important:: Remember to prepend ``rststyle-`` to your style names.

For checking RTL capabilities you can generate HTML output by running::

  rst2html --stylesheet=rtl.css intro.rst intro.html

And generate ODT output by running::

  rst2odt --stylesheet=rtl.odt intro.rst intro.odt

.. note:: If you only need the HTML output, you may use a simpler ``class``
          directive with a paragraph instead of ``container`` and a block.
 
          Example::
 
            .. class:: ltr
 
            Some LTR paragraph.

.. note:: I haven't been able to get ODT to support embedding directions
          using roles yet.

.. note:: I preferred to avoid LRM and RLM Unicode characters for simplicity.
            
------------------------------------
  Embedding directions using roles
------------------------------------

ابراهیم :lre:`C++` را با :lre:`/usr/bin/g++` دوست دارد!

-------------------------------------------------
  Embedding directions using Unicode characters
-------------------------------------------------

ابراهیم |lre| C++ |pdf| را دوست دارد!
پس برویم |lre| /etc/passwd |pdf| را با هم بخوانیم.

------------------------------------------------------------------------
  Manually setting direction of paragraph using classes of container
------------------------------------------------------------------------

.. container:: textbody-ltr ltr

 The same technique works for |rle| **چب-به-راست!** |pdf| languages!

والسلام
