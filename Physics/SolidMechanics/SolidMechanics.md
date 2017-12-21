## Solid Mechanics

[toc]

### Concepts

- strain: $\epsilon  =  du/dx$ ($u$: displacement)
	- logarithmic strain $d\epsilon_{ln} = dl/l$, $\epsilon_{ln} = \mathrm{ln}(l/l_0) $
	- for homogeneous deformation, $\epsilon = exp(\epsilon_{ln})-1 $
	- strain along diameter: $\bar \epsilon = (d-d_0)/d_0$
- Poisson's ratio: $\nu = - \bar \epsilon/\epsilon $
- stress $\sigma = F/A $ (true stress)
- nominal stress (engineer stress) $\sigma_0 = F/A_0 $
- stress power $\pi_i = \sigma \dot \epsilon$ (dot is time derivative)
- stress work $ a_i = \int \sigma d\epsilon $
	- complementary power $ \pi_i^* = \epsilon \dot \sigma $
	- complementary work $ a_i^* = \int \epsilon d\sigma  $
- final work $\epsilon \sigma = a_i + a_i^*$

Elasticity

Stress is in general a function (functional) of displacement:
- $\sigma(x_0)  = F(u(x))  = f(u(x_0),u'(x_0),u''(x_0),...) $
- after truncate, $\sigma = f_n(u', ...,u^{(n)})$ is called a gradient material of order $n$
- simple elastic material: $n=1$, $\sigma = f_1(u') = f(\epsilon) $
- for small deformation, $E = df/d\epsilon$: Young's modulus
	- Hooke's law: $\sigma = E \epsilon

Viscoelasticity
- simplest rate-dependent model: linear viscous law
	- $\sigma = D \dot \epsilon $. $D$: viscosity/damper constant. Called Newton element


