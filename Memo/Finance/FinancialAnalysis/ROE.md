# ROE

## General description
This section will discuss the ROE (Return on Equity). This ratio measures how well a company uses its equity to generate net income. The formula for ROE is:

$$
\begin{align}
    ROE(t) &= \frac{NetIncome}{Equity} = \frac{NetIncome(t)}{E(t)} \\
\end{align}
$$
This quantity is used to measure the profitability of a company. The higher the ROE, the more profitable the company is. However, the ROE is not a good measure of a company's profitability because it does not consider the leverage ratio. The ROE can be increased by increasing the leverage ratio. This is because the leverage ratio increases the equity. Therefore, the ROE can be increased by increasing the leverage ratio. This is why the ROE is not a good measure of a company's profitability.

## case study

### the effect of the change in the tax rate
We can consider not only the change in the tax rate but also this straightforward case because the ROE depends on the tax rate linearly.
We consider the case where the tax rate changes as follows:

$$
\begin{align}
    r_t(t) &\rightarrow r_t(t) + \delta r_t(t) \\
    \delta r_t(t) &: \text{The change in the tax rate at time $t$} \\
\end{align}
$$

Then, the ROE changes as follows:

$$
\begin{align}
    ROE(t) &\rightarrow ROE(t) + \delta ROE(t) \\
    \delta ROE(t) &= \frac{NetIncome(t, r_t(t) + \delta r_t(t))}{E(t)} - \frac{NetIncome(t, r_t(t))}{E(t)} \\
    &= \frac{NetIncome(t, r_t(t) + \delta r_t(t)) - NetIncome(t, r_t(t))}{E(t)} \\
    &= \frac{\left(r_t(t) + \delta r_t(t) \right) \cdot EBIT(t) - r_t(t) \cdot EBIT(t)}{E(t)} \\
    &= \frac{EBIT(t)}{E(t)} \cdot \delta r_t(t) \\
\end{align}
$$

Then, we can write the change in addition to the ROE as follows:

$$
\begin{align}
    \delta ROE(t) &= \frac{EBIT(t)}{E(t)} \cdot \delta r_t(t) \\
    &= \frac{EBIT(t)}{L(t) + (E(t) - L(t))} \cdot \delta r_t(t) \\
    &= \frac{EBIT(t)}{L_{i}(t) + E(t) + (E(t) - L_{i} - E(t))} \cdot \delta r_t(t) \\
    &= \frac{EBIT(t)}{L_{i}(t) + E(t)}\cdot \frac{1}{1 + \frac{E(t) - L_{i} - E(t))}{L_{i}(t) + E(t)}} \cdot \delta r_t(t) \\
    &= \frac{ROIC(t)}{1 + \frac{E(t) - L_{i} - E(t))}{L_{i}(t) + E(t)}} \cdot \delta r_t(t) \\
\end{align}
$$

### the relationship with the ROA
This relation is straightforward because the leverage ratio relates to the ROE and the ROA. We can write the relationship as follows:

$$
\begin{align}
    ROE(t) &= \frac{NetIncome(t)}{E(t)} \\
    &= \frac{NetIncome(t)}{A(t)} \cdot \frac{A(t)}{E(t)} \\
    &= ROA(t) \cdot \frac{A(t)}{E(t)} \\
    &\geq ROA(t) \\
\end{align}
$$

The last inequality holds because the total assets are always greater than or equal to the shareholders' equity.
