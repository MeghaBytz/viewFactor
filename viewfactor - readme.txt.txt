Function written by Nicolas Lauzier in collaboration with Daniel Rousse, Université Laval, 2003-2004

-----------------------------

To use the function, you need:

viewfactor.m
functionintegral.m
functionviewfactorarea.m

------------------------------

functionintegral.m and functionviewfactorarea.m are two functions used by viewfactor.m,
so you never need to use them directly.

viewfactor use the CDIF method to calculate view factors between planar polygons.
The polygons can be in any orientation and can have any shape. The only restriction
is that any of the two polygon must not cross the plane containing the other polygon.

------------------------------

The way to use the viewfactor is the following:

The function receive 3 parameters, which are the coordinates of 
both figures and the desired number of significant digits.

[vfactor12,vfactor21,area1,area2]=viewfactor(coord1,coord2,nbdigits)

coord1 and coord2 are the coordinates of the vertices that
set the outline of figures 1 and 2. It must be entered this way:
coord1=[[x1,y1,z1];[x2,y2,z2];[...,...,...];[xn,yn,zn]]

nbdigits is the desired number of significant digits.
The function display more digits but only 'nbdigits' 
are significant.

Example: Use the following command to calculate the view factors between two parallel
         triangles of coordinates (0,0,0),(1,0,0),(0,1,0) and (0,0,1),(2,0,1),(0,2,1)
         with a precision of 6 significal digits.


[vfactor12,vfactor21,area1,area2]=viewfactor([[0,0,0];[1,0,0];[0,1,0]],[[0,0,1];[2,0,1];[0,2,1]],6)

--------------------------------

Questions/comments: nlauzier@yahoo.com