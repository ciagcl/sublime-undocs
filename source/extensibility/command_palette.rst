.. warning::

   Want even better documentation for Sublime Text?

   We are starting a new round of writing and editing to improve this guide in many ways. If you find it useful, please `support us <https://www.bountysource.com/teams/st-undocs/fundraiser>`_.

===============
Command Palette
===============

.. seealso::

   :doc:`Reference for Command Palette <../reference/command_palette>`
      Complete documentation on the command palette options.


Overview
========

The *command palette* bound to :kbd:`Ctrl+Shift+P` is an interactive list
whose purpose is to execute commands. The command palette is fed by entries in
``.sublime-commands`` files. Usually, commands that don't warrant creating a
key binding of their own are good candidates for inclusion in a ``.sublime- commands``
files.

By default, the command palette includes many useful commands, and provides
convenient access to individual settings as well as settings files.


File Format (Commands Files)
============================

Commands files use JSON and have the ``.sublime-commands`` extension.

Here's an excerpt from ``Packages/Default/Default.sublime-commands``::

   [
       { "caption": "Project: Save As", "command": "save_project_as" },
       { "caption": "Project: Close", "command": "close_project" },
       { "caption": "Project: Add Folder", "command": "prompt_add_folder" },

       { "caption": "Preferences: Default File Settings", "command": "open_file", "args": {"file": "${packages}/Default/Base File.sublime-settings"} },
       { "caption": "Preferences: User File Settings", "command": "open_file", "args": {"file": "${packages}/User/Base File.sublime-settings"} },
       { "caption": "Preferences: Default Global Settings", "command": "open_file", "args": {"file": "${packages}/Default/Global.sublime-settings"} },
       { "caption": "Preferences: User Global Settings", "command": "open_file", "args": {"file": "${packages}/User/Global.sublime-settings"} },
       { "caption": "Preferences: Browse Packages", "command": "open_dir", "args": {"dir": "$packages"} }
   ]

``caption``
   Text for display in the command palette.
``command``
   Command to be executed.
``args``
   Arguments to pass to ``command``.


How to Use the Command Palette
==============================

#. Press :kbd:`Ctrl+Shift+P`
#. Select command

The command palette filters entries by context. This means that whenever you open it, you
won't always see all the commands defined in every ``.sublime-commands`` file.

.. warning::

   Want even better documentation for Sublime Text?

   We are starting a new round of writing and editing to improve this guide in many ways. If you find it useful, please `support us <https://www.bountysource.com/teams/st-undocs/fundraiser>`_.
