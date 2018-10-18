# pareto_fronts
A Python implementation of the NSGA-II algorithm (Kalyanmoy Deb, Samir Agrawal, Amrit Pratap, and T. Meyarivan. 2000. A Fast Elitist Non-dominated Sorting Genetic Algorithm for Multi-objective Optimisation: NSGA-II, [link](https://pdfs.semanticscholar.org/59a3/fea1f38c5dd661cc5bfec50add2c2f881454.pdf))

## The algorithm
The algorithm uses dynamic programming techniques to find all of the [Pareto fronts](https://en.wikipedia.org/wiki/Pareto_efficiency#Use_in_engineering_and_economics) in a given set of points. A naive approach where the algorithm for finding a Pareto front (which itself has a complexity of `O(mN^2)` where m is number of objectives and N is number of elements) is repeated after removing the elements belonging to the found front from the population would have a computational complexity of O(mN^3). The file `pareto_front.ipynb` uses this simple algorithm. With NGSA-II this complexity is reduced to `O(mN^2)` with the cost of increased memory complexity. This algorithm is implemented in `pareto_fronts_dynamic.ipynb`.

## Result
Given an example set of data points representing the mass-price tradeoff in bicycles where y axis is weight in kg, and x axis is the price of the bike:

![data](https://github.com/iibrahimli/pareto_fronts/blob/master/bike_data_points.png "Data points")

the algorithm produces the list of Pareto fronts like this:

![fronts](https://github.com/iibrahimli/pareto_fronts/blob/master/pareto_fronts.png "Pareto fronts")
