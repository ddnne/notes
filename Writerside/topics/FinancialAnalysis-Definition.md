# Definition of some math symbols

We use some fundamental mathematical symbols related to the financial analysis in this note. The definitions are as follows:

```tex
\begin{align}
    A(t) &: \text{The amount of asset at time $t$} \\
    L(t) &: \text{The amount of liability at time $t$} \\
    L_c(t) &: \text{The amount of current liabilities at time $t$} \\
    L_{nc}(t) = L(t) - L_c(t)&: \text{The amount of non-current liabilities at time $t$} \\
    L_{i}(t) &: \text{The amount of interest-bearing liabilities at time $t$} \\
    L_{ni}(t) = L(t) - L_{ib}(t)&: \text{The amount of non-interest-bearing liabilities at time $t$} \\
    E(t) &: \text{The amount of shareholders' equity at time $t$} \\
    r(t) &: \text{The interest rate} \\
    r_t(t) &: \text{The tax rate at time $t$} \\
    r_l(t) &: \text{The interest rate of the liabilities at time $t$} \\
    S(t) &: \text{The amount of sales at time $t$} \\
    COGS(t) &: \text{The amount of cost of goods sold at time $t$} \\
    GrossProfit(t) = S(t) - COGS(t)&: \text{The amount of gross profit at time $t$} \\
    SG\&A(t) &: \text{The amount of selling, general and administrative expenses at time $t$} \\
    EBIT(t) = GrossProfit(t) - SG\&A(t) &: \text{The amount of earnings before interest and tax at time $t$} \\
    Interest(t) = r_l(t) L_{i}(t)&: \text{The amount of interest at time $t$} \\
    Tax(t) = r_t(t) \cdot (EBIT(t) - Interest(t)) &: \text{The amount of tax at time $t$} \\
    NetIncome(t) = EBIT(t) - Interest(t) - Tax(t) &: \text{The amount of net income at time $t$} \\
    Depreciation(t) &: \text{The amount of depreciation at time $t$} \\
    Amortization(t) &: \text{The amount of amortization at time $t$} \\
    D\&A(t) = Depreciation(t) + Amortization(t) &: \text{The amount of depreciation and amortization at time $t$} \\
    EBIDA(t) = EBI(t) + D\&A(t) &: \text{The amount of earnings before interest, depreciation and amortization at time $t$} \\
\end{align}
```





