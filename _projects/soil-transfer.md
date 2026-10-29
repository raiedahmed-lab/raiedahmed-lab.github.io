---
layout: page
title: Can soil data travel across regions?
permalink: /research/soil-transfer/
description: Instance-based transfer learning for undrained shear-strength prediction under domain shift.
img: /images/paper-tluss.png
importance: 1
status: Published study
period: '2026'
methods: Transfer learning · Kernel ridge regression · SHAP
---

<p class="research-status">PUBLISHED · GEOSYSTEMS AND GEOENVIRONMENT · 2026</p>
<p class="project-lead">Local soil observations are scarce. Data collected elsewhere can help—but only if differences between the regions are taken seriously.</p>

<p class="research-actions"><a href="https://doi.org/10.1016/j.geogeo.2026.100519">Read the article ↗</a> <a href="https://github.com/raiedahmed-lab/TL_USS_Prediction">Explore the code ↗</a></p>

{% include figure.liquid path="images/paper-tluss.png" alt="Research figure accompanying the cross-regional soil-strength transfer-learning study" caption="Research figure from the published study. The paper provides the full experimental context." %}

## Research context and objectives

Undrained shear strength is a key parameter in the assessment of foundations, slopes, and embankments. Obtaining representative measurements requires field investigation and laboratory testing, while the available observations at an individual site are often limited.

Machine learning offers a way to relate strength to routinely measured soil properties. However, a model that performs well within one region may become unreliable when applied to soils with different geological histories and engineering characteristics. Additional data are therefore useful only when their relevance to the target setting is considered.

Developed from my undergraduate thesis in Civil and Environmental Engineering at Shahjalal University of Science and Technology (SUST), this study examined instance-based transfer learning as a response to this problem. Instead of treating all observations as equally transferable, these methods adjust the influence of source samples according to their usefulness for the target prediction task.

The investigation addressed three questions:

- How strongly do the source and target datasets differ, and what happens when a model is transferred without adaptation?
- Can instance-based transfer learning improve prediction relative to a model trained only on local observations?
- How do predictive performance and stability change as the amount of local training data decreases?

## My contribution and collaboration

My contributions included conceptualization, methodology, investigation, data curation, formal analysis, software, manuscript drafting, and review and editing. The research was conducted with Fahmida Rahman, Nur Md. Robiul Hoque, and Shriful Islam. It applies and evaluates established transfer-learning methods in a geotechnical case study.

## Data and cross-regional comparison

The study combined two datasets with the same five predictors: natural moisture content, bulk density, liquid limit, plastic limit, and plasticity index. Undrained shear strength was the response variable.

| Domain | Dataset | Role in the study |
|---|---|---|
| Source | 217 complete observations selected from the Finnish FI-CLAY/14/856 database | Provides observations from an existing regional database |
| Target | 134 valid observations from field and laboratory investigation in Sylhet, Bangladesh | Provides local training observations and held-out evaluation data |

The Finnish soils predominantly represent glaciomarine and glaciolacustrine clays, whereas the target samples were obtained from shallow depths within the SUST campus in Sylhet.

The contrast extended beyond geographical separation. Mean undrained shear strength was approximately 2.23 kPa in the source dataset and 45.39 kPa in the target dataset. Differences in moisture content and plasticity further demonstrated why the datasets could not simply be assumed interchangeable.

## Modeling and evaluation approach

### Diagnosing domain shift

Maximum mean discrepancy (MMD) and earth mover’s distance (EMD) were used to characterize distributional differences between the datasets. A separate control experiment tested the practical consequences of transferring a source-trained AdaBoost.R2 model directly to the target region without adaptation.

### Comparing transfer strategies

Three instance-based methods were evaluated:

- **TrAdaBoost.R2**, which iteratively adjusts observation weights during boosting.
- **Two-Stage TrAdaBoost.R2**, which separates aspects of source-sample reweighting and target-focused learning.
- **Instance-weighted kernel ridge regression (IWKRR)**, which combines nonlinear kernel regression with weighting that reduces the influence of less relevant source observations.

