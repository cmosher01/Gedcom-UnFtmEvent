# Gedcom-UnFtmEvent

Undoes Family Tree Maker’s turning unknown event tags (from imported
GEDCOM files) into `EVEN` records.

When importing a GEDCOM file with unknown
individual event tags, such as this:

    0 INDI
         1 _FOO value

into Family Tree Maker,
upon exporting to GEDCOM, will become this:

    0 INDI
         1 EVEN value
              2 TYPE _FOO

This program undoes that action, thus restoring the original tag.
In the example above, you would pass `--tag=_FOO` as the option
to the program.
