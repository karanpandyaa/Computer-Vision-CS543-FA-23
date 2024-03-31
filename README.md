#Assignments for Computer Vision CS543 taught by Prof.David S Forsyth (code private due to course policies)
## [Assignment 1: Registering Prokudin-Gorskii color separations of the Russian Empire](https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/blob/main/A1.pdf)
![image](https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/assets/50593664/d1805fd4-8565-4f4a-9a8a-52fdc6ed8402)

### Multiscale alignment:
```
For the high-resolution glass plate scans provided above, exhaustive search over all possible displacements will become prohibitively expensive. To deal with this case, implement a faster search procedure using an image pyramid.

An image pyramid represents the image at multiple scales (usually scaled by a factor of 2) and the processing is done sequentially starting from the coarsest scale (smallest image) and going down the pyramid, updating your estimate as you go.
```


## [Assignment 2: Fourier-based Alignment and Finding Covariant Neighborhoods](https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/blob/main/A2.pdf)

### Part 1: Fourier-based color channel alignment
Algorithm outline
```
The Fourier-based alignment algorithm consists of the following steps:
-For two color channels C1 and C2, compute corresponding Fourier transforms FT1 and FT2.
-Compute the conjugate of FT2 (denoted as FT2*- if you don't remember your complex numbers, look this up!), and compute the product of FT1 and FT2*.
-Take the inverse Fourier transform of this product and find the location of the maximum value in the output image. Use the displacement of the maximum value to obtain the offset of C2 from C1.
```
![image](https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/assets/50593664/e99b92a5-8980-47fc-832b-cc633f9a385e)
![image](https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/assets/50593664/f1a49e6e-a3c5-4762-86be-4432442bbc0f)

### Part 2: Scale-space blob construction

![image](https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/assets/50593664/befa1110-2d75-41ec-b37d-b40cdf834280)



## [Assignment 3: Homography stitching, shape from shading](https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/blob/main/A3.pdf)
Part 1: Stitching pairs of images
The first step is to write code to stitch together a single pair of images.

<img src="https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/assets/50593664/df43d63a-2352-4a54-9918-e1b77c752669" width="400" height="200">

<img src="https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/assets/50593664/e136e9c4-7932-4992-8573-f24d28339cf0)" width="400" height="200">

Finding matches:
<img src="https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/assets/50593664/3e518093-116d-4977-be14-c752723936c0">

Final output produced:
<img src="https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/assets/50593664/dea0ea70-c4cb-4aee-9b20-69d07056cdf1">

### Part2: Shape from shading
A: Estimate the albedo and surface normals
Given sample:
<img src="https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/assets/50593664/ec3065e9-26bd-4c60-bcc1-549721eaf78d" width="400" height="200">

Albedo estimated:
![image](https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/assets/50593664/63e29995-f83e-4354-9687-7e1dab39bda4)

Surface Normal estimated:
![image](https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/assets/50593664/22a48436-4350-447d-ad18-108bbf906f59)


## [Assignemnt 4: Single-view and two-view geometry](https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/blob/main/A4.pdf)

### Fundamental Matrix Estimation, Camera Calibration, Triangulation:
![image](https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/assets/50593664/c1f86379-0840-4cd7-aa39-31a13ec32cb9)

### visualize 3D camera centers and triangulated 3D points:
![image](https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/assets/50593664/6b114897-00ef-4643-9cfb-784b964b6a70)


## [Assignment 5: Affine factorization and binocular stereo](https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/blob/main/A5.pdf)
### Part 1: Affine Factorization
The goal of this part of the assignment is to implement the Tomasi and Kanade affine structure from motion method as described in lecture. You will be working with Carlo Tomasi's 101-frame hotel sequence.
![image](https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/assets/50593664/3ebb6af9-a6b9-4a82-896b-4884026f639b)

### Part 2: Binocular Stereo
The goal of this part is to implement a simple window-based stereo matching algorithm for rectified stereo pairs.

### Depth map estimation:
Original stereo image pair:
![image](https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/assets/50593664/51a6533c-0b62-4aa7-9455-080c0b8c777a)

Output depth map:
![image](https://github.com/karanpandyaa/Computer-Vision-CS543-FA-23/assets/50593664/ea9e01cb-8beb-4277-b003-66da9338f18a)


