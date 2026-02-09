+++
date = '2025-05-16T19:51:34-05:00'
draft = false
title = 'Publications'
layout = 'single'
+++

# Publications
---

## CAMUS: Scalable Phylogenetic Network Estimation

#### Abstract

**Motivation:**
Phylogenetic networks are models of evolution that go beyond trees, and so represent reticulate events such as horizontal gene transfer or hybridization, which are frequently found in many taxa. Yet, the estimation of phylogenetic networks is extremely computationally challenging, and nearly all methods are limited to very small datasets with perhaps 10 to 15 species (some limited to even smaller numbers). 

**Results:**
We introduce CAMUS (Constrained Algorithm Maximizing qUartetS), a scalable method for phylogenetic network estimation. CAMUS takes an input constraint tree T as well as a set Q of unrooted quartet trees that it derives from input, and returns a level-1 phylogenetic network N that is built upon T through the addition of edges, in order to maximize the number of quartet trees in Q that are induced in N. We perform a simulation study under the Network Multi-Species Coalescent and show that a simple pipeline using CAMUS provides high accuracy and outstanding speed and scalability, in comparison to two leading methods, PhyloNet-MPL used with a fixed tree and SNaQ. CAMUS is slightly less accurate than PhyloNet-MPL used without a fixed tree, but is much faster (minutes instead of hours) and can complete on inputs with 201 species while PhyloNet-MPL fails to complete on the inputs with more than 51 species. 

