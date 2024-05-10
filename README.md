# Kolmogorov-Arnold-Networks

### References - 
[KAN](https://kindxiaoming.github.io/pykan/)
[Research Paper](https://arxiv.org/abs/2404.19756)

KolmogorovArnold Networks (KANs) are proposed as alternatives to MLPs, with learnable activation functions on edges instead of fixed ones on nodes. KANs outperform MLPs in accuracy and interpretability. KANs are visually intuitive and interact well with humans. They serve as valuable collaborators in discovering mathematical and physical laws, suggesting promising improvements over MLP-based deep learning models.

<p align="center">
  <img src="https://private-user-images.githubusercontent.com/23551623/326219527-695adc2d-0d0b-4e4b-bcff-db2c8070f841.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTUzODI2MjYsIm5iZiI6MTcxNTM4MjMyNiwicGF0aCI6Ii8yMzU1MTYyMy8zMjYyMTk1MjctNjk1YWRjMmQtMGQwYi00ZTRiLWJjZmYtZGIyYzgwNzBmODQxLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDA1MTAlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwNTEwVDIzMDUyNlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWY2YTQ4NTUxM2ZmODAyM2NlMTM2YTBlMGJkMTRkYjk2N2FlMjA5MmIxZGZjOTIxNGFhNjQ2NTUzNTlkZGJkZjMmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.gH6G6WbqjpgM_pVMwB4ZUMM8fJ4_4LJRjMambIhUZjI" alt="A Kolmogorov-Arnold Network being trained overtime." width="400"/>
  
</p>
<video width="320" height="240" controls>
  <source src="video.mp4" type="video/mp4">
</video>

### Dataset
Dataset used is the heart disease dataset [here](https://ieee-dataport.org/open-access/heart-disease-dataset-comprehensive) which was collected and combined at one place to help advance research on CAD-related machine learning and data mining algorithms, and hopefully to ultimately advance clinical diagnosis and early treatment. 

Additionally, I've also added some implementation with the IRIS dataset and MNIST dataset for image classification. 

(Note - Images resized to 8x8 for ease of computation)

### How is KAN different from MLP?

While MLPs have fixed activation functions on their nodes, KANs have learnable activation functions on their edges. This means that instead of fixed weights connecting nodes, KANs have functions that determine the strength of connections, typically represented as splines.

This change means that KANs don't have linear weights like MLPs. Instead, the nodes in a KAN simply add up the incoming signals without applying any non-linear functions. This difference can lead to significant improvements in performance and makes the network more interpretable.

### How does it work?

Kolmogorov-Arnold Networks (KANs) work by learning both the structure of a problem and the functions within it.
 + Structure Learning (External Degrees of Freedom): KANs, like MLPs, understand how different input features relate to each other and contribute to the output. They do this through layers of nodes connected by edges.
 + Univariate Function Optimization (Internal Degrees of Freedom): Each edge in a KAN holds a learnable activation function, typically a spline. Splines are flexible, piecewise functions that can closely match complex univariate functions. During training, KANs adjust these spline activation functions to best fit the target function.
 + Combining Strengths of Splines and MLPs: Splines excel in accuracy for low-dimensional functions and local adaptability but struggle with high-dimensional problems due to the curse of dimensionality. On the other hand, MLPs are better suited for high-dimensional problems but face challenges in optimizing univariate functions effectively.

### Training KANs

KAN at initialization

KAN after training once

Pruned KAN




