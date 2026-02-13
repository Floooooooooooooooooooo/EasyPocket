# EasyPocket - 3D Model Specification (CAD Guide)

## Overview
This document provides detailed specifications for creating a 3D CAD model of the EasyPocket prototype V1. Use this with software like Fusion 360, Tinkercad, FreeCAD, or Blender.

## Model Structure

### Component Breakdown
1. **Main Body** - Single unified shell
2. **Card Pocket** - Internal cavity
3. **Cash Compartment** - Separate chamber with flap
4. **Attachment Surface** - Flat back panel
5. **Optional Features** - Engravings, logos

## Step-by-Step Modeling Guide

### Step 1: Create Base Body
```
1. Create sketch on XY plane
2. Draw rectangle: 60mm (width) × 90mm (height)
3. Fillet all corners with 2mm radius
4. Extrude: 8mm (base depth)
5. Shell operation: 1.5mm wall thickness
   - Leave bottom (attachment side) open initially
```

### Step 2: Create Card Pocket
```
1. Create sketch on front face
2. Position: 5mm from top, centered horizontally
3. Draw rectangle: 54mm (width) × 85mm (height)
4. Extrude cut: 6mm depth into body
5. Add 1° draft angle (wider at top)
6. Fillet top edges: 1mm radius for comfort
```

### Step 3: Create Card Slot Opening
```
1. Sketch on top face of card pocket
2. Opening size: 55mm × 3mm (width × height)
3. Chamfer inside edges: 0.5mm × 45°
4. Ensure smooth transition into pocket
```

### Step 4: Create Cash Compartment
```
1. Sketch on front face below card pocket
2. Position: Start at 70mm from top
3. Draw rectangle: 58mm × 40mm
4. Extrude cut: 4mm depth
5. Leave 3mm spacing from card pocket
```

### Step 5: Create Cash Flap
```
1. Sketch on top edge of cash compartment
2. Rectangle: 58mm × 25mm
3. Extrude: 1mm thickness
4. Add living hinge at base: 0.5mm thickness × 3mm length
5. Curve flap slightly (radius: 100mm) for natural fold
```

### Step 6: Create Attachment Surface
```
1. Fill/close the bottom (back) of main body
2. Ensure flat surface (no texture)
3. Measure and mark adhesive area:
   - 50mm × 30mm
   - Centered horizontally
   - 15mm from top edge
4. Optional: Create shallow recess (0.1mm) for adhesive
```

### Step 7: Add Details
```
1. Brand name/logo (optional):
   - Position: Bottom front, 5mm from edge
   - Method: Emboss or deboss 0.3mm
   - Font: Sans-serif, 4mm height

2. Texture (optional):
   - External surfaces only
   - Diamond knurl or dots pattern
   - Depth: 0.2mm
   - Spacing: 2mm

3. Ventilation holes (optional):
   - If moisture concern exists
   - Diameter: 1mm
   - Quantity: 4-6 holes
   - Position: Bottom corners of compartments
```

### Step 8: Final Refinements
```
1. Fillet all internal edges: 0.5mm radius
2. Check wall thickness everywhere: Minimum 1.2mm
3. Verify draft angles for card pocket: 1°
4. Ensure no overhangs >45° (except cash flap)
5. Add chamfers to external corners: 0.3mm
```

## Parametric Design Variables

### Key Parameters to Define
```
// Main dimensions
body_height = 90;        // mm
body_width = 60;         // mm
body_depth = 8;          // mm
wall_thickness = 1.5;    // mm
corner_radius = 2;       // mm

// Card pocket
card_pocket_width = 54;  // mm (bottom)
card_pocket_height = 85; // mm
card_pocket_depth = 6;   // mm
card_opening_width = 55; // mm
card_draft_angle = 1;    // degrees

// Cash compartment
cash_width = 58;         // mm
cash_height = 40;        // mm
cash_depth = 4;          // mm
flap_height = 25;        // mm
flap_thickness = 1;      // mm
hinge_thickness = 0.5;   // mm

// Attachment
adhesive_width = 50;     // mm
adhesive_height = 30;    // mm
adhesive_position_top = 15; // mm

// Fillets and chamfers
edge_fillet = 1;         // mm
internal_fillet = 0.5;   // mm
comfort_fillet = 1;      // mm
```

