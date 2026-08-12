# Quantifying parks as preventive health assets using population-scale mobility data

This repository contains the Python analysis code accompanying the Nature Communications paper:

> Hang Su, Wenjing Li, Sheng Li, Shuisong Ke, and Haoran Zhang. *Quantifying parks as preventive health assets using population-scale mobility data*. Nature Communications (accepted).

## Project overview

Urban parks are increasingly recognized as preventive-health assets, but their realized health benefits and economic performance are rarely quantified at the level of individual parks. This study combines population-scale mobility data, urban-park information, pedestrian-network distances, population distribution, land prices, and park cost estimates across Greater Tokyo.

The analysis is organized around three main questions:

1. How do mobility-inferred walking-related health benefits vary with residential network distance and park type?
2. How do park-level health benefits compare with land, construction, and operations and maintenance costs?
3. Can planning-stage information be used to screen and compare candidate locations for small urban parks?

## Analysis workflow

The four notebooks correspond to the main results and supplementary analysis in the paper:

| File | Description |
| --- | --- |
| `01_result1.ipynb` | Network-distance and distance–benefit analyses for Result 1 and Fig. 2. |
| `02_result2.ipynb` | Park-level economic accounting and discounted-payback analyses for Result 2 and Fig. 3. |
| `03_result3.ipynb` | Planning-stage benefit modelling and candidate-site analyses for Result 3 and Fig. 4. |
| `04_steps_sensitivity_analysis.ipynb` | Sensitivity analysis of inferred steps and payback outcomes. |

This is an analysis-code archive rather than a turnkey raw-data pipeline. The notebooks are not intended as a single linear `Run All` workflow; the final planning analysis requires intermediate files exchanged between `02_result2.ipynb` and `03_result3.ipynb`.

All input and output paths are project-relative, and generated files are written under `outputs/`.

## Requirements

The notebooks were developed in Python 3.11. Main dependencies include NumPy, pandas, SciPy, scikit-learn, Matplotlib, GeoPandas, Shapely, PyProj, Pyogrio/Fiona, NetworkX, OSMnx, DuckDB, PyArrow, tqdm, openpyxl, and Jupyter/IPython. Exact package versions were not locked in the original analysis environment.

## Data requirements and availability

The analyses use the following data sources:

### Public data

- **Urban parks:** Ministry of Land, Infrastructure, Transport and Tourism (MLIT), National Land Numerical Information (NLNI/KSJ), Urban Park dataset (P13): <https://nlftp.mlit.go.jp/ksj/gml/datalist/KsjTmplt-P13.html>
- **Population distribution:** MLIT NLNI/KSJ Population Concentrated Districts dataset (A16): <https://nlftp.mlit.go.jp/ksj/gml/datalist/KsjTmplt-A16-v2_3.html>
- **Land prices:** MLIT NLNI/KSJ Official Land Price Publication dataset (L01): <https://nlftp.mlit.go.jp/ksj/gml/datalist/KsjTmplt-L01-2019.html>

### Restricted mobility data

The anonymized individual-level mobile-phone location data were provided by BlogWatcher under a data-use agreement. These data are not publicly available because of privacy protections and contractual restrictions. Access may be requested from BlogWatcher, subject to their approval and applicable data-protection requirements.

Consequently, the repository contains the analysis code but does not include the restricted mobility records or mobility-derived individual-level tables.

Because the restricted mobility data are not included, the code can be inspected and adapted but cannot be used to reproduce all numerical results reported in the paper.

## Citation

Please cite the associated paper when using this code:

```text
Su, H., Li, W., Li, S., Ke, S. & Zhang, H. Quantifying parks as preventive
health assets using population-scale mobility data. Nature Communications
(accepted). DOI: to be added after publication.
```

## Contact

For questions about the paper or analysis code, please contact the corresponding author:

**Haoran Zhang**  
School of Urban Planning & Design, Peking University  
Email: [h.zhang@pku.edu.cn](mailto:h.zhang@pku.edu.cn)
