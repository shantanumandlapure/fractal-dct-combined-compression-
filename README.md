# fractal-dct-combined-compression

##This repository contains a MATLAB-based implementation of fractal image compression using the Discrete Cosine Transform (DCT). It includes scripts for encoding and decoding images, as well as utility functions for domain transformations.

Repository Structure:

FractalImageCompression/
├── README.md
├── LICENSE
├── src/
│ ├── fractal_dct_compress.m
│ ├── fractal_dct_decompress.m
│ ├── distortion_calculation.m
│ ├── mean_domain_calculation.m
│ ├── partition_no_search.m
│ └── utils/
│ ├── dct_transform.m
│ ├── idct_transform.m
│ └── normalization_matrix.m
├── data/
│ └── bridge.pgm
└── examples/
├── compression_example.m
└── decompression_example.m

## Files
- `src/fractal_dct_compress.m`: Implements the encoding process for fractal image compression using DCT.
- `src/fractal_dct_decompress.m`: Implements the decoding process for fractal image compression using DCT.
- `src/distortion_calculation.m`: Calculates the distortion between range and domain blocks without performing a search.
- `src/mean_domain_calculation.m`: Computes the mean of the domain block and applies necessary transformations.
- `src/partition_no_search.m`: Handles the partitioning of the image blocks without search.
- `src/utils/dct_transform.m`: Utility function for applying DCT.
- `src/utils/idct_transform.m`: Utility function for applying inverse DCT.
- `src/utils/normalization_matrix.m`: Contains normalization matrices used in the compression process.
- `data/bridge.pgm`: Sample image used for testing the compression algorithm.
- `examples/compression_example.m`: Example script for encoding an image.
- `examples/decompression_example.m`: Example script for decoding an image.

## Usage

1. Clone the repository.
2. Run `examples/compression_example.m` to encode an image.
3. Run `examples/decompression_example.m` to decode an image.

## Key Functions and Variables:

Normalization Matrices (normar1): These matrices are used for quantization in DCT.

**Image Processing and Block Partitioning:**

T1, T: The input image.
numrange, numdom: Sizes of the range and domain blocks.
dct2, idct2: Functions for the Discrete Cosine Transform and its inverse.

**Compression Parameters:**

ss, quan, errr: Parameters for scaling, quantization, and error threshold.
ym, hk, DDF, fdel: Various parameters for tracking the state of the compression process.

**Main Loop:** The main loop iterates over the image, applying DCT and partitioning it into smaller blocks.

## License







    

