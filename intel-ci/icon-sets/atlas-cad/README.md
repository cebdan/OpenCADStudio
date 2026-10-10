# Atlas CAD icon set

This is the standalone, canonical Atlas icon package used by OpenCADStudio.
It contains 16 production SVG icons for core CAD operations and is kept apart
from generic application chrome so it can be reused or exported intact.

## Visual system

- 24 × 24 artboard; neutral geometry is `#B4B6B9` and construction/action is
  `#6DB7ED`.
- `#E05050` is reserved for removed geometry in destructive operations.
- Main strokes are 1.75 px; construction-only detail is 1.2–1.25 px.
- Each icon depicts a CAD operation rather than a generic app metaphor.

The application’s semantic SVG renderer maps these palette tokens to the
active OpenCADStudio theme at runtime.
