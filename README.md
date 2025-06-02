# randomness-testing-batteries-dataset
Data collected for Dieharder, TestU01, NIST STS batteries
JSON: 
 * 'first' - list of dictionaries of first-order p-values from  
   - "battery": "battery name" one of
   - "subbattery": "sub-battery" one of
   - "test": "test name"
   - "id": "xxx_yyy_zzz" - xxx - ID of test, yyy,zzz other ids defining specific variant/parameterization of the test,  
   - "num_pvals": number of collected p-values (list P)
   - "unique": number of unique p-values (=set(P))
   - "ratio": float = num_pvals/unique 
   - "KS": p-value of KS test applied to P
   - "X\_bins": p-value of $\chi^2_{bins}$ test applied to P, the test uses $bin$ of bins to categorize p-values
   - "L\_i" - observed frequency in the i-th left tail $O^L_i=|\{p \in P, p\leq 10^{-i}\}|$ - number of p-values from $P$ that appear in the left tail $[0, 10^{-i}]$
   - "R\_i" - observed frequency in the i-th left tail $O^R_i=|\{p \in P, p\leq 10^{-i}\}|$ - number of p-values from $P$ that appear in the left tail $[1-10^{-i}, 1]$
   - "l\_i" - ratio of observed to expected frequency for i-th left tail $l_i=L_i/num\_pvals/10^{-i}$
   - "r\_i" - ratio of observed to expected frequency for i-th right tail $r_i=R_i/num\_pvals/10^{-i}$
   - "l\_i\_bin" - p-value of binomial test testing fit of L_i to expected $10^{-i}num\_pvals$.
   - "r\_i\_bin" - p-value of binomial test testing fit of R_i to expected $10^{-i}num\_pvals$.
   - "log\_L\_i\_bin" - logarithm of p-value of binomial test for left tails
   - "log\_R\_i\_bin" - logarithm of p-value of binomial test for right tails
   - "log\_X\_bins": logarithm of p-value of $\chi^2_{bins}$
   - "log\_KS": logarithm of p-value of $KS$