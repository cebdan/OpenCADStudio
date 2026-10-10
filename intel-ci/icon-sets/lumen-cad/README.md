# Lumen CAD — glossy 3D icon set

Lumen CAD is the premium, material-driven alternative to the preserved
`atlas-cad` set. It is designed for OpenCADStudio's dark toolbars and follows
the supplied GraphCad visual direction without embedding the showcase cards.

## Material language

- Transparent 32 × 32 SVG masters, scaled by the UI to 18.2, 22, and 39 px.
- Upper-left studio lighting: cold chrome, sapphire glass, and crisp highlights
  sit above restrained navy geometric shadows.
- Blue marks selected/created CAD geometry; green indicates an operation's
  direction or target; red appears only in Trim for removed geometry.
- Each asset is self-contained SVG: vector paths, gradients, and manual shadow
  layers only. No raster images, scripts, external resources, or filters.

The palette deliberately avoids the semantic recolouring tokens used by
`src/ui/icons.rs`, retaining the designed multi-stop material gradients.

## Curve construction modes

Every curve dropdown item uses its own SVG master (20 total):

- Arcs: `arc-3p`, `arc-sce`, `arc-sca`, `arc-scl`, `arc-sea`, `arc-sed`,
  `arc-ser`, `arc-cse`, `arc-csa`, `arc-csl`, `arc-cont`.
- Circles: `circle-center-radius`, `circle-center-diameter`, `circle-two-point`,
  `circle-three-point`, `circle-tangent-tangent-radius`,
  `circle-tangent-tangent-tangent`.
- Ellipses: `ellipse-center-axes`, `ellipse-axis-end`, `ellipse-arc`.

Spherical nodes, center targets, dimension arrows, angle sweeps, and tangent
contacts distinguish the construction methods. The original `arc.svg` and
`circle.svg` remain available as generic masters; the curve dropdowns use the
individual variants above. All variants render at 18, 22, and 39 px.

## Additional editing tools

Ten further toolbar icons: `mirror`, `scale`, `stretch`, `offset`, `explode`,
`chamfer`, `extend`, `array-rect`, `array-polar`, and `array-path`.
These replace the legacy assets in the editing commands and array dropdown.
Linear gradients use canvas coordinates so axis-aligned guides retain their
material highlights. Each icon is checked at 18, 22, and 39 px.
