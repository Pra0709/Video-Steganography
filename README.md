# Video-in-Video Steganography using OpenCV

## Overview

This project implements a simple video steganography technique that hides one video (secret video) inside another video (cover video) using alpha blending.

The project contains two modules:

1. **Embedding Module**
   - Embeds a secret video into a cover video.
   - Produces a stego video.
   - Calculates quality metrics such as MSE, PSNR, and SSIM.

2. **Extraction Module**
   - Extracts the hidden video from the stego video.
   - Uses the original cover video for recovery.

---

## Features

- Hide one video inside another
- Recover hidden video
- Automatic frame resizing
- Automatic looping of secret video if shorter
- Frame-by-frame processing
- Performance measurement
- Error analysis
- Quality metrics
  - MSE
  - PSNR
  - SSIM

---

## Project Structure

```
Video-Steganography/
│
├── embed.py
├── extract.py
├── cover.mp4
├── secret.mp4
├── stego.avi
├── extracted_secret.avi
├── requirements.txt
├── README.md
└── USER_MANUAL.md
```

---

## Algorithm

### Embedding

For every frame,

```
Stego Frame = Cover Frame + α × Secret Frame
```

where

- α = Embedding strength
- Smaller α → Better invisibility
- Larger α → Better extraction quality

---

### Extraction

```
Secret Frame = (Stego Frame − Cover Frame) / α
```

---

## Requirements

- Python 3.8+
- OpenCV
- NumPy
- scikit-image

Install dependencies

```bash
pip install -r requirements.txt
```

---

## Input Files

Place the following files in the project directory.

```
cover.mp4
secret.mp4
```

---

## Running Embedding

```bash
python embed.py
```

Output

```
stego.avi
```

---

## Running Extraction

```bash
python extract.py
```

Output

```
extracted_secret.avi
```

---

## Quality Metrics

The embedding program computes:

### Mean Squared Error (MSE)

Measures pixel-wise distortion.

Lower is better.

---

### Peak Signal-to-Noise Ratio (PSNR)

Measures image quality.

Typical values:

- >40 dB : Excellent
- 30–40 dB : Good
- <30 dB : Noticeable distortion

---

### Structural Similarity Index (SSIM)

Measures perceptual similarity.

Range:

0 – 1

1 indicates identical images.

---

## Performance Metrics

The embedding module reports

- Total processing time
- Frame processing time
- Frames per second
- Total processed frames
- Number of resized frames
- Secret frame reuse count

---

## Advantages

- Simple implementation
- Fast processing
- Easy to understand
- Lightweight
- Suitable for educational purposes

---

## Limitations

- Requires original cover video for extraction.
- Compression may reduce extraction quality.
- Not suitable for secure communication.
- No encryption is applied.

---

## Future Improvements

- AES encryption
- Frequency-domain embedding (DCT/DWT)
- Blind extraction
- Deep learning-based steganography
- Audio embedding
- Adaptive alpha selection

---

## Author

Praveen Singh

B.Tech CSE (Cyber Security & Digital Forensics)

VIT Bhopal University
