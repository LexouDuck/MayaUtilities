# MayaUtilities

---

![Custom Shelf](shelf.png)

All of the individual scripts on this repo are stored within the button shelf file 'shelf_Custom.mel'

It must be placed in %MAYA_FOLDER%/%VERSION%/prefs/shelves/ so that Maya can find and load the custom shelf

You may rename the shelf however you wish, in the format 'shelf_NewName.mel' (if you decide to do so, you also need to change the first line of the script accordingly)

Otherwise, the individual scripts can be placed in the Script Editor and saved as shelf buttons onto any existing shelf.



Here is a short description of each MEL script:
---
- **AlphaNodeCorrect**: Manually plugs in the output alpha of each texture node to its corresponding material node's input transparency. Use this if the parts of the model which should be transparent appear opaque.
- **TransparencyCorrect**: Make alpha channels work properly for imported models by setting 'alpha is luminance' to false. Use this when the entire model is more or less see-through, it will make the correct parts of the model opaque as they should be.
---
- **UnfilterAllTextures**: Sets every image texture in the scene to be unfiltered (ie: aliased, pixelated)
- **FilterAllTextures**: Sets every image texture in the scene to have quadratic bilinear filtering
---
- **MirrorAllTextureUVs**: Make it so all UV nodes in the scene have U & V mirrored texture space
- **UnMirrorAllTextureUVs**: Make all UV nodes in the scene have U & V mirroring set to false
---
- **TileAllTextureUVs**: Make it so all UV nodes in the scene have repeating tiled texture space
- **UnTileAllTextureUVs**: Make it so all UV nodes in the scene only have texture space within the 0-1 UV square, so the outside of this UV space is a solid color
---
- **ShowVertexColors**: Make all objects in the scene display their polygon vertex colors
- **HideVertexColors**: Make all objects in the scene hide their polygon colors
---
- **NoShade**: Make all materials full-lit 100% diffuse
- **CelShade**: Make every material's ambient lighting use a simple 3-step ramp shader
---
- **MergeAllVertices**: Merges together any vertices that are within 0.001 distance of each other
---
- **SoftenAllEdges**: Makes every edge of every polygon object have soft normal shading
- **HardenAllEdges**: Makes every edge of every polygon object have hard polygonal normal shading
---
and these last 2 scripts are specifically for submitting rips to the models resource
- **SmallScreenshot**: Saves a 168x145 png screenshot of the current view (without HUD elements and bone joints)
- **LargeScreenshot**: Saves a 750x650 png screenshot of the current view (without HUD elements and bone joints)
