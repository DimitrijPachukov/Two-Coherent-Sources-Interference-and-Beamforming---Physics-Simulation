# Two-Coherent-Sources-Interference-and-Beamforming---Physics-Simulation
The sketch is a two-element coherent wave interferometer — two point emitters ("towers") radiating waves of the same frequency, whose fields add by linear superposition. By controlling the relative phase, the relative amplitude, and the spacing of the second emitter, you reshape the combined field in space.
The physics it represents

Superposition and interference

In a linear medium (free space for radio, air for sound) fields add:

Etotal(r,t)=E1(r,t)+E2(r,t)E_{\text{total}}(\mathbf{r}, t) = E_1(\mathbf{r}, t) + E_2(\mathbf{r}, t)Etotal​(r,t)=E1​(r,t)+E2​(r,t)
Each source contributes a travelling wave. In the simulation the field map uses a
2-D cylindrical-wave form with a mild 1/r1/\sqrt{r}
1/r​ amplitude falloff:

Ei=Airi cos⁡ ⁣(kri−ωt+φi)E_i = \frac{A_i}{\sqrt{r_i}}\,\cos\!\left(k r_i - \omega t + \varphi_i\right)Ei​=ri​​Ai​​cos(kri​−ωt+φi​)
where k=2π/λk = 2\pi/\lambda
k=2π/λ is the wavenumber, ω=2πf\omega = 2\pi f
ω=2πf the angular frequency,
rir_i
ri​ the distance from source ii
i, and φi\varphi_i
φi​ its feed phase. Where crests meet
crests you get constructive interference (bright fringes); where crests meet troughs
you get destructive interference (dark nulls).

Far-field radiation pattern (array factor)

For two isotropic elements separated by distance dd
d along an axis, the far-field
intensity as a function of direction θ\theta
θ (measured from the array axis) is governed
by the array factor:

∣E(θ)∣2  ∝  A12+A22+2A1A2cos⁡ ⁣(kdcos⁡θ+Δφ)|E(\theta)|^2 \;\propto\; A_1^2 + A_2^2 + 2 A_1 A_2 \cos\!\big(k d \cos\theta + \Delta\varphi\big)∣E(θ)∣2∝A12​+A22​+2A1​A2​cos(kdcosθ+Δφ)
with Δφ\Delta\varphi
Δφ the relative feed phase. The main beam points where the bracket
vanishes, cos⁡θ=−Δφ/(kd)\cos\theta = -\Delta\varphi/(kd)
cosθ=−Δφ/(kd), which gives the beam-steering relation
(angle measured from broadside):

sin⁡θsteer=−Δφkd\sin\theta_{\text{steer}} = -\frac{\Delta\varphi}{k d}sinθsteer​=−kdΔφ​
This is exactly why changing one phase number swings the beam without moving hardware.

What each control does physically

ControlPhysical meaningEffectTower spacing (d/λd/\lambda
d/λ)Separation of the elements in wavelengthsSets fringe spacing and beam sharpness. Past ∼ ⁣1λ\sim\!1\lambda
∼1λ, grating lobes appear (extra copies of the main beam).Tower 2 phase (Δφ\Delta\varphi
Δφ)Relative time delay between the two feeds**Steers** the main beam off broadside. At Δφ\Delta\varphi
Δφ large enough the beam reaches *endfire* (along the array axis).Tower 2 power (A2A_2
A2​)Relative amplitude of the second emitterControls null depth. Equal amplitudes give perfect cancellation; setting it to zero collapses to a single omnidirectional source.

Key physical takeaway: energy is conserved

The pattern only ever redistributes energy — sharpening a beam or deepening a null
in one direction is paid for by reduced energy in another. Integrated over all
directions, the total radiated power equals the sum of what the two emitters supply
(Poynting's theorem / conservation of energy). You can synthesise directionality, focal
points, and even virtual sources that appear to radiate from empty space, but you can
never multiply the total energy or manufacture an independent new source for free.
