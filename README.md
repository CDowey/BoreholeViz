# BoreholeViz
3-Dimensional borehole visualization

### Subsurface Information
Subsurface information is essential for Vermont Geological Survey mapping projects and groundwater or geologic hazard investigations. It improves below-ground interpretations and subsurface models, allowing for more accurate construction of cross-sections, 3D bedrock elevation surfaces, overburden thickness (Isopach) maps and more. Subsurface data is obtained either through indirect measurments such as ground-penetrating radar, passive seismic readings, and bore-hole geophysical logging or direct measurements such as augers, core-logging, and vertical exposures to name a few.

### Geophysical Logging
Geophysical logging of drinking water wells is a key component of the Vermont Geological Survey's research on groundwater quality in fractured bedrock aquifers. We can use these logs derived from a series of instruments lowered down the borehole to indentify faults, contacts, bedding, fractures, veins and many other geologic features. Not only do these logs offer incredible detail about the rock itself but also the size, distribution, orientation, and character of flow pathways in the subsurface.

### 3D Visualization
Each geophysical log provides a wealth of information, but it is often overly simplified in geologic models and visualizations. By plotting information derived from boreholes in 3D, we can show a large amounts of detail plotted in x,y,z space. We use common structural geologic methods to identify fracture sets and common orientations and plot them using the [Plotly python library](https://plot.ly/python/). This results in interactive 3D plots that greatly aid geologists who interpreting borehole logs by illustrating the details of the logs in x,y,z space. 

### True Borehole Position and Planar Features
A key component of plotting in x,y,z space is calculating the true position of the borehole. In virutally all cases boreholes are not perfectly vertical and they either purposefully or not deflect from the vertical. To calculate the true position of the borehole at any depth I use a series of equations derived for horizontal drilling.

To plot planar features that intersect the borehole I use orientation information derived from the acoustic televiewer, optical televiewer, caliper, and other tools to derived the equation for each planar feature. Then I plot these planes along with the true borehole position and often colorize them based on certain properties. This provides a tremendous amount of information in an interactive 3D display. 

Example Plot

![3D_Fracture_Plot](../master/Fracture_3D_well.png)

[View interactive 3D Plotly display](https://nbviewer.jupyter.org/github/CDowey/BoreholeViz/blob/master/BenningtonWells/Borehole_26STL_WellFract.ipynb)

### Next step
In most cases the geophysical logs do not provide much information about how far features extend beyond the borehole, so I often plot features such as fractures closely around the borehole even though they could possibly extend far beyond. With other features such as bedding, with sound geologic mapping at the surface and in the subsurface, we can make sound interpretations about their continuation and orientation. We can project and plot these features and determine where the intersect the land surface, or other boreholes in the area.
