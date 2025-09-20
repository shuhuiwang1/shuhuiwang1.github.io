---
permalink: /
title: "Brief introduction"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am currently a PhD student in Computational Biology, in [Machine Learning and Learning Systems Lab](https://www.lamsade.dauphine.fr/wp/miles/) of  Dauphine Univeristy-PSL and [Biology and Evolution Lab](https://www.lbe.espci.fr/home/) of ESCPI-PSL. The PhD thesis is under the supervision of [Alexandre Allauzen](https://allauzen.github.io/) and [Philippe Nghe](https://scholar.google.com/citations?hl=fr&user=MF7e9eAAAAAJ&view_op=list_works&sortby=pubdate).

My research focused on leveraging deep learning methods to predict diverse biological interactions. My work integrates cutting-edge machine learning techniques with complex biological data, aiming to enhance our understanding and capabilities in areas such as drug discovery and disease modeling. I have a strong interest in precision medicine, generative modeling, drug design, and optimizing drug screening processes. I expect to complete my PhD by December and am actively seeking a postdoctoral position in precision medicine, where I can continue applying and expanding my expertise at the intersection of AI and biomedical research.

Summary of PhD thesis
======
The ultimate goal of this research is to facilitate the development of digital twins in personalized medicine, where AI-driven models automate drug discovery, optimize treatment strategies, and accelerate drug screening.
This research is structured into three key layers:
- Gene Exploration – Understanding gene interactions using a data-driven model to derive biological insights.
- Drug Response Prediction – Designing models to analyze high-dimensional gene expression data and predict the drug response of cancer cell post-drug administration.
- Drug Combination Therapy – Utilizing active learning to accelerate the discovery of synergistic drug combinations, improving treatment efficacy while minimizing toxicity and resistance.


Gene-gene interaction level 
---
<img src='/images/fig_dlim.png'>

In disease research and drug design, understanding genetic interactions enhances our understanding of disease evolution, enabling us to develop targeted treatments and personalized medicine based on disease-associated genes. However, from genes to observed fitness such as cancer cell inhibition ratio,  they involve multiple biophysical traits that interact in a highly nonlinear manner—ultimately changing the fitness landscape. In this study, we aim to build models for uncovering genotype-to-fitness mapping, that not only capture complex gene interactions but also provide biological insights into how molecular functions influence fitness.

We propose a machine learning approach for interpretable genotype-to-fitness mapping, the Direct-Latent Interpretable Model (D-LIM). The neural network is built on a strong hypothesis: mutations in different genes cause independent effects in phenotypes, which then interact via non-linear relationships to determine fitness. D-LIM predicts interpretable genotype-to-fitness maps with state-of-the-art accuracy. D-LIM offers interpretable features reminiscent of mechanistic models: the inference of phenotypes, identification of trade-offs, and fitness extrapolation outside of the data domain. 


Gene-drug interaction level 
---
<img src='/images/fig_dora.png'>

Predicting cellular responses to chemical perturbations poses a significant challenge due to the complex interactions within genetic and protein networks. Recent advancements in single-cell transcriptomics have provided insights into molecular mechanisms at unprecedented resolution. This information allows us to develop computational methods to predict cell states, specifically, whether the cells survive or are inhibited after drug administration based on gene expression change.  Additionally, we aim to identify biomarkers associated with cancer suppressors. This type of research is crucial for developing new drugs that target these biomarkers and optimize the drug dosages. 

To effectively model the perturbations induced by drug treatments and cell line variations defined by single-cell RNA sequencing (scRNA-seq) data, we developed a drug dosage response autoencoder model (DORA). This model is specifically designed to simulate cellular state transitions in response to variations of drug dosages, providing insights into how various treatments shift cellular states in a low-dimensional latent space.  Using the DORA’ latent representations, we further predicted drug effects on cancer cell states, achieving superior accuracy (PR-AUC reached 0.81). Employing feature importance analysis, we successfully identified a well-known oncogene BRCA1 and SMC1A which is a predictive biomarker for drug usage and some other genes related to tumor suppressor. The manuscript of this work is under preparation. 


Drug-drug interaction level 
---
<img src='/images/fig_drugsynergy.png'>


In cancer treatment, monotherapy often leads to high toxicity and drug resistance. To improve clinical outcomes, combination therapy is commonly used. Here, we focus on synergistic drug combinations, where the combined effect of two drugs is greater than the sum of their individual effects. Identifying these combinations is crucial for enhancing treatment efficacy. However, identifying synergistic drug combinations requires exploring a large space of conditions, which increase exponentially with the number of drugs and cell lines. 

While AI, particularly deep learning, has advanced synergy predictions, its effectiveness is limited by the low occurrence of synergistic drug pairs (~1%-10%). Active learning, which integrates experimental testing into the learning process, has been proposed to address this challenge. In this work, we explore the key components of active learning to provide recommendations for its implementation. This workflow can help biologist to design specific active learning procedures for their own research. In our study, we found that active learning can discover 60% of synergistic drug pairs by only exploring 10% of combinatorial space, which can significantly reduce expensive drug screening measurements. This work is published in Scientific reports. 
