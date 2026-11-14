### MP3: Fun with Vectors and Abstraction
# Overview:
This project focuses on applying 3D vector mathematics and object-oriented abstraction to simulate dynamic line segments and traveling entities within a bounded world box. The environment is defined by four perpendicular planes (LeftWall, RightWall, BackWall, and Floor). Key systems include:  

AimLine & BigLine Abstraction: Line segments are rendered using dynamically scaled and rotated cylinders stretched between two LineEndPt spheres. Endpoints are constrained to the four walls of the world box and can be interactively dragged via left-mouse clicks. AimLines (thin cylinders) are created by clicking the LeftWall, while BigLines (thick cylinders, width 1.9) are created by clicking the BackWall.  

Traveling Balls: Spheres that continuously spawn at the start endpoint of an AimLine and travel along the segment vector toward the end. Users control the Spawn Interval ([0.5,4] sec), Speed ([0.5,15] units/sec), and LifeSpan ([1,15] sec) via real-time GUI sliders.  

Interactive Deletion: Clicking directly on the cylinder segment of any AimLine or BigLine removes it from the scene. All mouse selection relies strictly on Unity's RayCast layer system (Wall, EndPt, and Line layers) without using the built-in physics engine.  

# Screenshots:
<figure>
  <img width="600" height="337" alt="Create" src="https://github.com/user-attachments/assets/5278a6b4-f0b2-4ed4-9768-9aa9918f7e61" />
  <br />
  <figcaption>Create new lines by clicking on walls.</figcaption>
</figure>
<br />

<figure>
  <img width="600" height="337" alt="MovingAndCreating_Lines" src="https://github.com/user-attachments/assets/255e9569-9020-4694-a02f-f9ad8c900a69" />
  <br />
  <figcaption>Demonstrating the capability of moving lines by clicking and dragging an endpoint and creating new lines by clicking on walls.</figcaption>
</figure>
<br />

<figure>
  <img width="600" height="337" alt="Sliders" src="https://github.com/user-attachments/assets/51f0da26-08eb-4d41-a07f-7553c5b4fc78" />
  <br />
  <figcaption>Demonstrating slider controls for the moving balls.</figcaption>
</figure>
<br />

<figure>
  <img width="600" height="337" alt="Extra_Credit" src="https://github.com/user-attachments/assets/eb4514e5-e747-4ccb-b42f-b622c3a7b830" />
  <br />
  <figcaption>Extra Credit - Implemented Sinusoidal and Radial movement about the MovementLine by pressing 'S' or 'R' on the keyboard.</figcaption>
</figure>
<br />

<figure>
  <img width="600" height="337" alt="Delete" src="https://github.com/user-attachments/assets/c72236e6-1f64-43dd-a695-2c0148e2ffd1" />
  <br />
  <figcaption>Deletion Feature - click on a line segment to delete the whole object</figcaption>
</figure>
<br />



