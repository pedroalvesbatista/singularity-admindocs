# Apptainer Admin Docs

This project uses [reStructured Text (RST)](http://docutils.sourceforge.net/rst.html)
and [ReadTheDocs](https://readthedocs.org/). As a library for the current theme,
[Sphinx Python library](https://pypi.org/project/Sphinx/lt="PyPI") was used,
using Python v. 2.7.

## Setting up an environment to contribute

First things first, you will need to install the following tools:

- [Install Python 2.7](https://www.python.org/download/releases/2.7/)
- After that then you will need to install Sphinx:

```sh
pip install -U Sphinx
```

You're all set! after this you will only need to use your favorite editor for
RST files.

## How to do stuff in RST

First of all, it is good to have an idea of some files and their functionality
in the project:

### Structure of the project

This project maintains the following structure:

1. Index.rst : contains the sections and the initial table of contents tree,
every section is referenced by a tag next to it. (e.g. ``Quick Start <quick_start>``)
2. All other files, are named as the same reference tag described before, so in
the previous example, a correspondent ``quick_start.rst`` file exists.
3. The configuration at the moment of compilation is given by the ``conf.py``
file, some more description about this file can be found below.

### **The conf.py file**

This file contains the themes, extensions, variables and naming for files that
the compilation process produces. Here are some important elements:

- ``version`` : Describes the current version (This one is a short version of
    the release)
- ``release``: Describes the current release (Complete or full version
    description. For a matter of simplicity we maintain both at the same value)
- ``html_theme``: Describes the theme to be used in the ``ReadtheDocs`` document.
- ``html_theme_options``: Describes the options needed for configuration in the
    theme (This varies from theme to theme, so we enforce using the options for
    the ``Sphinx theme`` only.
- ``html_context``: Options related to which is the github repository and what
    name it has.
- ``html_logo``: The logo for the sidebar
- ``html_favicon``: The ``favicon`` for the entire project
- ``htmlhelp_basename``: Default name of the document generated in Latex, we
    leave all these as default values.

### **Cheatsheet to get started with reStructured (RST) Text**

Some hints on how to write stuff on RST are described in this section.

#### **1. Create a section/subsection/subsubsection title**

Sections are all described as plain text, but have specific
notations/underlining for titles and subtitles, very similar to Markup Language.

- To create a main section title: A main section title is described as a
surrounded text (above and below) of ``=`` characters. Like in the following
example:

```sh
================
New Main Section
================
```

- To create a sub-section: A sub section title is described as a surrounded text
(above and below) of ``-`` characters. Like in the following example:

```sh
---------------
New Sub section
---------------
```

- To create a sub-sub-section: A sub-sub section title is described as a text
underlined by ``=`` characters. Like in the following example:

```sh
New sub-sub section
===================
```

- Last but not least, could happen that you would need to insert a sub-sub-sub
section, in that case the title is described as a text underlined by ``-``
characters. Like in the following example:

```sh
New sub-sub-sub section
-----------------------
```

#### 2. Reference sections

You might need to reference sections, for that aim you will need to first create
the reference above the title you need to reference and second to reference it
where you need the link reference. Remember that this type of references is very
different than that of hyperlinks, because at the moment of compilation, the
latex document generated will have the reference to the page in which that title
was referenced. Very cool, huh? Let's see how it works...

##### Step 1: Create the reference

To create the reference on the section you need to link, you will need to
specify a tag, allowed characters contain also ``-`` characters but they need to
be unique name tags. So for example, in the build-docker-module section we can
have something like:  

```sh
.. _build-docker-module:

-------------------
build-docker-module
-------------------
```

Note that it might not be necessarily that the section is called just as the
same as the tag-name.

##### Step 2: Reference it

You can do so by following the next syntax:

The name after the ref tag could also be different, the important thing is that
the tag between the ``<`` and ``>`` is the one that belongs to the previous
given tag name. Like in the following example:

```sh
:ref:`quickstart <quick-start>`
```

You can find a lot of information about RST on
[this site](http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html)

## Generating HTML files from RST

This is pretty straightforward by going to the root of the project on the
command line and then do:

```sh
make html
```

This will generate a folder called **_build** within which you'll see a folder
called **html** that contains all the html files you need.

## Generating PDF files from RST

This is very similar to the previous step, you will need to execute on command
line:

```sh
make latexpdf
```

With this, a new folder **latex** will be generated inside **_build**,
that will contain all `pdf` files generated from `RST`
(by default it is called "ReadTheDocsTemplate.pdf").

(Additional latex files are also generated if needed.)

## Generating EPUB files from RST

Very similar to the previous command, you will just need to execute on a command
line:

```sh
make epub
```

This will generate an **epub** folder inside **_build**. Inside **epub**,
you will find files with an `epub` extension.
