##

Also known as gaussian distribution 


Its a tool used in ML to create a statistical model which is able to perform some taks on future data . 

It might be 

- classificaiton 
- regression 



MLE is one flavor of parameter estimation in machine learning, and in order to perform parameter estimation, we need:

    
1. some data X
2. some hypothesized generating function of the data f(X,θ)
3. a set of parameters from that function θ
4. some evaluation of the goodness of our parameters (an objective function)




In statistics, the Gaussian case of Maximum Likelihood Estimation (MLE) involves estimating the parameters of a Gaussian (normal) distribution based on observed data. The Gaussian distribution is characterized by two parameters: the mean (μ) and the variance (σ^2). Maximum Likelihood Estimation is a method for finding the values of these parameters that make the observed data most likely.

Here's how you perform Maximum Likelihood Estimation for the Gaussian case:

**1. Likelihood Function**: Start by defining the likelihood function, which represents the probability of observing your data given the parameters μ and σ^2. For a sample of n observations, x_1, x_2, ..., x_n, from a Gaussian distribution, the likelihood function is given by:

   L(μ, σ^2 | x_1, x_2, ..., x_n) = Π [1 / (√(2πσ^2))] * exp[-(x_i - μ)^2 / (2σ^2)]

   where Π denotes the product of all terms in the sequence.

**2. Log-Likelihood Function**: Taking the natural logarithm of the likelihood function simplifies the mathematical calculations because it converts products into sums and makes differentiation easier:

   ln(L) = -n * ln(√(2πσ^2)) - Σ (x_i - μ)^2 / (2σ^2)

**3. Maximizing the Log-Likelihood**: To find the maximum likelihood estimates for μ and σ^2, you differentiate the log-likelihood function with respect to μ and σ^2 and set the derivatives equal to zero:

   ∂ln(L) / ∂μ = 0
   ∂ln(L) / ∂σ^2 = 0

   Solving these equations will give you the MLE estimates for μ and σ^2.

**4. Solving for MLE Parameters**:
   - For μ: Solve ∂ln(L) / ∂μ = 0 for μ. The solution will be the sample mean of the observed data.
   
   - For σ^2: Solve ∂ln(L) / ∂σ^2 = 0 for σ^2. The solution will be the sample variance of the observed data. Note that sometimes the MLE for σ^2 is calculated as the sample variance divided by (n-1) to account for the degrees of freedom.

Maximum Likelihood Estimation provides parameter estimates that are statistically efficient and asymptotically unbiased. In the Gaussian case, these estimates correspond to the sample mean (μ) and the sample variance (σ^2).

Once you have estimated the parameters, you can use the estimated Gaussian distribution to make predictions, perform hypothesis tests, calculate confidence intervals, and more in various statistical analyses and applications.


!()[docs/GaussianCaseUnknownMean.png]

!()[docs/GaussianCaseUnknownMeanandUnknownCovariance.png]



----------------------------------------------------------------------------------------------------

#### REFERENCES


- http://jrmeyer.github.io/machinelearning/2017/08/18/mle.html



