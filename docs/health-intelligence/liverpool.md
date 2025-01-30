---
hide:
- toc
tags:
- Stage 1
- Quantitative population intelligence
---

# Primary care data - Liverpool

## Methods
We invited to stakeholders -- including people with lived experience of MLTCs -- to a workshop focused on priority-setting.  We wanted participants to be able to access visualisations of multi-morbidity patterns around the Merseyside region.  To do this, we used an existing primary care dataset (extracted in 2021, from the [System P](https://www.strategyunitwm.nhs.uk/system-p) project) which contains anomymised counts of different combinations of conditions. 

We then processed the data in a number of ways to see if we could find useful visualisation to help stakeholders with priority-setting.

## Summary Descriptive Analyses

## Area-based Analysis
Acknowledging that our stakeholders (patients, carers, voluntary- and health-care sector representatives) may have different priorities reflected in terms of how deprivation, age and co-morbidities cluster together, we tried to find a way of representing this information for each of the 322 middle layer super output areas ([MSOA](https://www.ons.gov.uk/methodology/geography/ukgeographies/statisticalgeographies)) around Liverpool.   

### Multi-morbidity by Age and Area
We first take each [MSOA area](https://www.ons.gov.uk/methodology/geography/ukgeographies/statisticalgeographies) and produce a heatmap that summarises the area's morbidity prevalance data.  To do this, we count the number of individuals with e.g. asthma only, then asthma and one gastrointestinal condition and so on. To constrain the analyses and make tractable, the list of potential morbidities and combination multi-morbidities was based on the most common *individual* long-term conditions.  

With this tabulated data, we then divide the counts into 10-year age brackets.  This delivers a matrix of *age bracket x multiple conditions* where each 'cell' is the number of people in that age bracket with that condition (or combination of conditions).  As an example, the Walton Vale MSOA matrix is shown below:

<img src="../assets/Walton-Vale.png" alt="Walton Vale Morbidity Matrix" style="width:50%; height:auto;">

The grey cells are those where statistical disclosure control required that we report a floor value of 5 cases.

### Measuring Similar / Dis-similar Areas
Rather than manually inspecting these heatmaps -- deciding if different areas where more or less similar in their patterns of age, multi-morbidity and deprivation -- we construct a matrix of pairwise similarities between each of the available areas' multi-morbidity matrices.  We did this for 61 MSOA areas around Liverpool.

For example, consider three (arbitrarily-chosen) example areas:

  * Walton Vale
  * Central & Islington
  * Orell Park

![1](../assets/example-3-areas.png)

Visually, Orell Park and Walton Vale look more similar but both of these areas are appear different from Central & Islington.  As each heatmap is a matrix, we define similarity using [Frobenius](https://en.wikipedia.org/wiki/Matrix_norm#Frobenius_norm) distances (Deza and Deza, 2013; pp. 217) for the 61 areas to arrive at an distance matrix that describes how 'close' or 'distant' any area is to another.  For example, with the same three areas again:

![1](../assets/example-similarity.png)

### Constructing a Network Graph
Equipped with the 61 *x* 61 matrix of similarities, we can establish -- for any given area -- which area is the *most* similar.  We then:

 * represent each area by a 'node' and colour by the area's index of multiple deprivation (IMD)
 * plot each area (node) using geo-spatial co-ordinates for the approximate centroid of the MSOA
 * for each node, draw an edge (vertex) to the area (node) which is most similar in terms of the *age x multimorbidity* heatmap

The resulting visualisation is shown below:

![1](../assets/composite-network-plot-for-web.png)



### Interactive

<iframe src="https://systematic-nihr.github.io/network-interactive-example/networkInteractive1.html" title="D3" width="100%" height="400" style="border:none;"></iframe>
<br />


## Findings 

![1](../assets/glasgow-hi-1.PNG)
/// caption
Most common phenotypes (number of people affected)
///

<br>

![2](../assets/glasgow-hi-2.PNG)
/// caption
Differences in multimorbidity phenotypes by SIMD decile by proportion 
///

## References and Further Reading
 * Deza, E., Deza, M. M. (2013). [Encyclopedia of distances](https://link.springer.com/book/10.1007/978-3-662-52844-0). 2nd Edition. Springer Berlin Heidelberg.
 * 
