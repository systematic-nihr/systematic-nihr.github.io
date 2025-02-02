---
hide:
- toc
tags:
- Stage 1
- Systems Science
- Systems engineering
- computational models
- statistical models
- mathematical models
- 
---

# Definition
We propose 2nd-order approaches as those most aligned with systems engineering in healthcare (Clarkson 2018; RAE, 2017). 

In common with 1st-order approaches, systems are treated as ontological entities (i.e. a collection of components and dependencies that exists “in the real world”) at a defined level of abstraction.  2nd-order approaches also make use of and deliver formal models but differ from 1st-order approaches by allowing

 * specification of a system with broad and imperfectly specified boundaries
 * more tolerance for uncertainty and “unknowns”
 * less emphasis on analytical tractability and instead, numerical approximation and simulation methods are common; for example discrete event simulation models (Vázquez-Serrano, 2021), system dynamics (Sterman et al. 2015) or when detailed enumeration of a system’s components is difficult, statistical process control (Benneyan, Lloyd, and Plsek 2003). 

Qualitatively, 1st- and 2nd-order approaches differ because:

 * 1st-order models usually assume a mechanistic (often deterministic, law-like) relationship between system inputs and outputs
 * feedback -- either negative (damping) or positive (amplifying) -- is rarely explicitly modelled in 1st-order systems to maintain the tractability of the models
 * 2nd-order models allow for sophisticated behaviour-based descriptions of components (e.g. modelling clinicians as agents, with beliefs, goals and repetoires of actions having consequences external to the agent)
 * 2nd-order models allow for complex dependencies (e.g. the behaviour of one component or actor  has effects on others that may not be immediately or easily predicted by having a complete description of the components/actors)

Both attempt to both describe systems and enable predictions or synthetic experiments to test counter-factuals (e.g. "if we increase the number of beds, does an outcome change?") that are impractical or costly to test practically without being constrained by some modelling.

Importantly, because the system components are considered at a higher level of abstraction than those typifying 1st-order approaches, these models of multiple interacting components provides often emphasise simulation, sacrifice the detail and tractability that make 1st order modelling attractive.

We propose 2nd-order approaches are suitable for **system innovation** (e.g. improving care pathways/services by remodelling) and revision (i.e. “designing out” bugs in healthcare processes such as medication errors). Common framework tools are "people, systems, design and risk" combined with spiral process models to emphasise the iterative nature of engineering approaches.

 
## Examples
The healthcare digital twin ()

A helpful overview of systems approaches in health care can be found in [Komashie *et al*'s (2021)](https://bmjopen.bmj.com/content/bmjopen/11/1/e037667.full.pdf) systematic review.

# References and Further Reading
  * Clarkson, P. J. (2018). What has engineering design to say about healthcare improvement?. Design Science, 4, e17. [https://doi.org/10.1017/dsj.2018.13](https://doi.org/10.1017/dsj.2018.13)
  * Royal Academy of Enginerring (RAE) (2017) Engineering Better Care. [https://raeng.org.uk/media/wwko2fs4/final-report-engineering-better-care-version-for-website.pdf](https://raeng.org.uk/media/wwko2fs4/final-report-engineering-better-care-version-for-website.pdf)
  * Vázquez-Serrano, J.I., (2021). “Discrete-Event Simulation Modeling in Healthcare: A Comprehensive Review.” International Journal of Environmental Research and Public Health 18 (22): 12262. [https://www.mdpi.com/1660-4601/18/22/12262](https://www.mdpi.com/1660-4601/18/22/12262)
  * Sterman, J. *et al* (2015). “System Dynamics Perspectives and Modeling Opportunities for Research in Operations Management.” Journal of Operations Management 39: 40. [https://onlinelibrary.wiley.com/doi/10.1016/j.jom.2015.07.001](https://onlinelibrary.wiley.com/doi/10.1016/j.jom.2015.07.001)
  * Benneyan, JC, RC Lloyd, and PE Plsek. 2003. “Statistical Process Control as a Tool for Research and Healthcare Improvement.” [BMJ Quality & Safety](https://qualitysafety.bmj.com/content/qhc/12/6/458.full.pdf?casa_token=tbKNbw0ZOIAAAAAA:sIQycJmlh-3h9Y4IBSJD_16AKydevbrUhB1adjxr8UIV99HMufE4-D2pNoDStWUaf7VZqSnoZSKd) 12 (6): 458–64.
  * Masison, J., *et al* (2021). A modular computational framework for medical digital twins. Proceedings of the National Academy of Sciences, 118(20), e2024287118. [https://www.pnas.org/doi/pdf/10.1073/pnas.2024287118](https://www.pnas.org/doi/pdf/10.1073/pnas.2024287118)
  * Komashie, A., *et al* (2021). “Systems Approach to Health Service Design, Delivery and Improvement: A Systematic Review and Meta-Analysis.” BMJ Open 11 (1): e037667. [https://bmjopen.bmj.com/content/bmjopen/11/1/e037667.full.pdf](https://bmjopen.bmj.com/content/bmjopen/11/1/e037667.full.pdf)

