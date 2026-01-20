# Life Is Strange
**STEAM-ID**: `319630`

## Game crash on launch 
The game crashes before showing anything on screen.

The following errors are displayed:
```	
LifeIsStrange: error while loading shared libraries: libCoreFoundation.so.476: cannot open shared object file: No such file or directory
```

To fix this, open the game folder and add the following line in the point specified in the `LifeIsStrange.sh` file:   
`export LD_LIBRARY_PATH="${GAMEROOT}/lib/x86_64:${LD_LIBRARY_PATH}"`

```bash
# first part of the file... 
export LD_PRELOAD="${LD_PRELOAD_ADDITIONS}:${LD_PRELOAD}" 
#insert here <----------
#-----rest of the file...
cd "$GAMEROOT/bin"
```

Now the game should launch. 
