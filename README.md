# ETS_py3
sets up of the ETS packages from this repo for wxPython Phoenix, Python 3, and PyQT5.

To use this, first:
- install python3 (3.7) and dependencies, including wxPython version>=4 and pyVTK>=8.0
     Recommended:
     
         install python3 using Anaconda, 
         start an anaconda terminal for this Python 3 installation, then type the following:

         conda install -c anaconda vtk wxpython
         conda install configobj
         conda install pyopengl   [the traitsui demo launcher might otherwise crash with qt4 backend using pyqt5]
         pip install fonttools
         
         (might be necessary, particularly for Windows:
         conda install swig
         conda install git 
         ) 
         
         (for OSX, most likely, the following:
         export TTFPATH=/Library/Fonts )
         
        (for Windows, for building it is necessary to have a visual studio environment (community edition free for individual/academic/open-source use). The build succeeded with a 2015 community version) 
         
            
        
     
- Create a local directory with any name (say my_ets)
- download ets.py from the ETS_py3 repository and save to this directory
- Open a terminal and invoke conda environment. On Windows, this must be a Visual Studio 64-bit command window that can be invoked from the Start menu
- cd to my_ets

then type, from Anaconda Python 3 terminal for fresh install: 
  
      Fresh install all packages from master:
         python ets.py clone
         python ets.py build
         python ets.py develop (run from source directory) 
            ---OR---- 
         python ets.py install (install to and run from python site_packages directory)
         

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
