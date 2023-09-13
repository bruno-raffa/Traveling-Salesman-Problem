# Traveling Salesman Problem


The TSP can be defined as follows: for a given list of cities and the distances between each pair of them, we want to find the shortest possible route that goes to each city once and returns to the origin city.


The problem is defined here: https://miro.neos-server.org/app/tspmod

The approach used here involves the use of a Constrained Quadratic Model (CQM) from Dwave (https://cloud.dwavesys.com/). The solution is computed using the LeapHybridCQMSampler.

Here a series of all continental USA capital cities set is considered, but the practical case is applied to a subset of 10 cities, just to observe the provided result using a limited time of Dwave Hybrid tool. To solve the full problem, for all the 48 cities considered in the csv file, would require a much longer time to give the software the time to explore a vaster space in order to determine the better minimum.


### Objective
**Shortest Route**. Minimize the total distance of a route. A route is a sequence of capital cities where the salesperson visits each city only once and returns to the starting capital city.

### Constraints

1. Entering a capital city. For each capital city i, ensure that this city is connected to two other cities.
2. leaving a capital city. For each capital city i, ensure that this city is connected to two other cities.
3. Position constraints. these constraints ensure that for any subset of cities S of the set of Capitals, there is no cycle. That is, there is no route that visits all the cities in the subset and returns to the origin city.

### User Inputs
Initial co-ordinates of each cities in terms of latitude and longitude


### Output
Total cost of the optimized tour and a visual diagram with the route

## References

