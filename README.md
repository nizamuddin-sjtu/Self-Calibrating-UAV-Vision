# Self-Calibrating UAV Vision

Illumination-robust target recognition for UAV and 5G/6G aerial cyber-physical systems.

## Overview

This notebook develops a self-calibrating UAV vision workflow for color-based target recognition under illumination shift. It combines IID, cross-illumination, and leave-one-illumination-out evaluation with safe abstention policies.

## Highlights

- IID, cross-illumination, and LOIO protocols
- Illumination-specific calibration
- Reliability-guided abstention
- Paper-ready Excel tables and high-resolution figures

## Notebook

The full experiment is provided in [uav6gnetworks.ipynb](uav6gnetworks.ipynb). It is configured for Kaggle and expects the datasets described in the notebook to be attached through the **Add Input** panel.

## Running the experiment

1. Create a Kaggle notebook or open the included notebook in Jupyter.
2. Attach the required dataset and enable a GPU accelerator where noted.
3. Install the listed dependencies.
4. Run the notebook from top to bottom.

```bash
pip install -r requirements.txt
```

Datasets, trained weights, and generated experiment outputs are not stored in this repository.

## Citation

If you use this repository or the accompanying dataset in your work, please cite:

- Maitlo, N., Noonari, N., Ghanghro, S. A., Duraisamy, S., & Ahmed, F. (2024). Color recognition in challenging lighting environments: CNN approach. *2024 IEEE 9th International Conference for Convergence in Technology (I2CT)*, 1–7. https://doi.org/10.1109/I2CT61223.2024.10543537
- Maitlo, N., Noonari, N., Ahmed, F., & Hussain, A. (2026). Color-in-Context: A 12K-image dataset for color recognition under varied illumination. *Preprints*. https://doi.org/10.20944/preprints202604.0505.v1

## License

This project is available under the MIT License.
