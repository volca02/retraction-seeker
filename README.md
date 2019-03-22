# retraction-seeker

This project is WIP attempt at gcode generator that produces array of towers with various retraction settings between them.

* X axis changes retraction distance (by default 1.0 - 5.5 mm in 0.25 mm steps)
* Y axis changes retraction speed (by default 10.0 - 55.0 mm/s in 2.5 mm/s steps)
* Z axis changes temperature (by default 210 to 190 in 5C steps, 5mm each step)

The generated values for each of the axis are listed in the g-code and should be used as a key when observing the platter (ret_d_steps, ret_spd_steps, temp_steps).

All parameters of the generated g-code can be influneced (for now by modifying the settings dict in the source code, but config parser is planned if this project gets used more often).

Default parameters are set to similar values that prusa i3 mk3 would expect.

NOTE: Currently, the generated E axis movement is 7% more than expected (when compared to Slic3r generated g-code). Since this is a crucial part of the generation, more effort will be put to get the extrusion factor lined up correctly.
