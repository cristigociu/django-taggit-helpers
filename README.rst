*********************
django-taggit-helpers
*********************

``django-taggit-helpers`` makes it easier to work with admin pages of models associated with ``django-taggit`` tags.

.. contents:: :local:

Installation
============

**PyPI**

.. code-block:: sh

    pip install django-taggit-helpers

**GitHub**

.. code-block:: sh

    pip install https://github.com/mfcovington/django-taggit-helpers/releases/download/0.0.0/django-taggit-helpers-0.0.0.tar.gz

Helper Clases
=============

``TaggitCounter``
-----------------

Display (and sort by) number of Taggit tags associated with tagged items.

.. code-block:: python

    from taggit_helpers import TaggitCounter

    class MyModelAdmin(TaggitCounter, admin.ModelAdmin):    # TaggitCounter before ModelAdmin
        list_display = (
            ...
            'taggit_count',
        )

``TaggitListFilter``
--------------------

Filter records by Taggit tags for the current model only.
Tags are sorted alphabetically by name.

.. code-block:: python

    from taggit_helpers import TaggitListFilter

    class MyModelAdmin(admin.ModelAdmin):
        list_filter = [TaggitListFilter]

``TaggitStackedInline``
-----------------------

Add stacked inline for Taggit tags to admin.
Tags are sorted alphabetically by name.

.. code-block:: python

    from taggit_helpers import TaggitStackedInline

    class MyModelAdmin(admin.ModelAdmin):
        inlines = [TaggitStackedInline]

``TaggitTabularInline``
-----------------------

Add tabular inline for Taggit tags to admin.
Tags are sorted alphabetically by name.

.. code-block:: python

    from taggit_helpers import TaggitTabularInline

    class MyModelAdmin(admin.ModelAdmin):
        inlines = [TaggitTabularInline]

*Version 0.0.0*