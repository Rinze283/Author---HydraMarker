# **HydraMarker**

This is the demo code of the paper (under review), "HydraMarker: Effificient, Flexible, and Multifold Marker Field Generation"
## Introduction
An $n$-order marker field is a special binary matrix whose $n\times n$ sub-matrices are all distinct from each other in four orientations. For example, the following matrix is a 3-order marker field (black/white corresponds to 0/1 repectively).
<img src=https://github.com/Lilin2015/Author---HydraMarker/blob/main/README_md_files/field.jpeg width=50><br />
You cannot find two identical 3 $\times$ 3 sub-regions from this matrix, even with rotation. Every 3 $\times$ 3 sub-region is an **ID tag** of this marker field. The 3 $\times$ 3 mask used to extract ID tag is named **tag shape**.
With this toolkit, we can go further. For example, the following matrix is a 10 $\times$ 10 marker field with 3 tag shapes, including 3 $\times$ 3, 2 $\times$ 4, and 1 $\times$ 10. Try it.
 
