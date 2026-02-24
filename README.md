# 2D/3D House Designer – Concept Application (easy-home-planer)

## Overview

**2D/3D House Designer** is a browser-based architectural concept tool for creating technical building layouts.  
It allows users to draw and manage walls and building installations (water, electrical, ventilation) in a scalable 2D workspace with basic 3D (Z-axis) height parameters.

The application works on a centimeter scale:

> **Scale: 1 pixel = 1 cm**

It supports precise drawing, element editing, layer management, measurements, image overlays, and project export/import in JSON format.

---

# Main Features

## 1. Layer-Based Drawing System

You can draw elements on separate technical layers:

- **Walls (Construction)**
- **Water / Plumbing**
- **Electrical**
- **Ventilation**
- **Images (reference layer)**

Each layer:
- Has its own color
- Can be shown/hidden independently
- Is included in automatic length summaries

---

## 2. Drawing Mode

- Draw connected line segments (click → click).
- Continuous drawing: each new segment starts where the previous one ended.
- Adjustable thickness (diameter in cm).
- Supports Z-axis values (height start and end).

### Smart Input
- Type numbers while drawing to set exact length.
- Press **Enter** to confirm.
- Add **m** to enter meters (e.g., `2.5m` → 250 cm).

### Shift Constraint
- Hold **Shift** while drawing to lock to horizontal or vertical direction.

---

## 3. Selection & Editing Mode

Switch to selection mode to:

- Select elements
- Drag elements
- Modify:
  - X1, Y1, X2, Y2
  - Z1 and height (ΔZ auto-calculates Z2)
  - Thickness
  - Name
  - Total length

### Live Editing
- Drag elements with the mouse.
- Use arrow keys for precise movement:
  - 1 cm step
  - 10 cm step with Shift

---

## 4. Image Support

You can insert reference images (e.g., floor plans, sketches).

Image tools include:

- Drag to move
- Resize (bottom-right handle)
- Hold **Shift** to keep proportions
- Hold **Alt** + drag to rotate
- Flip horizontally (X)
- Flip vertically (Y)
- Adjust:
  - Width & height
  - Rotation
  - Z1 / Z2
  - Position

Images are saved as Base64 inside the project file.

---

## 5. Measurement Tool

Activate temporary measurement mode:

- Hold **CTRL + Click** on a line.
- Move the mouse to measure from the element edge.
- Press **Q** to switch orientation:
  - Perpendicular
  - Parallel

Measurement is displayed in centimeters.

---

## 6. Zoom & Navigation

Zoom methods:
- Slider (10% – 400%)
- **CTRL + Mouse Wheel**
- Reset View button

Zoom is smooth and scale-aware (line widths and UI adjust visually).

---

## 7. Length Summary (Per Layer)

Automatically calculates:

For each layer:
- Total XY length (horizontal projection)
- Total Z length (vertical elevation)

Displayed in centimeters.

This is useful for:
- Installation estimation
- Cable/pipe calculation
- Structural measurement

---

## 8. Undo System

- Supports history stack (up to 50 steps).
- Undo restores:
  - Elements
  - Images
  - Modifications

---

## 9. Save & Load Projects

Projects are saved as `.json` files including:

- All elements
- Z parameters
- Images (embedded Base64)
- Transformations (rotation, flip, scale)

Supports backward compatibility with older file formats.

---

# Keyboard Shortcuts

| Key | Function |
|------|----------|
| **S** | Toggle Selection / Drawing mode |
| **Delete** | Delete selected element/image |
| **Arrow Keys** | Move selected element (1 cm) |
| **Shift + Arrows** | Move 10 cm |
| **Shift (drawing)** | Lock to vertical/horizontal |
| **ESC** | Cancel drawing |
| **Enter** | Confirm typed length |
| **Backspace** | Delete typed length character |
| **CTRL + Click** | Start measurement |
| **Q** | Toggle measurement orientation |
| **X** | Flip selected image horizontally |
| **Y** | Flip selected image vertically |
| **ALT + Drag (image)** | Rotate image |
| **CTRL + Mouse Wheel** | Zoom |

---

# Technical Characteristics

- Pure HTML5 Canvas application
- No external libraries
- Large workspace (5000 × 5000 px)
- Real-world centimeter-based precision
- Grid background (20 cm spacing)

---

# Intended Use Cases

- Concept house planning
- Installation layout design
- Plumbing / electrical routing
- Renovation planning
- Technical measurement estimation
- Floor plan tracing over imported images

# Preview
<img src="example SS.png">

# Created with Google Gemini and ChatGPT