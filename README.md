# The Disparate Benefits of Deep Ensembles

[![arXiv](https://img.shields.io/badge/arXiv-xxx.XXXXX-2ca02c.svg)](https://arxiv.org/abs/x)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Kajetan Schweighofer<sup>1</sup>, Adrian Arnaiz-Rodriguez<sup>2</sup>, Sepp Hochreiter<sup>1,3</sup>, Nuria Oliver<sup>2</sup>

<sup>1</sup> ELLIS Unit, LIT AI Lab, Institute for Machine Learning, JKU Linz, Austria  
<sup>2</sup> ELLIS Alicante, Alicante, Spain  
<sup>3</sup> NXAI GmbH, Linz, Austria  

## Summary

This project explores the impact of Deep Ensembles on algorithmic fairness, revealing that performance gains from Deep Ensembles can unevenly favor different protected groups, leading to _disparate benefits_. 
Through empirical analysis on facial analysis and medical imaging datasets, our study identifies differences in the average predictive diversity as a potential cause for the effect.
Finally, we demonstrate that post-processing techniques can effectively alleviate the negative implications on fairness due to the disparate benefits effect, reducing unfairness while maintaining performance improvements of Deep Ensembles.

![Negative Consequences of the Disparate Benefits Effect](disparate_benefits.png "Negative Consequences of the Disparate Benefits Effect")

## Setup

To change where the datasets are loaded, results are stored, etc. change paths in [constants.py](/source/constants.py).  
The environment can be installed via
```
conda env create -f environment.yml
conda activate disparate_benefits
```

## Setting up the Face Detection Experiments



## Setting up Medical Imaging Experiments

First, follow the instructions given in [setup_chexpert.py](./setup_chexpert.py) for downloading raw data and run the file to create a downsized version of it for faster experiments and move the necessary csv files containing label and protected attribute information.
An account at https://stanfordaimi.azurewebsites.net is needed to download this dataset.

Raw data can be checked with [check_chexpert.ipynb](./notebooks/check_chexpert.ipynb) and the preprocessed data and the dataset pipeline can be tested with [test_chexpert.ipynb](./notebooks/test_chexpert.ipynb).

## Replicating the Results

## Contact

If you have any questions around the code or the paper itself, feel free to reach out to schweighofer@ml.jku.at

## Citation

If you find this work useful, please cite

```
@article{schweighofer2024disparate,
    title={On Information-Theoretic Measures of Predictive Uncertainty}, 
    author={Kajetan Schweighofer and Adrian Arnaiz-Rodriguez and Sepp Hochreiter and Nuria Oliver},
    journal={arXiv preprint arXiv:xxx},
    year={2024}
}
```