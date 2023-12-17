# ROA

## General description
This section will discuss the ROA (Return on Assets) ratio. This ratio is used to measure how well a company is using its assets to generate profit. The formula for ROA is:

$$
\begin{align}
    ROA(t) &= \frac{NetIncome}{TotalAssets} = \frac{NetIncome(t)}{A(t)} \\
\end{align}
$$

Attention! There are two types of the ROA. One is the ROA using the net income in the numerator and the total assets in the denominator. The other is the ROA using the EBIT in the numerator and the total assets in the denominator. We mainly use the first one in this note.

The ROA depends on these parameters, but we omit them from the argument for simplicity and will explicitly write them when necessary.

We sometimes use the denominator as the average total assets at the period’s beginning and end. This is because the total assets may change significantly during the period, for example, when the company issues new stocks or bonds. In this case, the formula for ROA is like the following:

$$
\begin{align}
    ROA(t) &= \frac{NetIncome(t)}{\frac{A(t) + A(t-1)}{2}} \\
\end{align}
$$

## Why use the net income in the numerator and the total assets in the denominator?
There are ROX (Return on X) ratios for various X. For example, the ROA, ROE, and ROIC. These ratios are used to measure the profitability of the company. The ROA is to measure the profitability of the total assets.

The measure of the profit in the numerator is not essential compared to the denominator. Therefore, the measure is sometimes different in the numerator; for example, as we denoted above, there are two famous ROA definitions and numerators: net income and EBIT.

## case study
In this case study, we consider some changes in the parameters of the ROA. Then, however, we assume the other parameters are unchanged for simplicity. Of course, in the real world, the parameters may change simultaneously. However, it is difficult to consider all the cases and the dynamics of the parameters.

Sometimes, we use the other indicators we will introduce later in this note. Please refer to the other sections for the definitions and details of the indicators.

### the effect of the change in the tax rate
We can consider not only the change in the tax rate but also this straightforward case because the ROA depends on the tax rate linearly.
We consider the case where the tax rate changes as follows:

$$
\begin{align}
    r_t(t) &\rightarrow r_t(t) + \delta r_t(t) \\
    \delta r_t(t) &: \text{The change in the tax rate at time $t$} \\ 
\end{align}
$$

Then, the ROA changes as follows:

$$
\begin{align}
    ROA(t) &\rightarrow ROA(t) + \delta ROA(t) \\
    \delta ROA(t) &= \frac{NetIncome(t, r_t(t) + \delta r_t(t))}{A(t)} - \frac{NetIncome(t, r_t(t))}{A(t)} \\
    &= \frac{NetIncome(t, r_t(t) + \delta r_t(t)) - NetIncome(t, r_t(t))}{A(t)} \\
    &= \frac{\left(r_t(t) + \delta r_t(t) \right) \cdot EBIT(t) - r_t(t) \cdot EBIT(t)}{A(t)} \\
    &= \frac{EBIT(t)}{A(t)} \cdot \delta r_t(t) \\
\end{align}
$$

Then, we can write the change in addition to the ROA as follows:

$$
\begin{align}
    \delta ROA(t) &= \frac{EBIT(t)}{A(t)} \cdot \delta r_t(t) \\
    &= \frac{EBIT(t)}{L(t) + (A(t) - L(t))} \cdot \delta r_t(t) \\
    &= \frac{EBIT(t)}{L_{i}(t) + E(t) + (A(t) - L_{i} - E(t))} \cdot \delta r_t(t) \\
    &= \frac{EBIT(t)}{L_{i}(t) + E(t)}\cdot \frac{1}{1 + \frac{A(t) - L_{i} - E(t))}{L_{i}(t) + E(t)}} \cdot \delta r_t(t) \\
    &= \frac{ROIC(t)}{1 + \frac{A(t) - L_{i} - E(t))}{L_{i}(t) + E(t)}} \cdot \delta r_t(t) \\
\end{align}
$$

### the relationship with the ROE
This relation is very simple because the ROA and the ROE are related by the leverage ratio. We can write the relationship as follows:

$$
\begin{align}
    ROA(t) &= \frac{NetIncome(t)}{A(t)} \\
    &= \frac{NetIncome(t)}{E(t)} \cdot \frac{E(t)}{A(t)} \\
    &= ROE(t) \cdot \frac{E(t)}{A(t)} \\
    &\leq ROE(t) \\
\end{align}
$$

The last inequality holds because the total assets are always greater than or equal to the shareholders' equity.

If we use another definition of the ROA which uses the EBIT in the numerator, then the formula is changed as follows:

$$
\begin{align}
    ROE(t) &= \frac{NetIncome(t)}{E(t)} \\
    &= \frac{EBIT(t) - Interest(t) - Tax(t)}{E(t)} \\
    &= \frac{(EBIT(t) - Interest(t)) \times (1 - r_t(t))}{E(t)} \\
    &= \frac{EBIT(t) - Interest(t)}{E(t)} \cdot (1 - r_t(t)) \\
    &= \frac{EBIT(t) - Interest(t)}{A(t)}\cdot \frac{A(t)}{E(t)} \cdot (1 - r_t(t)) \\
    &= \frac{EBIT(t) - r_l(t) D(t)}{A(t)}\cdot \frac{A(t)}{E(t)} \cdot (1 - r_t(t)) \\
    &= \left(ROA'(t)\cdot \frac{A(t)}{E(t)} - r_l(t) \frac{D(t)}{E(t)}\right) \cdot (1 - r_t(t)) \\
    &= \left(ROA'(t) + ROA'(t) \cdot \frac{A(t) - E(t)}{E(t)} - r_l(t) \frac{D(t)}{E(t)}\right) \cdot (1 - r_t(t)) \\
\end{align}
$$
We add the prime to the ROA to distinguish it from the ROA using the NetIncome in the numerator.

Compared to the previous case, it is not determined whether the ROA is greater than or less than the ROE because of the interest rate of the liabilities from interest-bearing liabilities.

In addition, there are two types of ROE: one is the ROE using the shareholders’ equity in the denominator, and the other is the ROE using the net assets in the denominator. In the latter case, the formula is changed as follows:

$$
\begin{align}
    ROE(t) &= \left(ROA'(t) + ROA'(t) \cdot \frac{A(t) - E(t)}{E(t)} - r_l(t) \frac{D(t)}{E(t)}\right) \cdot (1 - r_t(t)) \\
    &= \left(ROA'(t) + ROA'(t) \cdot \frac{D(t)}{E(t)} - r_l(t) \frac{D(t)}{E(t)}\right) \cdot (1 - r_t(t)) \\
    &= \left(ROA'(t) + \left( ROA'(t) - r_l(t)\right)\frac{D(t)}{E(t)}\right) \cdot (1 - r_t(t)) \\
\end{align}
$$


### the effect of the change in the shareholder's equity
In this case, we consider the case where the shareholders' equity changes, such as the company issuing new stocks or buying back stocks.

In this case, we can compute the effect to differentiate the ROA for the shareholders' equity. We can write the change in the ROA as follows:

$$
\begin{align}
    \delta ROA(t) &= \frac{d}{dE(t)} \left( \frac{NetIncome(t)}{A(t)} \right) \cdot \delta E(t) \\
    &= -ROA(t) \cdot \frac{\delta E(t)}{A(t)} \\
\end{align}
$$

From this result, if the ROA is positive, then the ROA increases when the shareholders' equity decreases, like in the buyback case. However, in general, the net income changes because of spending money to buy back stocks in the future. Therefore, we must consider the change's effect on the related parameters.