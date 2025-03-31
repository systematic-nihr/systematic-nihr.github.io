---
hide:
- toc
tags:
- Phase 2
- Work Streams
- Data
- AI
- Data science
- Natural Language Processing and Understanding
---

# WS2 Data and AI Connected Care

**Context**: Most data available for predictive care is stored in NHS electronic health records (EHRs) from
infrequent patient encounters. The data represent the ‘pitstops’ not ‘journeys’ of care. Yet most opportunities for prevention arise between clinical encounters. Better MLTC prevention and care needs ecologically valid tools for capturing more of the continuous patient experience, accounting for the
longitudinal and combinatorial nature of MLTCs. Innovations should complete the picture across primary-, secondary- and social-care data and interpolate between siloed, sparse and irregular EHR data. In addition, more useful predictive content needs exposing from narrative EHR data.

**Aims**: This WS will develop methodology for better understanding person-centred MLTC journeys via:
  1. **Technology for data collection and harvesting**: re-purposing commodity technology for passive
(wearables and nearables/ambient) and active sensing (experience sampling methods adapted for patient-facing clinical deployment);
  2. **Data fusion and processing for actionable insight**: developing an open interoperability platform to harmonise algorithms (statistical, machine learning / AI) and data from diverse commodity devices and technologies;
  3. **Natural Language Processing** as a core information processing and user-interface technology (LLMs, conversational- and agentic-AI) to include rigorous benchmarking, performance evaluation, and trustworthiness;
  4.  **Privacy preservation**: a responsible, sustainable engineering approach to (1-3) that preserves individual privacy.

