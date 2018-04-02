# Set Theory

## Computing a regular set algorithm

1. Expression $\lambda$ corresponds to the set $\{\Lambda\}$
2. if $x \in S$, then the regular expression $x$ corresponds to set $\{x\}$
3. if $\alpha$ and $\beta$ are regular expressions corresponding to subsets $A$ and $B$ of $S^{*}$, then $\alpha\beta$ corresponds to $A \cdot B = \{s \cdot t \: | \: s \in A \text{ and } x \in B\}$
4. if $\alpha$ and $\beta$ are regular expressions corresponding to subsets $A$ and $B$ of $S^{*}$, then $\alpha\vee\beta$ corresponds to $A \cup B$
5. if $\alpha$ is a regular expression that corresponds to subset $A$ of $S^{*}$, then $(\alpha)^{*}$ corresponds to set $A^{*}$