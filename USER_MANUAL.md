# USER MANUAL

# Video-in-Video Steganography System

---

## 1. Introduction

This software hides a secret video inside another video using alpha blending.

The system consists of two modules:

- Video Embedding
- Video Extraction

---

## 2. Software Requirements

Python 3.8 or later

Required libraries

- OpenCV
- NumPy
- scikit-image

Install them using

```bash
pip install -r requirements.txt
```

---

## 3. Hardware Requirements

Minimum

- Intel i3 Processor
- 4 GB RAM
- 500 MB free storage

Recommended

- Intel i5/i7
- 8 GB RAM
- SSD

---

## 4. Input Files

Place these files in the project folder.

```
cover.mp4
secret.mp4
```

---

## 5. Embedding Process

Run

```bash
python embed.py
```

The software will

- Read cover video
- Read secret video
- Resize frames if necessary
- Blend the videos
- Save stego video
- Calculate quality metrics

Output

```
stego.avi
```

---

## 6. Extraction Process

Run

```bash
python extract.py
```

The software will

- Read stego video
- Read original cover video
- Recover secret video
- Save extracted video

Output

```
extracted_secret.avi
```

---

## 7. Parameter

### Alpha

```
alpha = 0.04
```

Meaning

Small alpha

- Better invisibility
- Poor extraction

Large alpha

- Better extraction
- More visible changes

Recommended

```
0.03 – 0.08
```

---

## 8. Output Files

Embedding

```
stego.avi
```

Extraction

```
extracted_secret.avi
```

---

## 9. Error Messages

### Cover video not found

Solution

Place

```
cover.mp4
```

inside the project directory.

---

### Secret video not found

Solution

Place

```
secret.mp4
```

inside the project directory.

---

### Unable to open video

Possible reasons

- Wrong filename
- Unsupported codec
- Corrupted video

---

## 10. Performance Metrics

The program reports

- Processing time
- FPS
- MSE
- PSNR
- SSIM
- Average frame difference

---

## 11. Troubleshooting

Problem

Extracted video is dark

Solution

Increase alpha.

---

Problem

Stego video looks noisy

Solution

Reduce alpha.

---

Problem

Videos have different resolutions

Solution

The software automatically resizes secret frames.

---

## 12. Best Practices

- Use videos with similar resolutions.
- Avoid excessive compression.
- Keep alpha between 0.03 and 0.08.
- Store original cover video safely.

---

## 13. Applications

- Multimedia security
- Digital watermarking
- Copyright protection
- Covert communication
- Educational projects

---

## 14. Limitations

- Non-blind extraction
- Compression sensitive
- No encryption
- Frame synchronization required

---

## 15. Contact

Author

Praveen Singh

VIT Bhopal University
