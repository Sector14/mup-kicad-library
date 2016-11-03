# MUP Kicad Library 

This repository contains additional Kicad schematic symbols and 
footprints used in mup hardware projects.

# 3D Models

Some footprints include a reference to models from the GPL'd 3d library
by "kcswalter". These are optional models and not included in the mup 
Kicad library.

If you clone the walter repo:

  git clone git://smisioto.eu/kicad_libs.git 

You can have Kicad use these models during 3d preview mode
by adding a new env variable in PCBNew "Preferences/Configure Paths" 
called WALTER_KI3DMOD and with the path set to the 
<walter repo checkout path>/modules/packages3d/ directory. 

Any footprint in the mups library that has the 3d model path prefixed 
with {WALTER_KI3DMOD}/walter/ will then use the appropriate 3D model.

The same will apply to {MUPS_KI3DMOD}/mups/ although at this time I've
yet to create any custom 3D models and find it unlikely I will do so.

# License

Please refer to the LICENSES file.

Copyright 2016 Gary Preston <gary@mups.co.uk> 

