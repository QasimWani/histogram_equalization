# Local Histogram Equalization
Robust Local Histogram Equalization written from scratch

<p>
<a href="https://en.wikipedia.org/wiki/Histogram_equalization">Histogram Equalization</a> is a method in image processing of contrast manipulation using an image's histogram. 
A histogram is nothing but the probability distribution of its intensity values. This can be represented as a probability density function, pdf.
Using this idea, we can manipulate the intensity value of an image using its corresponding histogram value. 
</p>
<p>
There are two types of histogram equalization techniques, local and global. A global histogram equalization deals with manipulation of pixel values without
the consultation of any neighbors. What this means is that the output intensity is a function of just the input value and the corresponding transformation function.
On the other hand, a local histogram equalization considers neigboring pixels and creates a CDF (cumaltive density function) based approximating for the resulting
intensity.
</p>

# Demo:

## Input Picture:

![Input Image](images/hidden-symbols.png)

### Histogram

![Output Image](images/input_histogram.png)


## Local Histogram Equalization with kernel = 3

![Output Image](images/output_3kernel.png)

### Output Histogram

![Output Image](images/output_histogram_3kernel.png)

## Local Histogram Equalization with kernel = 7

![Output Image](images/output_7kernel.png)

### Output Histogram

![Output Image](images/output_histogram_7kernel.png)



```python
Procedure:
# steps:
# 1. replicate padding.
# 2. get slices (m x n) based on values for m and n.
# 3. compute pdf for slice_i
# 4. compute cdf for pdf(slice_i) with value z
# 5. find the middle element and replace with the round(cdf) value z.
# 6. return new matrix without the replicate padding.
# 7. Repeat for all slices.
# 8. reshape matrix to appropriate kernel formula if all values appended singularily.
```
# Run the [Colab](https://colab.research.google.com/drive/1UCgTdZMaFBSUlPakZFovCZ33bEMxJdo8) version to Reproduce results
