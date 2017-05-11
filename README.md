# ETS_py3
sets up of the ETS packages from this repo for wxPython Phoenix and Python 3.

To use this, first: 
- Create a local directory with any name (say my_ets)
- download ets.py and save to this directory
- then from a terminal cd to my_ets

then type: 

python3 ets.py -h | --help | clone [--ssh] | COMMAND [args] | ALIAS [args]
   -h, --help  Print this message.

   clone       Clone the entire Enthought Tool Suite into the current working
               directory, each actively maintained package placed in its own
               sub-directory.
               By default, the https github access URLs are used.
               The --ssh option changes this to SSH.

   COMMAND     Run this shell command, with any following arguments, inside
               each package's sub-directory. If any command arguments must be
               quoted, you may need to use nested quotes, depending on the
               quote handling in your shell. For example:
                  ets git commit -a -m "'commit comment for all packages'"

   ALIAS       Each alias is shorthand for a shell command with arguments.
               The available aliases are pre-defined by this script, not by
               the user. Any alias may be followed by optional additional
               arguments.


   The available aliases and their equivalent commands are:%s

   Examples:
      Fresh install all packages from master:
         mkdir ETS
         cd ETS
         ets clone
         ets develop

      Update all packages from master:
         ets pull

   The ETS packages referenced, in order of processing, are:\n%s"""

      pull     git pull
      status   git status
      branch   git branch
      checkout git checkout
      diff     git diff
      revert   git revert
      fetch    git fetch
      setup    python setup.py
      build    python setup.py build
      install  python setup.py install
      develop  python setup.py develop"""

======================================================================
ETS installation dependencies (documentation only).
Derived from ets_depends.log, holding the output of ets_depends.py.
Dependent packages are listed below and to the right of their dependencies.
======================================================================
casuarius
encore
traits
    codetools
    scimath
    pyface
        traitsui
            enable
                chaco
                graphcanvas
            apptools
                mayavi
                envisage
