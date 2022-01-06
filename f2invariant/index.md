# Dynamical invariant for the position-positon coupled harmonic oscillators


## 1. Introduction

Recently I found a new very nice article about dynamical invariants by Kumar _et al._ [1], that  is based on findings by Struckmeier and Riedel [2]. I been involved in the solution of time-dependent systems by means of orthogonal and Lewis-Ermakov invariants [3, 4] and I want to expand the understanding of this mathematical devices on systems who behave like damping phenomena. The methods they provide are interesting because of the generalization over the standard invariants. Here, I provide their use on some basic examples.

## 2. Theoretical background

There exists an operator $\hat{I}$, called invariant, that fulfills the condition

$$\frac{d\hat{I}}{dt} = \frac{\partial\hat{I}}{dt} + \left[\hat{I}, \hat{H}\right] = 0 $$

They find that $\hat{I}$ obeys and equation with and auxiliary function $f_{2}(t)$. For a one-dimensional time-dependent systems is defined as

$$\hat{I}\_{f_{2}} = 2f\_{2}(t)\hat{H}  - \dot{f}\_{2}(t)\sum\limits\_{i = 1}^{N} \hat{q}\_{i}\hat{p}\_{i} + \ddot{f}\_{2}(t)\sum\limits_{i = 1}^{N}\frac{1}{2}\hat{q}\_{i}^{2},$$

with the function $f_{2}(t)$ obeying the third order differential equation

$$ \dot{f}_{2}(t)\left(2\hat{V} + \sum\limits\_{i = 1}^{N}\hat{q}\_{i}\frac{\partial\hat{V}}{\partial \hat{q}\_{i}}\right) +2f\_{2}(t)\frac{\partial\hat{V}}{\partial t} + \overset{\cdots}{f}\_{2}(t)\sum\limits\_{i = 1}^{N}\frac{1}{2}\hat{q}\_{i}^{2} = 0.$$

## 3. The position-position coupling dynamical invariant

Starting with Hamiltonian for the position-position coupled harmonic oscillators

$$\hat{H} = \frac{1}{2}\sum\limits_{j=1}^{2}\left(\hat{p}_{j}^{2} + \omega_{j}(t)^{2}\hat{q}_{j}^{2}\right) + \lambda(t)\hat{q}_{1}\hat{q}_{2},$$

we see that this simple kind of coupling can lead to interesting phenomena because of the interchange of motion energy in the configuration space, plus the time-dependent coupling that acts as driven for increase or decrease strength coupling. The system is of such simplicity that the solution of the dynamical equations by means of the Hamilton equations is straightforward, we have

$$ \ddot{\hat{q}\_{1}} = -\omega\_{1}(t)^{2}\hat{q}\_{1} - \lambda(t)\hat{q}\_{2},\quad \ddot{\hat{q}\_{2}} = -\omega\_{2}(t)^{2}\hat{q}\_{2} - \lambda(t)\hat{q}_{1},$$

where, of course, when $\lambda(t) = 0$, we have the usual decoupled system.

### 3.1 Case 1. $\omega(t) = t, \lambda(t) = t^{2}$

As the title explicitly says, I define the individual harmonic oscillator frequency to be identical as a monotonic linear function $\omega_{i}(t) = t$. The position-position coupling is a quadratic function of time $\lambda(t) = t^{2}$, meaning, their strength increases faster than their own individual frequency of oscillation.

If we use this definitions, we arrive to the auxiliary function $f_{t}(t)$ after solving the third-order differential equation with initial conditions $f(0) = 1, \dot{f}(0) = 0, \ddot{f}(0) = 0$. The explicit form of the auxiliary function is then

$$ f\_{2}(t) = \Gamma\left(\frac{3}{4}\right)^{2}\textrm{J}\_{-1/4}\left(\frac{t^{2}}{2}\right)\frac{t}{2},$$

that shows a damping oscillatory behavior, as shown in the figure. It is worth to notice, that in this case of the Hamiltonian, the third-order differential equation for $f\_{2}(t)$ is independent of the explicit solution of the movement equation $q\_{i}(t)$.

{{< figure src = /posts/science/images/ft.jpg >}}

Now, if we also solve the movement equation for $q_{i}(t)$, we arrive to a damping oscillatory behavior as well, showing that the mean position of the individual oscillator are in a one and a halfway of the respective configuration space, and as a function of time, their amplitude of oscillation is decreasing after each period. The figure show the damping phenomena.

{{< figure src = /posts/science/images/qi.jpg >}}

## 4. Conclusions

I briefly show the calculations for the dynamical invariants involving a generalization of the standard invariants, namely Lewis-Ermakov for example. This method allow the calculation of an auxiliary function $f_{2}(t)$ that acts as a key component to understand the damping phenomena of the movement equations solutions, in the case of the position-position coupling. 

_____

[1] Kumar, N., Bhardwaj, S. B., Kumar, V., Singh, R. M., & Chand, F.  (2021). Dynamical invariants for time-dependent real and complex  Hamiltonian systems. In Journal of Mathematical Physics (Vol. 62, Issue  11, p. 112705). AIP Publishing. https://doi.org/10.1063/5.0061119

[2] Struckmeier, J., & Riedel, C. (2000). Exact Invariants for a Class  of Three-Dimensional Time-Dependent Classical Hamiltonians. In Physical  Review Letters (Vol. 85, Issue 18, pp. 3830–3833). American Physical  Society (APS). https://doi.org/10.1103/physrevlett.85.3830

