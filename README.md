# ETS_py3
sets up of the ETS packages from this repo for wxPython Phoenix and Python 3.

To use this, first:
- install python3 and dependencies, including wxPython Phoenix >=3 and pyVTK>=7.0
     Recommended:
     
         install python3 using Anaconda, 
         start an anaconda terminal for this Python 3 installation, then type the following
         conda install -c clinicalgraphics vtk=7.1.0
         conda install -c newville wxpython-phoenix=3.0.3
         pip install fonttools
         conda install swig 
         
         (for OSX, most likely, the following:
         export TTFPATH=/Library/Fonts )
            
        
     
- Create a local directory with any name (say my_ets)
- download ets.py and save to this directory
- open a terminal, cd to my_ets

then type, from Anaconda Python 3 terminal for fresh install: 
  
      Fresh install all packages from master:
         python ets.py clone
         python ets.py develop OR python ets.py build OR python ets.py install
         

      Update all packages from master:
         python ets.py pull
         python ets.py develop OR python ets.py build OR python ets.py install

The general usage has the template:

python ets.py -h | --help | clone [--ssh] | COMMAND [args] | ALIAS [args]
   -h, --help  Print this message.

       clone       
       Clone the entire Enthought Tool Suite into the current working
       directory, each actively maintained package placed in its own
       sub-directory.
       By default, the https github access URLs are used.
       The --ssh option changes this to SSH.

       COMMAND     
       Run this shell command, with any following arguments, inside
       each package's sub-directory. If any command arguments must be
       quoted, you may need to use nested quotes, depending on the
       quote handling in your shell. For example:
       ets git commit -a -m "'commit comment for all packages'"

       ALIAS       
       Each alias is shorthand for a shell command with arguments.
       The available aliases are pre-defined by this script, not by
       the user. Any alias may be followed by optional additional
       arguments.

   The ETS packages referenced, in order of processing, are:

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

ETS_py3 installation dependencies (documentation only).
======================================================================

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
