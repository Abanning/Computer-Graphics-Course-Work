### MP4: Scene Nodes and Scene Graph
# Overview:
This project explores pivoted transformations and hierarchical Scene Graph architecture by constructing an articulated, multi-generational 3D model (e.g., a robotic torso with branching left/right arms, upper arms, hands, and fingers). Key architectural elements include:  

Custom Model-View Matrix Shading: To demonstrate raw transform mathematics, all primitives in the hierarchy are rendered using a custom shader (451Shader) where the model transformation matrix is explicitly computed and loaded from script, bypassing Unity's default transform pipeline and UNITY_MATRIX_MVP.  

Hierarchical Articulation & Duplication: The hierarchy contains at least four generations of connected SceneNode objects. It includes a duplicated sub-hierarchy (e.g., two identical arms parented to a torso) to verify reusability. Each node features a sphere primitive positioned exactly at its rotation joint.  

Axis Frame & UI Manipulation: Users can select individual scene nodes via a GUI dropdown menu (SelectMenu) to manipulate their local transformations via XformControl. The active node prominently toggles an RGB Axis Frame oriented to its local pivot.  

Continuous Pivoted Animations: Three distinct primitives animate continuously across different hierarchy levels while maintaining structural connection: a Sphere rotating around a tangent axis on its circumference, a Cube rotating around an axis parallel to its surface, and a Capsule rotating around its tip.  
