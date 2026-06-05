
This project implements the Markowitz Mean-Variance Optimization framework in Python to construct an efficient investment portfolio. The primary goal is to demonstrate how matrix algebra and computational optimization can be used to navigate the trade-off between risk and reward in financial markets. I developed this project to explore how algorithmic decision-making models, commonly used in institutional fintech, can mitigate risk in volatile markets. I chose to implement the Mean-Variance Optimization (MVO) model because it bridges the gap between academic portfolio theory and practical data science. By utilizing Matrix Algebra to process the covariance matrix, this model quantifies the impact of diversification, demonstrating that the optimal portfolio is not merely the collection of highest-performing assets, but the combination that minimizes risk through non-correlated asset movement.

Mathematical Framework
To derive the optimal portfolio, the project utilizes the following quantitative foundations:
 * **Asset Returns:** Calculated as daily percentage changes to standardize asset performance.
 * **Covariance Matrix ($$\Sigma$$):** Used to quantify the interdependencies between asset classes, enabling effective diversification.
 * **Portfolio Risk:** Defined as:
   
$$ \sigma_p = \sqrt{w^T \Sigma w} $$
   
Where $$w$$ is the vector of asset weights and $$\Sigma$$ is the covariance matrix.
   
Optimization: The project employs the Sequential Least Squares Programming (SLSQP) algorithm via scipy.optimize to maximize the Sharpe Ratio, defined as:

$$ S = \frac{R_p - R_f}{\sigma_p} $$
   
Where $R_p$ is portfolio return and $R_f$ is the risk-free rate.

Visualization: The Efficient Frontier
The Efficient Frontier represents the set of optimal portfolios that offer the highest expected return for a defined level of risk.
Key Insights & Findings
 * **Diversification Strategy:** By analyzing the covariance matrix, the model quantitatively validates why assets with low correlation (e.g., Gold vs. Tech stocks) are critical for minimizing portfolio variance.
 * **Algorithmic Allocation:** The optimization process successfully determined non-intuitive weightings that theoretically outperform a simple equal-weighted strategy.
Technical Stack
 * **Language:** Python 3.x
 * **Libraries:** yfinance (Data acquisition), Pandas/NumPy (Data manipulation & Matrix Algebra), SciPy (Optimization), Matplotlib (
