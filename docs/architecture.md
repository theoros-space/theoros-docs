# Architecture

## One model, every satellite

Satellites differ in two ways: what their camera sees (the bands) and what
their computer can run. Theoros handles both on the ground.

1. **Train once.** The model learns from the physics of each band, its centre
   wavelength, bandwidth and ground sample distance, so it is not tied to any
   one camera. Training mixes many sensors and random subsets of their bands.
2. **Compile per satellite.** For a customer's instrument, the ground compiler
   produces a static network: the band-specific first layer is generated once,
   the camera calibration is folded into it, and the result contains only
   operators every flight processor supports.
3. **Fly.** The static int8 network runs on the satellite's existing computer
   or AI accelerator, under 1 MB.

## Design principles

- **Budget first.** Under one million parameters is a requirement, checked
  automatically on every change.
- **No "up" in space.** The first layer is exactly symmetric to rotations and
  mirrors of the image.
- **Honest capabilities.** A task the sensor cannot physically support is
  disabled and reported, never guessed.
- **Proof over testing.** Integer overflow and numerical equivalence are
  checked for every compiled model before it can be signed.
