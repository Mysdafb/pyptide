# pyptide

pyptide is a lightweight, high-performance Python library designed for streamlined peptide and protein exploration. Whether you are analyzing natural sequences, engineering novel antimicrobial peptides, or building predictive bioactivity models, `pyptide` bridges the gap between raw sequence data and machine learning-ready features.

## Key Features

* Robust FASTA Parsing: Seamlessly load, filter, and manipulate large protein and peptide sequence files with built-in validation.

* Comprehensive Molecular Descriptors: Automatically compute physicochemical properties, amino acid composition, atomic weights, hydrophobicity indices, and structural descriptors.

* Machine Learning Integration: Easily transform sequences into feature matrices optimized for scikit-learn, XGBoost, or deep learning pipelines to predict properties like toxicity, bioactivity, and stability.

## Installation
```Bash
pip install pyptide
```

## Quick Start

Here is a quick example of how to load a FASTA file, compute descriptors, and prepare data for modeling:

```Python
from pyptide import SequenceLoader, DescriptorCalculator

# 1. Load sequences from a FASTA file
loader = SequenceLoader("peptides.fasta")
sequences = loader.get_sequences()

# 2. Compute molecular descriptors
calculator = DescriptorCalculator(
    descriptors=["molecular_weight", "isoelectric_point", "hydrophobicity"]
)
features = calculator.compute(sequences)

print(features.head())
```
