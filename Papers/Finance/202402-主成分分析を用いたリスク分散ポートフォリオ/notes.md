
Article:  https://www.nikko-research.co.jp/wp-content/uploads/2012/08/1139.pdf

This article aims to maximize the entropy of the principal components to the total variance instead of minimizing the total variance. This approach can construct a portfolio biased to one of the (mainly first) principal components. 

We write the time as $t$, indices for the owned instruments as $i, j, k$, the owned weight as $w_i(t)$, the returns as $r_i(t)$, the variance as $\sigma_i^2$, the sample covariance matrix as $\Sigma^i_{\ j}$, the return of the total portfolio as $R_p(t)$, and the variance of the total portfolio as $Var = w_i \Sigma^i_{\ j} w^j$. Then, the covariance matrix is positively definite; therefore, we can diagonalize the matrix. We write the orthogonal matrix to diagonalize as $O$, then the owned weight of each principal component as $\tilde w_i = O_i^{\ j} w_j$ and the eigenvalue of the weight as $\lambda_i$. 

Next, we think the probability-like amount $p_i = \frac{\tilde w_i ^2 \lambda_i}{Var} = \frac{\tilde w_i ^2 \lambda_i}{\Sigma_j \tilde w_j ^2 \lambda_j}$. We compute the entropy by this probability-like amount as $S = -\Sigma_i p_i \log p_i$. The entropy is maximized if each probability is the same, i.e., in this case, the rates of the total variance are the same. The portfolio is considered a diverse portfolio in the sense of the principal component analysis. 
If there are no constraints, the probabilities are the same value, i.e.,  $\tilde w_i^2 \lambda_i = const \rightarrow \tilde w_i^2 \propto \lambda_i^{-1}$.

In this article, the diverse metric is defined as $N = \exp S$. This amount becomes the number of instruments if the portfolio is completely diversified. 

For the numerical experiment, we use instruments other than those introduced in the article because some of these instruments are no longer available. Still, the performance may be the same because these instruments are indices of the major and famous ones. 
We use the following, 

- The Japan bond index: https://www.am.mufg.jp/fund/928114.html
- The Japan equity index: https://www.am.mufg.jp/fund/928084.html
- The global bond index: https://www.am.mufg.jp/fund/928234.html
- The global equity index: https://www.am.mufg.jp/fund/928104.html
- The Japan REIT index: https://www.smtam.jp/fund/detail/_id_140837/
- The global REIT index: https://www.smtam.jp/fund/detail/_id_140838/
As a notice, the article did not use the REIT, i.e., the new inputs are of interest to me. 