A target-only AdaBoost.R2 model provided the non-transfer baseline.

The target dataset was partitioned into 80% training and 20% testing, with the source observations available to the transfer-learning models. Hyperparameter selection used the target training portion, while mutually exclusive target test data were reserved for evaluation. The principal comparison used 40 independent randomized trials, reporting mean performance and confidence intervals across trials.

### Testing sensitivity to local data availability

An ablation analysis varied the available target training observations from 30% to 100% of the 107-sample training pool, in 10% increments. The 217 source observations were held constant. This examined whether the benefits of transfer persisted when fewer local measurements were available.

## Principal findings

### Direct transfer performed poorly

The source-trained AdaBoost.R2 model achieved an R² of approximately 0.763 on source test data, but its performance deteriorated to R² = −4.482 and RMSE = 48.949 kPa when applied directly to the target dataset.

This control experiment demonstrates the central problem motivating the thesis: good performance within a source region does not establish suitability for another geological setting.

### IWKRR produced the strongest results among the evaluated models

The following values are the reported mean target-test results across the 40 trials.

| Model | Test R² | RMSE (kPa) | MAE (kPa) |
|---|---:|---:|---:|
| AdaBoost.R2 — target only | 0.8035 | 8.6749 | 6.8783 |
| TrAdaBoost.R2 | 0.8079 | 8.5778 | 6.8960 |
| Two-Stage TrAdaBoost.R2 | 0.8219 | 8.2471 | 6.4609 |
| IWKRR | 0.8763 | 6.8873 | 5.4600 |

IWKRR also exhibited the narrowest performance confidence intervals in the main comparison. The results show that the choice of transfer method matters: incorporating source data did not produce equally large or consistent gains across all approaches.

### Transfer remained useful under reduced local training data

The data-scarcity analysis found that IWKRR maintained comparatively strong performance as the target training pool was reduced. Its performance was more stable than the target-only baseline, which showed greater variability when fewer local observations were available.

This supports the potential value of selectively using existing regional data. It does not establish a universal minimum sample size or eliminate the need for local measurements.

### Density and moisture dominated model interpretation

SHAP analysis identified density and moisture content as the most influential predictors, while the Atterberg indices had lower global importance in this dataset. Higher density generally contributed to higher predicted strength, while higher moisture content generally contributed to lower predictions.

Density also showed comparatively small source–target distributional divergence. Together, these findings suggest that successful transfer in this case relied partly on predictors whose distributions remained relatively compatible across regions.

SHAP describes how the fitted model uses its inputs. These patterns should not be interpreted as independent causal effects or as a universal ranking of soil properties.

## Significance and limitations

The main contribution of this thesis is a cross-regional evaluation that connects distributional differences, predictive performance, data availability, and model interpretation. It demonstrates why transfer should be evaluated explicitly rather than assuming that a larger combined dataset will necessarily produce a better local model.

The evidence is limited to one source–target pairing, five predictors, and the investigated algorithms. Repeated random splits assess variability within the available dataset; they do not establish performance at independent sites, in other soil types, or under different testing conditions.

Because the comparison used a target-only AdaBoost.R2 baseline, it also does not isolate the benefit of source-data weighting relative to every possible target-only learner. A target-only kernel ridge regression comparison would help separate the effects of the underlying model from those of transfer.

Further work should examine multiple source regions, independent site-level validation, measurement compatibility, and prediction uncertainty. Practical engineering use would require additional verification against site investigation data and the requirements of the intended design application.

## Publication, code, and data

Nishat, R. A., Rahman, F., Hoque, N. M. R., and Islam, S. (2026). Transfer learning for undrained shear strength prediction: A case study with instance-based transfer. *Geosystems and Geoenvironment*, 5, Article 100519.

- [Published article ↗](https://doi.org/10.1016/j.geogeo.2026.100519)
- [Public repository ↗](https://github.com/raiedahmed-lab/TL_USS_Prediction)

[← All research]({{ '/research/' | relative_url }})
