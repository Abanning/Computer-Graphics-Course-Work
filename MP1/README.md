# Assignment Specification

# MP1: Orientation and Weekend Entertainment

> **Due:** Refer to the course website

---

## Objective

Familiarize with **Unity**, the learning tool used throughout this course. This assignment also serves to:

- Evaluate comfort level with the kind of self-directed learning expected — specifically, learning *as little as possible about Unity* to accomplish each task (not "learning Unity to build a game").
- Ensure understanding of what is involved in submitting a programming assignment.

⏱️ **Estimated time:** No more than 5–6 hours. Most of that time should be spent asking and searching for answers to *"how do I make Unity do …"*

---

## Approach

Refer to the instructor's reference solution (WebGL build — click and run).

### Initial Scene Objects

**CreationPlane** — a Quad with:
- Position: `(0, 0, 0)`
- Rotation: `(90, 0, 0)` — orients the Quad on the x/z plane
- Scale: `(14, 14, 14)` — corners span from **–7 to +7**

> If using a `Plane` instead of a `Quad`, transform settings will differ, but the final size and location must match the above.

**CreationTarget** — a Sphere with:
- Position: user-defined
- Rotation: `(0, 0, 0)`
- Scale: `(0.5, 0.5, 0.5)`
- Color: **black**

---

## Primitive Types

A radio button system allows the user to select and create one of three primitive types. Specifications for each:

### 🔵 Sphere
| Property | Value |
|---|---|
| Scale | `(0.5, 1, 1)` |
| Speed | 1 unit/sec along the **Y-axis** |
| Rotation | 45°/sec about the Y-axis |
| Range | `0 < y < 5` |
| Color (+Y) | `(1, 1, 1)` — White |
| Color (−Y) | `(1, 0, 1)` — Magenta |

> Scale is non-uniform so rotation is observable.

### 🟡 Cylinder
| Property | Value |
|---|---|
| Scale | `(0.5, 1, 1)` |
| Speed | 1.5 units/sec along the **Z-axis** |
| Rotation | 90°/sec about the Y-axis |
| Range | `0 < z < 5` |
| Color (+Z) | `(1, 1, 1)` — White |
| Color (−Z) | `(0, 1, 1)` — Cyan |

> Scale is non-uniform so rotation is observable.

### 🟥 Cube
| Property | Value |
|---|---|
| Scale | `(1, 1, 1)` |
| Speed | 2 units/sec along the **X-axis** |
| Rotation | 135°/sec about the Y-axis |
| Range | `0 < x < 5` |
| Color (+X) | `(1, 1, 1)` — White |
| Color (−X) | `(1, 1, 0)` — Yellow |

---

## Behaviors

### 1. Primitive Creation (Radio Buttons)
- Clicking a primitive type creates a new primitive at the **CreationTarget** position and keeps the radio button checked.
- Clicking the **same** primitive type a second time **unchecks** it — no new primitive is created.
- Deleting a primitive must uncheck all radio buttons.
- A newly created shape must rest on the CreationPlane and immediately begin traveling per its spec. If the creation position exceeds the valid range of 5, the shape begins traveling in the **negative** direction. After the first direction change, the shape must **never** leave the `0–5` range.

### 2. CreationTarget Manipulation
- **LMB** on the CreationPlane (not over any other object) moves the CreationTarget to the clicked position.
- The CreationTarget must always be **entirely above** the CreationPlane.

### 3. Object Deletion
- **LMB** on a created primitive deletes it.
- The **CreationPlane** and **CreationTarget** can **never** be deleted.

---

## Hints

1. **Camera:** Place MainCamera at position `(0, 8, -16)`, rotation `(23, 0, 0)`, FOV `45`.
   - Tip: Select the camera in the Hierarchy, then `RMB → Align With View`.
2. **Radio buttons:** Use `Toggle` and `ToggleGroup`. To add a ToggleGroup: select the GameObject → Inspector → `Add Component → UI`.
3. **Per-second movement:** Search *"unity elapsed time"* and look into [`Time.deltaTime`](https://docs.unity3d.com/ScriptReference/Time-deltaTime.html).
4. **Layer-based raycasting:** Place the CreationTarget sphere on a separate Layer. Use `Raycast(ray, hitInfo, layer-1)` (the default layer) to select only the floor or created objects — not the CreationTarget.
   - If the click hits the floor, move the CreationTarget to `(x, someValue, z)` from the hit point.
   - Search *"unity layer"* to learn more.
5. **Rotation:** Use `Rotate(Axis, degree)` to rotate a GameObject.

---

## Credit Distribution

| # | Category | Points |
|---|---|---|
| 1 | **Initial Frame** — CreationPlane and CreationTarget | 5% |
| | Correct size/color for both | +5% |
| | Both fully visible from runtime camera | +5% |
| | ❌ CreationPlane not fully visible at 1920×1080 | −50% |
| 2 | **CreationTarget Interaction** | 20% |
| | Proper LMB placement anywhere on the CreationPlane | +10% |
| | Sphere always drawn above CreationPlane | +5% |
| | Can never delete CreationTarget | +10% |
| 3 | **Primitive Radio Button Support** | 20% |
| | None checked initially | +5% |
| | Only creates when checking (unchecking does not create) | +5% |
| | Checking creates a primitive at CreationTarget | +10% |
| | None checked after deleting a primitive | +10% |
| 4 | **Primitive Appearance & Behavior** | 25% |
| | Created at CreationTarget, entirely above the CreationPlane | +5% |
| | Proper color changes (white when moving in positive direction) | +5% |
| | Correct speed & rotation: Sphere/Y/slow, Cylinder/Z/faster, Cube/X/fastest | +15% |
| | Movement always stays within range `0–5` | +10% |
| 5 | **Click to Delete** | 15% |
| | Correct deletion of clicked primitive | +10% |
| | Deletion does not move the CreationTarget | +10% |
| | Cannot delete the CreationPlane or CreationTarget | +10% |
| 6 | **Slider Support** *(CSS551 required / CSS451 extra credit)* | 10% |
| | 3 slider bars controlling the RGB channels of the CreationTarget | +10% |
| 7 | **Submission** | 15% |
| | All source code + EXE folder zipped | +10% |
| | Zip file named `FirstLastNameMP1.zip` | +10% |
| | EXE runs as a resizable window (not fullscreen) | +10% |

**Grading basis:**
- CSS551: Grade based on 110 points converted to a percentage.
- CSS451: Grade based on 100 points; slider bars count toward extra credit.

---

## Submission

- **Source code:** The `Assets` folder only.
- **Executable:** Include a separate `EXE` folder; build the executable into it.
  - `Build → Player Settings`
    - Fullscreen Mode: `Windowed`
    - Resolution: `1920×1080`
    - Resizable Window: ✅ **Checked**

---

## Extra Credit

Up to **10 points** of extra credit for any working experiment or additional feature. Be creative — more interesting ideas are valued over "more of the same."

**Less interesting (avoid):**
- Adding more primitive types — we already know how to do this.
- Making the CreationTarget more visually appealing — same concept, different asset.

**More interesting ideas:**
- Create a composite object (e.g., a car) instead of a single primitive.
- Support multiple CreationPlanes in different dimensions.
- Global behavior control: a button to stop/start all movement.
- Individual object control: stop/start movement per object.
- Customizable movement parameters per object.
- Leverage Unity's Scene support to create separate scenes for different test cases.

> There are 100 million different things you can do. 🚀

---

> ⚠️ **This is due next week.** MP2 arrives the following week. Start early — do not fall behind. It is difficult to catch up.