<!--**Availability and Implementation:**
The source code is available at [https://github.com/jsdoublel/camus](https://github.com/jsdoublel/camus).-->

[bioRxiv](https://doi.org/10.64898/2026.02.01.703143)

> Willson, James, and Tandy Warnow. "CAMUS: Scalable Phylogenetic Network Estimation" *bioRxiv preprint* bioRxiv:2026.02.01.703143 (2026).

<details>
	<summary class="bibtex">bibtex</summary>

```
@article{willson2026camus,
  title={CAMUS: Scalable Phylogenetic Network Estimation},
  author={Willson, James and Warnow, Tandy},
  journal={bioRxiv},
  pages={2026--02},
  year={2026},
  publisher={Cold Spring Harbor Laboratory}
}
```
</details>

## Axioms for clustering simple unweighted graphs: No impossibility result.

#### Abstract
In 2002, Kleinberg proposed three axioms for distance-based clustering, and proved that it was impossible for a clustering method to satisfy all three. While there has been much subsequent work examining and modifying these axioms for distance-based clustering, little work has been done to explore axioms relevant to the graph partitioning problem when the graph is unweighted and given without a distance matrix. Here, we propose and explore axioms for graph partitioning for this case, including modifications of Kleinberg’s axioms and three others: two axioms relevant to the “Resolution Limit” and one addressing well-connectedness. We prove that clustering under the Constant Potts Model satisfies all the axioms, while Modularity clustering and iterative k-core both fail many axioms we pose. These theoretical properties of the clustering methods are relevant both for theoretical investigation as well as to practitioners considering which methods to use for their domain science studies.

[Full Paper](https://doi.org/10.1371/journal.pcsy.0000011)

>Willson, James, and Tandy Warnow. "Axioms for clustering simple unweighted graphs: No impossibility result." *PLOS Complex Systems* 1, no. 2 (2024): e0000011.
<details>
	<summary class="bibtex">bibtex</summary>

```
@article{willson2024axioms,
  title={Axioms for clustering simple unweighted graphs: No impossibility result},
  author={Willson, James and Warnow, Tandy},
  journal={PLOS Complex Systems},
  volume={1},
  number={2},
  pages={e0000011},
  year={2024},
  publisher={Public Library of Science San Francisco, CA USA}
}
```
</details>

## DISCO+QR: rooting species trees in the presence of GDL and ILS.

#### Abstract

**Motivation:**
Genes evolve under processes such as gene duplication and loss (GDL), so that gene family trees are multi-copy, as well as incomplete lineage sorting (ILS); both processes produce gene trees that differ from the species tree. The estimation of species trees from sets of gene family trees is challenging, and the estimation of rooted species trees presents additional analytical challenges. Two of the methods developed for this problem are STRIDE, which roots species trees by considering GDL events, and Quintet Rooting (QR), which roots species trees by considering ILS.

**Results:** We present DISCO+QR, a new approach to rooting species trees that first uses DISCO to address GDL and then uses QR to perform rooting in the presence of ILS. DISCO+QR operates by taking the input gene family trees and decomposing them into single-copy trees using DISCO and then roots the given species tree using the information in the single-copy gene trees using QR. We show that the relative accuracy of STRIDE and DISCO+QR depend on the properties of the dataset (number of species, genes, rate of gene duplication, degree of ILS and gene tree estimation error), and that each provides advantages over the other under some conditions.

[Full Paper](https://doi.org/10.1093/bioadv/vbad015)

> Willson, James, Yasamin Tabatabaee, Baqiao Liu, and Tandy Warnow. "DISCO+QR: rooting species trees in the presence of GDL and ILS." *Bioinformatics Advances* 3, no. 1 (2023): vbad015.
<details>
	<summary class="bibtex">bibtex</summary>

```
@article{willson2023disco+,
  title={{DISCO+QR}: rooting species trees in the presence of {GDL} and {ILS}},
  author={Willson, James and Tabatabaee, Yasamin and Liu, Baqiao and Warnow, Tandy},
  journal={Bioinformatics Advances},
  volume={3},
  number={1},
  pages={vbad015},
  year={2023},
  publisher={Oxford University Press}
}
```
</details>

## DISCO: species tree inference using multicopy gene family tree decomposition.

#### Abstract
Species tree inference from gene family trees is a significant problem in computational biology. However, gene tree heterogeneity, which can be caused by several factors including gene duplication and loss, makes the estimation of species trees very challenging. While there have been several species tree estimation methods introduced in recent years to specifically address gene tree heterogeneity due to gene duplication and loss (such as DupTree, FastMulRFS, ASTRAL-Pro, and SpeciesRax), many incur high cost in terms of both running time and memory. We introduce a new approach, DISCO, that decomposes the multi-copy gene family trees into many single copy trees, which allows for methods previously designed for species tree inference in a single copy gene tree context to be used. We prove that using DISCO with ASTRAL (i.e., ASTRAL-DISCO) is statistically consistent under the GDL model, provided that ASTRAL-Pro correctly roots and tags each gene family tree. We evaluate DISCO paired with different methods for estimating species trees from single copy genes (e.g., ASTRAL, ASTRID, and IQ-TREE) under a wide range of model conditions, and establish that high accuracy can be obtained even when ASTRAL-Pro is not able to correctly roots and tags the gene family trees. We also compare results using MI, an alternative decomposition strategy from Yang Y. and Smith S.A. (2014), and find that DISCO provides better accuracy, most likely as a result of covering more of the gene family tree leafset in the output decomposition.

[Full Paper](https://doi.org/10.1093/sysbio/syab070), [Supplement](../pdfs/disco-suppl.pdf)

> Willson, James, Mrinmoy Saha Roddur, Baqiao Liu, Paul Zaharias, and Tandy Warnow. "DISCO: species tree inference using multicopy gene family tree decomposition." *Systematic Biology* 71, no. 3 (2022): 610-629.
<details>
	<summary class="bibtex">bibtex</summary>

```
@article{willson2022disco,
  title={{DISCO:} species tree inference using multicopy gene family tree decomposition},
  author={Willson, James and Roddur, Mrinmoy Saha and Liu, Baqiao and Zaharias, Paul and Warnow, Tandy},
  journal={Systematic Biology},
  volume={71},
  number={3},
  pages={610--629},
  year={2022},
  publisher={Oxford University Press}
}

```
</details>

## Comparing methods for species tree estimation with gene duplication and loss.

#### Abstract
Species tree inference from gene trees is an important part of biological research. One confounding factor in estimating species trees is gene duplication and loss, which can lead to gene family trees with multiple copies of the same species. In recent years there have been several new methods developed to address this problem that have substantially improved on earlier methods; however, the best performing methods (ASTRAL-Pro, ASTRID-multi, and FastMulRFS) have not yet been directly compared. In this study, we compare ASTRAL-Pro, ASTRID-multi, and FastMulRFS under a wide variety of conditions. Our study shows that while all three have nearly the same accuracy under most conditions, ASTRAL-Pro and ASTRID-multi are more reliably accurate than FastMuLRFS (with a small advantage to ASTRID-multi), and that ASTRID-multi is often faster than ASTRAL-Pro.

[Full Paper](https://doi.org/10.1007/978-3-030-74432-8_8)

>Willson, James, Mrinmoy Saha Roddur, and Tandy Warnow. "Comparing methods for species tree estimation with gene duplication and loss." In *International Conference on Algorithms for Computational Biology*, pp. 106-117. Cham: Springer International Publishing, 2021.
<details>
	<summary class="bibtex">bibtex</summary>

```
@inproceedings{willson2021comparing,
  title={Comparing methods for species tree estimation with gene duplication and loss},
  author={Willson, James and Roddur, Mrinmoy Saha and Warnow, Tandy},
  booktitle={International Conference on Algorithms for Computational Biology},
  pages={106--117},
  year={2021},
  organization={Springer}
}
```
</details>

