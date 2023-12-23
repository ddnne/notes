# Carry

## General Description
The carry is the return for holding financial instruments. Therefore, we have to compare the future value of the instrument with the current value, and then we also have to discount the future value from the current value. 
We denote the Carry at time $t$ and the holding period $\tau$ as $C(t, \tau)$, the price of the instrument at time $t$ as $P(t)$, and the discount rate at time $t$ as $r(t)$. Then we have

$$
C(t, \tau) =  \exp \left( -\int_t^{t+\tau} r(s) ds \right) P(t + \tau) - P(t).
$$

The first term on the right-hand side is the future value of the instrument discounted to time $t$ from time $t + \tau$. The second term is the current value of the instrument. 

If we use the theory of stochastic calculus, this means that the future value of the instrument and the discount rate are stochastic processes, then we can use the expected value of the carry. The expected value of the carry is

$$
\begin{aligned}
\mathbb{E} \left[ C(t, \tau) \left. \right| \mathcal{F}_t \right] &= \mathbb{E} \left[ \exp \left( -\int_t^{t+\tau} r(s) ds \right) P(t + \tau) - P(t) \left. \right| \mathcal{F}_t \right]\\
&= \mathbb{E} \left[ \exp \left( -\int_t^{t+\tau} r(s) ds \right) P(t + \tau) \left. \right| \mathcal{F}_t \right] - P(t).
\end{aligned}
$$

## If the holding period is infinitesimal $\tau \to 0$
To understand the carry, we have to understand the behavior of the carry when the holding period is infinitesimal $\tau = \delta t\to 0$. In this case, we have

$$
\begin{aligned}
C(t, \delta t) &= \exp \left( -\int_t^{t+\delta t} r(s) ds \right) P(t + \delta t) - P(t) \\
&\sim \left(1  -\int_t^{t+\delta t} r(s) ds \right) P(t + \delta t) - P(t) \\
&\sim \left(1  - r(t) \delta t \right) P(t + \delta t) - P(t) \\
&\sim \left(1  - r(t) \delta t \right) \left(P(t) + \delta P(t)\right) - P(t) \\
&\sim P(t) + \left(\delta P(t) - P(t)r(t)\delta t \right) - P(t) \\
&= \delta P(t) - P(t)r(t) \delta t.
\end{aligned}
$$

The first term on the right-hand side is the change of the instrument's price during the holding period. The second term is the cost of holding the instrument during the holding period. Therefore, carrying during the infinitesimal holding period is the difference between the return and the cost of holding the instrument. 

The $\delta P(t)$ is different for instruments. This term is expanded in some factors: the instrument's parameters. 

## If the instrument is a bond
The bond has some parameters: the face value $F$, the coupon rate $c$, the coupon frequency $n$, the maturity $T$, and the yield $y$. This section assumes the face value and coupon are not time-dependent, and we also assume that the yield is the simple yield for simplicity

$$
P(t, c, y(t, T), T) = F \frac{1 + c(T-t)}{1 + y(t, T)(T-t)}.
$$

Then, we have

$$
\begin{aligned}
\delta P(t) &= P(t + \delta t, c, y(t + \delta t, T), T) - P(t, c, y(t, T), T) \\
&\sim \frac{\partial P(t, c, y(t, T), T)}{\partial t} \delta t + \frac{\partial P(t, c, y(t, T), T)}{\partial y} \delta y\\
&\sim \left(y(t, T) - c\right) \delta t - D(t, T) F \delta y,
\end{aligned}
$$

where $D(t, T)$ is the duration of the bond. Therefore, we have

$$
\begin{aligned}
C(t, \delta t) &= \delta P(t) - P(t)r(t) \delta t \\
&\sim \left(y(t, T) - c\right) \delta t - D(t, T) F \delta y - P(t)r(t) \delta t \\
&\sim \left(y(t, T) - c - r(t) \right) \delta t - D(t, T) F \delta y.
\end{aligned}
$$

In some cases, we call the term multiplied by $\delta t$ as the carry, and the term multiplied by $\delta y$ as the roll. 

The carry is the return of holding the bond during the holding period $\delta t$ when the yield $y(t, T)$ is unchanged. The return is affected by decreasing the time to maturity $T-t$. If time passes, the value of the bond will increase by the yield $y(t, T)$ because the denominator of the bond price will decrease, decrease by the coupon $c$ because the numerator of the bond price will decrease, and decrease by the discount rate $r(t)$ because the rate represents the risk-free rate and discounts the future value. 

