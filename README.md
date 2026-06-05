
This project implements the Markowitz Mean-Variance Optimization framework in Python to construct an efficient investment portfolio. The primary goal is to demonstrate how matrix algebra and computational optimization can be used to navigate the trade-off between risk and reward in financial markets. I developed this project to explore how algorithmic decision-making models, commonly used in institutional fintech, can mitigate risk in volatile markets. I chose to implement the Mean-Variance Optimization (MVO) model because it bridges the gap between academic portfolio theory and practical data science. By utilizing Matrix Algebra to process the covariance matrix, this model quantifies the impact of diversification, demonstrating that the optimal portfolio is not merely the collection of highest-performing assets, but the combination that minimizes risk through non-correlated asset movement.

Mathematical Framework
To derive the optimal portfolio, the project utilizes the following quantitative foundations. Asset Returns are calculated as daily percentage changes to standardize asset performance, while the Covariance Matrix ($$\Sigma$$) is used to quantify the interdependencies between asset classes, enabling effective diversification. Portfolio Risk is defined as 

   $$ \sigma_p = \sqrt{w^T \Sigma w} $$
   
Where $$w$$ is the vector of asset weights and $$\Sigma$$ is the covariance matrix.
The project employs the Sequential Least Squares Programming (SLSQP) algorithm via scipy.optimize to maximize the Sharpe Ratio, defined as:

$$ S = \frac{R_p - R_f}{\sigma_p} $$
   
Where $R_p$ is portfolio return and $R_f$ is the risk-free rate.

Regarding methodology and data, I utilized the ⁠yfinance⁠ library to fetch historical stock data directly from Yahoo Finance APIs, chosen for its reliability and breadth. I used ⁠pandas⁠ and ⁠numpy⁠ for data manipulation, specifically to calculate daily percentage returns, as these are industry standards for time-series analysis due to their efficient vectorized operations. The core of the model relies on the ⁠scipy.optimize⁠ library, specifically using the ⁠SLSQP⁠ algorithm because it is highly effective at solving constrained optimization problems, such as ensuring that the sum of all asset weights equals \bm{1}. Finally, I implemented ⁠matplotlib⁠ to render the Efficient Frontier, providing a clear visual representation of the trade-off between volatility and expected return.
The analysis led to two primary insights. First, regarding diversification strategy, the model quantitatively validates why assets with low correlation, such as Gold versus Tech stocks, are critical for minimizing portfolio variance. Second, the algorithmic allocation process successfully determined non-intuitive weightings that theoretically outperform a simple equal-weighted strategy. The project was developed using Python 3.x and relies on the ⁠yfinance⁠, ⁠Pandas⁠, ⁠NumPy⁠, ⁠SciPy⁠, and ⁠Matplotlib⁠ libraries.
