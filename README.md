# MUP Kicad Library 

This repository contains additional Kicad schematic symbols and 
footprints used in mup hardware projects.

# Version Compatibility

  * Kicad 8: Commit 993653839ae8 8th Aug 2024 or newer.
  * Kicad 4: Commit 436f651d5c07 28th Nov 2016 or prior.

# Library Setup

In Kicad 8's "Preferences/Configure Paths" add the following variables
and set the path to the folder indicated within the mup-kicad-library

  | Name                | Directory          |
  |---------------------|--------------------|
  | MUPS_KI3DMOD        | modules/package3d  |
  | MUPS_SYMBOL_DIR     | library/           |
  | MUPS_FOOTPRINT_DIR  | modules/           |

## Eeschema

Via "Preferences/Manage Symbol Libraries" add each of the ".kicad_sym" files from 
the library directory to the global or project specific library.

If you setup the MUPS_SYMBOL_DIR path correctly, kicad will replace the absolute
path of the kicad_sym file with:

  ${MUPS_SYMBOL_DIR}/mups_maxim.kicad_sym 

Close and re-open Eeschema and all the schematic symbols should now be found.

## Footprints

As with Eeschema, add each ".pretty" footprint files from the modules/ directory
via the "Preferences/Manage Footprint Libraries".

Note: Some footprints are unchanged Kicad footprints saved to the
MUPS library in order to associate a 3d model with the footprint.
If the official Kicad library ever adds the missing models, the parts will
likely be removed from this repo.

## 3d Models

Some parts include a reference to models from the GPL'd 3d library by "kcswalter".
These are optional models not included in the MUPS Kicad library.

  git://smisioto.eu/kicad_libs.git 

Kicad will use these models during 3d preview mode if you add a new env variable 
via "Preferences/Configure Paths" named "WALTER_KI3DMOD" with path set to the 
modules/packages3d/ directory within the walter repo checkout. 

# License

Please refer to the LICENSES file.

Copyright 2016-2024 Gary Preston <gary@mups.co.uk> 

