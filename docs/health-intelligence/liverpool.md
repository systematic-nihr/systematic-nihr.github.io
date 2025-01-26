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

## Visualisations

### Most Similar Areas
We considered an experimental approach to visualisation by first taking each [LSOA area](https://www.data.gov.uk/dataset/c481f2d3-91fc-4767-ae10-2efdf6d58996/lower-layer-super-output-areas-lsoas) and producing a heatmap that summarised the area's morbidity prevalance data.  For example, if we consider three (arbitrary) example areas:

  * Walton Vale
  * Central & Islington
  * Orell Park

and then for each region, derive a heatmap that counts the prevalence of people with multiple conditions in 10 year age brackets then we arrive at:

![1](../assets/example-3-areas.png)

Grey cells are where statistical disclosure control results in a floor value of 5 people (in a given age bracket on the vertical axis, and with the conditions / combinations on the horizontal axis).  Notice that Orell Park and Walton Value had similar patterns of multi-morbidity but both of these areas are appear different from Central & Islington.  We produced similar heatmaps (counts of conditions by age bracket) for 322 areas.

Each heatmap is a matrix, so we then compute all pairwise [Frobenius](https://en.wikipedia.org/wiki/Matrix_norm#Frobenius_norm) distances (Deza and Deza, 2013; pp. 217) for the 322 areas to arrive at an distance matrix that describes how 'close' or 'distant' any area is to another.

![1](../assets/example-similarity.png)

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
