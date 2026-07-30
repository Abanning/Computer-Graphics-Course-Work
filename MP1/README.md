### MP1: Orientation and Weekend Entertainment
# Overview:
This project serves as an orientation to Unity as an interactive learning tool and graphics environment. The application renders a Creation Plane (a 14×14 quad on the XZ-plane) and a Creation Target (a marker sphere located above the plane). Using a custom UI radio button system (ToggleGroup), users can spawn three distinct primitives at the Creation Target: Spheres, Cylinders, and Cubes. Each primitive exhibits autonomous runtime behaviors:  

Sphere: Scales to (0.5,1,1), travels along the Y-axis at 1 unit/sec, rotates about the Y-axis at 45∘/sec, and oscillates between Y=0 and Y=5, changing color between white (+Y) and magenta (−Y).  

Cylinder: Scales to (0.5,1,1), travels along the Z-axis at 1.5 units/sec, rotates at 90∘/sec, and oscillates between Z=0 and Z=5, changing color between white (+Z) and cyan (−Z).  

Cube: Scales to (1,1,1), travels along the X-axis at 2 units/sec, rotates at 135∘/sec, and oscillates between X=0 and X=5, changing color between white (+X) and yellow (−X).  

Non-visible user interactions include Left-Mouse-Button (LMB) raycasting on the Creation Plane to reposition the Creation Target, and clicking on spawned primitives to delete them from the scene without moving the target.
