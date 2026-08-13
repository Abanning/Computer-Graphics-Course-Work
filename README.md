# Advanced 3D Computer Graphics & Rendering

**Author:** Alex Banning  
**Institution:** University of Washington Bothell  
**Course:** CSS 551 (Advanced 3D Computer Graphics)

---

## Overview

This repository contains a progressive series of Machine Problems (MPs) that explore the mathematical, theoretical, and architectural foundations of 3D computer graphics. Built within the Unity engine using C#, these projects intentionally bypass much of Unity's built-in physics and default transform pipelines. Instead, they focus on custom, CPU-based implementations of vector mathematics, hierarchical scene graphs, and explicit matrix transformations.

## Repository Structure

Each subfolder represents a standalone Unity project and contains its own detailed `README.md` with specific implementation notes, alongside pre-compiled executable builds for both macOS and Windows.

*   **`MP1/` - Orientation and Weekend Entertainment**  
    An interactive introduction to the graphics environment, featuring user-controlled spawning of autonomous geometric primitives (Spheres, Cylinders, Cubes) with continuous dynamic runtime behaviors and bounding constraints.

*   **`MP2/` - User Interaction and Simple MVC**  
    Implementation of a Model-View-Controller (MVC) architecture for a 3D scene editor. Features include raycast-based object selection, custom RGB axis frames, and continuous UI-driven slider controls for Translation, Scaling, and Quaternion-based Rotation.

*   **`MP3/` - Fun with Vectors and Abstraction**  
    A vector mathematics simulation that renders dynamic line segments and traveling entities within a bounded 3D world space. Relies on object-oriented abstraction and precise raycast layer masking for user interactions.

*   **`MP3a/` - Vector Applications in Interactions**  
    An extension of MP3 introducing planar intersections. Features advanced vector physics including surface normals, dynamic front-facing collision reflections, and mathematical shadow projections onto arbitrary user-controlled planes.

*   **`MP4/` - Scene Nodes and Scene Graph**  
    A custom hierarchical Scene Graph implementation. Demonstrates complex pivoted transformations across a multi-generational articulated model. Uses custom shaders to enforce explicit, script-calculated Model-View matrix multiplication.

*   **`MP5/` - Camera View and Manipulation**  
    A comprehensive camera control suite featuring orbital manipulation (Tumble, Track, Dolly) centered around a LookAt point. Includes a dynamically attachable Picture-in-Picture (PiP) viewport camera that tracks the accumulated world transformations of moving hierarchy nodes.

*   **`MP6/` - Simple Modeling Editor**  
    An interactive 3D modeling and texture-mapping environment. Features CPU-based procedural mesh generation (planar and swept cylinders), direct 3D vertex manipulation, and a custom 2D affine transformation pipeline (`Matrix3x3`) for real-time UV texture mapping.

---

## Technology Stack & Core Concepts
*   **Environment:** Unity 3D
*   **Language:** C#
*   **Key Paradigms:** 
    *   Linear Algebra & Quaternion Mathematics
    *   Custom Transform Hierarchies & Scene Graphs
    *   Procedural Mesh Generation
    *   Model-View-Controller (MVC) Architecture
    *   Direct Matrix Manipulation & Custom Shaders
 

Code samples can be released by request due to protected intellectual property of the University of Washington and its professors/faculty.
