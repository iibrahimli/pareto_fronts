# pareto_fronts
A Python implementation of the NSGA-II algorithm (Kalyanmoy Deb, Samir Agrawal, Amrit Pratap, and T. Meyarivan. 2000. A Fast Elitist Non-dominated Sorting Genetic Algorithm for Multi-objective Optimisation: NSGA-II, [link](https://pdfs.semanticscholar.org/59a3/fea1f38c5dd661cc5bfec50add2c2f881454.pdf))

# The algorithm
The algorithm uses dynamic programming techniques to find all of the [Pareto fronts](https://en.wikipedia.org/wiki/Pareto_efficiency#Use_in_engineering_and_economics) in a given set of points. A naive approach where the algorithm for finding a Pareto front is repeated after removing the elements belonging to the found front from the population would have a computational complexity of O(m$N^3$) where m is number of objectives and N is number of elements. With NGSA-II this complexity is reduced to O(m$N^2$) with the cost of increased memory complexity.