The roll-down is the return of the yield change during the holding period $\delta t$ when the time ($\sim$ maturity) is not unchanged. We must calculate the yield change $\delta y$ to calculate the roll-down. However, the yield is not observable sufficiently. Therefore, we must use some assumptions to the yield curve $y(t, T)$ to calculate the roll-down. In practice, we sometimes assume that the yield curve $y(t, T)$ is not time-dependent. This means $y(t, T) = y(T)$. With this assumption, we can calculate $\delta y$ by constructing the yield curve using methods such as interpolating treasury yields.

From the above discussion, the carry and the roll-down are separated by the coefficients of $\delta t$ and $\delta y$. This separation can be valid when the holding period is short and the yield change is small. However, for example, when the holding period is long or the yield change is not small, the separation will not be valid because the second-order terms of $\delta t$ and $\delta y$ will not be negligible.

## If the instrument is a swap
The swap has some parameters: the notional as $N$, today (swap start date) as $t$, the swap end date (maturity) as $T$, the fixed rate as $K(t, T)$, and the floating rate as $L(t)$. The swap price $P(t, K(t, T), T)$ is as

$$
P(t, K(t, T), T) = N \int_t^T \left(L(s) - K(t, T)\right) \exp \left( -\int_t^s r(u) du \right) ds.
$$

For simplicity, we use the continuous cash flow. 

This formula represents the cash flows, which consist of the floating rate minus the fixed rate during the swap period $[t, T]$ discounted by the discount rate $r(t)$. 

Next, we calculate the carry. The present value of the swap must be zero at time $t$ with the fixed rate $K(t, T)$. Therefore, we have

$$
\begin{aligned}
\exp \left(-\int_t^{t+\delta t}r(s) ds \right)P(t+\delta t, K(t, T), T) - P(t, K(t, T), T) &= P(t + \delta, K(t, T), T) \\
&= N \int_{t+\delta t}^T \left(L(s) - K(t, T)\right) \exp \left( -\int_{t}^s r(u) du \right) ds \\
&= N \int_{t+\delta t}^T L(s) \exp \left( -\int_{t}^s r(u) du \right) ds - N \int_{t+\delta t}^T K(t, T) \exp \left( -\int_{t}^s r(u) du \right) ds \\
&= N \int_{t+\delta t}^T L(t+\delta t, T) \exp \left( -\int_{t}^s r(u) du \right) ds - N \int_{t+\delta t}^T K(t, T) \exp \left( -\int_{t}^s r(u) du \right) ds \\
&= N \left(K(t+\delta t, T) - K(t, T)\right) \int_{t+\delta t}^T \exp \left( -\int_{t}^s r(u) du \right) ds \\
&\sim N \left(K(t+\delta t, T) - K(t, T)\right) \int_{t}^T \exp \left( -\int_{t}^s r(u) du \right) ds \\
&= \left(K(t+\delta t, T) - K(t, T)\right) N D(t, T),
\end{aligned}
$$

where $K(t+\delta t, T)$ is the forward rate at time $t+\delta t$ for the period $[t+\delta t, T]$, and $D(t, T)$ is the duration of the swap. Therefore, the swap carry is the difference between the forward and fixed rates multiplied by the duration.

The carry term has another form as follows

$$
\begin{aligned}
\exp \left(-\int_t^{t+\delta t}r(s) ds \right)P(t+\delta t, K(t, T), T) - P(t, K(t, T), T) &= P(t + \delta, K(t, T), T) \\
&= N \int_{t+\delta t}^T \left(L(s) - K(t, T)\right) \exp \left( -\int_{t}^s r(u) du \right) ds \\
&\sim N\left(K(t, T) - L(t)\right) \delta t
\end{aligned}
$$

Next, we calculate the roll-down. The roll-down is

$$
\begin{aligned}
p(t, K(t, T) + \delta K, T) - P(t, K(t, T), T) &= N \int_t^T \left(L(s) - K(t, T) - \delta K\right) \exp \left( -\int_t^s r(u) du \right) ds - N \int_t^T \left(L(s) - K(t, T)\right) \exp \left( -\int_t^s r(u) du \right) ds \\
&= -N \int_t^T \exp \left( -\int_t^s r(u) du \right) ds \delta K \\
&= -N D(t, T) \delta K.
\end{aligned}
$$

Therefore, the total of the carry and the roll-down is

$$
\begin{aligned}
N\left[\left(K(t, T) - L(t)\right)\delta t - D(t, T) \delta K\right].
\end{aligned}
$$

The interpretation of the carry is, for example, the value of the swap is roughly the difference between the floating and the fixed rates times the duration of the swap. As time passes, the duration of the swap decreases, and the value of the swap changes by the difference. 
Next, the interpretation of the roll-down is, for example, the value of the swap is dependent on the minus of the fixed rate times the duration of the swap. If the fixed rate increases, the product of the fixed rate and the duration decreases because of the minus sign. 
