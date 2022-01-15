# Gibbs-like oscillations in one-dimensional discrete signals


## 1 Introduction: Continuous signals

It is well known that a well suitable periodic one-dimensional signal (or function) $f(x)$ in $\mathcal{L}^{2}$ can be expanded and encoded in the coefficients of the Fourier series $f_{n}$ [1, pp.]

$$f_{n} = \left(2\pi\right)^{-1/2}\int_{-\pi}^{\pi}dx f(x)\exp\left(-\mathrm{i}nx\right),\qquad (1)$$

that are used to reconstruct the original waveform $f(x)$ up to a $N$ degree,

$$f(x) \equiv \left(2\pi\right)^{-1/2}\sum\limits_{n = 0}^{N - 1}f_{n}\exp\left(\mathrm{i}nx\right).\qquad (2)$$

The _Gibbs phenomena_ is assigned to the behavior of the reconstructed signal under a truncation of the sum on $(2)$, at most $K < N$. It was shown [1, pp. ] that in the continuous case $(1)$, the truncation leads a discontinuity over the edges on sharp input function, that is, oscillations that doesn't increase nor disappear. This is because $N$ is theoretically infinite, ipso facto, we have to stop the sum at some point $<\infty$

Because equation $(1)$ deals with an analytic periodic function over a symmetric range $[-\pi, \pi]$, we want to know, what happen to discrete signals who has odd or even number or entries, how the Gibbs phenomena appear in the discrete version of the Fourier transform, and the subsequent reconstruction.

## 2. Discrete signals

A discrete signal is understanded as a row vector $\vec{v} = \left(v_{n}\right)_{n\in I}$. Where the interval $I$ can have odd, or even number of entries $N$. 

The Discrete Fourier Transform (DFT) is defined as the one-to-one map $\mathcal{F}\left(\vec{v}\right):\mathbb{R}^{N}\Rightarrow\mathbb{C}^{N}$

$$\mathcal{F}\left(\vec{v}\right)\equiv \tilde{v}_{n} = \frac{1}{\sqrt{N}}\sum\limits\_{m = 0}^{N-1}v\_{n}\mathcal{K}\_{n,m},\qquad (3)$$

where $\mathcal{K}_{n,m} := \exp\left(-\frac{2\pi\mathrm{i}nm}{N}\right)$ is the Fourier matrix that leads the map. Furthermore, the Fourier matrix has the properties of unitarity and inversion, $\mathcal{K}\mathcal{K}^{\dagger} = 1$, $\mathcal{K}^{\dagger} = \mathcal{K}^{-1}$. We see that the range of the original interval $I = \\{0, ..., N-1\\}$, is the usual way to perform the sum. Nevertheless, we can have a pair of cases when we deal with signals that have an odd or even number of elements.

### Even interval

When $N$ is even, we can construct a symmetric interval $I$ of indexes that can be used to evaluate the sum in $(3)$, although, we have to deal with half-integer elements in the interval (spin-like representation), then the index $m, n$ belongs to the set

$$m, n\in\\{-\frac{N-1}{2}, ..., -\frac{1}{2}, \frac{1}{2}, ..., \frac{N-1}{2}\\} = I\_{even}.$$

### Truncated Reconstruction

When we have the information of a signal $\vec{v}$ encoded in the $N$ Fourier coefficients given by $\tilde{v}_{n}$, we can reconstruct the signal using the so-called _Fourier series_, that are the linear superposition of the coefficients on the inverse basis given by $\mathcal{K}$,

$$\left(\vec{v}\right)\_{n}\approx \frac{1}{\sqrt{N}}\sum\limits\_{m \in I\_{even}}\tilde{v}\_{m}\mathcal{K}\_{n,m}^{-1}.\qquad (4)$$

This last equation, inherit the properties of the symmetric interval $I_{even}$, so for given a correct truncation of summation terms, we need to cutoff on each side of the interval. If $K$ is the truncation degree, the truncated reconstruction can be done ripping of the $K$-terms of the interval $I_{even}$, we obtain

$$I\_{even}^{(K)} = \\{-\frac{N - 1 + K}{2}, ..., -\frac{1 + K}{2}, \frac{1 - K}{2}, ..., \frac{N - 1 - K}{2}\\\},$$

that can be applied to $(4)$ to finally have the truncated reconstrucion

$$\left(\vec{v}^{(K)}\right)\_{n}\approx \frac{1}{\sqrt{N}}\sum\limits_{m \in I_{even}^{(K)}}\tilde{v}_{m}\mathcal{K}_{n,m}^{-1}.\qquad (5)$$

In the next figure is showed the reconstruction of a symmetrical step function between $[-1,1]$. The input signal is a discretized vector of $N = 200$ points. For the truncation in the reconstruction series, the values of $K$ are $25$ in the upper figure, and $50$ in the lower figure.

{{< figure src = /posts/science/images/fs11.png >}}

We see that the oscillations near the sharp edge of the step are constantly present, this is a signature of a Gibss-like phenomena when the periodicity of the signal is broken due the use of truncation.

## 3. Conclusions

We show that the DFT can be used, as in the same way of the continuous version, as the kernel for reconstruct discrete signal. Furthermore, when we reformulate the system in a symmetric interval, the truncation of the Fourier series at a degree $K < N$ exhibit a phenomena of oscillation called _Gibbs phenomena_. Nevertheless, one caveat in treat the DFT as a way to reconstruct signals is that the exact reconstruction is possible when the number of terms in the sum is exact the number of points in the input signal, that is $N$. 

____

[1] Wolf, K. (1979). *Integral Transforms in Science and Engineering*. Kluwer Academic/Plenum.

