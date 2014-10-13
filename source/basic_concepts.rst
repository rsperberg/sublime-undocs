==============
Basic Concepts
==============


Overview
========

To fully understand the rest of this guide,
you need to be familiar
with the concepts presented in this section.


General Conventions
===================

.. TODO: add note about emphasis in style guide

This guide is written from the perspective of a **Windows** user.
Most instructions will only require trivial changes
to work on other platforms.

.. TODO: add e. g. and i. e. notes to style guide

Unless otherwise noted,
Relative paths (for example, :file:`Packages/User`)
start at `the Data Directory`_.

.. TODO: add note about you're vs your are to style guide?

We assume default key bindings
when indicating keyboard shortcuts.
If you are using a non-English keyboard layout,
some key bindings may not match your layout.
This is due to the way Sublime Text
processes key strokes internally.


Mastering Sublime Text Takes Time
=================================

This guide will teach you
how to use and configure Sublime Text.

.. TODO: add note to style guide about em dashes

Sublime Text is a versatile editor for programmers,
buy you don't need to be one
in order to use it,
or to configure it extensively—
it's an efficient tool out of the box.
Hackers, however, will appreciate
all the customization and extensibility opportunities.

Mastering Sublime Text requires time and practice.
Luckily, it's built around
a handful of concepts
that make for a consistent
and easily understandable system
once all the pieces come together.

In the following paragraphs,
we'll outline key aspects
that you'll quickly get familiar with
after you've spent some time using the editor.


The *Data* Folder
==================

Nearly all of the interesting files for users
live under the *data directory*.
The data directory is
a platform-dependent location:

* **Windows**: *%APPDATA%\\Sublime Text 3*
* **OS X**: *~/Library/Application Support/Sublime Text 3*
* **Linux**: *~/.config/sublime-text-3*

For **portable installations** (Windows only),
look for *{Sublime Text 3}/Data*.
Here, *{Sublime Text 3}*
refers to the directory
to which you've extracted
the compressed portable files.

Note that a directory named *Data*
only exists as such in portable installations.
For the remaining installation types,
it is one of the locations
indicated above.


The *Packages* Folder
=====================

This is a **key directory**:
all resources for supported programming
and markup languages
are stored here.
(More on *packages* and *resources* later.)

.. TODO: link term above to glossary?

You can access the packages directory
from the main menu (**Preferences | Browse Packages...**),
by means of an API call: ``sublime.packages_path()``,
or by other means
that will be explained in later topics.

In this guide, we refer to the packages folder
as *Packages*, *packages path*, *packages folder* or *packages directory*.


The ``User`` Package
********************

:file:`Packages/User` is a catch-all directory
for custom plugins, snippets, macros, etc.
Consider it your personal area
in the packages folder.
Sublime Text will never
overwrite the contents of :file:`Packages/User`
during upgrades.


The Python Console and the Python API
=====================================

This information is useful for programmers.
For other users,
you just need to know
that Sublime Text
enables users with programming skills
to add their own features to the editor.

Sublime Text comes with an embedded Python interpreter.
It's useful
to inspect the editor's settings
and to quickly test API calls
while developing plugins.

To open the Python console,
press :kbd:`Ctrl+\``
or select **View | Show Console**
from the main menu.


Your System's Python vs the Sublime Text 3 Embedded Python
**********************************************************

Sublime Text 3 comes with its own Python interpreter
and it's separate
from your system's Python interpreter
(if available).

The embedded interpreter is only intended
to interact with the plugin API,
not for general development.


Packages, Plugins, Resources and Other Terms
============================================

Almost every aspect of Sublime Text
can be extended or customized.
Among other things,
you can modify the editor's behavior,
add macros and snippets, extend menus...
You can even create whole new features
using the editor's API to build complex
plugins.
This vast flexibility is the reason
why you will learn
about so many configuration files:
there simply must be a place
to specify all possible preferences.

Configuration files in Sublime Text
are simply text files
that follow a predefined structure or *format*:
JSON predominates,
but you'll find XML files too.
Finally, for the more advanced
extensibility options,
Python files are used.

For brevity, in this guide
we sometimes refer to all these
disparate configuration files collectively as *resources*.

Sublime Text will look for resources
inside the packages folder.
We'll talk at length about *packages* later,
but the short version is that,
to keep things tidy,
Sublime Text has a notion of a *package*,
that is, a folder (or zip archive)
that contains resources
that belong together
(maybe they help
compose emails faster,
write HTML efficiently,
enhance the coding experience for C, Ruby, Go...).


Textmate Compatibility
======================

This information is useful
for Textmate users
who are now using Sublime Text.

Textmate is an editor for the Mac.

Sublime Text compatibility with Textmate bundles
is good excluding commands,
which are incompatible.
Additionally, Sublime Text requires
all syntax definitions to have the *.tmLanguage* extension,
and all preferences files
to have the *.tmPreferences* extension.
This means that *.plist* files
will be ignored,
even if they are located
under a *Syntaxes* or *Preferences* subdirectory.


Vi/Vim Emulation
================

This information is useful for Vim users
who are now using Sublime Text.

Vi is an ancient modal editor
that lets the user perform all operations
from the keyboard.
Vim, a modern version of vi,
is still in widespread use.

Sublime Text provides vi emulation
through the *Vintage* package.
The Vintage package is *ignored* by default.
Learn more about Vintage_
in the official documentation.

An evolution of Vintage, called Vintageous_,
offers a better vi/vim editing experience
and is updated more often than Vintage.
Vintageous_ is an open source project.

.. _Vintage: http://www.sublimetext.com/docs/3/vintage.html
.. _Vintageous: http://guillermooo.bitbucket.org/Vintageous


Emacs
=====

This information is useful
for emacs users who are
now using Sublime Text.

Sublime Text does not offer
any built-in emacs emulation,
but you can try third-party packages
created by other Sublime Text users.
