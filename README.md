# tikz-manipulator
Generate tikz-cd diagrams.

Version 1.0.0 is a proof-of-concept.  
The front-end is built in webpack and runs from the webpack dev server.  (port 8080)
The backend is a Node Express server. (port 3000)

These may be changed, but you'll need to reconfigure CORS in texserver.js appropriately.

The front-end uses Material-UI react components:  http://www.material-ui.com/#/
State management is handled by redux:  http://redux.js.org/

The backend uses fs and child_processes to write/read files and execute pdflatex.  Hence:

Requires an installation of pdflatex in your system PATH.
See:  https://miktex.org/about

MikTeX comes with a package manager.  Packages amsmath, amsfonts, and amssymb should come with the native installation.
Use the package manager to install tikz-cd.  Dependencies for tikz-cd, e.g. tikz and pgf, should install automatically.

tikz-manipulator is intended to be supplementary to a tex editor for slow-to-typeset bits.
For a full editor, I recommend texmaker:
http://www.xm1math.net/texmaker/

Documentation for the tikz-cd package may be found here:  mirrors.ibiblio.org/CTAN/graphics/pgf/contrib/tikz-cd/tikz-cd-doc.pdf

Development was done on a Windows 10 machine using Google Chrome browser.  Still, everything should translate...

--- VERSION 1.0.0 NOTES ---
 - Still on webpack dev server.
 - Choice of directories for tex/pdf files is currently restricted to src/public/tex.
 - Existing files may be selected in the application, but the logic for reading arbitrary tex back into the application state
   is not yet implemented.
