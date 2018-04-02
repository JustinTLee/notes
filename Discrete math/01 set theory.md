# Set theory

---

## Table of Contents

01. [Sets](#sets)
02. [Sequences](#sequences)
03. [Regular expressions](#regular-expressions)
04. [Equations](#equations)
05. [Theorems](#theorems)
06. [References](#references)

---

## Sets

* a **set** is a well-defined collection of **elements**
* elements that exist within a set are called **members**
    * member order is not important
    * each member is distinct


<br/>

* enumerate contents of set $S$ with $n$ members:

\begin{equation*}
S = {A_{1}, \dotso, A_{n}}
\end{equation*}

<br/>

* $x \in S$ defines that $x$ **is** a member of set $S$
* $x \notin S$ defines that $x$ **is not** a member of set $S$

<br/>

* define set by a property that all members have in common where $P(x)$ denotes true proposition concerning member $x$:

\begin{equation*}
S = \{x \: | \: P(x)\}
\end{equation*}

<br/>

* commonly encountered sets:
    * $Z^{+} = \{x \: | \: x \text{ is a positive integer}\}$
    * $N = \{x \: | \: x \ge 0 \text{ and } x \text{ is an integer}\}$
    * $Z = \{x \: | \: x \text{ is an integer}\}$
    * $\mathbb{R} = \{x \: | \: x \text{ is real number}\}$
    * $\emptyset$ has no elements ($S = \{\}$)

<br/>

* **equal** sets have same elements:

\begin{equation*}
S_{1} = S_{2}
\end{equation*}

* If $x \in A$ and $x \in B$ for all $x$, then $A$ is a **subset** of $B$:

\begin{equation*}
A \subseteq B
\end{equation*}

* $\emptyset \subseteq S$

<br/>

* **finite** set has $n$ distinct elements
* $n$ is **cardinality** of set $S$
    * denoted by $|S|$
* **power set** is set of all subsets of $S$
    * denoted by $P(S)$
* if $|S| = n$, then $|P(S)| = 2^{n}$

<br/>

* **union** between two sets:

\begin{equation*}
S_{1} \cup S_{2} = \{x \: | \: x \in S_{1} \text{ or } x \in S_{2}\}
\end{equation*}

* union between $k$ sets: $\bigcup_{i = 1}^{k} S_{i}$.
* **intersection** between two sets:

\begin{equation*}
S_{1} \cap S_{2} = \{x \: | \: x \in S_{1} \text{ and } x \in S_{2}\}
\end{equation*}

* intersection between $k$ sets: $\bigcap_{i = 1}^{k} S_{i}$.

* **disjoint** sets  have no common elements:

\begin{equation*}
S_{1} \cup S_{2} = \emptyset
\end{equation*}

* **complement** of two sets:

\begin{equation*}
S_{1} - S_{2} = \{x \: | \: x \in S_{1} \text{ and } x \notin S_{2}\}
\end{equation*}

* complement of a set compared to some universal set: $\overline{S}$.

* **symmetric difference** between two sets are all the elements that belong to either one of the sets but not to both:

\begin{equation*}
S_{1} \oplus S_{2} = \{x \: | \: (x \in S_{1} \text{ and } x \notin S_{2}) \text{ or } (x \notin S_{1} \text{ and } x \in S_{2})\}
\end{equation*}

<br/>

#### Theorem: algebraic properties of sets

**Commutative**:

* $S_{1} \cup S_{2} = S_{2} \cup S_{1}$
* $S_{1} \cap S_{2} = S_{2} \cap S_{1}$

**Associative**:

* $S_{1} \cup (S_{2} \cup S_{3}) = (S_{1} \cup S_{2}) \cup S_{3}$
* $S_{1} \cap (S_{2} \cap S_{3}) = (S_{1} \cap S_{2}) \cap S_{3}$

**Distributive**:

* $S_{1} \cup (S_{2} \cap S_{3}) = (S_{1} \cap S_{2}) \cup (S_{1} \cap S_{3})$
* $S_{1} \cap (S_{2} \cup S_{3}) = (S_{1} \cup S_{2}) \cap (S_{1} \cup S_{3})$

**Idempotent**:

* $S_{1} \cup S_{1} = S_{1}$
* $S_{1} \cap S_{1} = S_{1}$

**Complement rules**:

* $\overline{(\overline{S_{1}})} = S_{1}$
* $S_{1} \cup \overline{S_{1}} = U$
* $S_{1} \cap \overline{S_{1}} = \emptyset$
* $\overline{\emptyset} = U$
* $\overline{U} = \emptyset$
* $\overline{S_{1} \cup S_{2}} = \overline{S_{1}} \cap \overline{S_{2}}$
* $\overline{S_{1} \cap S_{2}} = \overline{S_{1}} \cup \overline{S_{2}}$

**Universal rules**:

* $S_{1} \cup U = U$
* $S_{1} \cap U = S_{1}$

**Null rules**:

* $S_{1} \cup \emptyset = S_{1}$
* $S_{1} \cap \emptyset = \emptyset$

**End theorem.**

<br/>

#### Theorem: addition principle

For two disjoint sets, the cardinality of their union is:

\begin{equation*}
|S_{1} \cup S_{2}| = |S_{1}| + |S_{2}|
\end{equation*}

For two non-disjoint sets, the cardinality of their union is given by the **addition principle**:

\begin{equation*}
|S_{1} \cup S_{2}| = |S_{1}| + |S_{2}| - |S_{1} \cap S_{2}|
\end{equation*}

**End theorem.**

<br/>

* **characteristic function** of a set:

\begin{equation*}
f_{S}(x) =
\begin{cases}
1 \quad \text{if } x \in S \\
0 \quad \text{if } x \notin S
\end{cases}
\end{equation*}

<br/>

#### Theorem: properties of characteristic functions

Characteristic functions of subsets satisfy the following properties:

* $f_{S_{1} \cup S_{2}}(x) = f_{S_{1}}(x)f_{S_{2}}(x)$
* $f_{S_{1} \cap S_{2}}(x) = f_{S_{1}}(x) + f_{S_{2}}(x) - f_{S_{1}}(x)f_{S_{2}}(x)$
* $f_{S_{1} \oplus S_{2}}(x) = f_{S_{1}}(x) + f_{S_{2}}(x) - 2f_{S_{1}}(x)f_{S_{2}}(x)$

**End theorem.**

<br/>

* **ordered pair** - a listing of objects $a$ and $b$ in a prescribed order $(a, b)$ 
    * same as a sequence of length 2

<br/>

* **Cartesian product** of $A$ and $B$:

\begin{equation*}
A \times B = \{(a, b) | \, a \in A \; \text{and} \; b \in B\}
\end{equation*}

<br/>

#### Theorem: cardinality of Cartesisan product

For any two finite, non-empty sets $A$ and $B$, $|A \times B| = |A| |B|$.

**End theorem.**

<br/>

* for any non-empty sets $A_{1}$, $A_{2}$, ..., $A_{n}$, the Cartesian product is:

\begin{equation*}
A_{1} \times A_{2} \times \cdots \times A_{n} = \{(a_{1}, a_{2}, \dots, a_{n}) | \, a_{i} \in A_{i} \; \text{for} \; i = 1, \dots, n\}
\end{equation*}

<br/>


* **partition** is collection of non-empty subsets of $S$ such that:
    * $A_{i} \cap A_{j}$ = \emptyset$
    * $s \in S$ and $s \in A_{i}$ for at least one $A_{i}$
        * where $A_{i} \subseteq S$ for all $i$
* $A_{i}$ is a **block** of the partition

---

[(back to top)](#table-of-contents)

---

## Sequences

* **sequence** is list of elements ordered by increasing value
    * list may be finite or infinite
    * list items can be non-distinct
* general sequence can be written as $a_{1}, a_{2}, a_{3}, \dotsc$ or $(a_{i})_{1 \leq i < \infty}$.

<br/>

* **countable** set is set corresponding to all distinct elements in a sequence
    * set $S^{*}$ consists of all finite sequences of the members of $S$
* if the members of $S$ are symbols, $S^{*}$ is **alphabet**
* finite sequences in $S^{*}$ are **strings**
    * $S^{*}$ includes empty string $\Lambda$
    * the **catenation** of two strings is equivalent to:

\begin{equation*}
s \cdot w = \underbrace{s_{1}s_{2}s_{3}}_{\text{string #1}} \underbrace{w_{1}w_{2}w_{3}}_{\text{string #2}}
\end{equation*}

* Catenation with empty string is identity:
    * $s \cdot \Lambda = s$
    * $\Lambda \cdot s = s$

<br/>

#### Theorem: multiplication principle

If independent tasks $T_{i}$ for $i = 1, \dotsc, n$ are to be performed in sequence and each $T_{i}$ can be performed $N_{i}$ ways, then the sequence $T_{1}T_{2} \dotsc T_{n}$ can be performed $\prod_{i = 1}^{n} N_{i}$ ways.

**End theorem.**

<br/>

* for set $|S| = n$, arrangement of the members of S into sequence of length $n$ is **permutation** of S
* for sequence that is length $r$ taken from set $S$, it is known as a **permutation of $S$ taken $r$ at a time**

<br/>

#### Theorem: permutation

If $|S| = n$ and $1 \leq r \leq n$, then the number of permutations of $S$ taken $r$ at a time is:

\begin{equation*}
P_{r}^{n} = \frac{n!}{(n - r)!}
\end{equation*}

This formula is also known as a **permutation**.

**End theorem.**

<br/>

#### Theorem: combination

If $|S| = n$ and $1 \leq 0 \leq n$, then the number of $r$-element subsets of $S$ is:

\begin{equation*}
C_{r}^{n} = \frac{n!}{r!(n - r)!}
\end{equation*}

This formula is also known as a **combination**.

**End theorem.**

---

[(back to top)](#table-of-contents)

---

## Regular expressions

* **regular expression** over set $S$ is string constructed from the elements of $S$ and/or the following symbols:
    * (
    * )
    * $\vee$
    * $*$
    * $\lambda$
* rules for regular expressions:
    * the symbol $\lambda$ is a regular expression
    * if $x \in S$ then $x$ is a regular expression
    * if $\alpha$ and $\beta$ are regular expressions, then $\alpha\beta$ is a regular expression
    * if $\alpha$ and $\beta$ are regular expressions, then $\alpha\vee\beta$ is a regular expression
    * if $\alpha$ is a regular expression, then $(\alpha)^{*}$ is a regular expression

* set $S^{*}$ is called a **regular set** of $S$

<br/>

#### Algorithm: computing a regular set

Computing a regular set involves the following algorithm:

1. Expression $\lambda$ corresponds to the set $\{\Lambda\}$
2. if $x \in S$, then the regular expression $x$ corresponds to set $\{x\}$
3. if $\alpha$ and $\beta$ are regular expressions corresponding to subsets $A$ and $B$ of $S^{*}$, then $\alpha\beta$ corresponds to $A \cdot B = \{s \cdot t \: | \: s \in A \text{ and } x \in B\}$
4. if $\alpha$ and $\beta$ are regular expressions corresponding to subsets $A$ and $B$ of $S^{*}$, then $\alpha\vee\beta$ corresponds to $A \cup B$
5. if $\alpha$ is a regular expression that corresponds to subset $A$ of $S^{*}$, then $(\alpha)^{*}$ corresponds to set $A^{*}$

**End algorithm.**

---

[(back to top)](#table-of-contents)

---

## Equations

#### Cardinality of power set:

\begin{equation*}
|P(S)| = 2^{n}
\end{equation*}

#### Addition principle of disjoint sets:

\begin{equation*}
|S_{1} \cup S_{2}| = |S_{1}| + |S_{2}|
\end{equation*}

#### Addition principle of non-disjoint sets:

\begin{equation*}
|S_{1} \cup S_{2}| = |S_{1}| + |S_{2}| - |S_{1} \cap S_{2}|
\end{equation*}

#### Characteristic function:

\begin{equation*}
f_{S}(x) =
\begin{cases}
1 \quad \text{if } x \in S \\
0 \quad \text{if } x \notin S
\end{cases}
\end{equation*}

#### Permutation:

\begin{equation*}
P_{r}^{n} = \frac{n!}{(n - r)!}
\end{equation*}

#### Combination:

\begin{equation*}
C_{r}^{n} = \frac{n!}{r!(n - r)!}
\end{equation*}

---

[(back to top)](#table-of-contents)

---

## Theorems

#### _Theorem 01.01 (**Sets**)_:

The algebraic properties of sets are:

* **Commutative**: 
	* $S_{1} \cup S_{2} = S_{2} \cup S_{1}$
	* $S_{1} \cap S_{2} = S_{2} \cap S_{1}$
* **Associative**: 
	* $S_{1} \cup (S_{2} \cup S_{3}) = (S_{1} \cup S_{2}) \cup S_{3}$
	* $S_{1} \cap (S_{2} \cap S_{3}) = (S_{1} \cap S_{2}) \cap S_{3}$
* **Distributive**:
	* $S_{1} \cup (S_{2} \cap S_{3}) = (S_{1} \cap S_{2}) \cup (S_{1} \cap S_{3})$
	* $S_{1} \cap (S_{2} \cup S_{3}) = (S_{1} \cup S_{2}) \cap (S_{1} \cup S_{3})$
* **Idempotent**:
	* $S_{1} \cup S_{1} = S_{1}$
	* $S_{1} \cap S_{1} = S_{1}$
* **Complement rules**:
	* $\overline{(\overline{S_{1}})} = S_{1}$
	* $S_{1} \cup \overline{S_{1}} = U$
	* $S_{1} \cap \overline{S_{1}} = \emptyset$
	* $\overline{\emptyset} = U$
	* $\overline{U} = \emptyset$
	* $\overline{S_{1} \cup S_{2}} = \overline{S_{1}} \cap \overline{S_{2}}$
	* $\overline{S_{1} \cap S_{2}} = \overline{S_{1}} \cup \overline{S_{2}}$
	* $S_{1} \cup U = U$
	* $S_{1} \cap U = S_{1}$
* **Null rules**:
	* $S_{1} \cup \emptyset = S_{1}$
	* $S_{1} \cap \emptyset = \emptyset$

#### _Theorem 01.02 (**Sets - addition principle**)_:

If two sets are disjoint, the cardinality of their union is:

\begin{equation*}
|S_{1} \cup S_{2}| = |S_{1}| + |S_{2}|
\end{equation*}

If two sets are not disjoint, the cardinality of their union is given by the **addition principle**:

\begin{equation*}
|S_{1} \cup S_{2}| = |S_{1}| + |S_{2}| - |S_{1} \cap S_{2}|
\end{equation*}

#### _Theorem 01.03 (**Sets**)_:

Characteristic functions of subsets satify the following properties:

* $f_{S_{1} \cup S_{2}}(x) = f_{S_{1}}(x)f_{S_{2}}(x)$
* $f_{S_{1} \cap S_{2}}(x) = f_{S_{1}}(x) + f_{S_{2}}(x) - f_{S_{1}}(x)f_{S_{2}}(x)$
* $f_{S_{1} \oplus S_{2}}(x) = f_{S_{1}}(x) + f_{S_{2}}(x) - 2f_{S_{1}}(x)f_{S_{2}}(x)$

#### _Theorem 01.04 (**Sets**)_:

For any two finite, non-empty sets $A$ and $B$, $|A \times B| = |A| |B|$.

#### _Theorem 01.05 (**Sequences - multiplication principle**)_:

If independent tasks $T_{i}$ for $i = 1, \dotsc, n$ are to be performed in sequence and each $T_{i}$ can be performed $N_{i}$ ways, then the sequence $T_{1}T_{2} \dotsc T_{n}$ can be performed $\prod_{i = 1}^{n} N_{i}$ ways.

#### _Theorem 01.06 (**Sequences - permutation**)_:

If $|S| = n$ and $1 \leq r \leq n$, then the number of permutations of $S$ taken $r$ at a time is:

\begin{equation*}
P_{r}^{n} = \frac{n!}{(n - r)!}
\end{equation*}

#### _Theorem 01.07 (**Sequences - combination**)_:

If $|S| = n$ and $1 \leq 0 \leq n$, then the number of $r$-element subsets of $S$ is:

\begin{equation*}
C_{r}^{n} = \frac{n!}{r!(n - r)!}
\end{equation*}

---

## References

---

[(back to top)](#table-of-contents)

---