Travelling Salesman Problem (TSP)

ALGORITHM:
1.Initialize: Define cities and distances between them.
2.Generate Permutations: Create all possible routes.
3.Calculate Costs: Compute the total distance for each route.
4.Find Minimum: Identify the route with the minimum total distance.
5.Return Solution: Return the shortest route and its cost.

PROGRAM:
from itertools import permutations
def calculate_path_cost(distance_matrix, path):
    cost = 0
    for i in range(len(path) - 1):
        cost += distance_matrix[path[i]][path[i + 1]]
    cost += distance_matrix[path[-1]][path[0]]
    return cost
def tsp_bruteforce(distance_matrix):
    n = len(distance_matrix)
    cities = list(range(n))
    min_cost = float('inf')
    best_path = []
    for perm in permutations(cities):
        current_cost = calculate_path_cost(distance_matrix, perm)
        if current_cost < min_cost:
            min_cost = current_cost
            best_path = perm
    return min_cost, best_path
def main():
    distance_matrix = [
        [0, 10, 15, 20],
        [10, 0, 35, 25],
        [15, 35, 0, 30],
        [20, 25, 30, 0]
    ]
    min_cost, best_path = tsp_bruteforce(distance_matrix)
    print("Optimal Path:", best_path)
    print("Minimum Cost:", min_cost)
if __name__ == "__main__":
    main()
