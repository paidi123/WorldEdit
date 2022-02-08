# WorldEdit

A Terraria plugin including many mass tile editing features. Documentation on commands is included.

----

### //point1 //p1
Sets the first point of the selection.  
_You can use the Grand Design to drag a full region, this selects all tiles in said region._  

----

### //point2 //p2
Sets the second point of the selection.  

----

### //set (tile) [=> boolean expr]
Sets all of the tiles in the selection to (tile).  

----

### //setwall //sw (wall) [=> boolean expr]
Sets all of the walls in the selection to (wall).

----  

### //setwire (wire) (state) [=> boolean expr]
Sets (wire) with (state) in the selection.  

----

### //cut
Removes/Cuts the selection and copies it to the clipboard.

----  

### //copy //c
Copies the selection to the clipboard.  

----

### //paste //p (direction)
Pastes the clipboard to the first point. Directions can be appointed to change from what point the clipboard pastes.  
- Applicable directions:
  - **tl** : TopLeft (default), this pastes the clipboard from the top left to the bottom right.  
  - **bl** : BottomLeft, bottom left to the top right.  
  - **tr** : TopRight, top right to bottom left.  
  - **br** : BottomRight, bottom right to top left.  

----

### //spaste //sp (position) [flags] [=> boolean expr]
Pastes with special flags.
- Flags applicable:
  - **-t**  - Excludes tiles from the clipboard.
  - **-tp** - Excludes tile paint.
  - **-w**  - Excludes walls.
  - **-wp** - Excludes wall paint.
  - **-wi** - Excludes wires.
  - **-l**  - Excludes liquids.

----

### //undo [steps] [account]
Undoes that many (Worldedit)actions for the account, if possible.  

----

### //redo [steps] [account]
Redoes that many (Worldedit)actions for the account, if possible. 

---- 

### //paint (color) [=> boolean expr]
Paints all the tiles in the selection to (color). You can use "blank" to remove paint.  

----

### //paintwall //paw (color) [=> boolean expr]
Paints all the walls in the selection to (color). You can use "blank" to remove paint.  

----

### //region [name]
Selects a complete TShock region to perform actions on. 

---- 

### //drain
Drains all liquids in the selection.  

----

### //flood (liquid)
Floods the selection with (liquid).  

----

### //schematic //schem /sc
Shows schematic commands. 

#### delete (name)
Deletes the schematic (name) if possible. 

#### help 
Lists all schematic commands.  

#### list [page]
Lists all the available schematics.  

#### load (name)
Loads the schematic (name) to the clipboard if it exists.  

#### save (name)
Saves the contents of the clipboard to the schematic (name).  

----

### //biome (biome1) (biome2)
Converts all of the tiles in the selection that correspond to (biome1) to the tiles that correspond with (biome2).  
- Biome’s applicable:
  - **forest**  
  - **crimson**  
  - **corruption**  
  - **hallow**  
  - **jungle** (Only works with Mushroom)  
  - **mushroom** (Only works with Jungle)  
  - **desert** (Does not work with anything)  
  - **snow** (Does not work with anything)  

----

### //inactive (on/off/reverse)
Actuates tiles in the worldedit selection, turning them active/inactive.  

----

### //activate
Activates non-working signs, chests or item frames  

----

### //fixghosts
Fixes invisible signs, chests and item frames.  

----

### //fixgrass
Fixes suffocated grass in the selection.  

----

### //fixhalves
Fixes covered half blocks in the selection. 

---- 

### //fixslopes
Fixes covered slopes in the selection.  

----

### //mow
Mows grass, thorns, and vines in the selection.  

----

### //near (radius)
Selects an area around you.  

----

### //flip (direction)
Flips the contents of the clipboard. (direction) can contain any amount of X's and Y's; each occurrence will flip the direction. E.g., XXYY would leave the clipboard unchanged.  

----

### //all
Selects the entire world.  

----

### //outline (tile) (color) (state) [=> boolean expr]
Sets (tile) outline around blocks in selection.  

----

### //outlinewall (wall) [color] [=> boolean expr]
Sets (wall) outline around the walls in selection.  

----

### //resize (direction(s)) (amount)
Resizes the selection to (direction(s)) by amount.  
Directions are left, right, up and down. The amount is measured in blocks.  

----

