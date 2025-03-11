1. phantom_registration.ipynb

it calculatess the rigid transformation between CT coordinate system {CT} and Polaris Coordinate system {PO}: {CT} <-> {PO}
and registers the CT/Phantom in {PO}

Prerequisites: 
a. a probe/tool optically tracked by Polaris, ex. Medtronic Chicken Foot and its .rom file,
b. 3D model of the CT/Phantom,
c. Markers and their locations on CT/Phantom in {CT} (.fcsv file or equivalent), the marker locations can be marked in Slicer or Solidworks using the 3D Model of the CT/Phantom

2. visualization_streaming.ipynb

it visualizes the probe/tool and the CT/Phantom,
and helps validate the calculated transformation {CT} <-> {PO}

Prerequisites:
a. a probe/tool optically tracked by Polaris, ex. Metronic Chicken Foot and its .rom AND .stl files,
b. 3D model of the CT/Phantom (.stl or .vtk files)
c. Transformation {CT} <-> {PO} calculated by phantom_registration.ipynb

NOTES:

Make sure you have installed the packages:
1. Using scikit-surgery ndi tracker to get data from Polaris

2. Using VTK to visualize the tool in 3D

Potential Problems:
1. Don't know why the NDI ToolBox couldn't find the Polaris (worked well last week)
2. Can still start the Polaris without NDI ToolBox using API:
`$ telnet P9-25027.local 8765`