## Providing Actionable Insights
Our engineering approach adopts co-design principles to ensure solutions are actionable, sustainable, and equitable. We specifically target critical gaps between clinical diagnosis and patient self-management, integrating contextual physical and psychological dimensions. We acknowledge the concern over potential 'parameter soup' in ambient sensing applications; however, our team employs a methodologically rigorous hierarchical integration approach where: 

  1. at the individual patient level, each ambient parameter is carefully contextualised with relevant physiological and behavioural information to establish meaningful relationships;
  2. at the population level, structured feature engineering enables discovery of clinically actionable patterns. Furthermore, our approach stands out through the targeted integration of specific sensing modalities with clinical records, addressing gaps in MLTC prognosis and diagnosis by better characterising confounding variables using denser recordings and contextual data [1](#refs).

While ambient home-based sensing is already being explored, our innovation lies in the systematic integration of these data streams (more detail below). To our knowledge, no existing work comprehensively bridges the gap between intermittent clinical observations and continuous home-based monitoring in a way that offers:
  * Enhanced Clinical Prediction and Decision-Support
  * Personalised Support for Self-management
  * Context-Aware Recommendations
  * Proactive Interventions
  * Feedback Loop for Continuous Improvement

This technical integration recognises the bidirectional relationship between mental and psychological health in MLTCs, where psychological factors can exacerbate physical symptoms and vice versa. By capturing and analysing these interactions, our system provides personalised, context-aware support addressing the whole person rather than isolated conditions.  For example, a patient with hypertension, atrial fibrillation, chronic lung disease and an anxiety disorder presents multiple monitoring challenges. Our integration strategy addresses this through a hierarchical approach, starting with basic sensing monitoring followed by more contextual analysis:

  * Contextual Blood Pressure (BP) Monitoring: Ambient/wearable sensors detect activity levels and stress indicators, providing clinically relevant context for interpreting BP and ECG readings
  * Sleep Pattern Analysis: Bedroom ambient sensors capture restlessness and breathing patterns that correlate with arrhythmia episodes or exacerbations of lung disease
  * Psychological State Assessment: Natural language processing of voice patterns during routine interactions detects linguistic markers of anxiety and mood fluctuations
  * Behavioural Routine Analysis: Activity pattern recognition identifies disruptions in daily routines that often precede psychological decompensation in MLTCs
  * Biopsychosocial Integration Engine: Our systems engineering approach correlates physiological indicators (heart rate variability, sleep disruption) with psychological state markers (voice sentiment, linguistic content) and behavioural patterns
  * Adaptive Intervention Triggering: The patient digital twin integrates these multidimensional inputs to guide better interventions

## Multi-source Data Fusion
Fusing data from multiple sources is an active research challenge for healthcare, especially MLTC care [2](#refs). We will focus on fusion at the feature and decision levels rather than the data level - i.e. mid-/late-stage not early-stage fusion [3](#refs). Feature-level techniques involving matrix- and tensor-decomposition methods are well-studied candidates [4-6](#refs), requiring a common representation and sharing computational principles with deep-learning, especially representation learning such as encoder-decoder models. 

More recently, flexible transformer-based models [7](#refs) and graph neural networks [8](#refs) have shown promise but remain untested for multi-scale and temporally/spatially complex data that are common in MLTCs. We anticipate maintaining separation of sources at the data and feature levels, and using “source” or “modality” expert approaches – e.g. one group of experts on temporally-coarse clinical data, another on high-temporal-resolution wearable data. We will then bring experts together in a ‘mixture-of-experts’ approach using ensemble and meta-learning (e.g. fusion at the decision-level) and weighted voting or expert-output averaging. This approach is easier to interrogate than those that fuse data earlier. It offers clear relative contributions and uncertainty quantification of different sources. In addition, it de-risks model development. Individual experts can be validated and may have value in their home source even if a late-fusion / mixture-of-experts approach fails to be useful. 

## Large Language Models for Natural Language Processing
A common concern with LLM-based approaches to natural language processing and understanding (NLP/U) are that vast amounts of training data are required and expensive compute resource are required to train these models.  Until recently, developing application-specific LLMs required either domain adapatation and transfer learning to revise pre-trained LLMs, or, to adopt cloud-based "as a service" LLMs like Claude or ChatGPT and use prompt engineering methods to develop the desired functionality.  To develop the functionality required from driver projects P4 and P5 (as well as the NLU interfaces for applications patient-facing technology in P1) the former is prohibitively expensive and impractical.  The latter approach (prompt engineering) was difficult to justify because "as a service" LLMs could not guarantee the security and privacy of confidential medical information being transmitted and processed outside of secure data environments required by the NHS.  However, with the advent of [quantised LLMs such as gemma3](https://ollama.com/library/gemma3) derived from industry-leading foundation models for question answering, summarisation, and 'reasoning', it is possible to develop prompt-based functionality locally (i.e. privately, on a local installation of ollama) on a single GPU with performance approaching that of the ''full precision'' model.  These recent advances in LLM technology enable our LLM-based work -- critical for the implementation of P4 and P5 -- to re-use existing (but quantised) foundation models, averting the needs for unrealistically large amounts of data or excessive compute resources.  Our approach combining prompt engineering with validation of performance, ground-truthing via benchmarks and acceptability/usability is specified on pages 8, 9 and 17 of the proposal.


## Privacy Preservation
  * **Implement ε-differentially private stochastic gradient descent** (DP-SGD) with adaptive noise calibration to ensure mathematical privacy guarantees while training robust machine learning models for multi-modal health data
  * Optimize the **privacy-utility trade-off through gradient perturbation techniques** that selectively apply noise based on parameter sensitivity analysis; our preliminary results demonstrate performance improvement of DP models of more than 10% by leveraging structured sparsity patterns in the models' gradient manifolds during training
  * Implement **model compression pipeline combining knowledge distillation with quantization-based training and pruning techniques** to reduce model size, while maintaining accuracy within 3% of full-sized models, ensuring deployment feasibility on resource-constrained devices in home environments
  * Develop **data anonymization frameworks that exploit local differential privacy**, thus enable on-device computation while preserving raw data confidentiality
  * Conduct **rigorous empirical privacy assessments** through model inversion attacks, membership inference attacks, and attribute inference attacks to quantify potential information leakage under realistic adversarial scenarios

## Frameworks for regulatory-compliant healthcare AI evaluation
Our clinical evaluation of machine learning models builds on Steyerberg and Vergouwe [9](#refs), with the validity of our prediction models assessed in fully independent data through the four key measures: 1) calibration in the large, 2) calibration slope, 3) discrimination performance established both with internal and external validation, 4) decision-curve analysis.

We will apply the PROBAST-AI framework, a risk-of-bias assessment tool specifically designed for AI-based prediction models to ensure methodological rigor [10](#refs) and the DECIDE-AI framework which guides the evaluation of AI systems during early clinical implementation, focusing on iterative improvement and safety monitoring [11](#refs). Where appropriate we will apply extended guidelines incorporating additional safeguards that encompass fairness, explainability, privacy-preservation and interoperability, all of which are crucial for developing trustworthy AI prediction models in healthcare [12-15](#refs).

<a id="refs"></a>
### References
1. https://osf.io/preprints/psyarxiv/jw37c_v1
2. https://arxiv.org/pdf/2402.19348
3. https://doi.org/10.1109/TBDATA.2015.2465959
4. https://doi.org/10.1109/JPROC.2015.2460697
5. https://arXiv.org/1707.07250
6. https://doi.org/10.1093/bib/bbab569
7. https://doi.org/10.1145/3649447
8. https://doi.org/10.1038/s41467-021-23774-w
9. https://doi.org/10.1093/eurheartj/ehu207
10. https://doi.org/10.1136/bmjopen-2020-048008
11. https://doi.org/10.1038/s41591-022-01772-9
12. https://doi.org/10.48550/arXiv.2501.09628
13. https://doi.org/10.1038/s41746-021-00549-7
14. https://doi.org/10.1093/eurheartj/ehac238
15. https://bmvc2024.org/proceedings/902/
