# Bin-Packing-Problem

The bin packing problem is an optimization problem where given a number of items with a respective weight, we look at the best arrangement of the items to minimize the number of bins or containers needed. The restriction, in this case, is the capacity of the bins which cannot surpass a certain weight. This problem has many real applications in areas as loading trucks with a weight restriction, filling up containers, and FPGA semiconductors chip design. 

In terms of complexity, the bin packing problem is an NP-hard problem. However, there are efficient algorithms that allow the arrangement of a large number of items. One of them is the first fit, which provides a fast but not optimal solution to the problem. 

In this tutorial, we will explore the solution of the bin packing problem, using a quantum computing representation in terms of quadratic unconstraint binary optimization (QUBO) and using the quantum approximation optimization (QAOA) algorithm. 

## 1. Problem statement

<img src="https://render.githubusercontent.com/render/math?math=\underset{\chi, \xi}{minimize}\sum_{i=1}^m \chi_i">

subject to:

<img src="https://render.githubusercontent.com/render/math?math=\sum_{i=1}^m \xi_{ij} = 1 \qquad j=1,...,n">

<img src="https://render.githubusercontent.com/render/math?math=\sum_{j=1}^n w_{j}\xi_{ij} \le Q \chi_i \qquad i = 1, ..., m">

<img src="https://render.githubusercontent.com/render/math?math=\xi_{ij}\in  \{0,1\} \qquad i=1,..,m \qquad j=1,..,n">

<img src="https://render.githubusercontent.com/render/math?math=\chi_{i}\in  \{0,1\} \qquad i=1,..,m">

- n is the number of items
- m is the number of bins
- <img src="https://render.githubusercontent.com/render/math?math=w_j"> is the jth item weight
- <img src="https://render.githubusercontent.com/render/math?math=\chi_i"> is ith bin
- <img src="https://render.githubusercontent.com/render/math?math=\xi_{ij}"> is the variable that represent if the item j is in the bin i.
