---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

I am **Raied Ahmed Nishat** — a Civil & Environmental Engineering graduate (SUST, Bangladesh) and currently an **Adjunct Lecturer** at Leading University, Sylhet. I am also a **Research Assistant** at SUST, working at the intersection of **machine learning and geotechnical engineering**.

My work focuses on applying transfer learning, and hybrid ML models to soil strength prediction, foundation settlement. I also have experience in seismic risk assessment research. My undergraduate thesis, *A Transfer Learning Approach for Soil Strength Prediction* introduced instance-based transfer learning to cross-regional geotechnical datasets. I am actively seeking a **PhD position in ML / Computational Geomechanics** for Spring 2027/Fall 2027.

I am open to research collaborations. Feel free to reach out!

Thanks for dropping by!

# 🔬 Research Interests

- ML & Transfer Learning for Geotechnics
- Probabilistic & Transformer-Based Models  
- Soil Strength & Stabilization
- Seismic Risk & Resilience Assessment  
- Hydroclimatic Trend Analysis  

I am passionate about bridging classical engineering problems with data-driven approaches.

# 🔥 News

- 🎉 2026.03 – Transfer learning paper (USS prediction) published at *Geosystems and Geoenvironment (Elsevier)*
- 🎉 2026.02 - Joined as **Adjunct Lecturer**, Dept. of Civil Engineering, Leading University, Sylhet, Bangladesh
- 📢 2026.02 – Abstract accepted on Foundation Settlement Prediction with TabPFN at ICCESD 2026, KUET
- 🎉 2026.01 – Article on Kaolin soil stabilization was accepted for peer review.
- 🎉 2025.10 – Article on TL for soil strength prediction was accepted for peer review.
- 🎉 2025.04 – Published an inauguration Video for ICERIE 2025, SUST [YouTube Link](https://youtu.be/jUUbEcVFshs?si=Eko4HVqP4Z-UD90E)

# 📝 Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">GG 2025</div><img src='images/paper-tluss.png' alt="TL for USS Prediction" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Instance-Based Transfer Learning for Cross-Regional Prediction of Undrained Shear Strength of Soils](https://doi.org/10.1016/j.geogeo.2026.100519)  

**Raied Ahmed Nishat**, Fahmida Rahman, Nur Md. Robiul Hoque, Dr. Shriful Islam  

*Geosystems and Geoenvironment (Elsevier), 2026*  

- **Core contribution:** Designed and implemented three instance-based transfer learning frameworks: TrAdaBoost.R2, Two-Stage TrAdaBoost.R2, and Importance Weighted Kernel Ridge Regression (IWKRR) to predict undrained shear strength (USS) of Bangladeshi soils using source data from Finnish soil database.
- Identified core research gap: cross domain applicability. Resolved domain covariate shift through instance re-weighting strategies.
- Applied SHAP-based interpretability to decompose feature contributions and validate geotechnical consistency of learned transfer weights.

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">AJSE 2026</div><img src='paper-embankment.png' alt="Soil stabilization with fly ash, lime and polyester fiber" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Strength and mechanical behavior of fly ash and lime stabilized embankment soil reinforced with polyester fiber](#)  

Shriful Islam, Ananya Soheli Chowdhury, **Raied Ahmed Nishat**, Mohsina Faiza Naba, Md. Nazmul Islam Rafi

*Arabian Journal of Science and Engineering (Springer), 2026 (Under Review)*  

- Experimental study on performance improvement of expansive Sunamganj haor embankment soil with fly ash, lime and polyester fiber reinforcement.
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">IJGG 2026</div><img src='images/paper-kaolin.jpg' alt="Kaolin stabilization with lime and activated slag" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Effect of lime and alkali-activated LRF slag on geotechnical properties and microstructural behavior of kaolin clay](#)  

Shriful Islam, **Raied Ahmed Nishat**, Arnob Sutradhar, Nur Md. Robiul Hoque, Md. Nazmul Islam Rafi, Md. Sohel Rana

*International Journal of Geosynthetics and Ground Engineering (Springer), 2026 (Under Review)*  

- Explores the chemical stabilization of kaolin using lime and NaOH-activated steel slag.
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">TJRRI 2025</div><img src='images/paper1.png' alt="Brahmaputra-Jamuna Study" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Investigating the Trends of Rainfall and Discharge along the Brahmaputra-Jamuna River System](https://rri.portal.gov.bd/sites/default/files/files/rri.portal.gov.bd/page/4787fdda_a3b5_4185_806e_5f5480c8edbc/2025-06-06-15-43-90cf05b8b611bbd58f562f6b8e43b366.pdf#page=83)

**Raied Ahmed Nishat**, Mahfujur Rahman Joy

*Technical Journal of River Research Institute, 17(1), 2025*  

[**Project**](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=f-9zK80AAAAJ&citation_for_view=f-9zK80AAAAJ:u-x6o8ySG0sC) <strong><span class='show_paper_citations' data='f-9zK80AAAAJ:u-x6o8ySG0sC'></span></strong>
- A comprehensive hydroclimatic trend analysis using visual and statistical tools to assess seasonal discharge variability under changing climate conditions.
</div>
</div>

<div class='paper-box'>
  <div class='paper-box-image'>
    <div>
      <div class="badge">DCE (Under Review)</div>
      <img src='images/paper-soil-review.PNG' alt="Soil ML Review" width="100%">
    </div>
  </div>
  <div class='paper-box-text' markdown="1">

[Machine Learning in Soil Strength Prediction: A Review](#)  
**Raied Ahmed Nishat**, Fahmida Rahman  
*Submitted to Discover Civil Engineering (Springer)*  
- Critical survey of classical and modern ML approaches (ANN, SVM, tree ensembles, deep learning) for predicting soil strength parameters.
- Identifies domain adaptation and physics-informed learning as key open challenges.
</div>
</div>

<div class='paper-box'>
  <div class='paper-box-image'>
    <div>
      <div class="badge">HESS (Under Review)</div>
      <img src='images/paper-ganges-ml.png' alt="Ganges Water ML" width="100%">
    </div>
  </div>
  <div class='paper-box-text' markdown="1">

[Hydroclimatic Trend Analysis and Machine Learning-Based Water Level Prediction for the Ganges (Padma) River Basin](#)  
Mahfujur Rahman Joy, **Raied Ahmed Nishat**  
*Submitted to River (Wiley)*  
- Trend analysis of rainfall, discharge and temperature with machine learning forecasting models for water level prediction in the Ganges basin.

</div>
</div>

# 📝 Conference Papers

<div class='paper-box'>
  <div class='paper-box-image'>
    <div>
      <div class="badge">ICCEI 2025</div>
      <img src='images/paper-ucsprediction.png' alt="UCS Prediction Model" width="100%">
    </div>
  </div>
  <div class='paper-box-text' markdown="1">

[Prediction of Soil Unconfined Compressive Strength with Decision Tree-Based Hybrid Machine Learning Model](#)  
**Raied Ahmed Nishat**, Fahmida Rahman, Nur Md. Robiul Hoque, Md. Nazmus Islam Rafi, Dr. Shriful Islam  
*Accepted at International Conference on Civil Engineering Research & Innovations (ICCEI) 2025 – RUET*  
- Proposes a hybrid model combining Decision Trees with metaheuristic optimization to predict UCS of soils, benchmarked against traditional regressors.

</div>
</div>

<div class='paper-box'>
  <div class='paper-box-image'>
    <div>
      <div class="badge">ICCESD 2026</div>
      <img src='images/paper-settlement.png' alt="Settlement Prediction Model" width="100%">
    </div>
  </div>
  <div class='paper-box-text' markdown="1">

[A Probabilistic Transformer-Based Machine Learning Model for Shallow Foundation Settlement Prediction](https://www.researchgate.net/publication/401704041_A_Probabilistic_Transformer-Based_Machine_Learning_Model_for_The_Prediction_of_Settlement_for_Shallow_Foundation)  
**Raied Ahmed Nishat**, Abdun Nur Tusar, Dr. Shriful Islam and Moriam Akter Monni 
*8th International Conference on Civil Engineering for Sustainable Development (ICCESD 2026) – KUET*  
- Introduced TabPFN to the field of geotechnical engineering. Shallow foundation settlement prediction performance using TabPFN achieved higher predictive performance when compared to baseline models in literature.

</div>
</div>
# 🔬 Undergraduate Thesis

- **A Transfer Learning Approach for Soil Strength Prediction**  
  Raied Ahmed Nishat, Fahmida Rahman  
  *Advisor: [Dr. Shriful Islam](https://www.sust.edu/departments/cee/faculty/sharif-cee@sust.edu), [Nur Md. Robiul Hoque](https://www.sust.edu/departments/cee/faculty/hoque-cee@sust.edu)*  
  - Submitted manuscript based on this work is currently published at Geosystems and Geoenvironemnt.
  - Applies domain adaptation to predict Undrained Shear Strength using cross-regional datasets.

# 🔬 Ongoing Research

1. **Seismic Risk and Resilience Analysis of Chittagong**  
[Ram Krishna Mazumder](https://scholars.georgiasouthern.edu/en/persons/ram-krishna-mazumder/), Raied Ahmed Nishat, [Abul Hasnat](https://scholar.google.com/citations?user=iOVyW58AAAAJ&hl=en)
  *Manuscript in preparation*  
  - Evaluates seismic vulnerability and resilience using spatial analysis and structural fragility modeling.

2. **Sustainable Stabilization of Clay Soil Using Rice Husk Ash, Induction Furnace Slag, and Lime**  
  *Advisor: Dr. Shriful Islam*  
  - Manuscript writing in progress.
  - Investigates mechanical enhancement of clay soils through combined stabilization Rice husk ash, Induction furnace slag and Lime.  
  - Contributions: Research planning, data interpretation, documentation, and manuscript review.

3. **Alkali activated slag for collapsible soil stabilization: A case study in Sylhet, Bangladesh**
   *Supervisor: Dr. Shriful Islam*  
  - Investigates the practical improvement of collapsible soils found in sylhet with the use of industrial by-product LRF and its activated form. 
  - Contributions: Research planning, experimentation, data interpretation, documentation, and manuscript preparation.

# 📖 Education

| Degree | Institution | Year | Result |
|--------|-------------|------|--------|
| **B.Sc. (Engg.), Civil & Environmental Engineering** | Shahjalal University of Science & Technology (SUST) | 2025 | CGPA 3.64/4.00 |
| HSC (Science) | Al Amin Academy, Chandpur | 2019 | GPA 5.00/5.00 |
| SSC (Science) | Hasan Ali Govt. High School, Chandpur | 2017 | GPA 5.00/5.00 |

---

# 💼 Professional Experience

**Adjunct Lecturer**
Department of Civil Engineering, Leading University, Sylhet &nbsp; *(Jan 2026 – Present)*  
Teaching regular courses and mentoring undergraduate students in conducting research, from literature review and experimental planning to data analysis and scientific writing.

**Junior Project Engineer**
CRTC, SUST &nbsp; *(Dec 2025 – Jan 2026)*  
Supervised SPT field operations at Sylhet Gas Field; laboratory soil classification, strength testing, and geotechnical report preparation.

**Research Assistant**
Department of CEE, SUST &nbsp; *(Apr 2024 – Present)*  
Advisor: [Prof. Dr. Shriful Islam](https://www.sust.edu/departments/cee/faculty/sharif-cee@sust.edu) 
Experimental and computational ML-based geotechnical modeling; data analysis and manuscript preparation.


---

# 🎖 Honors and Awards
- Semifinalist, Hult Prize at SUST, 2023
- Chandpur District Parishad Higher Secondary Merit Scholarship
- Merit Scholarship, Secondary School Certificate
- Chandpur District Parishad Secondary School Merit Scholarship
- Ashutosh Education Scholarship, Brahmanbaria

# 🧾 Training and Certifications
- *2025.10* “A complete guide to the key components of a research article” offered by Wiley Researcher Academy.
- *2025.08* “Job Readiness Training” provided by Career Hub Powered by BRAC.
- *2024.12* “Introduction to GIS Mapping” offered by University of Toronto in Coursera.

# 🎨 Beyond Research

Outside of research, I serve as **General Secretary of AAJ Muktomancho** (SUST's cultural organization), where I lead the 15th executive committee and convened a 1,000+ attendee cultural concert. I enjoy graphic design, video editing, and playing the guitar and flute.
