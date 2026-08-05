### MP3a: Vector Applications in Interactions
# Overview:
An extension to MP3 that introduces TheBarrier—a user-controlled planar surface with an active circular intersection region (represented by a flattened sphere)—to implement advanced vector projections, shadows, and geometric reflections. Features include:  

TheBarrier & GUI Two-Way Binding: Users can spawn instances of TheBarrier by clicking on the Floor. Clicking within the active region binds the barrier to the BarrierControl GUI, allowing real-time adjustments of its position and rotation. The barrier always renders a visible normal vector line segment.  

Traveling Ball Shadow Projection: When a TravelingBall is in front of TheBarrier and its projected coordinates fall within the active region, a black flattened shadow sphere is rendered on the plane surface. A thin black line segment (0.02 width) connects the ball to its shadow.  

Front-Facing Reflection: If a TravelingBall collides with TheBarrier from the front, its velocity vector reflects across the surface normal. Balls approaching from the rear pass through unaffected.  

AimLine & BigLine Intersections: When an AimLine intersects the active region of TheBarrier from the front, its reflected path is calculated and displayed as a separate green line segment of identical length. Additionally, TravelingBalls project white shadow markers and reflecting paths onto nearby BigLines when passing within a 10-unit perpendicular threshold.
