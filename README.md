# NEP-CuC

NEP-CuC is a transferable machine-learned interatomic potential for copper-carbon
(Cu-C) systems based on the Neuroevolution Potential (NEP) framework. This
repository provides five trained NEP4 models and the development dataset for
molecular dynamics simulations with [GPUMD](https://gpumd.org/).

The potential was developed to describe elemental Cu, diverse carbon structures,
Cu-C interfaces and defects. Applications examined in the accompanying paper
include amorphous-carbon formation, Cu shock compression, and Cu deposition,
annealing and tensile loading on diamond.

**Paper:** [A Transferable Machine-Learned Potential Enabling Large-Scale
Copper-Carbon Simulations from Equilibrium to Extreme
Conditions](https://arxiv.org/abs/2610.18545).

## Files

| File | Description |
| --- | --- |
| [`final-models/seed_2026/nep.txt`](final-models/seed_2026/nep.txt) | Trained model M1. |
| [`final-models/seed_2027/nep.txt`](final-models/seed_2027/nep.txt) | Trained model M2. |
| [`final-models/seed_2028/nep.txt`](final-models/seed_2028/nep.txt) | Trained model M3. |
| [`final-models/seed_2029/nep.txt`](final-models/seed_2029/nep.txt) | Trained model M4. |
| [`final-models/seed_2030/nep.txt`](final-models/seed_2030/nep.txt) | Trained model M5. |
| [`nep.in`](nep.in) | NEP training input file specifying model parameters and optimization settings. |
| [`train.xyz`](train.xyz) | Development dataset containing 2,727 configurations with energies, forces and virials in extended XYZ format. |
| [`LICENSE`](LICENSE) | MIT License. |

Seeds 2026-2030 correspond to models M1-M5 in the paper. Each model used a
geometry-grouped, stratified training/validation split of approximately 95:5 from
the development dataset. `train.xyz` contains the full development set;


## Citation

If you use NEP-CuC or the dataset in your work, please cite:

```bibtex
@misc{zhou2026transferablemachinelearnedpotentialenabling,
  title = {A Transferable Machine-Learned Potential Enabling Large-Scale Copper-Carbon Simulations from Equilibrium to Extreme Conditions},
  author = {Feiyu Zhou and Wei Qiu and Yan Chen and Jiahui Liu and Yilun Liu and Shengying Yue and Penghua Ying},
  year = {2026},
  eprint = {2610.18545},
  archivePrefix = {arXiv},
  primaryClass = {cond-mat.mtrl-sci},
  url = {https://arxiv.org/abs/2610.18545}
}
```

## License

This repository is distributed under the [MIT License](LICENSE).
