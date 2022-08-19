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
A commercial example, the camera-based digital pen. The pen captures and converts handwritten analog information into digital data. It locates itself on a digital paper based on a bottom view camera. The camera observes the dot array hidden in the paper, but only a small sub-region (typically 6 $\times$ 6). The pen must read its absolute position on this paper based on this 6 $\times$ 6 ID tag. See the trick?
<br />
<img src=https://github.com/Lilin2015/Author---HydraMarker/blob/main/README_md_files/digital_pen.png width=200><br />
Well, the dot array is actually built from **de Bruijn sequence**. It is different from marker field, but the purpose of "position-sensing" is the same. In many applications, the visual conditions is as good as this pen-paper configuration. There might be occlusions, disturbance, curved surface. More importantly, reading 4 states might be unreliable (2D position-sensing marker built from de Bruijn sequence has 4 states, but from marker field only has 2 states). So we need marker field.
However, generating marker field is not easy. The most practical method is proposed by Szentandrasi *et al*.

    I. Szentandrasi, M. Zacharias, J. Havel, A. Herout, M. Dubska, and R. Kajan, “Uniform marker fifields: Camera localization by
    orientable de bruijn tori,” in Proc. IEEE International Symposium on Mixed and Augmented Reality. IEEE, 2012, pp. 319–320.
 You can download some ready-make marker fields from their project page, http://www.fit.vutbr.cz/research/groups/graph/MF/.
 However, if you want to customize your marker fields, but do not have a supercomputer, this HydraMarker toolkit is your best choice, at least for now.

