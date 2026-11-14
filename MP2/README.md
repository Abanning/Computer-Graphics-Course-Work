### MP2: User Interaction and Simple MVC
# Overview:
This project introduces a Model-View-Controller (MVC) architectural pattern within Unity to construct a small-scale hierarchical 3D scene editor. The scene begins with a static reference plane and a three-level object hierarchy: GrandParent (blue-ish Cube) → Parent (green-ish Sphere) → Child (red-ish Cylinder). Key features include:  

Object Selection & Axis Frame Display: Left-click raycasting selects any GameObject in the scene. Selected objects are highlighted in a distinct semi-transparent color and display an RGB Axis Frame (red/green/blue cylinders representing the local X/Y/Z Cartesian axes) at their center. Clicking empty space unselects the object and restores its original material.  

Transform Control (XformControl GUI): A custom editor panel that binds to the Transform component of the active selection. It provides continuous numeric slider controls for Translation ([−10,10]), Scaling ([0.1,5]), and Rotation ([−180∘,180∘]). Rotations use incremental Quaternion multiplication (Quaternion.AngleAxis) to cleanly concatenate angular changes without gimbal lock or Euler-angle snapping.  

Hierarchical Primitive Creation (CreatePrimitive GUI): Users can dynamically spawn new primitive objects (Sphere, Cylinder, Cube) as children of the currently selected object. New root objects spawn at (0.5,0.5,0.5) in black, while new child objects spawn offset from their siblings/parent and are colored cyan.  

# Screenshots:
<figure>
  <img width="600" height="337" alt="Demo1" src="https://github.com/user-attachments/assets/472def13-251d-4080-bd23-0326d2ca4f78" />
  </br>
  <figcaption>Demonstration of hierarchical TSR manipulation using custom sliders.</figcaption>
</figure>

</br>
</br>

<figure>
  <img width="600" height="337" alt="Tornado" src="https://github.com/user-attachments/assets/d71fe555-10e0-4fb2-b311-4de3551d805b" />
  </br>
  <figcaption>Extra Credit - Tornado animation reset scene</figcaption>
</figure>
</br>
