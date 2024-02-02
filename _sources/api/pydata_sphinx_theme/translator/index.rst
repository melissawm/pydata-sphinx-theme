:py:mod:`pydata_sphinx_theme.translator`
========================================

.. py:module:: pydata_sphinx_theme.translator

.. autoapi-nested-parse::

   A custom Sphinx HTML Translator for Bootstrap layout.

   ..
       !! processed by numpydoc !!


Module Contents
---------------

Classes
~~~~~~~

.. autoapisummary::

   pydata_sphinx_theme.translator.BootstrapHTML5TranslatorMixin



Functions
~~~~~~~~~

.. autoapisummary::

   pydata_sphinx_theme.translator.setup_translators



Attributes
~~~~~~~~~~

.. autoapisummary::

   pydata_sphinx_theme.translator.logger


.. py:class:: BootstrapHTML5TranslatorMixin(*args, **kwds)


   
   Mixin HTML Translator for a Bootstrap-ified Sphinx layout.

   Only a couple of functions have been overridden to produce valid HTML to be
   directly styled with Bootstrap, and fulfill acessibility best practices.















   ..
       !! processed by numpydoc !!
   .. py:method:: starttag(*args, **kwargs)

      
      Ensure an aria-level is set for any heading role.
















      ..
          !! processed by numpydoc !!

   .. py:method:: visit_table(node)

      
      Custom visit table method.

      Copy of sphinx source to *not* add 'docutils' and 'align-default' classes but add 'table' class.















      ..
          !! processed by numpydoc !!


.. py:function:: setup_translators(app)

   
   Add bootstrap HTML functionality if we are using an HTML translator.

   This re-uses the pre-existing Sphinx translator and adds extra functionality defined
   in ``BootstrapHTML5TranslatorMixin``. This way we can retain the original translator's
   behavior and configuration, and _only_ add the extra bootstrap rules.
   If we don't detect an HTML-based translator, then we do nothing.















   ..
       !! processed by numpydoc !!

.. py:data:: logger

   

