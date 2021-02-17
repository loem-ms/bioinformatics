Sequence Alignment
==================
\[week1\]

## Individual differences in genome sequence

In genetics a single-nucleotide polymorphism (SNP: pronounced “snip”) is a substitution of a single nucleotide at a specific position in the genome. It is the most common type of genetic variation among organisms. It is known to occur once in every 1000 nucleotides. Most SNPs have no effect on health but they have proven to be very critical key to help predict an individual’s feature such as certain drugs responses or reactions. SNPs can also be important to track the inheritance of disease genes, and to study the association between complex diseases such as heart disease, diabetes, and cancer.

![Figure 1](images/cont-1/Picture1-geneexpression.png)

\[Figure from [gendai.ismedia.jp](https://gendai.ismedia.jp/articles/-/56804)\]

## Sequence Alignment

As mentioned before, genetic information can be presented as sequences of A,T,C,G. And like in case of SNP analysis, comparison between A,T,C,G sequences is one of essential process in bioinformatics which leads to deep understanding and interesting discovery between organisms or species. 

A **Sequence Alignment** is a process of arranging and comparing sequences of DNA or RNA or protein to find similarity. 

### Sequence Comparison

In sequence comparison, abolute position of each character is compared. In a simple approach, counting number of matched and unmatched positions is used. However, in some application, representing the similarity as a numerical value is necessary. In that case, similarity score is used. In the following example, there are 3 matched positions and (+3)+(+3)+(-2)+(+3)=+7 of similarity score.

![sequence comparison](images/cont-1/sequence-comparison.png)

### Alignment Score

In alignment, we arrange the sequence pair to identify the similarity. In this case, gaps are added to sequences in order to optimize the comparison. To do this, we consider scoring method on match, unmatch and gap positions. This scoring method can be flexible based on feature of comparing sequences.

![alignment score](images/cont-1/alignment-score.png)

The sequence alignment can be presented as a graph model as shown in the following example.

![alignment gap](images/cont-1/alignment-gap.png)

## Optimal Path Search Problem

Therefore, a problem of arrange sequences in sequence aligment can be considered as an optimal path search problem. Here, start node is the top left node of the graph model, and end node is the bottom right node. In this case, optimal path is the path with the maximum value of similarity score.

To solve this problem, we can use a well-known algorithm in computer science field, **Dynamic Programming**.

![alignment DP](images/cont-1/alignment-DP.png)



## Local and Global Alignment

## References

* What are single nucleotide polymorphisms (SNPs)?. MedlinePlus. U.S. National Library of Medicine [[SNP]](https://medlineplus.gov/genetics/understanding/genomicresearch/snp/)(Retrieved on 2021/01/31)