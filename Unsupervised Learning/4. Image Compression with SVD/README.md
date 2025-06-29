# Image Compression with SVD

Singular Value Decomposition (SVD) is a matrix factorization technique that can be used to compress images by reducing the amount of data needed to represent them.

![svd_compression.png](svd_compression.png)

An image can be represented as a matrix (for grayscale) or three matrices (for RGB channels). SVD factors a matrix A into three matrices:

A = U Σ Vᵀ

U is an m×m orthogonal matrix.

Σ is an m×n diagonal matrix with singular values σ₁ ≥ σ₂ ≥ … ≥ σₖ ≥ 0.

Vᵀ is an n×n orthogonal matrix.

By keeping only the top r singular values and corresponding vectors, we form a rank‑r approximation A₍ᵣ₎:

A₍ᵣ₎ = U₍:,₁…r₎ Σ₍₁…r,₁…r₎ Vᵀ₍₁…r,:₎

where:

U₍:,₁…r₎ contains the first r columns of U

Σ₍₁…r,₁…r₎ contains the top r singular values on its diagonal

Vᵀ₍₁…r,:₎ contains the first r rows of Vᵀ

### SVD Algorithm
- Load Image: Convert image to grayscale matrix or separate RGB channels
- Compute SVD: Apply SVD to each channel matrix A
- Truncate: Choose r ≪ min(m, n) to keep only top r singular values
- Reconstruct: Form compressed matrix A₍ᵣ₎ for each channel and combine channels

### Advantages
- Dimensionality Reduction: Significant compression by storing only r singular values
- Quality Control: Trade-off between compression ratio and image quality by adjusting r
- Mathematically Sound: Provides the best rank‑r approximation in Frobenius norm

### Disadvantages
- Computational Cost: SVD is O(m n min(m,n)) – expensive for large images
- Storage of Factors: Need to store U, Σ, and Vᵀ (though truncated)
- Color Images: Must perform SVD per channel, increasing computation

### The image

I used an image of a [dog in the sun](https://knowyourmeme.com/editorials/guides/what-is-the-cooked-dog-meme-the-dog-closing-eyes-in-sunset-reaction-image-and-its-memes-on-tiktok-explained), which I thought would be a good example because its contrast between light and shadow helps keep the image recognizable even for very low values of k.

### Packages

In addition to previous packages, I used:
 
- [PIL Image module](https://pillow.readthedocs.io/en/latest/reference/Image.html)


