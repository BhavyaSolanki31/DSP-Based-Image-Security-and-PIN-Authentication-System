# DSP-Based-Image-Security-and-PIN-Authentication-System

A MATLAB-based image security system designed to protect confidential visual information through advanced data hiding and authentication techniques. The system conceals secret images within cover images while preserving visual quality and ensuring secure extraction through PIN-based authentication.

## Overview

It is an image security framework developed using MATLAB and Digital Signal Processing (DSP) principles. The project combines bit-plane slicing, pseudo-random embedding, and PIN-protected authentication to achieve secure image transmission with high imperceptibility and accurate reconstruction.

Unlike traditional steganographic approaches, SecureVision introduces randomized embedding patterns and controlled bit allocation strategies to enhance security while maintaining image fidelity.

## Key Features

- PIN-based authentication for authorized image recovery
- Secure hiding of secret images within cover images
- Bit-plane slicing for controlled data embedding
- Pseudo-random sequence generation for randomized embedding locations
- 3-3-2 bit embedding strategy to balance capacity and image quality
- Achieved PSNR values greater than **40 dB** across 20+ test images
- 100% accurate reconstruction using the correct authentication PIN
- Maintains imperceptibility against visual steganalysis
- User-friendly MATLAB GUI for sender and receiver operations
- Optional watermark support for enhanced ownership verification


## System Architecture

### Sender Side

1. Input Cover Image
2. Input Secret Image
3. Enter Authentication PIN
4. Perform Bit-Plane Analysis
5. Generate Pseudo-Random Embedding Sequence
6. Apply 3-3-2 Bit Embedding
7. Embed Secret Data into Cover Image
8. Generate Stego Image

### Receiver Side

1. Load Stego Image
2. Enter Authentication PIN
3. Validate User Credentials
4. Extract Embedded Data
5. Reconstruct Secret Image
6. Verify Recovery Accuracy

## Methodology

### 1. Bit-Plane Slicing

The secret image is decomposed into bit planes before embedding. This allows selective insertion of image information into lower significance regions of the cover image while minimizing visual distortion.

### 2. Pseudo-Random Sequence Generation

Embedding positions are determined using a pseudo-random sequence derived from the authentication key. This randomization significantly increases resistance against unauthorized extraction attempts.

### 3. 3-3-2 Bit Embedding

Secret bits are distributed among RGB channels using a 3-3-2 allocation scheme:

- Red Channel → 3 bits
- Green Channel → 3 bits
- Blue Channel → 2 bits

This strategy offers an effective trade-off between:

- Embedding capacity
- Visual quality
- Robustness

### 4. PIN-Based Authentication

A user-defined PIN is utilized during both embedding and extraction processes.

- Correct PIN → Successful reconstruction
- Incorrect PIN → Extraction failure and unusable output

This additional security layer prevents unauthorized access to hidden information.

## Performance Analysis

### Evaluation Metrics

#### Peak Signal-to-Noise Ratio (PSNR)

PSNR is used to quantify the visual similarity between cover and stego images.

**Observed Results:**

- PSNR > 40 dB
- Tested on 20+ image pairs
- Minimal perceptible distortion

#### Reconstruction Accuracy

- Correct PIN Accuracy: **100%**
- Incorrect PIN Accuracy: **0% meaningful recovery**

#### Visual Imperceptibility

Stego images remain visually indistinguishable from original cover images under normal inspection.

## Experimental Results

| Parameter | Result |
|-----------|---------|
| Test Images Evaluated | 20+ |
| Embedding Technique | 3-3-2 Bit Embedding |
| Security Mechanism | PIN Authentication |
| Embedding Pattern | Pseudo-Random |
| Reconstruction Accuracy | 100% |
| Average PSNR | > 40 dB |
| Visual Distortion | Negligible |
| GUI Support | Yes |

## Technologies Used

- MATLAB
- Digital Signal Processing (DSP)
- Image Processing Toolbox
- MATLAB GUI (GUIDE/App Designer)
- Bit-Plane Slicing
- Pseudo-Random Sequence Generation
- Least Significant Bit (LSB) Steganography
- PIN-Based Authentication
- Image Quality Assessment Metrics

### Usage

#### Embedding Process

1. Launch the sender interface.
2. Select the cover image.
3. Select the secret image.
4. Enter a secure PIN.
5. Click **Embed**.
6. Save the generated stego image.

#### Extraction Process

1. Launch the receiver interface.
2. Load the stego image.
3. Enter the correct PIN.
4. Click **Extract**.
5. Recover and save the secret image.


## Future Enhancements

- AES-based encryption before embedding
- Multi-factor authentication
- Deep learning-assisted steganalysis resistance
- Adaptive embedding strategies
- Support for video steganography
- Cloud-based secure image sharing

##  Applications

- Secure military communication
- Medical image confidentiality
- Digital evidence protection
- Intellectual property preservation
- Secure exchange of confidential documents
- Covert communication systems


## Author

**Bhavya Solanki**

B.Tech Electronics and Communication Engineering  

Interested in AI, Machine Learning, Digital Signal Processing, and Secure Embedded Systems.

---

## ⭐ If you found this project useful, consider giving it a star!
