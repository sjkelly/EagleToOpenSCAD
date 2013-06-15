##Eagle to OpenSCAD
This work is derived from EagleUp. Currently this script has support for board and component export. The board portion has been heavily tested for the generation of test jigs. The script will export a component and position in `translate()module()` form. However, none of these modules for components exist and this output is therefore untested. 

##Use
![Screenshot](./screenshot.png)

###Outline layer
Existing functionality from EagleUp.

###3D Export
####3D CSG
Uses 3D primitives to generate the board model.
####Extrude
Creates a 2D drawing of the board holes and uses `linear_extrude()` to extrude the sketch into 3D. OpenSCAD interprets this slower than 3D CSG.

###Holes
####Regular
Uses the traditional OpenSCAD `cylinder()` to create holes.
####Polyholes (requires Magpie)
Uses [polyholes by nophead](http://hydraraptor.blogspot.com/2011/02/polyholes.html) to create accurately sized holes for 3D printing. The functionality is imported from the[Magpie hardware library](https://github.com/sjkelly/Magpie) for OpenSCAD. See the library readme for installation instructions.

##Bugs and Contributions
Send issues and pull requests to @sjkelly on GitHub. 

