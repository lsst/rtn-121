.. image:: https://img.shields.io/badge/rtn--121-lsst.io-brightgreen.svg
   :target: https://rtn-121.lsst.io
.. image:: https://github.com/lsst/rtn-121/workflows/CI/badge.svg
   :target: https://github.com/lsst/rtn-121/actions/

######################################################################################
Rubin Observatory's Approach to Providing Sustainable Scientific User Support at Scale
######################################################################################

RTN-121
=======

An overview of the Rubin Observatory’s strategy to provide a sustainable community science model at scale, for thousands of users worldwide, including policies, guidelines, and workflows for documentation, tutorials, activities, user support, and issue resolution.

Links
=====

- Live drafts: https://rtn-121.lsst.io
- GitHub: https://github.com/lsst/rtn-121

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst/rtn-121

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the `acronyms.tex` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
