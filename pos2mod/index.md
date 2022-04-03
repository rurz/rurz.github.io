# Three-dimensional position-to-modes discrete mapping


## Introduction

On previous works [1, 2], we explore the map between position and mode basis for discrete two-dimensional fields, aka., pixellated images. The extension to the three-dimensional case is straightforward since the discrete and finite basis spawned by the Kravchuk functions $\psi_{n}^{(j)}(q)$ is complete and their composition to upper dimensions is the direct product of the individual basis,

$$\begin{aligned}\Psi_{n\_{1}, n\_{2}, n\_{3}}^{(j)}(q\_{1}, q\_{2}, q\_{3}) &= \psi_{n\_{1}}^{(j)}(q\_{1})\otimes\psi_{n\_{2}}^{(j)}(q\_{2})\otimes \psi_{n\_{3}}^{(j)}(q\_{3})\\\ &=: \langle q\_{1}, q\_{2}, q\_{3}\vert n\_{1}, n\_{2}, n\_{3}\rangle.\end{aligned}$$

The ket form shows that the Kravchuk functions are the overlap between the position and mode space, so we can use it to encode a three-dimensional field in position space, to their equivalent in mode space.

## Position to mode map

The map is direct since we have the overlap of the position and mode basis. If we have a position field spawned by the ket $\vert q\_{1}, q\_{2}, q\_{3}\rangle$, the translation between the easy-to-discern position space is send to the not-to-easy-to-discern mode space as

$$\vert n\_{1}, n\_{2}, n\_{3}\rangle = \sum\limits\_{q\_{1}, q\_{2}, q\_{3} = -j}^{j} \vert q\_{1}, q\_{2}, q\_{3}\rangle\hspace{0.5em} \langle q\_{1}, q\_{2}, q\_{3}\vert n\_{1}, n\_{2}, n\_{3}\rangle.$$

The new space spawned by the ket $\vert n\_{1}, n\_{2}, n\_{3}\rangle$ is completely equivalent to the previous one, just like in the Fourier transform pairs. On the figure below we see a generic three-dimensional field, a kind of T on two directions. When we look at it on the position space, it is obvious what are we looking, but when we see the mode space, it is a bit hard to state what are we looking. But it is worth to notice that the map is unitary, meaning that the position and mode space have exactly the same amount of information.

{{< figure src = /posts/science/images/pos2mod.png >}}

___

#### References

[1] Wolf, K. B., & Alieva, T. (2008). Rotation and gyration of finite  two-dimensional modes. In Journal of the Optical Society of America A  (Vol. 25, Issue 2, p. 365). The Optical Society.  https://doi.org/10.1364/josaa.25.000365

[2] Urzúa, A. R., & Wolf, K. B. (2016). Unitary rotation and gyration of pixelated images on rectangular screens. In Journal of the Optical  Society of America A (Vol. 33, Issue 4, p. 642). The Optical Society.  https://doi.org/10.1364/josaa.33.000642


