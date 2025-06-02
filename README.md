# randomness-testing-batteries-dataset
JSON: 
'first' - list of dictionaries of first-order p-values from Dieharder, TestU01, NISTSTS 
- "battery": "battery name" one of
- "subbattery": "sub-battery" one of
- "test": "test name"
- "id": "xxx_yyy_zzz" - xxx - ID of test, yyy,zzz other ids defining specific variant/parameterization of the test,  
- "num_pvals": number of collected p-values (list P)
- "unique": number of unique p-values (=set(P))
- "ratio": float = num_pvals/unique 
- "KS": p-value of KS test applied to P
- "L\_i" - observed frequency in the i-th left tail $O^L_i=|\{p \in P, p\leq 10^{-i}\}|$ - number of p-values from $P$ that appear in the left tail $[0, 10^{-i}]$
- "R\_i" - observed frequency in the i-th left tail $O^R_i=|\{p \in P, p\leq 10^{-i}\}|$ - number of p-values from $P$ that appear in the left tail $[1-10^{-i}, 1]$
- "l\_i" - ratio of observed to expected frequency for i-th left tail $l_i=L_i/num\_pvals/10^{-i}$
- "r\_i" - ratio of observed to expected frequency for i-th right tail $l_i=L_i/num\_pvals/10^{-i}$