### //rotate (degrees)
Rotates the clipboard's contents by the specified angle, in degrees. Only multiples of 90 are accepted.  

----

### //select (selection type)
Sets the way that tiles are selected.  
- Arguments applicable:_  
  - **normal** : Default selection, Sets in the full region  
  - **altcheckers** : Sets in an alternate checker pattern  
  - **checkers** : Sets in a checker pattern  
  - **ellipse** : Sets round shapes  
  - **random** : Sets in a random pattern  
  - **outline** : Sets around all abstract block shapes in the region  
  - **border** : Sets the border of the region  
  - **45** : Sets on a 45 degree angle  
  - **225** : Sets on a 225 degree angle  
  _Always set the selection back to this selection after finishing your edits!_  

----

### //shift (direction(s)) (amount)
Moves the selection to (direction) by (amount). Directions are left, right, up and down. The amount is measured in blocks.  

----

### //scale (scale)
Scale the clipboard  

----

### //smooth
Smooths blocks in the selection.  

----

## Boolean expressions

**This chapter elaborates functionality within booleans & how to use them.**

Some commands accept boolean expressions, allowing you to change the conditions of the command. To use boolean expressions you have to know and use the right variables.  
  _Applicable boolean values:_  
      **tile (t)  
      wall (w)  
      tilepaint (tp)  
      wallpaint (wp)  
      honey  
      water  
      liquid  
      lava  
      wire  
      wire2  
      wire3  
      wire4**  

Boolean expressions work like this: **=> t** checks if there's a tile. | **=> t = dirt** checks if the tile is dirt.  

An exception boolean is: **=> !t** checks if there are no tiles | **=> !w** checks if there is no wall.  

With boolean expressions you can do stuff like this:  
    **//set dirt => t = stone.**  
  _This would change every stone in the selected area to dirt._  
Another example:  
    **//setwall wood => tp = green**  
  _This would add a wood wall to every green painted tile in the selected area._  


## Permissions

**A complete list of all permissions related to WorldEdit! Every permission starts with 'worldedit', the rest of the permission is attached below.**

**.selection.all** : /all  

**.selection.point** : /point1(2), /p1(2), p1(2)  

**.selection.near** : /near  

**.selection.outline** : /outline, /ol  

**.selection.outlinewall** : /outlinewall, /olw  

**.selection.region** : /region  

**.selection.resize** : /resize  

**.selection.selecttype** : /select  

**.selection.inactive** : /inactive, /ia  

**.selection.shift** : /shift  

**.selection.text** : /text  

**.region.set** : /set  

**.region.setwall** : /setwall, /swa  

**.region.setwire** : /setwire, /swi  

**.region.paint** : /paint, /pa  

**.region.paintwall** : /paintwall, /paw  

**.region.slope** : /slope  

**.region.delslope** : /delslope  

**.region.smooth** : /smooth  

**.region.shape** : /shape, /shapefill, /shapewall, /shapewallfill  

**.region.replace** : /replace, /rep  

**.region.replacewall** : /replacewall, /repw  

**.region.fill** : /fill  

**.region.fillwall** : /fillwall, /fillw  

**.region.biome** : /biome  

**.region.move** : /move  

**.region.actuator** : /actuator  

**.clipboard.copy** : /copy, /c  

**.clipboard.cut** : /cut  

**.clipboard.paste** : /paste  

**.clipboard.spaste** : /spaste, /sp  

**.clipboard.flip** : /flip  

**.clipboard.rotate** : /rotate  

**.clipboard.scale** : /scale  

**.utils.activate** : /activate  

**.utils.fixghosts** : /fixghosts  

**.utils.fixgrass** : /fixgrass  

**.utils.fixhalves** : /fixhalves  

**.utils.fixslopes** : /fixslopes  

**.utils.killempty** : /killempty  

**.utils.drain** : /drain  

**.utils.flood** : /flood  

**.utils.mow** : /mow  

**.utils.size** : /size  

**.history.undo** : /undo  

**.history.redo** : /redo  

**.schematic** : /schematic, /schem, /sc, sc  

**.magic.wand** : /magicwand, /mwand  

**.documentation** : /edithelp, /wedithelp  

**.admin** : /worldedit, /wedit  

**.usage.everywhere** : Use commands outside of regions.

