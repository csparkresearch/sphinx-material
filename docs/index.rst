===================
Material for Sphinx
===================

.. image:: images/screenshot.png
    :alt: Material for Sphinx Screenshots

This theme provides a responsive Material Design theme for Sphinx
documentation. It derives heavily from
`Material for MkDocs <https://squidfunk.github.io/mkdocs-material/>`_,
and also uses code from
`Guzzle Sphinx Theme <https://github.com/guzzle/guzzle_sphinx_theme>`_.


Roadmap
-------
`Material for Sphinx <https://github.com/bashtage/sphinx-material>`_ is a work in progress.  While
I believe that it is ready for use, there are a number of important limitation.  The most
important it to improve the CSS generation to use
`SASS <https://en.wikipedia.org/wiki/Sass_(stylesheet_language)>`_. It uses some python to
modify Sphinx output, which is not ideal.

The other issues are:

* improving the documentation;
* providing examples;
* sidebar customization;
* improving the search box; and
* ensuring that all Sphinx blocks work as intended.

You can see how it works on the
`statsmodels development branch documentation <https://statsmodels/org/devel>`_.

.. toctree::
    :caption: Contents Caption

    customization
    specimen
    additional_samples
    pymethod
    numpydoc
    notebook.ipynb
    markdown.md
    rst-cheatsheet/rst-cheatsheet
    change-log
    license

Getting Started
---------------
Install from git

.. code-block:: bash

   pip install git+https://github.com/bashtage/sphinx-material.git

Update your ``conf.py`` with the required changes:

.. code-block:: python

    import sphinx_material

     # Register the theme as an extension to generate a sitemap.xml
    extensions.append('sphinx_material')

    # Choose the material theme
    html_theme = 'sphinx_material'
    # Get the them path
    html_theme_path = sphinx_material.html_theme_path()
    # Register the required helpers for the html context
    html_context = sphinx_material.get_html_context()


There are a lot more ways to customize this theme. See :ref:`Customization`
or ``theme.conf`` for more details.

.. code-block:: python

    import sphinx_material

    # # Required theme setup
    extensions.append('sphinx_material')
    html_theme = 'sphinx_material'
    html_theme_path = sphinx_material.html_theme_path()
    html_context = sphinx_material.get_html_context()

    # Material theme options (see theme.conf for more information)
    html_theme_options = {

        # Set the name of the project to appear in the navigation.
        'nav_name': 'Project Name',

        # Set you GA account ID to enable tracking
        'google_analytics_account': 'UA-XXXXX',

        # Specify a base_url used to generate sitemap.xml. If not
        # specified, then no sitemap will be built.
        'base_url': 'https://project.github.io/project',

        # Set the color and the accent color
        'color_primary': 'blue',
        'color_accent': 'light-blue'

        # Set the repo location to get a badge with stats
        'repo_url': 'https://github.com/project/project/',
        'repo_name': 'Project',

        # Visible levels of the global TOC; -1 means unlimited
        'globaltoc_depth': 3,
        # If False, expand all TOC entries
        'globaltoc_collapse': False,
        # If True, show hidden TOC entries
        'globaltoc_includehidden': False,
    }


Index
~~~~~
:ref:`genindex`
