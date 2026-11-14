### MP1: Orientation and Weekend Entertainment
# Overview:
This project serves as an orientation to Unity as an interactive learning tool and graphics environment. The application renders a Creation Plane (a 14×14 quad on the XZ-plane) and a Creation Target (a marker sphere located above the plane). Using a custom UI radio button system (ToggleGroup), users can spawn three distinct primitives at the Creation Target: Spheres, Cylinders, and Cubes. Each primitive exhibits autonomous runtime behaviors:  

Sphere: Scales to (0.5,1,1), travels along the Y-axis at 1 unit/sec, rotates about the Y-axis at 45∘/sec, and oscillates between Y=0 and Y=5, changing color between white (+Y) and magenta (−Y).  

Cylinder: Scales to (0.5,1,1), travels along the Z-axis at 1.5 units/sec, rotates at 90∘/sec, and oscillates between Z=0 and Z=5, changing color between white (+Z) and cyan (−Z).  

Cube: Scales to (1,1,1), travels along the X-axis at 2 units/sec, rotates at 135∘/sec, and oscillates between X=0 and X=5, changing color between white (+X) and yellow (−X).  

Non-visible user interactions include Left-Mouse-Button (LMB) raycasting on the Creation Plane to reposition the Creation Target, and clicking on spawned primitives to delete them from the scene without moving the target.

To try the project, navigate to the Executables folder and download the zip file for your system (MacOS Intel or Apple Silicon, Windows 7+ - x64 or x86). Further instructions will be provided in the next README. If your system is not available, you may request a new build by contacting me at banning.alexanderjames@gmail.com. Demo videos of each project being added soon.

# Screenshots:
<figure>
  <img width="600" alt="Create_Sphere" src="https://github.com/user-attachments/assets/a36e1fe0-781e-4bbc-9160-8e8e45370938" />
  <figcaption>Create Sphere function</figcaption>
</figure>

<figure>
  <img width="600" height="338" alt="Create_Cylinder" src="https://github.com/user-attachments/assets/aa1c81b4-f9d0-4049-bcd3-8ea10e7df2b1" />
  <figcaption>Create Cylinder function</figcaption>
</figure>

<figure>
  <img width="600" height="338" alt="Create_Cube" src="https://github.com/user-attachments/assets/89697415-81a6-4b95-b652-c7f3897a111d" />
  <figcaption>Create Cube function</figcaption>
</figure>

<figure>
  <img width="600" height="338" alt="CreationTarget" src="https://github.com/user-attachments/assets/5d93513d-1663-48e3-9107-5e3edccd7076" />
  <figcaption>CreationTarget functions - Move and Color</figcaption>
</figure>

<figure>
  <img width="600" height="338" alt="Freeze_All" src="https://github.com/user-attachments/assets/b42cb7c7-f1a4-4f14-98fc-bac7ffb199d7" />
  <figcaption>Freeze All Objects</figcaption>
</figure>

<figure>
  <img width="600" height="338" alt="Avatar" src="https://github.com/user-attachments/assets/b7010fb9-b9a8-4372-ac91-3562e91190cb" />
  <figcaption>Extra Credit - Avatar Elements</figcaption>
</figure>

### Code Release Restrictions
Because this is a University of Washington Bothell course, I cannot publicly release my code solutions to these problems. However, code samples may be sent by request for hiring purposes (e.g. reviewing my previous work as it relates to a software engineering job).

