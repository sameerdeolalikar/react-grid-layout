# Pending drag movement

Native Chromium and Firefox screenshots from the same mouse sequence on current upstream ec4ab79 (before) and the pending-delta fix (after). No synthetic DOM geometry is used in these browser checks.

Starting from a fresh drag, pointer displacements are (1,1), (0,0), (2,1), then (9,4) CSS pixels. The first three moves stay below the default 3px threshold. Before: the item moves only (7,3). After: it moves (9,4), retaining the grabbed point. This holds for ordinary transform, absolute, and scale 0.5 positioning; repeated reverse gestures also pass after the fix. Screenshots show the first threshold-crossing move. `none` is ordinary transform positioning; `scaled` is scale 0.5. The small two-pixel error is verified numerically by the committed Playwright regression.

Six browser cases fail before and pass after. Screenshots are unmodified browser captures. WebKit/mobile were not run. Prepared with AI assistance.
