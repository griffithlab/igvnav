Using IGVNav for Mac:

Just download [IGVNav.zip](dist/IGVNav.zip), unzip and add to Applications/ folder.

Open IGV, open your session file, then open IGVNav app. 

IGVNav app will prompt you to open a manual review file.

Expected manual review file format is a TSV file with columns:
Chromosome   Start   Stop   Reference   Variant   Call   Tags   Notes

Last three columns can be missing on first load. Saving will overwrite
this opened file, and delete any extra columns you have, so stick to the
recipe.

The column names do not have to match exactly the above, but they do
have to be the correct data in the same column order. Column names will
be replaced when you save the file.


For developers:

clone the repo/ sub-folder

The code is mostly in IGVNav.py

To build:
You will need to install wxPython and py2applet
$ python setup.py py2app

App will be placed in dist/ sub-directory of the repository