# 🧩 Fractal + DCT Image Compression

## 📘 Overview

This repository contains a **MATLAB-based implementation** of image compression using a hybrid approach that combines **Fractal Image Compression** and the **Discrete Cosine Transform (DCT)**. It includes scripts for encoding and decoding images, utility functions for image transformation, block partitioning, and distortion/error calculation.

## 📁 Repository Structure

- **`README.md`** – Project documentation
- **`LICENSE`** – MIT license file

- **`data/`**
  - `bridge.pgm` – Sample grayscale test image

- **`examples/`**
  - `compression_example.m` – Example script to compress an image
  - `decompression_example.m` – Example script to decompress an image

- **`src/`**
  - `fractal_dct_compress.m` – Implements the Fractal-DCT compression
  - `fractal_dct_decompress.m` – Implements the Fractal-DCT decompression
  - `distortion_calculation.m` – Calculates distortion (no-search method)
  - `mean_domain_calculation.m` – Computes domain block means
  - `partition_no_search.m` – Handles non-search block partitioning
  - **`utils/`**
    - `dct_transform.m` – Forward DCT function
    - `idct_transform.m` – Inverse DCT function
    - `normalization_matrix.m` – DCT normalization matrices


## ▶️ Usage

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/fractal-dct-combined-compression.git
   cd fractal-dct-combined-compression

## Open MATLAB, then execute the following scripts:

% Run compression
examples/compression_example.m

% Run decompression
examples/decompression_example.m


## 🧠 Key Concepts and Parameters

### 🔹 Image Processing and Partitioning

- **`T1`, `T`**: Input image matrices  
- **`numrange`, `numdom`**: Range and domain block sizes  
- **`dct2`, `idct2`**: MATLAB functions for Discrete Cosine Transform and its inverse  

### 🔹 Compression Parameters

- **`ss`, `quan`, `errr`**: Scaling factor, quantization level, and error threshold  
- **`ym`, `hk`, `DDF`, `fdel`**: Parameters used to track compression state and decision logic  

### 🔄 Main Loop Functionality

- Applies **DCT** to image blocks  
- Leverages **fractal similarity** for encoding  
- Performs **block partitioning** and encoding without exhaustive domain block search  

---

## 📊 Goals

- 📦 **Reduce file size** with minimal quality degradation  
- 🔁 **Combine fractal self-similarity** with **frequency-domain DCT** techniques  
- ⚡ **Improve computational efficiency** using fast quantization and non-search-based compression  

---

## 📄 License

This project is licensed under the **MIT License**.  
See the [`LICENSE`](./LICENSE) file for full details.

