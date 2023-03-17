# Undergrad-research (work in progress)

## Domain

<p align="center">$x \in [0,L]$,  $y \in [-H,H]$, $t \in [0,T]$</p>

## Governing equations

x-direction momentum equation

$$\rho \left( \frac{\partial u}{\partial t} + u \frac{\partial u}{\partial x} + v \frac{\partial u}{\partial y} \right)
 = -\frac{\partial p}{\partial x}+2\frac{\partial}{\partial x}\left(\eta \frac{\partial u}{\partial x} \right) + \frac{\partial}{\partial y}\left(\eta \left(\frac{\partial u}{\partial y} + \frac{\partial v}{\partial x}\right)\right)$$

y-direction momentum equation

$$\rho \left( \frac{\partial v}{\partial t} + u \frac{\partial v}{\partial x} + v \frac{\partial v}{\partial y} \right)
= -\frac{\partial p}{\partial y}+2\frac{\partial}{\partial y}\left(\eta \frac{\partial v}{\partial y} \right) + \frac{\partial}{\partial x}\left(\eta \left(\frac{\partial u}{\partial y} + \frac{\partial v}{\partial x}\right)\right)$$

Continuity equation

$$\frac{\partial u}{\partial x} + \frac{\partial v}{\partial y} = 0$$

Shear rate

$$\dot{\gamma} = \sqrt{2\left(\frac{\partial u}{\partial x}\right)^2 + 2\left(\frac{\partial v}{\partial y}\right)^2 + \left(\frac{\partial u}{\partial y} + \frac{\partial v}{\partial x}\right)^2}$$

Carreau fluid model

$$\eta\left(\dot{\gamma}\right) = \eta_\infty + (\eta_0 - \eta_\infty)\left(1 + \left(\lambda\dot{\gamma}\right)^2\right)^\frac{n-1}{2}, n<1$$

## Boundary conditions

$$u(x, y=H, t) = 0$$

$$u(x, y=-H, t) = 0$$

$$v(x, y=H, t) = 0$$

$$v(x, y=-H, t) = 0$$

$$u(x=0, y, t) = u_{max}\left(1+\frac{y}{H}\right)\left(1-\frac{y}{H}\right)(1+m_A\sin(2\pi ft))$$

$$v(x=0, y, t) = 0$$

$$p(x=L, y, t) = 0$$

