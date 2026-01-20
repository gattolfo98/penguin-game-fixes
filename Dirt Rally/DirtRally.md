# Dirt Rally
**STEAM-ID**: `310560`

## Game crash on launch 
The game crashes before showing anything on screen.

The following errors are displayed:
```	
libSDL2-2.0.5.so => not found
libSDL2_image-2.0.1.so => not found
libcef.so => not found
libpdf.so => not found


DirtRally: error while loading shared libraries: libSDL2-2.0.5.so: cannot open shared object file: No such file or directory.
```

To fix this, open the game folder and add the following line at the end of the `config/extra-environment.sh` file:   
`export LD_LIBRARY_PATH="${GAMEROOT}/lib/x86_64:${LD_LIBRARY_PATH}"`

Now the game should launch. 


**NOTE**: 
If you had any saves made on Windows/Proton, they will likely be considered corrupted, and you'll need to create a new save.
