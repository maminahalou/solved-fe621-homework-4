Download Link: https://assignmentchef.com/product/solved-fe621-homework-4
<br>
<strong>Problem 1. Comparing different Monte Carlo schemes.</strong>

Consider the Black-Scholes setup (geometric Brownian motion) with <em>r </em>= 3%<em>, δ </em>= 1%<em>,σ </em>= 20%<em>, S</em><sub>0 </sub>= 100, and assume we want to price an European option with strike <em>K </em>= 100 and maturity <em>T </em>= 1.

<ul>

 <li>Implement a simple Monte Carlo scheme using <em>m </em>simulation trials for European Call and Put options. This should be a function of <em>n </em>(number of time steps) and <em>m</em>. In all practical applications you should use at least 300 time steps and at least 1 million simulated paths. Furthermore, implement a calculation of the standard error of the estimate of the option price and a way to time the simulation routine. Please output the results obtained when varying <em>n </em>(300 -700) and <em>m </em>(1-5 million). Pick just a few values in each range.</li>

 <li>Implement a Monte Carlo scheme for European call and put options using the antithetic variates method, the delta–based control variate with <em>β</em><sub>1 </sub>= −1, and the combined antithetic variates with delta-based control variate method. Report the values obtained in four columns: Monte Carlo (MC), MC with Antithetic Variates, MC with Delta-based Control Variate, and MC with both Antithetic Variates and Delta-based Control Variate. Report the estimated option values, the corresponding standard deviations, as well as the time it takes to obtain each result. Write a short paragraph comparing the results you obtained. Discuss the methods implemented.</li>

</ul>

<strong>Problem 2. Path-dependent options using Monte Carlo (30 points) </strong>In this question, we shall consider the valuation of two representative pathdependent options using the Monte Carlo method. The stock price follows a geometric Brownian motion, and parameters are: <em>S</em><sub>0 </sub>= 100<em>,K </em>= 100<em>,r </em>= 3%<em>, δ </em>= 1%<em>,σ </em>= 20%<em>,T </em>= 1. The number of time steps is <em>n </em>= 120, and the number of simulations is <em>m </em>= 1 million.

<ul>

 <li>Consider the valuation of a discretely-monitored arithmetic Asian call option. Assume there are 12 monitoring points, i.e. the stock price is monitored every month, <em>t<sub>i </sub></em>= <em>i/</em>12<em>,i </em>= 1<em>,…,</em>12, and the payoff is given by</li>

</ul>

. Hint: note that you are simulating 120 observations

and you will need to use exactly 12 of those. Use the end of the month observations for this purpose.

<ul>

 <li>Consider the valuation of a discretely-monitored up and out barrier call option. The barrier level is <em>H </em>= 110. Assume there are 12 monitoring points, i.e. the stock price is monitored every month, 12, and the payoff is given by (.</li>

</ul>

<strong>Problem 3. Generating correlated BM and pricing basket options.</strong>

<ul>

 <li>Given a correlation matrix A,</li>

</ul>

<em> ,</em>

perform a Cholesky decomposition of the matrix <em>A</em>, which is a decomposition of the form <em>A </em>= <em>LL<sup>T</sup></em>, when <em>A </em>is symmetric and positive definite matrix. The function you construct should return the lower triangular matrix, <em>L</em>.

Consider three assets, starting with <em>S</em>(0) = [100<em>,</em>101<em>,</em>98]. The assets are assumed to follow a standard geometric Brownian motion of the form

<em>dS<sub>i</sub></em>(<em>t</em>) = <em>µ<sub>i</sub>S<sub>i</sub></em>(<em>t</em>)<em>dt </em>+ <em>σ<sub>i</sub>S<sub>i</sub></em>(<em>t</em>)<em>dW<sub>i</sub></em>(<em>t</em>)<em>.</em>

We assume <em>µ </em>= [0<em>.</em>03<em>,</em>0<em>.</em>06<em>,</em>0<em>.</em>02], the volatility <em>σ </em>= [0<em>.</em>05<em>,</em>0<em>.</em>2<em>,</em>0<em>.</em>15], and the BM’s have the correlation matrix <em>A </em>(e.g., <em>d &lt; W</em><sub>1</sub><em>,W</em><sub>2 </sub><em>&gt;</em>= <em>a</em><sub>12</sub><em>dt </em>= 0<em>.</em>5<em>dt</em>).

<ul>

 <li>We take maturity <em>T </em>= 100 days and the number of simulated paths is <em>m </em>= 1000, Consider one day sampling frequency, i.e. ∆<em>t </em>= 1<em>/</em> Generate a 3−dimensional matrix where each row represents a time step, each column represent a separate simulation for a specific asset and the 3-rd dimension represents different assets in the basket. Plot one realization (sample path) for this 3−dimensional process.</li>

 <li>Basket options are options on a basket of assets. A commonly traded basket option is a vanilla call/put option on a linear combination of assets. To clarify, suppose <em>S<sub>i</sub></em>(<em>t</em>)<em>,i </em>= 1<em>,…,N </em>are the prices of <em>N </em>stocks at time <em>t </em>and let <em>a<sub>i</sub>,i </em>= 1<em>,…,N </em>are real constants. Set</li>

</ul>

<em>N</em>

<em>U</em>(<em>t</em>) = <sup>X</sup><em>a<sub>i</sub>S<sub>i</sub></em>(<em>t</em>)

<em>i</em>=1

A vanilla basket option is simply a vanilla option on <em>U</em>(<em>T</em>). Specifically, on the exercise date <em>T</em>, the payoff of the option is max{<em>α</em>(<em>U</em>(<em>T</em>)−<em>K</em>)<em>,</em>0}, where <em>K </em>is the exercise price and <em>α </em>= 1 for a call and <em>α </em>= −1 for a put. Price an European call option and an European put option with <em>K </em>= 100 on the 3 asset basket given in part (b), using a Monte Carlo simulation. Consider a simple average basket <em>a</em><sub>1 </sub>= <em>a</em><sub>2 </sub>= <em>a</em><sub>3 </sub>= 1<em>/</em>3.

<ul>

 <li>Please price an exotic option on the basket in part (b), described using the following conditions where we use <em>B </em>= 104, and <em>K </em>= 100:

  <ul>

   <li>If the asset 2 (<em>S</em><sub>2</sub>) hits the barrier <em>B &lt; S</em><sub>2</sub>(<em>t</em>) for some <em>t </em>then the payoff of the option is equal to an European Call option written on the asset</li>

  </ul></li>

</ul>

2;

<ul>

 <li>If max<em><sub>t</sub></em><sub>∈[0<em>,T</em>] </sub><em>S</em><sub>2</sub>(<em>t</em>) <em>&gt; </em>max<em><sub>t</sub></em><sub>∈[0<em>,T</em>] </sub><em>S</em><sub>3</sub>(<em>t</em>), then the payoff of the option is</li>

</ul>

;

<ul>

 <li>Take), the average of the daily values for stock</li>

