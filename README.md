# CVL_Assignment01: Image Enhancement & Processing

This project implements various **Image Enhancement** techniques in Python to improve image quality under different distortion conditions, such as low-light, over-exposure, noise, blur, and low resolution.

---

### Objectives

The primary objectives of this assignment are:
* Implement and analyze spatial domain image enhancement algorithms.
* Evaluate the impact of different filters and adjustments on pixel intensity distributions using **Histograms**.
* Quantify image quality changes using **PSNR (Peak Signal-to-Noise Ratio)**.

---

### Methods Implemented

1. **Under-Exposure / Low-Light Enhancement:**
   * **Gamma Correction ($\gamma < 1$):** Non-linear transformation to brighten dark regions.
   * **CLAHE (Contrast Limited Adaptive Histogram Equalization):** Enhances local contrast while preventing over-amplification of noise.

2. **Over-Exposure Correction:**
   * **Gamma Correction ($\gamma > 1$):** Suppresses excessive brightness and restores details in washed-out areas.
   * **Linear Contrast Stretching:** Adjusts the dynamic range linearly.

3. **Noise Reduction & Smoothing:**
   * **Median Filtering:** Effective for removing *salt-and-pepper* noise while preserving edges.
   * **Gaussian Blur:** Reduces high-frequency noise and smooths over-sharpened textures.

4. **Sharpening & Detail Enhancement:**
   * **Laplacian Sharpening:** Highlights edges and fine details.
   * **Unsharp Masking:** Enhances edges precisely by subtracting a blurred version from the original.

5. **Resolution Upscaling:**
   * **Nearest Neighbor Interpolation:** Fast scaling with blocky artifacts.
   * **Bicubic Interpolation:** Smooth interpolation using cubic polynomials.

---

### Evaluation Metrics

The results are evaluated and compared using:
* **Visual Inspection:** Subjective comparison of structural details.
* **Color / Grayscale Histograms:** Analyzing the shift and spread of pixel intensity distributions.
* **PSNR (Peak Signal-to-Noise Ratio):** Measuring the structural distortion and fidelity relative to the reference/input image.
