### MP5: Camera View and Manipulation
# Overview:
Building directly on top of the MP4 Scene Graph hierarchy, this project implements a comprehensive camera control suite and multi-viewport rendering. The scene is populated with at least 12 distinct decoration objects surrounding the hierarchy to provide spatial reference during camera transforms. Features include:  

Main Camera Orbital Manipulation: Implements standard 3D modeling camera controls centered around an adjustable LookAt Position (X/Y/Z UI sliders):  

Tumble: Alt + LMB drag rotates the camera horizontally and vertically around the LookAt point.  

Track: Alt + RMB drag translates the camera along its local right and up axes.  

Dolly: Alt + Scroll Wheel moves the camera along its view vector toward or away from the LookAt point.  

Small View Camera (Picture-in-Picture): A secondary camera is dynamically calculated and attached to a leaf node of the hierarchy (e.g., the "Head" node). Its position and orientation continuously track the accumulated world transformations of its parent node. It renders to a viewport occupying the bottom-right 30% of the screen (45∘ FOV) and projects a visible line segment representing its view vector.  

Dynamic Node Attachment (Advanced): Users can dynamically reattach the Small View Camera to any currently selected SceneNode in the hierarchy at runtime.  

# Screenshots:
<figure>
  <img width="600" height="336" alt="Normal" src="https://github.com/user-attachments/assets/6a49ecb2-8d72-40fc-ba09-a033d1b8a9cf" />
  <br />
  <figcaption>Demonstrating normal operation. Notice how in this version, the small camera in the bottom left follows whichever the selected node is and looks out from its object coordinate space origin.</figcaption>
</figure>
<br />

<figure>
  <img width="600" height="336" alt="LookAtPosition_Sliders" src="https://github.com/user-attachments/assets/1da24e75-f8d1-4c89-9e5d-0f3d89d23556" />
  <br />
  <figcaption>This updated version of MP4 now introduces camera controls and a LookAtPosition (the small axis frame on the base plate). Moving the sliders in the top right control the position that the main camera looks at.</figcaption>
</figure>
<br />

<figure>
  <img width="600" height="336" alt="Small_Cam_Example" src="https://github.com/user-attachments/assets/ab8a0675-bffa-401d-9c89-a0062c1f31c8" />
  <br />
  <figcaption>Demonstrating more of the small camera perspective. Animated child objects move in their own object spaces.</figcaption>
</figure>
<br />

<figure>
  <img width="427" height="239" alt="Camera_Manipulation" src="https://github.com/user-attachments/assets/b8162719-3d40-40e7-af8e-73f4880792df" />
  <br />
  <figcaption>This project introduces Camera Manipulation. Hold left alt (option on Mac) + Left mouse button for tumbling, left alt + RMB for pan (moves LookAtPosition dynamically), left alt + scroll wheel for zooming.</figcaption>
</figure>
<br />
