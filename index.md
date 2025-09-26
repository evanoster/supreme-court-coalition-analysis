---
layout: default
title: Home
--- 

# Supreme Court Coalition Analysis

Welcome to my analysis of Supreme Court voting coalitions and judicial behavior patterns! This site showcases insights and visualizations generated from Python analysis of Supreme Court decisions using Jupyter notebooks.

## Project Overview

This project analyzes Supreme Court voting patterns to identify coalitions, examine judicial behavior, and understand decision-making trends over time. The analysis includes data cleaning, exploratory data analysis, coalition detection algorithms, and visualization of key judicial relationships and patterns.

## Key Findings

### Main Results Summary

- **Coalition Patterns**: Identification of consistent voting blocs among justices across different case types
- **Temporal Trends**: How judicial coalitions have evolved over different Supreme Court eras
- **Case Type Analysis**: Voting behavior variations across constitutional law, civil rights, and other legal domains

### Featured Visualizations

#### Coalition Network Analysis
![Coalition Network]({{ site.baseurl }}/assets/images/coalition_network.png)
*Figure 1: Network visualization showing justice voting coalitions and agreement patterns*

#### Voting Patterns Over Time
![Voting Trends]({{ site.baseurl }}/assets/images/voting_trends.png)
*Figure 2: Temporal analysis of coalition stability and ideological drift*

## Interactive Analysis

For interactive charts and detailed exploration:

<div style="width: 100%; height: 600px; border: 1px solid #ddd; margin: 20px 0;">
  <iframe src="{{ site.baseurl }}/assets/charts/interactive_chart.html" 
          width="100%" height="100%" frameborder="0">
    <p>Your browser does not support iframes. <a href="{{ site.baseurl }}/assets/charts/interactive_chart.html">View the interactive chart here</a>.</p>
  </iframe>
</div>

## Methodology

### Data Sources
- **Supreme Court Database**: Historical voting records and case metadata
- **Data Coverage**: [Specify time period and number of cases analyzed]
- **Key Variables**: Justice votes, case topics, decision dates, case outcomes

### Analysis Approach
1. **Data Cleaning**: Processing voting records, handling missing data, standardizing justice names
2. **Coalition Detection**: Network analysis and clustering algorithms to identify voting blocs
3. **Temporal Analysis**: Time-series analysis of coalition stability and changes
4. **Statistical Modeling**: Regression analysis of factors influencing coalition formation

### Tools Used
- **Python Libraries**: pandas, numpy, matplotlib, seaborn, plotly, networkx, scikit-learn
- **Specialized Tools**: Network analysis libraries for coalition detection
- **Environment**: Jupyter Notebook
- **Version Control**: Git/GitHub

## Repository Contents

### Files and Notebooks
- **[Main Analysis Notebook]({{ site.baseurl }}/your_notebook.ipynb)**: Complete analysis with code and explanations
- **Data Files**: Located in `/data/` directory
- **Generated Charts**: Static images in `/assets/images/`, interactive in `/assets/charts/`

### Code Highlights

Here's a sample of the key analysis code:

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import networkx as nx

# Load Supreme Court voting data
df = pd.read_csv('data/supreme_court_votes.csv')
print(f"Dataset shape: {df.shape}")

# Calculate justice agreement matrix
agreement_matrix = df.pivot_table(
    index='justice1', 
    columns='justice2', 
    values='agreement_rate'
)

# Create coalition network
G = nx.from_pandas_adjacency(agreement_matrix)
plt.figure(figsize=(12, 8))
nx.draw_spring(G, with_labels=True, node_color='lightblue')
plt.title('Supreme Court Justice Coalition Network')
plt.show()
```

## Results Summary

### Statistical Summary

| Metric | Value |
|--------|-------|
| Total Cases Analyzed | [Your number] |
| Time Period | [Your date range] |
| Number of Justices | [Your count] |
| Major Coalitions Identified | [Your findings] |
| Average Coalition Stability | [Your metric] |

### Legal and Political Implications

1. **Coalition Stability**: Understanding how consistent voting blocs influence court decisions
2. **Ideological Shifts**: Tracking changes in judicial philosophy over time  
3. **Predictive Insights**: How coalition patterns might inform future court behavior

## Navigation

- **[Detailed Analysis]({{ site.baseurl }}/pages/detailed-analysis)** - In-depth exploration of results
- **[Methodology]({{ site.baseurl }}/pages/methodology)** - Technical details of the analysis approach
- **[Data Dictionary]({{ site.baseurl }}/pages/data-dictionary)** - Variable definitions and descriptions
- **[GitHub Repository](https://github.com/evanoster/supreme-court-coalition-analysis)** - Full source code and data

## Contact & Collaboration

Interested in this analysis or have questions? Feel free to:
- Open an issue on the [GitHub repository](https://github.com/evanoster/supreme-court-coalition-analysis/issues)
- Connect with me on [LinkedIn](https://linkedin.com/in/yourprofile) 
- Email: your.email@example.com

---

*Last updated: {{ site.time | date: "%B %d, %Y" }}*
