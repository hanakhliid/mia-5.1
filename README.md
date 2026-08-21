# mia-5.1
# Phase II - Task 5.1: Signal Filtering & Classical Computer Vision

## Project Overview
This repository contains solutions for Task 5.1 of MIA Phase II, covering audio signal denoising and classical computer vision-based object detection using OpenCV.

---

## Task 1.1: Audio Denoising & Feature Isolation
- **Objective:** Filter heavy background noise from an audio sample (`task5_1.wav`) to extract the spoken word.
- **Methodology:** Applied **Spectral Subtraction** via Short-Time Fourier Transform (STFT) using `librosa` to profile noise power from initial silent frames and subtract it, followed by signal normalization.
- **Output:** Extracted clear audio saved as `cleaned_audio.wav`.

---

## Task 1.2: Ball Detection & Bounding Box Labeling
- **Objective:** Detect red and blue balls across 20 dataset images and generate YOLO-formatted annotation files (`.txt`).
- **Methodology:**
  - Converted RGB images to **HSV color space**.
  - Defined HSV thresholds for **Blue (Class 0)** and **Red (Class 1)**.
  - Applied Gaussian blurring and morphological operations (`MORPH_OPEN`) to clear noise.
  - Extracted contours and normalized bounding box coordinates (`x_center`, `y_center`, `width`, `height`).
- **Output:** 20 label files generated in the `labels/` directory.
