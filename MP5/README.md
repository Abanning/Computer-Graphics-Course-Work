### MP5: Camera View and Manipulation
# Overview:
Building directly on top of the MP4 Scene Graph hierarchy, this project implements a comprehensive camera control suite and multi-viewport rendering. The scene is populated with at least 12 distinct decoration objects surrounding the hierarchy to provide spatial reference during camera transforms. Features include:  

Main Camera Orbital Manipulation: Implements standard 3D modeling camera controls centered around an adjustable LookAt Position (X/Y/Z UI sliders):  

Tumble: Alt + LMB drag rotates the camera horizontally and vertically around the LookAt point.  

Track: Alt + RMB drag translates the camera along its local right and up axes.  

Dolly: Alt + Scroll Wheel moves the camera along its view vector toward or away from the LookAt point.  

Small View Camera (Picture-in-Picture): A secondary camera is dynamically calculated and attached to a leaf node of the hierarchy (e.g., the "Head" node). Its position and orientation continuously track the accumulated world transformations of its parent node. It renders to a viewport occupying the bottom-right 30% of the screen (45∘ FOV) and projects a visible line segment representing its view vector.  

Dynamic Node Attachment (Advanced): Users can dynamically reattach the Small View Camera to any currently selected SceneNode in the hierarchy at runtime.  
