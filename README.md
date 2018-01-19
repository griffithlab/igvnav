PURPOSE:

IGVNavigator (IGVNav) is a tool that was developed to assist in analyzing 
variants during manual review. Its input is a text file with variant 
coordinates and its output provides an annotation of these variant 
coordinates. This annotation includes the call (i.e. somatic, germline, 
ambiguous, or fail), tags to provide additional information if a variant 
is called ambiguous or fail, and a notes section for free text

EXAMPLE INTERFACE:

![alt text](https://github.com/griffithlab/igvnav/blob/master/IGVNav_interface.png)


DOWNLOAD:

Steps to download IGVNav for Mac:

1) Download [IGVNav.zip](https://github.com/griffithlab/igvnav/raw/master/dist/IGVNav.zip)

2) Unzip File

3) Add unzipped file to Applications/ folder.



INSTRUCTIONS FOR USE:

1) Open IGV

2) Load session file (e.g. .bam files)

3) open IGVNav applicaiton 

4) IGVNav app will prompt you to open a manual review file.

5) Open a manual review file whereby the format of this file
is a TSV file with columns:
   
   Chromosome   Start   Stop   Reference   Variant   Call   Tags   Notes

6) The first six columns (Chromosome, Start, Stop, Reference, and Variant)
should be filled-out and the remaining columns will be blank.

NOTE: The column names do not have to match exactly the above, but they do
have to be the correct data in the same column order.

7) Navigate through the manual review file using the arrows on the 
IGVNav interface.

8) Ensure that coordinates on IGVNav interface match the IGV interface.

9) Select a Call for each variant based on support for variant.

10) Select various Tags for each variant if variant is labeled
as ambiguous or fail.

11) Input any notes required in the free-text box.

12) Periodically save the manual review file to ensure that calls
are recorded. Be sure to save the manual review file prior to closing
the IGVNav session.



INSTRUCTIONS FOR DEVELOPING:

1) clone the repo/ sub-folder

2) Edit IGVNav.py

To build, you will need to install wxPython and py2applet:
$ python setup.py py2app

App will be placed in dist/ sub-directory of the repository
