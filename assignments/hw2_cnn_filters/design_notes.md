# Design Notes — HW2: CNN Filters

**Goal:** Build intuition for how classical image filters work before students encounter learned convolutional filters in CNNs.

**Structure:**
- First half is run-and-observe: students apply Sobel, Prewitt, Laplacian, Sharpen, Emboss, Box Blur, and Gaussian Blur filters to a sample image and compare outputs
- Second half asks analytical questions on why filters behave differently (edge sensitivity, noise sensitivity, directionality)
- Final two questions require students to design their own 3×3 kernels (diagonal edge detector, texture/line detector) — this pushes them from observation to construction

**Concepts targeted:**
- Edge detection vs. noise sensitivity trade-offs (Sobel vs. Prewitt)
- Second-derivative filters (Laplacian) vs. first-derivative filters
- Connecting hand-designed kernels to what a CNN learns automatically

**Assets:** Sample grayscale image(s) provided for students to run filters on; students can swap in their own image.