</ul>

<ol>

 <li><em>i</em>. If <em>A</em><sub>2</sub>(0<em>,T</em>) <em>&gt; A</em><sub>3</sub>(0<em>,T</em>), then the payoff is (<em>A</em><sub>2</sub>(0<em>,T</em>) − <em>K</em>)<sub>+</sub>;</li>

</ol>

<ul>

 <li>otherwise, the option is a vanilla call option on the basket, similar to part (c) of this problem.</li>

</ul>

<strong>Problem 4. (BONUS) Simulating the Heston model. </strong>

Consider the Heston stochastic volatility model with parameters: <em>S</em><sub>0 </sub>= 100<em>, V</em><sub>0 </sub>= 0<em>.</em>010201<em>, κ </em>= 6<em>.</em>21<em>, θ </em>= 0<em>.</em>019<em>, σ </em>= 0<em>.</em>61<em>, ρ </em>= −0<em>.</em>7<em>, r </em>= 3<em>.</em>19%.

<ul>

 <li>Apply the Euler discretization schemes as presented in Table 1 of the paper [1]. Please implement all the five schemes listed there and use Monte Carlo simulations to price a call option with strike <em>K </em>= 100 and maturity <em>T </em>= 1. The exact call option price (benchmark) is in this case <em>C</em><sub>0 </sub>= 6<em>.</em>8061<em>. </em>Provide a table listing the estimated call option price, the bias, the root mean square error (RMSE), and the computation time in seconds. Report the results for each of the five schemes in one table.</li>

 <li>Quadrature methods can be used to price options under the Heston Model. The paper [2] provides a good implementation of the Heston Model and the corresponding pricing problem. Compute numerically the price of the option from part (<em>a</em>) using the formula (1.4) in [2], with the parameters provided in the same paper in Section 6. Please note that in order to calculate the option price <em>C</em>(<em>S</em><sub>0</sub><em>,K,V</em><sub>0</sub><em>,t,T</em>) one needs to evaluate the integral in equation (1.5) in [2]. Use Simpson’s Rule for this purpose, with tolerance <em>ε </em>= 10<sup>−4</sup>.</li>

 <li>Compare and contrast the two approaches.</li>

</ul>

<h1>References</h1>

<ul>

 <li>Lord, Roger, Remmert Koekkoek, and Dick Van Dijk. <em>A comparison of biased simulation schemes for stochastic volatility models. </em>Quantitative Finance 10.2 (2010): 177-194.</li>

 <li>Mikhailov, Sergei and Nogel, Ulrich. “Heston’s stochastic volatility model: Implementation, calibration and some extensions”Wilmott Journal, 2004.</li>

</ul>