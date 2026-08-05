### MP3: Fun with Vectors and Abstraction
# Overview:
This project focuses on applying 3D vector mathematics and object-oriented abstraction to simulate dynamic line segments and traveling entities within a bounded world box. The environment is defined by four perpendicular planes (LeftWall, RightWall, BackWall, and Floor). Key systems include:  

AimLine & BigLine Abstraction: Line segments are rendered using dynamically scaled and rotated cylinders stretched between two LineEndPt spheres. Endpoints are constrained to the four walls of the world box and can be interactively dragged via left-mouse clicks. AimLines (thin cylinders) are created by clicking the LeftWall, while BigLines (thick cylinders, width 1.9) are created by clicking the BackWall.  

Traveling Balls: Spheres that continuously spawn at the start endpoint of an AimLine and travel along the segment vector toward the end. Users control the Spawn Interval ([0.5,4] sec), Speed ([0.5,15] units/sec), and LifeSpan ([1,15] sec) via real-time GUI sliders.  

Interactive Deletion: Clicking directly on the cylinder segment of any AimLine or BigLine removes it from the scene. All mouse selection relies strictly on Unity's RayCast layer system (Wall, EndPt, and Line layers) without using the built-in physics engine.  
