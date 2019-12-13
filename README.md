# 2D-shallow-water-model-diffeq
This is a class project for Numerical Weather Prediction

Project Description Below:


CLIM 470 Numerical Weather Prediction
Final Project
Due Monday, December 16, 2019
The shallow water equations with bottom topography can be written as
∂V + qk × V∗ + ∇(K + Φ) = 0 (1)
∂t
Here, the potential vorticity, q, and the mass flux, V∗ are defined by q≡ζ+f
h (3) V∗ ≡ hV
and V is the horizontal velocity, t the time, f the Coriolis parameter, ζ the vorticity, k the vertical unit vector, ∇ the horizontal del operator, h the vertical fluid column above the bottom surface, K the kinetic energy per unit mass (= 1/2V2), g the gravitational acceleration, hs the bottom surface height, and
Φ ≡ g(h + hs) (4) Multiplying (1) by V∗ and combining the result with (2) yield the equation for the
time change of total kinetic energy
∂ (hK) + ∇ · (V∗K) + V∗ · ∇Φ = 0 (5)
∂t
Multiplying (2) by Φ gives the equation for the time change of potential energy,
∂ (1/2gh2 + ghhs) + ∇ · (V∗Φ) − V∗ · ∇Φ = 0. (6) ∂t
1
∂h + ∇ · V∗ = 0 (2) ∂t

The summation of (6) and (7) the yields a statement of the conservation of total energy
∂ [h(K + 1/2gh + ghs)] = 0, (7) ∂t
where the overbar denotes the mean over a finite domain with no inflow or outflow through the boundaries.
Assignment
Program the shallow water model with bottom topography (1)–(2) in the follow- ing way:
1. Use the C-grid for the spatial discretization as described by Arakawa and Lamb, 1981. For details see the paper posted on BB.)
2. Third-order Adams-Bashforth time differencing for the advection terms of the momentum, the Coriolis, and pressure-gradient terms of the momentum equation, and the mass divergence term of the continuity equation. You will have to do some- thing different on the first two time steps.
3. Use a domain with Lx = 6000 km and Ly = 2000 km. Use the ”rigid wall” boundary conditions in the y-direction mean v = 0 and also use a ”computational” boundary condition in the y-direction, which is vorticity = 0. This simply means that if you need a value of the vorticity that is ”outside the domain,” i.e. beyond the walls, set that value to zero.
4. Use the periodic boundary condition in the x-direction.
5. Use the bottom topography in the form of a narrow ridge, centered at x = 3000 km, with maximum height of 2 km and a bottom width of 1000 km. For a graphic depiction of this topography consult Fig. 2 in Arakawa and Lamb, 1981.
a) Perform simulations with three different resolutions: d = 500, 250, and 125 km and present the dependence of the results on the grid spacing
b) Investigate if the scheme conserves the total energy.
 
