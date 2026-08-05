### MP6: Simple (fake) Modeling Editor: Polygonal Modeling and File Texture Mapping
# Overview:
An interactive 3D modeling and texture-mapping editor that combines custom CPU-based procedural mesh generation, direct vertex manipulation, UV space transformations, and camera controls. Features include:  

Planar & Cylindrical Mesh Modeling: Generates custom N×M indexed triangle meshes for both a planar surface and a rotational sweep General Cylinder. Users control mesh resolution ([4,20] vertices) and cylinder sweep angles ([10∘, 360∘]) via UI sliders. Normal vectors are reconciled along the closing seam of 360∘ cylinders to prevent illumination artifacts.

Direct Vertex Manipulation: Pressing Left-Control reveals selectable control spheres and surface normal vectors at each mesh vertex. Ctrl + LMB selects a vertex, spawning an interactive RGB 3D Translation Manipulator (three-cylinder axis frame) at the vertex position. Dragging the manipulator handles translates the vertex in 3D space, dynamically updating the mesh geometry and normals in real time.  

CPU-Based UV Texture Mapping (Matrix3x3): Implements a custom 2D affine transformation pipeline using a Matrix3x3 library to map textures onto the planar mesh. Users adjust Translation, Rotation, and Scaling (TRS) of the UV space through the GUI, with transformations calculated on the CPU and applied directly to the vertex UV coordinates.

Illumination & Integrated Camera Controls: Integrates the orbital Tumble/Track/Dolly camera system (Alt + LMB) from MP5. Includes a lighting system featuring a Directional Light aligned with the camera view and a user-controlled Point Light with adjustable X/Y/Z positional sliders.
