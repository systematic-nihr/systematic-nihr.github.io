---
hide:
- toc
tags:
- Phase 2
- Work Streams
- Data
- AI
- Data science
- 
- Harm Reduction
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
  2. at the population level, structured feature engineering enables discovery of clinically actionable patterns. Furthermore, our approach stands out through the targeted integration of specific sensing modalities with clinical records, addressing gaps in MLTC prognosis and diagnosis by better characterising confounding variables using denser recordings and contextual data [2]. While ambient home-based sensing is already being explored, our innovation lies in the systematic integration of these data streams (more detail below). To our knowledge, no existing work comprehensively bridges the gap between intermittent clinical observations and continuous home-based monitoring in a way that offers:

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


### References
[2] https://osf.io/preprints/psyarxiv/jw37c_v1
[3] https://arxiv.org/pdf/2402.19348
[4] https://doi.org/10.1109/TBDATA.2015.2465959
[5] https://doi.org/10.1109/JPROC.2015.2460697
[6] https://arXiv.org/1707.07250
[7] https://doi.org/10.1093/bib/bbab569
[8] https://doi.org/10.1145/3649447
[9] https://doi.org/10.1038/s41467-021-23774-w
