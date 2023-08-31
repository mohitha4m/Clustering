# Clustering Linear Data into groups  of variable sizes
This is a python implementation of specified R code here -
https://stats.stackexchange.com/questions/128868/clustering-data-into-bins-of-variable-sizes

A dynamic program to minimize the sum of group variances subject to size constraints

<img width="617" alt="Figure" src="https://github.com/mohitha4m/Clustering/assets/79994111/2403233c-c449-41e3-ad86-e48eccc182bf">

It computes the solution recursively, achieving efficiency by caching the results as it goes along. The program cluster(x,i) finds (and records) the best solution starting at index i in the data array x by searching among all feasible windows of lengths n.min through n.max beginning at index i. It returns the best value found so far (and, within the global variable cache$Breaks, leaves behind an indicator of the indexes that start each group). It can process arrays of thousands of elements in seconds, depending on how large the range n.max-n.min is. For larger problems it would have to be improved to include some branch-and-bound heuristics to limit the amount of searching.


