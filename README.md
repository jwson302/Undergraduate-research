# Undergrad-research (work in progress)

## Domain (2D channel)

<p align="center">$x \in [0,L]$,  $y \in [-H,H]$, $t \in [0,T]$</p>

## Governing equations (2D channel)

$u$ is $x$-direction velocity, $v$ is $y$-direction velocity, $p$ is pressure.

$x$-direction momentum equation

$$\rho \left( \frac{\partial u}{\partial t} + u \frac{\partial u}{\partial x} + v \frac{\partial u}{\partial y} \right)
 = -\frac{\partial p}{\partial x}+2\frac{\partial}{\partial x}\left(\eta \frac{\partial u}{\partial x} \right) + \frac{\partial}{\partial y}\left(\eta \left(\frac{\partial u}{\partial y} + \frac{\partial v}{\partial x}\right)\right)$$

$$= -\frac{\partial p}{\partial x} + \frac{\partial \eta}{\partial y}\left(\frac{\partial u}{\partial y} + \frac{\partial v}{\partial x}\right) + \eta\frac{\partial^2 u}{\partial y^2} + \eta\frac{\partial^2 v}{\partial x\partial y} + 2\frac{\partial \eta}{\partial x}\frac{\partial u}{\partial x} + 2\eta\frac{\partial^2 u}{\partial x^2}$$


$y$-direction momentum equation

$$\rho \left( \frac{\partial v}{\partial t} + u \frac{\partial v}{\partial x} + v \frac{\partial v}{\partial y} \right)
= -\frac{\partial p}{\partial y}+2\frac{\partial}{\partial y}\left(\eta \frac{\partial v}{\partial y} \right) + \frac{\partial}{\partial x}\left(\eta \left(\frac{\partial u}{\partial y} + \frac{\partial v}{\partial x}\right)\right)$$

$$= -\frac{\partial p}{\partial y} + \frac{\partial \eta}{\partial x}\left(\frac{\partial u}{\partial y} + \frac{\partial v}{\partial x}\right) + \eta\frac{\partial^2 v}{\partial x^2} + \eta\frac{\partial^2 u}{\partial x\partial y} + 2\frac{\partial \eta}{\partial y}\frac{\partial v}{\partial y} + 2\eta\frac{\partial^2 v}{\partial y^2}$$

Continuity equation

$$\frac{\partial u}{\partial x} + \frac{\partial v}{\partial y} = 0$$

Shear rate

$$\dot{\gamma} = \sqrt{2\left(\frac{\partial u}{\partial x}\right)^2 + 2\left(\frac{\partial v}{\partial y}\right)^2 + \left(\frac{\partial u}{\partial y} + \frac{\partial v}{\partial x}\right)^2}$$

Carreau fluid model

$$\eta\left(\dot{\gamma}\right) = \eta_\infty + (\eta_0 - \eta_\infty)\left(1 + \left(\lambda\dot{\gamma}\right)^2\right)^\frac{n-1}{2}, n<1$$

## Boundary conditions (2D channel)

$$u(x, y=H, t) = 0$$

$$u(x, y=-H, t) = 0$$

$$v(x, y=H, t) = 0$$

$$v(x, y=-H, t) = 0$$

$$u(x=0, y, t) = u_{max}\left(1+\frac{y}{H}\right)\left(1-\frac{y}{H}\right)(1+m_A\sin(2\pi ft))$$

$$v(x=0, y, t) = 0$$

$$p(x=L, y, t) = 0$$

$$u(x, y, t=0) = u_{max}\left(1+\frac{y}{H}\right)\left(1-\frac{y}{H}\right)$$

$$v(x, y, t=0) = 0$$

## Parameters in SI units (2D channel)

$$H = 0.025$$

$$\rho = 1500$$

$$\eta_0 = 60$$

$$\eta_\infty = 0.01$$

$$\lambda = 0.8$$

$$n = 0.5$$

$$f = 4$$

$$L = 0.5$$


## Domain (cylindrical pipe)

<p align="center">$r \in [0,R]$,  $z \in [0,L]$, $t \in [0,T]$</p>

## Governing equations (cylindrical pipe)

$u$ is $z$-direction velocity, $v$ is $r$-direction velocity, $p$ is pressure.

$z$-direction momentum equation

$$\rho \left( \frac{\partial u}{\partial t} + u \frac{\partial u}{\partial z} +v \frac{\partial u}{\partial r}\right) 
= -\frac{\partial p}{\partial z} + \eta \left(\frac{1}{r}\frac{\partial u}{\partial r} + \frac{\partial^2 u}{\partial r^2} + \frac{\partial^2 u}{\partial z^2}\right) + 2\frac{\partial \eta}{\partial z}\frac{\partial u}{\partial z} + \frac{\partial \eta}{\partial r}\frac{\partial u}{\partial r} + \frac{\partial \eta}{\partial r}\frac{\partial v}{\partial z}$$

$r$-direction momentum equation

$$\rho \left( \frac{\partial v}{\partial t} + u \frac{\partial v}{\partial z}+ v \frac{\partial v}{\partial r}\right)
 = -\frac{\partial p}{\partial r} + \eta \left(\frac{1}{r}\frac{\partial v}{\partial r} + \frac{\partial^2 v}{\partial r^2} + \frac{\partial^2 v}{\partial z^2} - \frac{v}{r^2}\right) + 2\frac{\partial \eta}{\partial r}\frac{\partial v}{\partial r} + \frac{\partial \eta}{\partial z}\frac{\partial u}{\partial r} + \frac{\partial \eta}{\partial z}\frac{\partial v}{\partial z}$$

Continuity equation

$$\frac{\partial v}{\partial r} + \frac{\partial u}{\partial z} + \frac{v}{r} = 0$$

Shear rate

$$\dot{\gamma} = \sqrt{2\left(\frac{v}{r}\right)^2+2\left(\frac{\partial u}{\partial z}\right)^2 + 2\left(\frac{\partial v}{\partial r}\right)^2 + \left(\frac{\partial u}{\partial r} + \frac{\partial v}{\partial z}\right)^2}$$

Carreau fluid model

$$\eta\left(\dot{\gamma}\right) = \eta_\infty + (\eta_0 - \eta_\infty)\left(1 + \left(\lambda\dot{\gamma}\right)^2\right)^\frac{n-1}{2}, n<1$$

## Boundary conditions (cylindrical pipe)

$$u(z, r=R, t) = 0$$

$$\frac{\partial u}{\partial r}(z, r=R, t) = 0$$

$$v(z, r=R, t) = 0$$

$$v(z, r=0, t) = 0$$

$$u(z=0, r, t) = u_{max}\left(1+\frac{r}{R}\right)\left(1-\frac{r}{R}\right)(1+m_A\sin(2\pi ft))$$

$$v(z=0, r, t) = 0$$

$$p(z=L, r, t) = 0$$

$$u(z, r, t=0) = u_{max}\left(1+\frac{r}{H}\right)\left(1-\frac{r}{H}\right)$$

$$v(z, r, t=0) = 0$$

## Parameters in SI units (cylindrical pipe)

$$R = 0.025$$

$$\rho = 1500$$

$$\eta_0 = 60$$

$$\eta_\infty = 0.01$$

$$\lambda = 0.8$$

$$n = 0.5$$

$$f = 4$$

$$L = 0.5$$

$$T = 1$$

$$u_{max} = 1.02$$

$$m_A = 0.1$$
