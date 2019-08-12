# Digi-Key Tables

The Digi-Key tables repository contains XML descriptions of various `.csv` tables
that can be downloaded from Digi-Key.

# Introduction

The XML format is still under development some code being developed in the associated
[table_tools](https://github.com/waynegramlich/digikey_tables) repository.

These tables are produced using some code that basically selectively downloads the
first 500 entries of `.csv` table from Digi-Key.  The table is heuristically scanned
to guess the format of the data under each column heading.  The code that does this
scanning is not currently released and is unlikely to ever be released.  The reason for
this is that many fairly large`.csv` files are downloaded.  If many of people did this,
Digi-Key might deside to remove the `[Download CSV]` button from their Web interface.
Longer term, it would be nice to find an alternative way of getting this information
from Digi-Key.

## Basic Data Organization

The `.xml` files are organized into directories and sub directories.
The file names represent the basic Digi-Key catitogories and sub categories.
Spaces are encoded with an underscore ('_') and all many other characters
are encoded using the "%XX" format, where XX is the character number in hex.
The xml files tend to be of the form "name1-...-nameN", where "nameI" is just
a sequence of letters and digits.  The final suffix is ".xml".  That is it.

Without getting into the XML file format details, it has a table name
followed by a list of parameter names, where each parameter name corresponds
to a single column in the associated.csv file.  The "<Parameter>" tag also
specifies the heuristically defined format of the data.

