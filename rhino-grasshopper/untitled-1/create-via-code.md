---
description: Generating Geometry Gym IFC models via code.
---

# Create via Code

## Starting a Model

## Assigning Beams

{% tabs %}
{% tab title="Python" %}
```python
import clr
import sys

clr.AddReferenceToFileAndPath(r"C:\Program Files\Geometry Gym\Rhino3d\ggRhinoIFC.dll")

import GeometryGym.Ifc as gg 

from System.Collections.Generic import List
from System import Guid
from Rhino.Geometry import Transform
from Rhino.Geometry import Point3d
from Rhino.Geometry import Vector3d
from Rhino.Geometry import Line
from Rhino.Geometry import Plane

ipe = "IPE300"
db = gg.DatabaseIfc(True,gg.ModelView.Ifc2x3Coordination) 

building = gg.IfcBuilding(db,"PythonBuilding")
project = gg.IfcProject(building,"PythonProject", gg.IfcUnitAssignment.Length.Millimetre)
s355 = gg.IfcMaterial(db,"S355JR") 
s355.Category = "STEEL"
pd = gg.IfcIShapeProfileDef(db,ipe,150,300,7.1,10.7)
pd.FilletRadius = 15
#ifcBeamTypeID = GuidEncoder.Encode(Guid("{FA07940E-19FC-417a-B7F1-09A0CCF39B74}")) 
#Can create a unique identifier if you wish else leave blank

mp = gg.IfcMaterialProfile(ipe,s355,pd)

mpUsage = gg.IfcMaterialProfileSetUsage(mp)

#bt = gg.IfcBeamType(ipe,mp,gg.IfcBeamTypeEnum.BEAM)
#ln = Line(Point3d(0,0,0),Point3d(1000,0,0)) 
#clipPlanes = List[Plane]()

#beam = gg.IfcBeamStandardCase(building,bt,ln,Vector3d.YAxis, gg.IfcCardinalPointReference.MID,clipPlanes)

axisPlacement = gg.IfcAxis2Placement3D(gg.IfcCartesianPoint(db,0,0,0),gg.IfcDirection(db,1,0,0),gg.IfcDirection(db,0,1,0))

beam = gg.IfcBeamStandardCase(building,mpUsage,axisPlacement,1000)

a = db.ToString()
```
{% endtab %}

{% tab title="C\#" %}

{% endtab %}
{% endtabs %}

