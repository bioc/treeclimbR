
# treeclimbR
<!-- badges: start -->
[![R-CMD-check](https://github.com/fionarhuang/treeAGG2/workflows/R-CMD-check/badge.svg)](https://github.com/fionarhuang/treeAGG2/actions)
<!-- badges: end -->

`treeclimbR` is an algorithm to pinpoint the data-dependent resosultion on hierarchcial hypotheses.

## Installation
``` r
devtools::install_github("fionarhuang/treeclimbR")
```

## Basic example ([here](https://fionarhuang.github.io/treeclimbR_toy_example/toy_signal.html))

We first generate a random tree with 100 leaves, each leaf representing an entity. Then we sample counts of entities in each sample from a multinomial distribution. In total, there are 40 samples (20 in group A and the other 20 in group B). 18 entities are randomly selected to have their counts multiplied by 2 in group A.

To run `treeclimbR`, we perform wilcoxon sum rank test on all nodes of the tree to obain P-values and directions. Details are [here](https://fionarhuang.github.io/treeclimbR_toy_example/toy_signal.html). Candidates proposed at different `t` values are shown in the animation below.

<p align="center"> 
<img src="https://github.com/fionarhuang/treeclimbR_toy_example/blob/master/output/signal_cands.gif">
</p>

Heatmap shows counts of entities (rows) in samples (columns) split by groups. Branches that include entities with signals are colored in orange.

### treeclimbR vs BH
Nodes identified by `treeclimbR` are compared to those identified by `BH` under FDR 0.05.

<p align="center"> 
<img src="https://github.com/fionarhuang/treeclimbR_toy_example/blob/master/output/signal_result.png">
</p>


## More scenarios ([here](https://htmlpreview.github.io/?https://github.com/fionarhuang/treeclimbR_animation/blob/master/docs/index.html))
1. BS

![Alt Text](https://github.com/fionarhuang/treeclimbR_animation/blob/master/output/pk_BS.gif)

2. SS

![Alt Text](https://github.com/fionarhuang/treeclimbR_animation/blob/master/output/pk_SS.gif)

## Learn more
More examples about using `treeclimbR` could be found [here](https://github.com/fionarhuang/treeclimbR_article)