## Export Settings

### For 3D Printing (STL Export)
```
Format: STL (binary)
Units: Millimeters
Resolution: High
  - Chord tolerance: 0.01mm
  - Angle tolerance: 15°
Orientation: Back face (attachment side) down on build plate
```

### For Visualization (OBJ/FBX Export)
```
Format: OBJ or FBX
Include textures: Yes
Include normals: Yes
Include UV mapping: Yes
Scale: 1:1
```

## File Naming Convention
```
EasyPocket_V1_Main.stl           // Primary print file
EasyPocket_V1_Main_Mirror.stl    // If making left/right versions
EasyPocket_V1_Flat_Pattern.dxf   // For hand-cutting
EasyPocket_V1_Assembly.step      // Full CAD assembly
```

## CAD Software Recommendations

### Beginner-Friendly
**Tinkercad** (Web-based, free)
- Pros: Very simple, great for basic shapes
- Cons: Limited advanced features
- Best for: Quick prototypes, learning

### Intermediate
**Fusion 360** (Free for personal use)
- Pros: Parametric, professional features
- Cons: Learning curve
- Best for: Precise engineering, iterations

**FreeCAD** (Free, open source)
- Pros: Powerful, customizable
- Cons: Interface can be complex
- Best for: Budget-conscious, Linux users

### Advanced
**SolidWorks** (Professional, paid)
- Pros: Industry standard, powerful
- Cons: Expensive, Windows only
- Best for: Professional development

**Rhino 3D** (Professional, paid)
- Pros: Excellent for organic shapes
- Cons: Cost, learning curve
- Best for: Complex surface modeling

## Modeling Tips

### For Flexible Materials (TPU)
1. Avoid thin, unsupported sections (<1mm)
2. Add fillets to reduce stress concentration
3. Design with flex in mind (living hinges)
4. Test wall thickness for desired flexibility
5. Consider print orientation for layer strength

### For Structural Integrity
1. Ensure uniform wall thickness
2. Add ribs for reinforcement if needed
3. Round internal corners (stress relief)
4. Test that no section is too thin (<1mm)
5. Check overhang angles (<45° needs support)

### For Printability
1. Minimize support requirements
2. Orient longest dimension along Z-axis for strength
3. Check that all surfaces can be reached by nozzle
4. Consider split models if size is too large
5. Add registration features if printing in parts

## Quality Checks

### Before Export
- [ ] All dimensions match specifications
- [ ] No thin walls (<1mm)
- [ ] All edges properly filleted
- [ ] No self-intersecting geometry
- [ ] No naked/open edges (unless intentional)
- [ ] Model is manifold (watertight)
- [ ] Proper scale (measure a known dimension)
- [ ] Orientation correct for printing

### STL File Validation
- [ ] No errors in mesh
- [ ] Normal directions consistent
- [ ] No holes or gaps
- [ ] File size reasonable (<10MB for this part)
- [ ] Preview in slicer software looks correct

## Alternative: Flat Pattern for Hand-Cutting

If creating a flat pattern for fabric/leather:

```
1. Unfold 3D model to 2D pattern
2. Add 5mm seam allowance on all edges
3. Mark fold lines with dashed lines
4. Add alignment notches
5. Label each piece
6. Export as DXF or PDF
7. Scale to 1:1 for printing
```

### Pattern Pieces Needed
- Main body: 90mm × 60mm
- Card pocket front: 85mm × 55mm
- Card pocket back: 85mm × 55mm
- Cash pocket: 60mm × 40mm
- Cash flap: 60mm × 25mm
- Attachment backing: 50mm × 30mm

## Rendering for Presentation

Optional: Create photorealistic renders
```
1. Apply TPU material (matte black rubber)
2. Add environment lighting
3. Place sample cards in pocket
4. Render at 1920×1080 or higher
5. Create multiple angles:
   - Front view
   - Isometric view
   - With phone mockup
   - Detail of card insertion
```

## Version Control
- Save incremental versions (V1.0, V1.1, V1.2)
- Export STL after each major change
- Keep source CAD files organized
- Document changes in commit messages or log

---
*CAD Specification Version: 1.0*
*Last Updated: 2025-11-18*
*Compatible with: Fusion 360, FreeCAD, SolidWorks, Tinkercad*
