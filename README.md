CUPS Booklet backend
====================

This script can be used as a backend for the CUPS printing system. It will convert your printjobs into
booklet format and send them to another printer of your choice to be printed.

Usage
-----

1. Copy this script to /usr/lib/cups/backend/booklet and make it executable.
2. Go to http://localhost:631 and login.
3. Create a new printer of the booklet type ("Print a document in booklet form")
3.1. Specify as the "Connection" URI: booklet:/MyPrinter (Single slash!, MyPrinter should be a printer known to CUPS, e.g. booklet:/My-HP-PrintJet)
3.2. Specify a name like "Booklet printer"
3.3. Setup the printer as a Generic PostScript printer (Make: Generic, Model: Generic PostScript Printer (en))
3.4. Set the default options of the printer.


Debugging
---------

If things don't work as planned, you can set "debug=true" in the script so it will 
save a copy of its temporary files in /tmp/print-*
