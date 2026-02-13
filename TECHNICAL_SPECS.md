# EasyPocket Technical Drawings & Specifications

## Front View
```
┌─────────────────────────────────┐
│                                 │  ← Top edge (rounded 2mm radius)
│        CARD POCKET              │
│      ┌───────────────┐          │
│      │               │          │  60mm width
│      │    CARD 1     │          │
│      │    CARD 2     │          │
│      │               │          │  90mm height
│      └───────────────┘          │
│                                 │
│    [CASH COMPARTMENT FLAP]      │
│                                 │
└─────────────────────────────────┘
         Bottom edge
```

## Side View (Cross-section)
```
Phone Surface
     ║
     ║  [Adhesive Layer] 0.5mm
     ║══════════════════════════
     ║  [Main Body Wall] 1.5mm
     ║─────────────────────────┐
     ║                          │
     ║  Card Storage Space      │  8-12mm depth
     ║  (Internal cavity)       │
     ║                          │
     ║─────────────────────────┘
     ║  [Outer Wall] 1.5mm
```

## Top View
```
┌─────────────────────────────────┐
│  ┌─────────────────────────┐   │
│  │   Card Slot Opening     │   │  55mm opening
│  │   (slightly tapered)    │   │
│  └─────────────────────────┘   │
│                                 │  60mm total width
│  ================================ │  Cash compartment divider
│         Cash area               │
└─────────────────────────────────┘
```

## Detailed Dimensions

### Main Body
- Overall Height: 90mm ± 1mm
- Overall Width: 60mm ± 1mm
- Base Depth: 8mm (minimum)
- Maximum Depth: 12mm (at capacity)
- Corner Radius: 2mm
- Edge Thickness: 1.5mm

### Card Pocket
- Pocket Height: 85mm (internal)
- Pocket Width: 55mm (opening), 54mm (bottom)
- Pocket Depth: 6mm (internal)
- Taper Angle: 1° (for easy removal)
- Opening Lip Height: 3mm

### Cash Compartment
- Compartment Height: 40mm
- Compartment Width: 58mm (internal)
- Compartment Depth: 4mm
- Flap Overlap: 5mm
- Flap Thickness: 1mm

### Attachment Area
- Adhesive Panel: 50mm x 30mm
- Positioned: 15mm from top, centered horizontally
- Surface Texture: Smooth (for optimal adhesion)

## Material Specifications

### TPU Properties
- Tensile Strength: 26-40 MPa
- Elongation at Break: 400-600%
- Hardness: Shore A 60-70
- Temperature Range: -30°C to 80°C
- Flexibility: Medium (maintains shape but flexes for insertion)

### Adhesive Specifications
- Type: 3M VHB (Very High Bond) or equivalent
- Thickness: 0.5mm
- Adhesion: >1000 g/25mm
- Removable: Yes (with minimal residue)
- Surface: Compatible with silicone, plastic, metal

## Tolerances
- Critical dimensions (card slot): ±0.5mm
- Non-critical dimensions: ±1mm
- Wall thickness: ±0.2mm
- Surface finish: Ra 3.2 μm (standard 3D print)

## Assembly Points

### 3D Printing Settings
```
Layer Height:        0.2mm
Wall Thickness:      3 layers (1.2mm)
Top/Bottom Layers:   4 layers
Infill Density:      20%
Infill Pattern:      Gyroid or Grid
Print Speed:         30mm/s (TPU)
Bed Temperature:     60°C
Nozzle Temperature:  220-230°C
Cooling:             Minimal (20%)
Retraction:          2mm at 25mm/s
```

### Support Structures
- Only needed for cash flap overhang
- Use tree supports for easy removal
- Interface layers: 2
- Interface density: 80%

## Critical Design Features

### Card Retention Mechanism
```
Side view of card slot:
    
    ║ \  ← 1° taper for easy insertion
    ║  \
    ║   [CARD]
    ║  /
    ║ /  ← Friction points (textured surface)
    ║
```

### Cash Flap Design
```
Front view:
┌─────────────┐
│             │  ← Flap body (flexible)
│   ┌─────┐   │
│   │ [F] │   │  ← Fold line/hinge point
└───┴─────┴───┘
    │     │
    └─────┘      ← Tuck-under edge
```

## Weight Distribution
- Main body: 15g
- Adhesive: 2g
- Empty total: 17g
- With 3 cards: 22g
- With cards + cash: 25g
- Maximum recommended: 30g

## Center of Gravity
- Position: 45mm from top, 30mm from left edge
- With cards: Shifts down 5mm
- Ensure weight doesn't pull phone sideways

## Surface Treatments

### Interior (Card/Cash Contact)
- Texture: Smooth
- Purpose: Prevent card damage, easy sliding
- Post-processing: Light sanding if needed

### Exterior
- Texture: Matte finish
- Purpose: Grip, aesthetic
- Treatment: As-printed or light texture spray

### Attachment Surface
- Texture: Perfectly smooth
- Purpose: Maximum adhesive contact
- Treatment: Polish if necessary

## Optional Enhancements (V1.1+)

### RFID Blocking Layer
- Material: Thin aluminum sheet or RFID-blocking fabric
- Thickness: 0.1mm
- Position: Between card slot walls
- Weight impact: +3g

### Magnetic Closure
- Type: Small neodymium magnets (5mm x 1mm)
- Position: Flap corners
- Quantity: 2 magnets
- Polarity: Attracting configuration

## Testing Points
Mark these areas for stress testing:
1. Card pocket opening (most stressed)
2. Cash flap hinge point
3. Adhesive attachment corners
4. Bottom corners (impact points)

## Quality Control Checklist
- [ ] All dimensions within tolerance
- [ ] No sharp edges or burrs
- [ ] Smooth card insertion/removal
- [ ] Adhesive properly centered
- [ ] Material flexibility adequate
- [ ] Print quality acceptable (no gaps/holes)
- [ ] Color consistent (if applicable)
- [ ] Markings/logos clear (if included)

## Scale Reference
```
Standard Credit Card: 85.60 × 53.98 × 0.76 mm
US Dollar Bill: 156 × 66 mm (folded to ~52 × 66 mm)
Typical Phone: 140-160mm height × 70-80mm width
```

---
*Drawing Version: 1.0*
*Date: 2025-11-18*
*Units: All dimensions in millimeters unless otherwise noted*
