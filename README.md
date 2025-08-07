# supreme-court-coalition-analysis
Multidimensional analysis of Supreme Court justice coalition voting patterns using MDS, t-SNE, PCA, and network analysis to identify ideological coalitions and cross-party agreements.


# Supreme Court Coalition Analysis

## 🏛️ Project Overview
Multidimensional analysis of Supreme Court justice voting patterns using MDS, t-SNE, and network analysis to identify ideological coalitions and cross-party agreements.

## 🎯 Key Findings
- **t-SNE reveals clear ideological clustering** (KL divergence: 0.033)
- **MDS shows poor fit** (stress: 4.463) for this high-dimensional data
- **Cross-party coalitions** identified between justices from different appointing parties
- **Quantitative party separation index** measures institutional vs. partisan voting

## 🔧 Technologies Used
- **Python**: pandas, numpy, scikit-learn, matplotlib, plotly
- **Dimensionality Reduction**: MDS, t-SNE, PCA
- **Network Analysis**: NetworkX, coalition detection
- **Data**: Supreme Court Database (SCDB) from Washington University Law

## 🚀 Quick Start
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/yourusername/supreme-court-coalition-analysis/HEAD)

```bash
git clone https://github.com/yourusername/supreme-court-coalition-analysis.git
cd supreme-court-coalition-analysis
pip install -r requirements.txt
jupyter notebook
