# ML-models-for-predicting-radius-of-gyration-from-sequence
A few neural network architectures for predicting the radius of gyration (Rg) of intrinsically disordered proteins using features derived directly from sequence. The dataset consists of 6400 Rg simulations I ran in LAMMPS using the Mpipi model. Sequences were generated with differing lengths, compositions (with baseline composition based on the human IDRome), and residue patternings.

The dataset uses a reduced 6-bead amino acid representation rather than the full 20-amino-acid alphabet. Simulations were run using adjusted Mpipi interaction potentials I worked on previously. This simplification from 20 amino acids down to 6 beads makes the prediction problem significantly noisier but made the ML training faster.

Current models are only trained on a fixed-length subset of 150-bead sequences (800 samples) so that the networks predict based on sequence composition rather than sequence length, which is the strongest predictor of Rg. The goal is for the models to learn the underlying chemistry instead of relying on trivial length scaling.

