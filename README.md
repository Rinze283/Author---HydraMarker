# **HydraMarker**

This is the demo code of the paper (under review), "HydraMarker: Effificient, Flexible, and Multifold Marker Field Generation"
## Introduction
An $n$-order **marker field** is a special binary matrix whose $n\times n$ sub-matrices are all distinct from each other in four orientations. For example, the following matrix is a 3-order marker field (black/white corresponds to 0/1 repectively).
<img src=https://github.com/Lilin2015/Author---HydraMarker/blob/main/README_md_files/field.jpeg width=200><br />
You cannot find two identical 3 $\times$ 3 sub-regions from this matrix, even with rotation. Every 3 $\times$ 3 sub-region is an **ID tag** of this marker field. The 3 $\times$ 3 mask used to extract ID tag is named **tag shape**.
With this toolkit, we can go further. For example, the following matrix is a 60 $\times$ 60 marker field with 4 tag shapes, including 4 $\times$ 4, 3 $\times$ 6, 2 $\times$ 9, and 1 $\times$ 20. Try it.<br />
<img src=https://github.com/Lilin2015/Author---HydraMarker/blob/main/README_md_files/field2.png width=200><br />
Why we need marker field? The most reason is **position-sensing marker**. Imaging a remote control vehicle sliding on the marker, and locating itself by a bottom view camera, which has a very limited field-of-view, as shown below. The vehicle can still estimate its position on this marker, because the sub-region it observes is unique.<br />
<img src=https://github.com/Lilin2015/Author---HydraMarker/blob/main/README_md_files/ps_marker.png width=200><br />
A commercial example, the camera-based digital pen. The pen captures and converts handwritten analog information into digital data. It locates itself on a digital paper based on a bottom view camera, and the dot array hidden in the paper.
<br />
<img src=https://github.com/Lilin2015/Author---HydraMarker/blob/main/README_md_files/digital_pen.png width=200><br />

