---
hide:
- toc
tags:
- Stage 1
- Systems Science
---

# Definition
A 1st-Order approach treats a system as a concrete ontological entity (i.e. a collection of components and dependencies that exists “in the real world”) that can be captured by a formal model – at a single level of abstraction – that is amenable to description and analysis using research methods from the formal sciences and engineering (e.g. operations research, mathematical programming/optimisation and control theory). 1st-order approaches emphasise the regulation/control of a system’s output by feedback and error correction (as in industrial control) generally using analytically-tractable – often deterministic – and mature mathematical methods. 

1st-Order approaches are suited to **optimising components** of larger healthcare systems where:

  * the boundaries of a given model are well-circumscribed -- for example, modelling a single outpatient department, ward or other finite healthcare resource
  * inputs, outputs and processes can be captured quantitatively, precisely (i.e. without significant unmeasurable uncertainty) -- for example, the inputs are numbers or rates of patients requiring or entering a service and similarly, outputs are the number of patients provided a service in a given period of time
  * sources of natural variation (or noise) admit well-understood formalisms -- for example, variability can be modelled as a random variable, with a convenient parametric distribution on the inputs to the model
  * and the interactions (and dependencies) between components can be described using well-understood mathematics -- for example, stochastic [queueing models](https://en.wikipedia.org/wiki/Queueing_theory)
 
 ## Examples
 Griffiths, Knight, and Komenda (2013) used queue theory to optimise bed utilisation in a critical care unit (CCU).  In this example, a queueing model can be described by three components: 
	
  * the *arrival* distribution: here, a Poisson model was used
  * the *service* distribution: modelled as two processes, one for elective and another for emergency admission with exponential distributions
  * and the number of *service channels*: in Griffiths *et al*, there are 24 beds in the CCU

The proposed parameterised queue model was fit to existing hospital data and the resulting model used to optimise the numbers of nurses required to service a critical care unit with varying demands in terms of elective and unplanned / emergency admissions.

A helpful systematic review of pathway modelling can be found in [Aspland *et al* (2021)](https://doi.org/10.1080/20476965.2019.1652547).

# References and Further Reading
  * Griffiths, Jeffrey Deacon, V Knight, and Izabela Komenda. 2013. “Bed Management in a Critical Care Unit.” IMA Journal of Management Mathematics 24 (2): 137–53. [https://doi.org/10.1093/imaman/dpr028](https://doi.org/10.1093/imaman/dpr028)
  * Aspland, E., Gartner, D., & Harper, P. (2021). Clinical pathway modelling: A literature review. Health Systems, 10(1), 1–23. [https://doi.org/10.1080/20476965.2019.1652547](https://doi.org/10.1080/20476965.2019.1652547)
  * Computational modelling: Blackett review. (2018). [https://www.gov.uk/government/publications/computational-modelling-blackett-review](https://www.gov.uk/government/publications/computational-modelling-blackett-review)
  * Calder, M., *et al* (2018). Computational modelling for decision-making: Where, why, what, who and how. Royal Society Open Science, 5(6), 172096. [https://doi.org/10.1098/rsos.172096](https://doi.org/10.1098/rsos.172096)



