# Adaptive-ACO-in-Stock-Portfolio-Optimization
## I. Project Background
In the field of financial investment, optimizing stock portfolios is of utmost importance. Investors aim to maximize returns while keeping risks under control. Traditional methods such as the mean - variance model have limitations when dealing with complex market conditions and real - world constraints. The ant colony algorithm, as an emerging heuristic optimization algorithm, offers good global search ability and adaptability, providing a new approach to stock portfolio optimization. This project aims to enhance the performance of the ant colony algorithm in stock portfolio optimization through improvements, assisting investors in making more rational investment decisions.
## II. Technical Principles
### (I) Foundation of the Ant Colony Algorithm
Basic Principle: The ant colony algorithm mimics the foraging behavior of ant colonies. Ants communicate information by releasing pheromones. Paths with higher pheromone concentrations are more likely to be chosen by subsequent ants, forming a positive feedback mechanism that guides the colony to find the optimal path. Meanwhile, pheromones evaporate over time to prevent the algorithm from getting trapped in local optima.

Mathematical Model: Taking the classic Traveling Salesman Problem (TSP) as an example, symbols such as the number of ants, distances between cities, heuristic functions, and pheromone intensities are defined. Ants choose paths based on the transition probability formula, and pheromones are dynamically adjusted according to the update rules.
### (II) Improvement Strategies
Max - Min Ant System (MMAS): The pheromone intensity is restricted to the interval [τmin, τmax] to avoid premature convergence of the algorithm. Initially, the pheromone is set to τmax, allowing ants to explore new paths more fully in the early stages of the algorithm.

Adaptive Pheromone Update: A smoothing mechanism is adopted to adaptively adjust the pheromone update, reducing the range of pheromone differences among paths, balancing deterministic and random selections, and enhancing the global search ability.

Elite Ant Strategy: Ants whose path - finding results are highly similar to the previously discovered optimal results are designated as elite ants. Their path - finding results have a greater impact on the search for the global optimal solution, improving the algorithm's efficiency.

<div align=center>
<img src="https://github.com/Seailvia/Adaptive-ACO-in-Stock-Portfolio-Optimization/blob/main/Structure of Adjusted-ACO.png" width = 600>
</div>

### (III) Stock Portfolio Optimization Model
Mean - Variance Model: Based on Markowitz's theory, the mean of the portfolio's expected return and the variance of the return standard deviation are used to measure the return and risk of the investment portfolio. A quadratic optimal programming model is constructed to find the optimal investment portfolio on the efficient frontier.

Application of the Improved Ant Colony Algorithm: The stock portfolio problem is modeled, and relevant symbols are defined. Ants determine the transition probability to select stocks based on the heuristic function and pheromone intensity, thereby constructing an investment portfolio. After each cycle, the pheromone is updated according to the improved pheromone update method, and elite ants are recorded to optimize the algorithm's solution process.


<div align=center>
<img src="https://github.com/Seailvia/Adaptive-ACO-in-Stock-Portfolio-Optimization/blob/main/ex02.png" width = 600>
</div>

## III. Experimental Process and Results
### (I) Data Processing
Data from five A - share stocks, namely China Southern Airlines, Shanghai Pufa Bank, Xinhuamedia Investment Co., Ltd., Sinopec, and Ping An Insurance (Group) Company of China, Ltd., for a total of 95 trading days from March 1, 2023, to May 26, 2023, were selected. The daily returns were calculated, and the return change curves were plotted. The mean and variance were calculated to measure the risk and return.
### (II) Experimental Comparison
The improved ant colony algorithm and the traditional ant colony algorithm were used to optimize the investment portfolios of the five stocks respectively. The results show that the investment portfolio obtained by the improved ant colony algorithm has a higher return (0.002978005 > 0.002332791) and lower risk (0.000430079 < 0.000461677). The Sharpe ratio of the improved ant colony algorithm is 0.136, significantly higher than that of the traditional ant colony algorithm (0.101), indicating that the improved algorithm can provide a higher investment return based on unit risk.

<div style="max-width: 800px; margin: 0 auto;">
|  | Rate of Return | Risk |
| --- | --- | --- |
| Traditional Ant Colony | 0.002332791 | 0.000461677 |
| Improved Ant Colony | 0.002978005 | 0.000430079 |
</div>

## IV. Project Advantages
Efficiency: Through various optimization strategies, the improved ant colony algorithm has a faster convergence speed and can find a relatively optimal solution in fewer iterations, improving the efficiency of portfolio optimization.

Accuracy: It effectively avoids the algorithm from getting trapped in local optima and can more accurately find the optimal investment portfolio that balances risk and return in complex stock market data.
Adaptability: The improvement strategies take into account the characteristics of the stock market, such as price fluctuations, making the algorithm more suitable for the scenario of stock portfolio optimization.
