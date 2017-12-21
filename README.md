# Gedcom-UnFtmEvent

Undoes Family Tree Maker's turning unknown event tags from imported
GEDCOM files to EVEN records.

When importing a GEDCOM file to Family Tree Maker (2017) with unknown
inidividual event tags, such as this:

0 INDI
  1 _FOO value

upon exporting to GEDCOM, will become this:

0 INDI
  1 EVEN value
    2 TYPE _FOO

This program undoes that. In this case, pass "-t _FOO" option
to the program.
