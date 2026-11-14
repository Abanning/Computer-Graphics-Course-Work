### MP6: Simple (fake) Modeling Editor: Polygonal Modeling and File Texture Mapping
# Overview:
An interactive 3D modeling and texture-mapping editor that combines custom CPU-based procedural mesh generation, direct vertex manipulation, UV space transformations, and camera controls. Features include:  

Planar & Cylindrical Mesh Modeling: Generates custom N×M indexed triangle meshes for both a planar surface and a rotational sweep General Cylinder. Users control mesh resolution ([4,20] vertices) and cylinder sweep angles ([10∘, 360∘]) via UI sliders. Normal vectors are reconciled along the closing seam of 360∘ cylinders to prevent illumination artifacts.

Direct Vertex Manipulation: Pressing Left-Control reveals selectable control spheres and surface normal vectors at each mesh vertex. Ctrl + LMB selects a vertex, spawning an interactive RGB 3D Translation Manipulator (three-cylinder axis frame) at the vertex position. Dragging the manipulator handles translates the vertex in 3D space, dynamically updating the mesh geometry and normals in real time.  

CPU-Based UV Texture Mapping (Matrix3x3): Implements a custom 2D affine transformation pipeline using a Matrix3x3 library to map textures onto the planar mesh. Users adjust Translation, Rotation, and Scaling (TRS) of the UV space through the GUI, with transformations calculated on the CPU and applied directly to the vertex UV coordinates.

Illumination & Integrated Camera Controls: Integrates the orbital Tumble/Track/Dolly camera system (Alt + LMB) from MP5. Includes a lighting system featuring a Directional Light aligned with the camera view and a user-controlled Point Light with adjustable X/Y/Z positional sliders.

# Screenshots:






<figure>
  <img width="600" height="336" alt="MeshControls_Sliders" src="https://github.com/user-attachments/assets/60d18194-33f7-48b3-b22b-7afe3dacd122" />
  <br />
  <figcaption>Demonstrating texture slider controls - translation and scaling of texture on a custom mesh object.</figcaption>
</figure>
<br />

<figure>
  <img width="600" height="336" alt="MeshControls_Res" src="https://github.com/user-attachments/assets/d2e182bc-163e-4090-84b2-324e556ecdce" />
  <br />
  <figcaption>Resolution Slider control. Increasing resolution means more vertex positions on the mesh.</figcaption>
</figure>
<br />

<figure>
  <img width="600" height="336" alt="MeshControls_ResolutionControl" src="https://github.com/user-attachments/assets/a64b36c4-4900-4fc7-8c23-bf7b88b3f50a" />
  <br />
  <figcaption>Demonstrating mesh resolution controls. Holding left ctrl displays the vertex positions of the mesh. Clicking the vertex position opens an axis frame, and clicking and dragging one of the axes of the axis frame allows the user to drag a vertex to a new position, modifying the mesh.</figcaption>
</figure>
<br />

<figure>
  <img width="600" height="336" alt="Cylinder_Sliders" src="https://github.com/user-attachments/assets/36040f39-4bd3-4c4f-b99c-338601ff17f3" />
  <br />
  <figcaption>Demonstrating basic slider function on cylinder mesh object. Uses sweeping about an axis to create the mesh object based on sweep angle and the number of vertex positions determines the level of detail (curve in this case).</figcaption>
</figure>
<br />

<figure>
  <img width="600" height="336" alt="Cylinder_VertexDrag" src="https://github.com/user-attachments/assets/d723ca3b-50de-4d1b-9a02-a438db7854cd" />
  <br />
  <figcaption>Same functionality with vertex repositioning as the mesh object.</figcaption>
</figure>
<br />
