<h1 align="center">Self-Calibrating UAV Vision</h1>

<p align="center">
  <a href="https://doi.org/10.1109/I2CT61223.2024.10543537"><img src="https://img.shields.io/badge/Paper-IEEE_I2CT-2f6f9f.svg" alt="Paper"></a>
  <a href="uav6gnetworks.ipynb"><img src="https://img.shields.io/badge/Notebook-uav6gnetworks.ipynb-F37626.svg" alt="Notebook"></a>
  <a href="https://www.kaggle.com/nizamuddinmaitlo"><img src="https://img.shields.io/badge/Datasets-Kaggle-20BEFF.svg" alt="Kaggle datasets"></a>
  <a href="https://scholar.google.com/citations?user=bvyKhaEAAAAJ&hl=en"><img src="https://img.shields.io/badge/Publications-Google_Scholar-4285F4.svg" alt="Google Scholar"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/Code_License-MIT-2ea44f.svg" alt="MIT License"></a>
</p>

<p align="center"><b>Nizamuddin Maitlo</b></p>

<p align="center">Illumination-robust target recognition for UAV and 5G/6G aerial cyber-physical systems.</p>

## 🔥 Overview

This notebook develops a self-calibrating UAV vision workflow for color-based target recognition under illumination shift. It combines IID, cross-illumination, and leave-one-illumination-out evaluation with calibration and reliability-guided abstention.

## ✨ Contributions

- IID, cross-illumination, and LOIO protocols.
- Illumination-specific confidence calibration.
- Reliability-guided safe abstention.
- Research-ready Excel tables and high-resolution figures.

## 🧪 Experimental protocol

- Images are indexed from the color and illumination folder hierarchy.
- Evaluation separates in-distribution and held-out lighting conditions.
- Abstention policies are selected using validation confidence and evaluated on held-out samples.

## 📓 Notebook

The complete experiment is implemented in [uav6gnetworks.ipynb](uav6gnetworks.ipynb). Data discovery, preprocessing, training, evaluation, and export steps are kept together so the workflow can be reviewed and rerun from top to bottom.

## 🛠️ Installation

Create a Python environment and install the listed dependencies:

```bash
python -m pip install -r requirements.txt
```

The notebook is configured for Kaggle. A CUDA-capable GPU is recommended where GPU training is enabled.

## 📦 Datasets

Datasets, trained weights, and generated experiment outputs are not stored in this repository.

| Resource | Purpose | Link |
|---|---|---|
| Different Colors in Challenging Lightening v2 | Illumination-robust UAV target recognition | [Kaggle dataset](https://www.kaggle.com/datasets/nizamuddinmaitlo/different-colors-in-challenging-lightening-v2) |

On Kaggle, attach the dataset through **Add Input** before running the notebook. External datasets remain subject to the licenses and terms on their source pages.

## 🚀 Running the experiment

### Kaggle

1. Upload or import [uav6gnetworks.ipynb](uav6gnetworks.ipynb).
2. Attach the dataset listed above through **Add Input**.
3. Enable a GPU accelerator when required by the configured model.
4. Run the notebook from top to bottom.

### Local Jupyter

```bash
python -m pip install -r requirements.txt
jupyter notebook uav6gnetworks.ipynb
```

Dataset paths may need to be changed when running outside Kaggle.

## ♻️ Reproducibility

- Keep the documented train, validation, and test protocol unchanged when comparing models.
- Fit thresholds, calibration parameters, and feature transformations without using final test labels.
- Record the random seed, package versions, accelerator, and dataset version for each run.
- Treat saved tables and figures under the notebook's output directory as generated artifacts rather than source files.

## 📚 Paper information

The publications below provide the challenging-light color-recognition foundation and the dataset descriptor used by this research line.

| Publication | Venue | Year | Link |
|---|---|---:|---|
| Color Recognition in Challenging Lighting Environments: CNN Approach | 2024 IEEE 9th International Conference for Convergence in Technology (I2CT), 1–7 | 2024 | [DOI](https://doi.org/10.1109/I2CT61223.2024.10543537) |
| Color-in-Context: A 12K-Image Dataset for Color Recognition Under Varied Illumination | Preprints | 2026 | [DOI](https://doi.org/10.20944/preprints202604.0505.v1) |

## ⭐ Citation

For research building on this repository, cite the relevant publication or dataset descriptor:

```bibtex
@inproceedings{maitlo2024color,
  title     = {Color Recognition in Challenging Lighting Environments: CNN Approach},
  author    = {Maitlo, Nizamuddin and Noonari, Nooruddin and Ghanghro, Sajid Ahmed and Duraisamy, Sathishkumar and Ahmed, Fayaz},
  booktitle = {2024 IEEE 9th International Conference for Convergence in Technology (I2CT)},
  pages     = {1--7},
  year      = {2024},
  doi       = {10.1109/I2CT61223.2024.10543537}
}
```

```bibtex
@article{maitlo2026colorincontext,
  title   = {Color-in-Context: A 12K-Image Dataset for Color Recognition Under Varied Illumination},
  author  = {Maitlo, Nizamuddin and Noonari, Nooruddin and Ahmed, Fayaz and Hussain, Afifa},
  journal = {Preprints},
  year    = {2026},
  doi     = {10.20944/preprints202604.0505.v1}
}
```

## ⚠️ Scope and limitations

The notebook evaluates image classification and abstention on a fixed dataset; it does not validate detection range, motion blur, camera stabilization, or closed-loop UAV navigation in flight.

## 📄 License

Repository code is released under the [MIT License](LICENSE). Datasets and publications retain their own licenses and terms.

## 🤝 Acknowledgements

The experiments use public datasets, open-source Python libraries, and Kaggle compute infrastructure. We thank the dataset contributors and software maintainers who support reproducible research.
