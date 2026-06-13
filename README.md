Two Coherent Sources: Interference and Beamforming

What the simulation is

The sketch is a two-element coherent wave interferometer — two point emitters
("towers") radiating waves of the same frequency, whose fields add by linear
superposition. By controlling the relative phase, the relative amplitude, and
the spacing of the second emitter, you reshape the combined field in space.

It is the canonical model behind a whole family of real experiments and engineering
systems. Depending on which knob you emphasise, the same setup is:


Young's double-slit experiment (the optics original) — two coherent sources a
fixed distance apart producing interference fringes.
A two-element phased array (radio / radar / 5G / ultrasound) — controlling phase
and amplitude per element to steer a beam and place nulls electronically, with no
moving parts.
A minimal radio interferometer (radio astronomy, e.g. the principle behind the
VLA and VLBI) — combining signals from separated antennas to synthesise directional
sensitivity.
A demonstration of Huygens' principle — many elementary sources summing into a
shaped wavefront, the basis of acoustic wave field synthesis.
Superposition and interference
In a linear medium (free space for radio, air for sound) fields add:
$$E_{\text{total}}(\mathbf{r}, t) = E_1(\mathbf{r}, t) + E_2(\mathbf{r}, t)$$
Each source contributes a travelling wave. In the simulation the field map uses a
2-D cylindrical-wave form with a mild $1/\sqrt{r}$ amplitude falloff:
$$E_i = \frac{A_i}{\sqrt{r_i}},\cos!\left(k r_i - \omega t + \varphi_i\right)$$
where $k = 2\pi/\lambda$ is the wavenumber, $\omega = 2\pi f$ the angular frequency,
$r_i$ the distance from source $i$, and $\varphi_i$ its feed phase. Where crests meet
crests you get constructive interference (bright fringes); where crests meet troughs
you get destructive interference (dark nulls).
Far-field radiation pattern (array factor)
For two isotropic elements separated by distance $d$ along an axis, the far-field
intensity as a function of direction $\theta$ (measured from the array axis) is governed
by the array factor:
$$|E(\theta)|^2 ;\propto; A_1^2 + A_2^2 + 2 A_1 A_2 \cos!\big(k d \cos\theta + \Delta\varphi\big)$$
with $\Delta\varphi$ the relative feed phase. The main beam points where the bracket
vanishes, $\cos\theta = -\Delta\varphi/(kd)$, which gives the beam-steering relation
(angle measured from broadside):
$$\sin\theta_{\text{steer}} = -\frac{\Delta\varphi}{k d}$$
This is exactly why changing one phase number swings the beam without moving hardware.
What each control does physically
Control	Physical meaning	Effect
Tower spacing ($d/\lambda$)	Separation of the elements in wavelengths	Sets fringe spacing and beam sharpness. Past $\sim!1\lambda$, grating lobes appear (extra copies of the main beam).
Tower 2 phase ($\Delta\varphi$)	Relative time delay between the two feeds	Steers the main beam off broadside. At $\Delta\varphi$ large enough the beam reaches endfire (along the array axis).
Tower 2 power ($A_2$)	Relative amplitude of the second emitter	Controls null depth. Equal amplitudes give perfect cancellation; setting it to zero collapses to a single omnidirectional source.
