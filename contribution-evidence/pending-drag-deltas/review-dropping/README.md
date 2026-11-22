# Pending external dropping review regression

On published head 76ee76f, dragover positions 1, 2, then 9 CSS pixels from the start move the dropping item 12 pixels. The repair supplies consecutive synthetic deltas so the result is 9 pixels. Four new browser cases (Chromium/Firefox, transform/absolute positioning) fail before and pass after; six existing native mouse cases remain passing.

These are unmodified browser screenshots with real layout, driven by synthetic DOM dragover events. They do not claim OS drag-and-drop or touch/WebKit coverage. Three unit regressions also fail before and pass after at scales 0.5/1/2. Prepared with AI assistance.
